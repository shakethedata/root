---
date: 2018-05-06T21:33:05-04:00
description: "Karma's comorbitity"
featured_image: ""
tags: []
title: "First Post: Comorbitity (to be d3'ified)"
---
# Comorbidity

The comorbidity, or co-occurrence of Adverse Events can show trends and help determine causal relationships of Drug Related Adverse Events [(Wang et al, 2009)](https://www.ncbi.nlm.nih.gov/pubmed/23703825/)

Furthermore, the co-occurence patterns of Adverse events, particularly under co-administration of multiple drugs is poorly understood. 

Here we will examine the use of social networking algorithms to detect co-occuring adverse events.


## Data collection

Initially we hoped to use the tweet data from previous sections for this analysis. However we simply did not have enough data points available. 

The FDA provides quarterly downloadable files of Adverse Events reported for use in post-marketing safety surveillance from [here](http://www.fda.gov/Drugs/GuidanceComplianceRegulatoryInformation/Surveillance/AdverseDrugEffects/). We consequently decided that this was a clean, abundant and reliable source of data to perform the analysis on.


###A First look at the data

Reading in the Adverse Events, and the drugs the patients were on.

```{r message=FALSE}
#A First look at the data

require(knitr)
require(dplyr)
require(ggplot2)
require(rafalib)
require(igraph)

# Adverse Event data
ae.data <- read.delim2("../data/REAC15Q4.txt",sep="$", stringsAsFactors = FALSE)

# Associated drug data
drug.data <- read.delim2("../data/DRUG15Q4.txt",sep="$", stringsAsFactors = FALSE)
```



The Drug data contains information on repeat dosing, as well as missed doses. We will only keep patients that had an actual dose of study drug and that the drug was the primary suspect of the AE.

```{r message=FALSE}
drug.data <- drug.data %>%
  filter(cum_dose_chr !="" && role_cod =="PS") %>%
  select(primaryid, drugname) %>%
  unique()

# Print the drugs with the most patients
drug.data %>%
  group_by(drugname)%>%
  summarize(n=n())%>%
  arrange(-n) %>% 
  head %>% 
  kable

#How many incidences does vyvanse have
drug.data %>%
  filter(tolower(drugname)=="vyvanse") %>%
  group_by(drugname) %>%
  summarize(n=n())%>%
  arrange(-n) %>%  kable
```

We can see that there are a lot of patients here, and it would be very tricky to visualise graphs of these sizes, so for this analysis, we will look specifically at Vyvanse. This was the most frequent drug on the tweet analysis section.

Similary, taking a look at the Adverse event dataset, we will keep only those where the primary suspect is Vyvanse.

```{r message=FALSE}
# Get an idea of how many data points we are looking at in the total AE dataset
ae.data %>% 
  summarize(n_patients = n_distinct(primaryid),
            n_aes      = n_distinct(pt))

# Select only vyvanse patients 
vyvanse <- drug.data %>%
  filter(tolower(drugname)=="vyvanse") %>%
  select(primaryid) %>%
  unique()

# Filter the AE dataset for these patients
ae.data.subset <- ae.data %>%
  filter(primaryid %in% vyvanse$primaryid)

# plot the frequencies of the 20 most common AEs
counts <- count(ae.data.subset,pt) %>% 
  arrange(-n) %>% 
  head(20)

ggplot(counts, aes(x = reorder(pt, n), y = n)) +
         geom_bar(stat = "identity") + 
         xlab("Preferred Term") +
         ggtitle ("20 most frequent Adverse Events for Vyvanse") +
  coord_flip()
```

### Building the network graph

We will start by creating an adjacency list to build the graph object. We will also add weights to each of the edges where the weight will be the probability of that edge (1/number of edges) for that patient.

```{r message=FALSE}
# We will only consider at most, one co-occurence of Adverse Events per patient

# Calculate the number of AEs per patient
ae.data.obs <-ae.data.subset %>% 
  dplyr::select(primaryid, pt) %>% 
  group_by(primaryid) %>%
  mutate(obs=n()) %>%
  ungroup

# Cartesian product of adverse events, we reduce this so we are not double counting edges. ie A->B != B->A
ae.data.expand <- ae.data.obs %>% full_join(ae.data.obs,by="primaryid") %>%
  filter (pt.x<pt.y) %>%
  mutate(from=pt.x, to=pt.y, wgt=1/obs.x) %>%
  group_by(from, to)%>%
  summarise(weight=sum(wgt)) %>%
  ungroup

# Build the graph object from the data
g <- graph.data.frame(ae.data.expand, directed = FALSE)
```


Now that we have our graph object, we will assign the frequencies of the Adverse events to the nodes.

We will then do some simple interrogation of the graph.

```{r, warning=FALSE}
# Calculate the frequency of each Adverse Event
pt.freq <- ae.data.obs %>%
  group_by(pt) %>%
  summarise(nc=n()) %>%
  ungroup 

# Match the AE frequencies to their ordering in the Graph object
name.ord <- data.frame(names=V(g)$name,ord=seq(1:length(V(g)$name))) %>%
  left_join(pt.freq, by=c("names"="pt")) %>%
  arrange(ord)

# Apply the frequencies to be the node counts
V(g)$node_count <- name.ord$nc

# Preliminary plot to see the structure of the graph
plot(g, 
     main="Identity graph of Adverse Event Comorbidity",
     vertex.label=NA,
     vertex.size=1,
     vertex.color="green")

# Number of vertices
vcount(g)

# Number of edges
ecount(g)
```

We can see from our preliminary plot that we have one large cluster of AEs, and a few very small clusters as well as a few isolates that consist of only one edge.


### Cluster analysis

Lets first take a look at some of the smaller clusters and isolates.


```{r message=FALSE}
# We don't expect all our Adverse events to be connected, so taking a look at the number of distinct clusters
g.components <- clusters(g)

# print sizes of each cluster
g.components$csize

# We can see that we have one large cluster of 474, 4 small and 10 isolates that consist of a single unconnected pair. 

# Lets plot the small clusters together
g.small <- induced.subgraph(g, which(g.components$membership != which.max(g.components$csize)))

#Edges have been weighted by the degree
g.small.layout <-  layout.reingold.tilford(g.small, circular=TRUE)
plot(g.small,
     main="Small isolated clusters of AE comorbidity",
     vertex.size = 4,
     vertex.color ="green",
     vertex.label.family = "sans",
     vertex.label.cex = .8,
     vertex.label.color ="darkorange"
     )

# Isolates with small degrees are likely either rare or due to chance and have little to do with the Drug
```

It's hard to see the groupings properly above, so we will focus on the two main groups of interest.

```{r message=FALSE}
plot_subgraph <- function(gr, title,color){
   plot(gr,
     main=title,
     #vertex.size = 4,
     vertex.color =color,
     vertex.label.family = "sans",
     vertex.label.cex = .8,
     vertex.label.color ="black"
     )
}

g.mother <- induced.subgraph(g, which(g.components$membership == 4))
g.child <- induced.subgraph(g, which(g.components$membership == 3))

par(mfrow=c(1,2))
plot_subgraph(g.mother,"Maternal Adverse Events","red")
plot_subgraph(g.child,"Feotal Adverse Events","blue")
par(mfrow=c(1,1))

# We will continue the rest of the analysis keeping only the large central network
g.big <- induced.subgraph(g, which(g.components$membership == which.max(g.components$csize)))
```

We can see some interesting groupings from the small clusters already. One cluster points to neonatal AEs such as : 
- Jaundice Neonatal
- Premature baby
- Feotal exposure during pregnancy
- Drug withdrawal sympton neonatal
- Feotal distress syndrome

We also have a separate cluster that contains the AEs from the mother:
- Premature delivery
- Caesarian section
The linked AEs of Rhesus incompatibility and infusion is likely due to an infusion during delivery


### Community detection

Having explored the smaller cluster, we are still left with a strongly connected, large cluster. In order to help visualise it, we will split the cluster into communities using a random walk. We will then investigate a few clusters between 10 and 40 nodes.

```{r message=FALSE}
set.seed(1234)
# Detecting community strucution via short random walks
wc <- walktrap.community(g.big, weights = E(g.big)$weight, steps = 120, merges =
          TRUE, modularity = TRUE, membership = TRUE)

# Print the sizes of our communities
sizes(wc)

plot_cluster <- function(clust,title, edges=FALSE){ 
  g.prune <- induced.subgraph(g.big, which(membership(wc)==clust))
  g.prune.layout <-  layout.reingold.tilford(g.prune,circular=TRUE)
  
  plot(g.prune,
     main = title, 
     layout =g.prune.layout,
     vertex.size = (V(g.prune)$node_count),
     vertex.color ="lightgreen",
     vertex.label.cex = .7,
     vertex.label.family = "sans",
     vertex.label.color ="black",
     edge.label = ifelse(edges,round(E(g.prune)$weight,3),NA),
     edge.label.cex = .6,
     edge.label.color = "darkred",
     edge.width = E(g.prune)$weight)

}

plot_cluster(1,"AE Cluster 1",edges=TRUE)
```

In the above graphs, the size of the node represents the frequency of that AE. The edge weight is given by the sum of probabilies of the co-occurence of the two connected AEs. 
For example, we can see in cluster 1 that a decreased appetite and somnolence are quite common on vyvanse and having a decreased appetite if you have somnolence is more likely than experiencing feeling jittery.

```{r message=FALSE}
plot_cluster(5,"AE Cluster likely related to psychological trauma")
```

Cluster 5 looks shows terms mostly to do with psychological trauma. Bipolar disorder, suicidal ideation and fatigue are known to be strongly linked and we can see this here also. 

The downside of this type of analysis, where we are only looking at co-occurence is that we cant tell the direction of action. That is, we can see that gynocomastia is linked with depression, but we dont have evidence of a causal link (even though its probably unlikely that depression would cause gynocomastia).

```{r message=FALSE}
plot_cluster(6,"Cluster likely related to auto-immune reactions")
```

Cluster 6 seems to primarily be auto-immune reactions. 

We will now look at the last cluster in a heatmap


```{r message=FALSE}
plot_heat <- function(clust){
    g.prune <- induced.subgraph(g.big, which(membership(wc)==clust))
    e <- get.adjacency(g.prune,attr="weight")
    e <- e+0.001 #getting rid of nas
    heatmap(as.matrix(e),
            main = "Heatmap likely related to autoimmune events")
  
}

plot_heat(6)
```

From the heatmap we can see clustering and labels a bit better, and there are 3-4 clusters. In general, throughout the analysis, adverse events of similar clinical groupings have been clustering together. We suspected this might be the case, but the clustering has done a better than expected job of grouping the AE terms.



