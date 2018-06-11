---
date: 2018-05-06T21:33:05-04:00
description: "Comorbitity Git HTML D3 Gist test"
featured_image: ""
tags: []
title: "Comorbitity Gist D3"
---
 
 
 
 
 
 
 


<meta charset="utf-8">
<p>
<div margin = '150px 0 150px 0'>	

<h1 align="center"> Identity graph of Adverse Event Comorbidity</h1>

<svg id='Comorb' width="900" height="500"></svg>
<svg id='Clust' width="900" height="500"></svg>


<script src="https://d3js.org/d3.v4.min.js"></script>

<style>

.links line {
  stroke: #999;
  stroke-opacity: 0.6;
}

.nodes circle {
  stroke: #fff;
  stroke-width: 0px;
}

</style>

<script>

var graph = {
  "nodes":[
		{"id" : "Abdominal adhesions", "freq": 2, "group": 1},
		{"id" : "Abdominal discomfort", "freq": 5, "group": 1},
		{"id" : "Abdominal pain lower", "freq": 18, "group": 1},
		{"id" : "Abdominal pain upper", "freq": 12, "group": 1},
		{"id" : "Abdominal pain", "freq": 21, "group": 1},
		{"id" : "Abdominal tenderness", "freq": 4, "group": 1},
		{"id" : "Abnormal behaviour", "freq": 27, "group": 1},
		{"id" : "Abnormal loss of weight", "freq": 39, "group": 1},
		{"id" : "Accident", "freq": 4, "group": 1},
		{"id" : "Accidental overdose", "freq": 14, "group": 1},
		{"id" : "Activities of daily living impaired", "freq": 18, "group": 1},
		{"id" : "Adnexal torsion", "freq": 2, "group": 1},
		{"id" : "Adverse drug reaction", "freq": 8, "group": 1},
		{"id" : "Adverse event", "freq": 15, "group": 1},
		{"id" : "Affect lability", "freq": 27, "group": 1},
		{"id" : "Affective disorder", "freq": 5, "group": 1},
		{"id" : "Aggression", "freq": 53, "group": 1},
		{"id" : "Agitation", "freq": 57, "group": 1},
		{"id" : "Akathisia", "freq": 12, "group": 1},
		{"id" : "Alcohol abuse", "freq": 3, "group": 1},
		{"id" : "Alopecia", "freq": 1, "group": 1},
		{"id" : "Amnesia", "freq": 23, "group": 1},
		{"id" : "Amphetamines negative", "freq": 2, "group": 1},
		{"id" : "Anaphylactic reaction", "freq": 24, "group": 1},
		{"id" : "Anger", "freq": 31, "group": 1},
		{"id" : "Angioedema", "freq": 4, "group": 1},
		{"id" : "Anhedonia", "freq": 17, "group": 1},
		{"id" : "Anorgasmia", "freq": 14, "group": 1},
		{"id" : "Antibody test positive", "freq": 5, "group": 1},
		{"id" : "Antisocial behaviour", "freq": 14, "group": 1},
		{"id" : "Anxiety", "freq": 134, "group": 1},
		{"id" : "Apathy", "freq": 39, "group": 1},
		{"id" : "Aphasia", "freq": 11, "group": 1},
		{"id" : "Appendicitis", "freq": 3, "group": 1},
		{"id" : "Appetite disorder", "freq": 1, "group": 1},
		{"id" : "Application site vesicles", "freq": 1, "group": 1},
		{"id" : "Arthralgia", "freq": 36, "group": 1},
		{"id" : "Arthritis", "freq": 4, "group": 1},
		{"id" : "Arthropathy", "freq": 5, "group": 1},
		{"id" : "Asthenia", "freq": 40, "group": 1},
		{"id" : "Asthma", "freq": 4, "group": 1},
		{"id" : "Attention deficit\/hyperactivity disorder", "freq": 29, "group": 1},
		{"id" : "Autoimmune disorder", "freq": 4, "group": 1},
		{"id" : "Back disorder", "freq": 11, "group": 1},
		{"id" : "Back pain", "freq": 9, "group": 1},
		{"id" : "Balance disorder", "freq": 18, "group": 1},
		{"id" : "Bedridden", "freq": 4, "group": 1},
		{"id" : "Benign intracranial hypertension", "freq": 1, "group": 1},
		{"id" : "Benign neoplasm of thyroid gland", "freq": 2, "group": 1},
		{"id" : "Binge eating", "freq": 2, "group": 1},
		{"id" : "Bipolar disorder", "freq": 25, "group": 1},
		{"id" : "Blindness unilateral", "freq": 2, "group": 1},
		{"id" : "Blood cholesterol increased", "freq": 4, "group": 1},
		{"id" : "Blood creatine phosphokinase increased", "freq": 2, "group": 1},
		{"id" : "Blood glucose decreased", "freq": 9, "group": 1},
		{"id" : "Blood glucose increased", "freq": 19, "group": 1},
		{"id" : "Blood iron abnormal", "freq": 11, "group": 1},
		{"id" : "Blood oestrogen abnormal", "freq": 3, "group": 1},
		{"id" : "Blood pressure decreased", "freq": 3, "group": 1},
		{"id" : "Blood pressure increased", "freq": 30, "group": 1},
		{"id" : "Blood pressure systolic increased", "freq": 9, "group": 1},
		{"id" : "Body temperature increased", "freq": 9, "group": 1},
		{"id" : "Bone contusion", "freq": 2, "group": 1},
		{"id" : "Brain injury", "freq": 4, "group": 1},
		{"id" : "Breakthrough pain", "freq": 4, "group": 1},
		{"id" : "Breast cancer stage IV", "freq": 1, "group": 1},
		{"id" : "Breast tenderness", "freq": 4, "group": 1},
		{"id" : "Breech presentation", "freq": 5, "group": 1},
		{"id" : "Bruxism", "freq": 20, "group": 1},
		{"id" : "Burning sensation", "freq": 6, "group": 1},
		{"id" : "Caesarean section", "freq": 4, "group": 1},
		{"id" : "Calcinosis", "freq": 4, "group": 1},
		{"id" : "Cardiac arrest", "freq": 1, "group": 1},
		{"id" : "Cardiac disorder", "freq": 1, "group": 1},
		{"id" : "Cardiac failure congestive", "freq": 21, "group": 1},
		{"id" : "Cardiomegaly", "freq": 4, "group": 1},
		{"id" : "Cardiomyopathy", "freq": 12, "group": 1},
		{"id" : "Cardiovascular disorder", "freq": 13, "group": 1},
		{"id" : "Catatonia", "freq": 5, "group": 1},
		{"id" : "Central nervous system lesion", "freq": 2, "group": 1},
		{"id" : "Cerebrovascular accident", "freq": 1, "group": 1},
		{"id" : "Cervical spinal stenosis", "freq": 3, "group": 1},
		{"id" : "Change in sustained attention", "freq": 5, "group": 1},
		{"id" : "Chest discomfort", "freq": 3, "group": 1},
		{"id" : "Chest pain", "freq": 14, "group": 1},
		{"id" : "Chills", "freq": 17, "group": 1},
		{"id" : "Complex regional pain syndrome", "freq": 13, "group": 1},
		{"id" : "Concussion", "freq": 4, "group": 1},
		{"id" : "Condition aggravated", "freq": 79, "group": 1},
		{"id" : "Confusional state", "freq": 21, "group": 1},
		{"id" : "Constipation", "freq": 35, "group": 1},
		{"id" : "Contusion", "freq": 8, "group": 1},
		{"id" : "Costochondritis", "freq": 12, "group": 1},
		{"id" : "Cough", "freq": 13, "group": 1},
		{"id" : "Crohn's disease", "freq": 12, "group": 1},
		{"id" : "Crying", "freq": 57, "group": 1},
		{"id" : "Cystic fibrosis related diabetes", "freq": 9, "group": 1},
		{"id" : "Cytogenetic abnormality", "freq": 7, "group": 1},
		{"id" : "Decreased appetite", "freq": 75, "group": 1},
		{"id" : "Decreased interest", "freq": 12, "group": 1},
		{"id" : "Dehydration", "freq": 4, "group": 1},
		{"id" : "Delusion", "freq": 2, "group": 1},
		{"id" : "Dental care", "freq": 1, "group": 1},
		{"id" : "Depressed level of consciousness", "freq": 3, "group": 1},
		{"id" : "Depressed mood", "freq": 13, "group": 1},
		{"id" : "Depression", "freq": 99, "group": 1},
		{"id" : "Derealisation", "freq": 7, "group": 1},
		{"id" : "Dermatitis", "freq": 20, "group": 1},
		{"id" : "Device breakage", "freq": 6, "group": 1},
		{"id" : "Diabetes mellitus", "freq": 2, "group": 1},
		{"id" : "Diarrhoea", "freq": 25, "group": 1},
		{"id" : "Disability", "freq": 12, "group": 1},
		{"id" : "Discomfort", "freq": 16, "group": 1},
		{"id" : "Disease progression", "freq": 13, "group": 1},
		{"id" : "Disorganised speech", "freq": 5, "group": 1},
		{"id" : "Disorientation", "freq": 4, "group": 1},
		{"id" : "Dissociation", "freq": 9, "group": 1},
		{"id" : "Disturbance in attention", "freq": 85, "group": 1},
		{"id" : "Disturbance in social behaviour", "freq": 47, "group": 1},
		{"id" : "Diverticulitis", "freq": 20, "group": 1},
		{"id" : "Dizziness", "freq": 39, "group": 1},
		{"id" : "Drug abuse", "freq": 9, "group": 1},
		{"id" : "Drug administered at inappropriate site", "freq": 2, "group": 1},
		{"id" : "Drug administered to patient of inappropriate age", "freq": 36, "group": 1},
		{"id" : "Drug dispensing error", "freq": 1, "group": 1},
		{"id" : "Drug diversion", "freq": 11, "group": 1},
		{"id" : "Drug dose omission", "freq": 80, "group": 1},
		{"id" : "Drug dose titration not performed", "freq": 2, "group": 1},
		{"id" : "Drug effect decreased", "freq": 102, "group": 1},
		{"id" : "Drug effect delayed", "freq": 8, "group": 1},
		{"id" : "Drug effect incomplete", "freq": 4, "group": 1},
		{"id" : "Drug effect increased", "freq": 34, "group": 1},
		{"id" : "Drug effect variable", "freq": 11, "group": 1},
		{"id" : "Drug hypersensitivity", "freq": 8, "group": 1},
		{"id" : "Drug ineffective", "freq": 140, "group": 1},
		{"id" : "Drug interaction", "freq": 28, "group": 1},
		{"id" : "Drug prescribing error", "freq": 1, "group": 1},
		{"id" : "Drug screen false positive", "freq": 1, "group": 1},
		{"id" : "Drug screen negative", "freq": 2, "group": 1},
		{"id" : "Drug tolerance", "freq": 15, "group": 1},
		{"id" : "Drug withdrawal convulsions", "freq": 11, "group": 1},
		{"id" : "Drug withdrawal syndrome neonatal", "freq": 5, "group": 1},
		{"id" : "Drug withdrawal syndrome", "freq": 13, "group": 1},
		{"id" : "Dry mouth", "freq": 16, "group": 1},
		{"id" : "Dry skin", "freq": 10, "group": 1},
		{"id" : "Dysgeusia", "freq": 10, "group": 1},
		{"id" : "Dysgraphia", "freq": 11, "group": 1},
		{"id" : "Dyskinesia", "freq": 22, "group": 1},
		{"id" : "Dyspareunia", "freq": 10, "group": 1},
		{"id" : "Dyspepsia", "freq": 9, "group": 1},
		{"id" : "Dysphagia", "freq": 1, "group": 1},
		{"id" : "Dyspnoea", "freq": 22, "group": 1},
		{"id" : "Dysuria", "freq": 4, "group": 1},
		{"id" : "Educational problem", "freq": 12, "group": 1},
		{"id" : "Embolism arterial", "freq": 1, "group": 1},
		{"id" : "Emotional disorder", "freq": 23, "group": 1},
		{"id" : "Emotional distress", "freq": 14, "group": 1},
		{"id" : "Eosinophilic oesophagitis", "freq": 14, "group": 1},
		{"id" : "Epistaxis", "freq": 34, "group": 1},
		{"id" : "Erythema", "freq": 4, "group": 1},
		{"id" : "Euphoric mood", "freq": 5, "group": 1},
		{"id" : "Eye irritation", "freq": 21, "group": 1},
		{"id" : "Eye movement disorder", "freq": 13, "group": 1},
		{"id" : "Eye swelling", "freq": 6, "group": 1},
		{"id" : "Faecal incontinence", "freq": 2, "group": 1},
		{"id" : "Fall", "freq": 16, "group": 1},
		{"id" : "Family stress", "freq": 2, "group": 1},
		{"id" : "Fatigue", "freq": 111, "group": 1},
		{"id" : "Fear", "freq": 36, "group": 1},
		{"id" : "Feeding disorder", "freq": 20, "group": 1},
		{"id" : "Feeling abnormal", "freq": 85, "group": 1},
		{"id" : "Feeling hot", "freq": 2, "group": 1},
		{"id" : "Feeling jittery", "freq": 13, "group": 1},
		{"id" : "Feeling of despair", "freq": 7, "group": 1},
		{"id" : "Feeling of relaxation", "freq": 4, "group": 1},
		{"id" : "Fibromyalgia", "freq": 4, "group": 1},
		{"id" : "Flat affect", "freq": 19, "group": 1},
		{"id" : "Flatulence", "freq": 2, "group": 1},
		{"id" : "Flight of ideas", "freq": 8, "group": 1},
		{"id" : "Fluid overload", "freq": 9, "group": 1},
		{"id" : "Flushing", "freq": 11, "group": 1},
		{"id" : "Foetal distress syndrome", "freq": 5, "group": 1},
		{"id" : "Foetal exposure during pregnancy", "freq": 5, "group": 1},
		{"id" : "Food craving", "freq": 1, "group": 1},
		{"id" : "Food hoarding", "freq": 4, "group": 1},
		{"id" : "Foot fracture", "freq": 3, "group": 1},
		{"id" : "Foot operation", "freq": 7, "group": 1},
		{"id" : "Foreign body", "freq": 2, "group": 1},
		{"id" : "Formication", "freq": 20, "group": 1},
		{"id" : "Frustration", "freq": 22, "group": 1},
		{"id" : "Fungal infection", "freq": 10, "group": 1},
		{"id" : "Gait disturbance", "freq": 18, "group": 1},
		{"id" : "Gastritis", "freq": 23, "group": 1},
		{"id" : "Gastroenteritis viral", "freq": 13, "group": 1},
		{"id" : "Gastrointestinal stenosis", "freq": 5, "group": 1},
		{"id" : "Gastrooesophageal reflux disease", "freq": 16, "group": 1},
		{"id" : "General physical health deterioration", "freq": 20, "group": 1},
		{"id" : "Genital haemorrhage", "freq": 12, "group": 1},
		{"id" : "Glossodynia", "freq": 1, "group": 1},
		{"id" : "Glucose tolerance impaired", "freq": 1, "group": 1},
		{"id" : "Grief reaction", "freq": 12, "group": 1},
		{"id" : "Grimacing", "freq": 1, "group": 1},
		{"id" : "Growing pains", "freq": 12, "group": 1},
		{"id" : "Growth accelerated", "freq": 14, "group": 1},
		{"id" : "Gynaecomastia", "freq": 4, "group": 1},
		{"id" : "Haemophobia", "freq": 1, "group": 1},
		{"id" : "Haemorrhagic diathesis", "freq": 3, "group": 1},
		{"id" : "Haemorrhoids", "freq": 14, "group": 1},
		{"id" : "Hair colour changes", "freq": 2, "group": 1},
		{"id" : "Hair texture abnormal", "freq": 2, "group": 1},
		{"id" : "Hallucination", "freq": 1, "group": 1},
		{"id" : "Hallucinations, mixed", "freq": 11, "group": 1},
		{"id" : "Hangover", "freq": 1, "group": 1},
		{"id" : "Headache", "freq": 78, "group": 1},
		{"id" : "Heart rate decreased", "freq": 18, "group": 1},
		{"id" : "Heart rate increased", "freq": 4, "group": 1},
		{"id" : "Heart rate irregular", "freq": 4, "group": 1},
		{"id" : "Hepatic enzyme increased", "freq": 17, "group": 1},
		{"id" : "Hepatitis C", "freq": 1, "group": 1},
		{"id" : "Hernia", "freq": 1, "group": 1},
		{"id" : "Hormone level abnormal", "freq": 10, "group": 1},
		{"id" : "Hospitalisation", "freq": 9, "group": 1},
		{"id" : "Hostility", "freq": 21, "group": 1},
		{"id" : "Hot flush", "freq": 7, "group": 1},
		{"id" : "House dust allergy", "freq": 2, "group": 1},
		{"id" : "Hunger", "freq": 7, "group": 1},
		{"id" : "Hyperhidrosis", "freq": 13, "group": 1},
		{"id" : "Hyperphagia", "freq": 13, "group": 1},
		{"id" : "Hypersensitivity", "freq": 22, "group": 1},
		{"id" : "Hypersomnia", "freq": 34, "group": 1},
		{"id" : "Hypertension", "freq": 8, "group": 1},
		{"id" : "Hyperventilation", "freq": 4, "group": 1},
		{"id" : "Hypoaesthesia oral", "freq": 9, "group": 1},
		{"id" : "Hypoaesthesia", "freq": 32, "group": 1},
		{"id" : "Hypokinesia", "freq": 2, "group": 1},
		{"id" : "Hypophagia", "freq": 1, "group": 1},
		{"id" : "Hypotension", "freq": 18, "group": 1},
		{"id" : "Hypothyroidism", "freq": 12, "group": 1},
		{"id" : "Impaired driving ability", "freq": 9, "group": 1},
		{"id" : "Impaired healing", "freq": 18, "group": 1},
		{"id" : "Impaired work ability", "freq": 26, "group": 1},
		{"id" : "Implant tissue necrosis", "freq": 1, "group": 1},
		{"id" : "Impulse-control disorder", "freq": 2, "group": 1},
		{"id" : "Impulsive behaviour", "freq": 20, "group": 1},
		{"id" : "Inappropriate schedule of drug administration", "freq": 48, "group": 1},
		{"id" : "Incoherent", "freq": 11, "group": 1},
		{"id" : "Incorrect dose administered", "freq": 45, "group": 1},
		{"id" : "Increased appetite", "freq": 51, "group": 1},
		{"id" : "Infection", "freq": 6, "group": 1},
		{"id" : "Influenza like illness", "freq": 4, "group": 1},
		{"id" : "Infusion related reaction", "freq": 5, "group": 1},
		{"id" : "Initial insomnia", "freq": 8, "group": 1},
		{"id" : "Injection site bruising", "freq": 3, "group": 1},
		{"id" : "Injection site pain", "freq": 8, "group": 1},
		{"id" : "Injection site reaction", "freq": 3, "group": 1},
		{"id" : "Injection site swelling", "freq": 3, "group": 1},
		{"id" : "Injury", "freq": 21, "group": 1},
		{"id" : "Insomnia", "freq": 94, "group": 1},
		{"id" : "Intentional overdose", "freq": 12, "group": 1},
		{"id" : "Intentional product misuse", "freq": 2, "group": 1},
		{"id" : "Intentional self-injury", "freq": 13, "group": 1},
		{"id" : "Intervertebral disc protrusion", "freq": 18, "group": 1},
		{"id" : "Intestinal obstruction", "freq": 2, "group": 1},
		{"id" : "Intestinal polyp", "freq": 5, "group": 1},
		{"id" : "Invasive ductal breast carcinoma", "freq": 18, "group": 1},
		{"id" : "Irregular breathing", "freq": 1, "group": 1},
		{"id" : "Irritability", "freq": 33, "group": 1},
		{"id" : "Irritable bowel syndrome", "freq": 8, "group": 1},
		{"id" : "Jaundice neonatal", "freq": 5, "group": 1},
		{"id" : "Job dissatisfaction", "freq": 6, "group": 1},
		{"id" : "Joint stiffness", "freq": 4, "group": 1},
		{"id" : "Knee operation", "freq": 7, "group": 1},
		{"id" : "Lactose intolerance", "freq": 14, "group": 1},
		{"id" : "Large intestinal stenosis", "freq": 5, "group": 1},
		{"id" : "Laziness", "freq": 32, "group": 1},
		{"id" : "Learning disorder", "freq": 1, "group": 1},
		{"id" : "Legal problem", "freq": 2, "group": 1},
		{"id" : "Lethargy", "freq": 12, "group": 1},
		{"id" : "Leukopenia", "freq": 1, "group": 1},
		{"id" : "Libido decreased", "freq": 18, "group": 1},
		{"id" : "Limb discomfort", "freq": 2, "group": 1},
		{"id" : "Limb injury", "freq": 7, "group": 1},
		{"id" : "Lip exfoliation", "freq": 4, "group": 1},
		{"id" : "Lip haemorrhage", "freq": 4, "group": 1},
		{"id" : "Lip swelling", "freq": 10, "group": 1},
		{"id" : "Lipids increased", "freq": 3, "group": 1},
		{"id" : "Local swelling", "freq": 4, "group": 1},
		{"id" : "Logorrhoea", "freq": 24, "group": 1},
		{"id" : "Loss of consciousness", "freq": 19, "group": 1},
		{"id" : "Loss of control of legs", "freq": 9, "group": 1},
		{"id" : "Loss of employment", "freq": 3, "group": 1},
		{"id" : "Malabsorption", "freq": 11, "group": 1},
		{"id" : "Malaise", "freq": 62, "group": 1},
		{"id" : "Mania", "freq": 21, "group": 1},
		{"id" : "Maternal exposure during pregnancy", "freq": 4, "group": 1},
		{"id" : "Medical device discomfort", "freq": 12, "group": 1},
		{"id" : "Medical device pain", "freq": 12, "group": 1},
		{"id" : "Memory impairment", "freq": 34, "group": 1},
		{"id" : "Meniscus injury", "freq": 4, "group": 1},
		{"id" : "Menorrhagia", "freq": 1, "group": 1},
		{"id" : "Mental disorder", "freq": 16, "group": 1},
		{"id" : "Mental impairment", "freq": 34, "group": 1},
		{"id" : "Metrorrhagia", "freq": 1, "group": 1},
		{"id" : "Micturition urgency", "freq": 1, "group": 1},
		{"id" : "Migraine", "freq": 28, "group": 1},
		{"id" : "Mood altered", "freq": 11, "group": 1},
		{"id" : "Mood swings", "freq": 20, "group": 1},
		{"id" : "Motor dysfunction", "freq": 7, "group": 1},
		{"id" : "Mouth swelling", "freq": 4, "group": 1},
		{"id" : "Movement disorder", "freq": 12, "group": 1},
		{"id" : "Multiple sclerosis", "freq": 3, "group": 1},
		{"id" : "Muscle injury", "freq": 4, "group": 1},
		{"id" : "Muscle spasms", "freq": 32, "group": 1},
		{"id" : "Muscle twitching", "freq": 9, "group": 1},
		{"id" : "Musculoskeletal disorder", "freq": 8, "group": 1},
		{"id" : "Musculoskeletal pain", "freq": 10, "group": 1},
		{"id" : "Musculoskeletal stiffness", "freq": 15, "group": 1},
		{"id" : "Myalgia", "freq": 14, "group": 1},
		{"id" : "Mycobacterium test positive", "freq": 9, "group": 1},
		{"id" : "Mydriasis", "freq": 12, "group": 1},
		{"id" : "Myoclonic epilepsy", "freq": 7, "group": 1},
		{"id" : "Narcolepsy", "freq": 2, "group": 1},
		{"id" : "Nasal discomfort", "freq": 4, "group": 1},
		{"id" : "Nasopharyngitis", "freq": 37, "group": 1},
		{"id" : "Nausea", "freq": 65, "group": 1},
		{"id" : "Neck pain", "freq": 16, "group": 1},
		{"id" : "Negative thoughts", "freq": 5, "group": 1},
		{"id" : "Nerve injury", "freq": 13, "group": 1},
		{"id" : "Nervousness", "freq": 8, "group": 1},
		{"id" : "Neuralgia", "freq": 4, "group": 1},
		{"id" : "Neutropenia", "freq": 1, "group": 1},
		{"id" : "Nightmare", "freq": 21, "group": 1},
		{"id" : "No adverse event", "freq": 11, "group": 1},
		{"id" : "No therapeutic response", "freq": 9, "group": 1},
		{"id" : "Nonspecific reaction", "freq": 13, "group": 1},
		{"id" : "Obsessive thoughts", "freq": 17, "group": 1},
		{"id" : "Obsessive-compulsive disorder", "freq": 4, "group": 1},
		{"id" : "Obstructive airways disorder", "freq": 9, "group": 1},
		{"id" : "Oedema peripheral", "freq": 12, "group": 1},
		{"id" : "Oedema", "freq": 9, "group": 1},
		{"id" : "Oesophagitis", "freq": 11, "group": 1},
		{"id" : "Off label use", "freq": 31, "group": 1},
		{"id" : "Optic nerve neoplasm", "freq": 11, "group": 1},
		{"id" : "Oral administration complication", "freq": 10, "group": 1},
		{"id" : "Oral candidiasis", "freq": 2, "group": 1},
		{"id" : "Oral discomfort", "freq": 5, "group": 1},
		{"id" : "Osteoarthritis", "freq": 20, "group": 1},
		{"id" : "Overdose", "freq": 4, "group": 1},
		{"id" : "Oxygen saturation decreased", "freq": 9, "group": 1},
		{"id" : "Pain in extremity", "freq": 28, "group": 1},
		{"id" : "Pain in jaw", "freq": 12, "group": 1},
		{"id" : "Pain", "freq": 60, "group": 1},
		{"id" : "Pallor", "freq": 2, "group": 1},
		{"id" : "Palpitations", "freq": 20, "group": 1},
		{"id" : "Panic attack", "freq": 31, "group": 1},
		{"id" : "Panic disorder", "freq": 7, "group": 1},
		{"id" : "Panic reaction", "freq": 3, "group": 1},
		{"id" : "Papilloedema", "freq": 1, "group": 1},
		{"id" : "Paraesthesia oral", "freq": 3, "group": 1},
		{"id" : "Paraesthesia", "freq": 33, "group": 1},
		{"id" : "Paranasal sinus hypersecretion", "freq": 9, "group": 1},
		{"id" : "Paranoia", "freq": 11, "group": 1},
		{"id" : "Performance status decreased", "freq": 23, "group": 1},
		{"id" : "Peripheral swelling", "freq": 9, "group": 1},
		{"id" : "Peripheral vascular disorder", "freq": 1, "group": 1},
		{"id" : "Personality change", "freq": 10, "group": 1},
		{"id" : "Pharyngitis streptococcal", "freq": 9, "group": 1},
		{"id" : "Pleural effusion", "freq": 12, "group": 1},
		{"id" : "Pneumonia", "freq": 28, "group": 1},
		{"id" : "Pollakiuria", "freq": 1, "group": 1},
		{"id" : "Poor quality sleep", "freq": 20, "group": 1},
		{"id" : "Post procedural discomfort", "freq": 12, "group": 1},
		{"id" : "Post-traumatic neck syndrome", "freq": 4, "group": 1},
		{"id" : "Pre-existing condition improved", "freq": 2, "group": 1},
		{"id" : "Premature baby", "freq": 5, "group": 1},
		{"id" : "Premature delivery", "freq": 4, "group": 1},
		{"id" : "Prescribed overdose", "freq": 25, "group": 1},
		{"id" : "Prescribed underdose", "freq": 2, "group": 1},
		{"id" : "Procedural pain", "freq": 12, "group": 1},
		{"id" : "Product quality issue", "freq": 63, "group": 1},
		{"id" : "Product substitution issue", "freq": 21, "group": 1},
		{"id" : "Product tampering", "freq": 4, "group": 1},
		{"id" : "Product use issue", "freq": 45, "group": 1},
		{"id" : "Pruritus generalised", "freq": 1, "group": 1},
		{"id" : "Pruritus", "freq": 13, "group": 1},
		{"id" : "Pseudomonas infection", "freq": 9, "group": 1},
		{"id" : "Psychiatric symptom", "freq": 7, "group": 1},
		{"id" : "Psychomotor hyperactivity", "freq": 37, "group": 1},
		{"id" : "Psychotic disorder", "freq": 23, "group": 1},
		{"id" : "Pulmonary arterial hypertension", "freq": 9, "group": 1},
		{"id" : "Pulmonary embolism", "freq": 7, "group": 1},
		{"id" : "Pulmonary mass", "freq": 1, "group": 1},
		{"id" : "Pyoderma gangrenosum", "freq": 1, "group": 1},
		{"id" : "Pyrexia", "freq": 35, "group": 1},
		{"id" : "Radiculitis brachial", "freq": 13, "group": 1},
		{"id" : "Rales", "freq": 9, "group": 1},
		{"id" : "Rapid eye movements sleep abnormal", "freq": 16, "group": 1},
		{"id" : "Rash erythematous", "freq": 2, "group": 1},
		{"id" : "Rash macular", "freq": 3, "group": 1},
		{"id" : "Rash pruritic", "freq": 20, "group": 1},
		{"id" : "Rash pustular", "freq": 18, "group": 1},
		{"id" : "Rash", "freq": 11, "group": 1},
		{"id" : "Rebound effect", "freq": 5, "group": 1},
		{"id" : "Renal impairment", "freq": 2, "group": 1},
		{"id" : "Respiratory failure", "freq": 9, "group": 1},
		{"id" : "Respiratory tract infection", "freq": 3, "group": 1},
		{"id" : "Restlessness", "freq": 32, "group": 1},
		{"id" : "Retching", "freq": 4, "group": 1},
		{"id" : "Rhesus incompatibility", "freq": 4, "group": 1},
		{"id" : "Rhinalgia", "freq": 4, "group": 1},
		{"id" : "Right ventricular failure", "freq": 9, "group": 1},
		{"id" : "Road traffic accident", "freq": 32, "group": 1},
		{"id" : "Sarcoidosis", "freq": 1, "group": 1},
		{"id" : "Scab", "freq": 3, "group": 1},
		{"id" : "Scar", "freq": 20, "group": 1},
		{"id" : "Screaming", "freq": 9, "group": 1},
		{"id" : "Seizure", "freq": 22, "group": 1},
		{"id" : "Self injurious behaviour", "freq": 6, "group": 1},
		{"id" : "Self-injurious ideation", "freq": 5, "group": 1},
		{"id" : "Sensory loss", "freq": 4, "group": 1},
		{"id" : "Serotonin syndrome", "freq": 9, "group": 1},
		{"id" : "Severe acute respiratory syndrome", "freq": 12, "group": 1},
		{"id" : "Sexual dysfunction", "freq": 1, "group": 1},
		{"id" : "Shoulder arthroplasty", "freq": 1, "group": 1},
		{"id" : "Sinus disorder", "freq": 13, "group": 1},
		{"id" : "Sinus headache", "freq": 4, "group": 1},
		{"id" : "Sinusitis", "freq": 5, "group": 1},
		{"id" : "Sjogren's syndrome", "freq": 4, "group": 1},
		{"id" : "Skin candida", "freq": 2, "group": 1},
		{"id" : "Skin discolouration", "freq": 4, "group": 1},
		{"id" : "Skin exfoliation", "freq": 1, "group": 1},
		{"id" : "Skin mass", "freq": 18, "group": 1},
		{"id" : "Sleep apnoea syndrome", "freq": 4, "group": 1},
		{"id" : "Sleep disorder", "freq": 27, "group": 1},
		{"id" : "Sluggishness", "freq": 3, "group": 1},
		{"id" : "Social avoidant behaviour", "freq": 30, "group": 1},
		{"id" : "Social phobia", "freq": 21, "group": 1},
		{"id" : "Somnambulism", "freq": 4, "group": 1},
		{"id" : "Somnolence", "freq": 44, "group": 1},
		{"id" : "Spinal osteoarthritis", "freq": 3, "group": 1},
		{"id" : "Stereotypy", "freq": 2, "group": 1},
		{"id" : "Stress urinary incontinence", "freq": 1, "group": 1},
		{"id" : "Stress", "freq": 26, "group": 1},
		{"id" : "Suicidal ideation", "freq": 19, "group": 1},
		{"id" : "Suicide attempt", "freq": 5, "group": 1},
		{"id" : "Surgery", "freq": 4, "group": 1},
		{"id" : "Swelling face", "freq": 3, "group": 1},
		{"id" : "Swollen tongue", "freq": 2, "group": 1},
		{"id" : "Syncope", "freq": 20, "group": 1},
		{"id" : "Syringe issue", "freq": 1, "group": 1},
		{"id" : "Tachycardia", "freq": 3, "group": 1},
		{"id" : "Tachyphrenia", "freq": 33, "group": 1},
		{"id" : "Tearfulness", "freq": 14, "group": 1},
		{"id" : "Tension", "freq": 4, "group": 1},
		{"id" : "Therapeutic product ineffective", "freq": 1, "group": 1},
		{"id" : "Therapeutic response unexpected", "freq": 24, "group": 1},
		{"id" : "Therapy cessation", "freq": 28, "group": 1},
		{"id" : "Thinking abnormal", "freq": 12, "group": 1},
		{"id" : "Thirst", "freq": 25, "group": 1},
		{"id" : "Thoracic outlet syndrome", "freq": 13, "group": 1},
		{"id" : "Thyroid disorder", "freq": 2, "group": 1},
		{"id" : "Tic", "freq": 19, "group": 1},
		{"id" : "Tinnitus", "freq": 5, "group": 1},
		{"id" : "Tobacco user", "freq": 1, "group": 1},
		{"id" : "Tooth infection", "freq": 20, "group": 1},
		{"id" : "Tooth loss", "freq": 20, "group": 1},
		{"id" : "Toothache", "freq": 20, "group": 1},
		{"id" : "Tourette's disorder", "freq": 11, "group": 1},
		{"id" : "Toxicity to various agents", "freq": 3, "group": 1},
		{"id" : "Transfusion", "freq": 4, "group": 1},
		{"id" : "Treatment noncompliance", "freq": 1, "group": 1},
		{"id" : "Tremor", "freq": 15, "group": 1},
		{"id" : "Trismus", "freq": 4, "group": 1},
		{"id" : "Type 2 diabetes mellitus", "freq": 1, "group": 1},
		{"id" : "Underdose", "freq": 3, "group": 1},
		{"id" : "Underweight", "freq": 17, "group": 1},
		{"id" : "Unevaluable event", "freq": 15, "group": 1},
		{"id" : "Upper respiratory tract infection", "freq": 9, "group": 1},
		{"id" : "Upper-airway cough syndrome", "freq": 4, "group": 1},
		{"id" : "Urinary hesitation", "freq": 18, "group": 1},
		{"id" : "Urinary incontinence", "freq": 5, "group": 1},
		{"id" : "Urinary retention", "freq": 18, "group": 1},
		{"id" : "Urinary tract infection", "freq": 3, "group": 1},
		{"id" : "Urine amphetamine negative", "freq": 1, "group": 1},
		{"id" : "Urticaria", "freq": 7, "group": 1},
		{"id" : "Uterine perforation", "freq": 12, "group": 1},
		{"id" : "Vaginal discharge", "freq": 10, "group": 1},
		{"id" : "Vaginal haemorrhage", "freq": 1, "group": 1},
		{"id" : "Vaginal pH increased", "freq": 10, "group": 1},
		{"id" : "Vertigo", "freq": 26, "group": 1},
		{"id" : "Victim of abuse", "freq": 13, "group": 1},
		{"id" : "Victim of sexual abuse", "freq": 13, "group": 1},
		{"id" : "Viral infection", "freq": 12, "group": 1},
		{"id" : "Vision blurred", "freq": 6, "group": 1},
		{"id" : "Visual acuity reduced", "freq": 4, "group": 1},
		{"id" : "Vitamin D abnormal", "freq": 11, "group": 1},
		{"id" : "Vitamin D deficiency", "freq": 3, "group": 1},
		{"id" : "Vitreous floaters", "freq": 11, "group": 1},
		{"id" : "Vomiting", "freq": 55, "group": 1},
		{"id" : "Vulvovaginal dryness", "freq": 10, "group": 1},
		{"id" : "Vulvovaginal erythema", "freq": 10, "group": 1},
		{"id" : "Vulvovaginal pain", "freq": 10, "group": 1},
		{"id" : "Vulvovaginal swelling", "freq": 10, "group": 1},
		{"id" : "Weight decreased", "freq": 31, "group": 1},
		{"id" : "Weight increased", "freq": 72, "group": 1},
		{"id" : "White blood cell count increased", "freq": 2, "group": 1},
		{"id" : "Withdrawal syndrome", "freq": 6, "group": 1},
		{"id" : "Wrist fracture", "freq": 9, "group": 1},
		{"id" : "Wrong technique in product usage process", "freq": 41, "group": 1},
		{"id" : "Yawning", "freq": 10, "group": 1},
		{"id" : "Yellow skin", "freq": 4, "group": 1}
  ],

  "links": [
		  {
		    "source": "Abdominal adhesions",
		    "target": "Crohn's disease",
		    "weight": 0.3333
		  },
		  {
		    "source": "Abdominal adhesions",
		    "target": "Intestinal obstruction",
		    "weight": 0.3333
		  },
		  {
		    "source": "Abdominal discomfort",
		    "target": "Chest discomfort",
		    "weight": 0.3333
		  },
		  {
		    "source": "Abdominal discomfort",
		    "target": "Decreased appetite",
		    "weight": 0.3333
		  },
		  {
		    "source": "Abdominal discomfort",
		    "target": "Drug interaction",
		    "weight": 0.3333
		  },
		  {
		    "source": "Abdominal discomfort",
		    "target": "Dry mouth",
		    "weight": 0.3333
		  },
		  {
		    "source": "Abdominal discomfort",
		    "target": "Grimacing",
		    "weight": 0.5
		  },
		  {
		    "source": "Abdominal pain",
		    "target": "Aggression",
		    "weight": 0.3889
		  },
		  {
		    "source": "Abdominal pain",
		    "target": "Agitation",
		    "weight": 0.0556
		  },
		  {
		    "source": "Abdominal pain",
		    "target": "Anxiety",
		    "weight": 0.0556
		  },
		  {
		    "source": "Abdominal pain",
		    "target": "Crying",
		    "weight": 0.0556
		  },
		  {
		    "source": "Abdominal pain",
		    "target": "Decreased appetite",
		    "weight": 0.7222
		  },
		  {
		    "source": "Abdominal pain",
		    "target": "Diarrhoea",
		    "weight": 0.3333
		  },
		  {
		    "source": "Abdominal pain",
		    "target": "Dizziness",
		    "weight": 0.0556
		  },
		  {
		    "source": "Abdominal pain",
		    "target": "Drug effect decreased",
		    "weight": 0.0556
		  },
		  {
		    "source": "Abdominal pain",
		    "target": "Epistaxis",
		    "weight": 0.0556
		  },
		  {
		    "source": "Abdominal pain",
		    "target": "Flat affect",
		    "weight": 0.0556
		  },
		  {
		    "source": "Abdominal pain",
		    "target": "Headache",
		    "weight": 0.0556
		  },
		  {
		    "source": "Abdominal pain",
		    "target": "Influenza like illness",
		    "weight": 0.3333
		  },
		  {
		    "source": "Abdominal pain",
		    "target": "Insomnia",
		    "weight": 0.0556
		  },
		  {
		    "source": "Abdominal pain",
		    "target": "Irritability",
		    "weight": 0.3889
		  },
		  {
		    "source": "Abdominal pain",
		    "target": "Nausea",
		    "weight": 0.0556
		  },
		  {
		    "source": "Abdominal pain",
		    "target": "Obsessive thoughts",
		    "weight": 0.0556
		  },
		  {
		    "source": "Abdominal pain",
		    "target": "Oral candidiasis",
		    "weight": 0.3333
		  },
		  {
		    "source": "Abdominal pain",
		    "target": "Skin candida",
		    "weight": 0.3333
		  },
		  {
		    "source": "Abdominal pain",
		    "target": "Social avoidant behaviour",
		    "weight": 0.0556
		  },
		  {
		    "source": "Abdominal pain",
		    "target": "Tic",
		    "weight": 0.0556
		  },
		  {
		    "source": "Abdominal pain",
		    "target": "Vomiting",
		    "weight": 0.0556
		  },
		  {
		    "source": "Abdominal pain lower",
		    "target": "Anhedonia",
		    "weight": 0.0769
		  },
		  {
		    "source": "Abdominal pain lower",
		    "target": "Anxiety",
		    "weight": 0.0769
		  },
		  {
		    "source": "Abdominal pain lower",
		    "target": "Appendicitis",
		    "weight": 0.25
		  },
		  {
		    "source": "Abdominal pain lower",
		    "target": "Emotional distress",
		    "weight": 0.0769
		  },
		  {
		    "source": "Abdominal pain lower",
		    "target": "Flushing",
		    "weight": 0.25
		  },
		  {
		    "source": "Abdominal pain lower",
		    "target": "Frustration",
		    "weight": 0.0769
		  },
		  {
		    "source": "Abdominal pain lower",
		    "target": "Gastritis",
		    "weight": 0.25
		  },
		  {
		    "source": "Abdominal pain lower",
		    "target": "General physical health deterioration",
		    "weight": 0.0769
		  },
		  {
		    "source": "Abdominal pain lower",
		    "target": "Genital haemorrhage",
		    "weight": 0.0769
		  },
		  {
		    "source": "Abdominal pain lower",
		    "target": "Hyperhidrosis",
		    "weight": 0.25
		  },
		  {
		    "source": "Abdominal pain lower",
		    "target": "Injury",
		    "weight": 0.0769
		  },
		  {
		    "source": "Abdominal pain lower",
		    "target": "Medical device discomfort",
		    "weight": 0.0769
		  },
		  {
		    "source": "Abdominal pain lower",
		    "target": "Medical device pain",
		    "weight": 0.0769
		  },
		  {
		    "source": "Abdominal pain lower",
		    "target": "Post procedural discomfort",
		    "weight": 0.0769
		  },
		  {
		    "source": "Abdominal pain lower",
		    "target": "Procedural pain",
		    "weight": 0.0769
		  },
		  {
		    "source": "Abdominal pain lower",
		    "target": "Pyrexia",
		    "weight": 0.25
		  },
		  {
		    "source": "Abdominal pain lower",
		    "target": "Uterine perforation",
		    "weight": 0.0769
		  },
		  {
		    "source": "Abdominal pain lower",
		    "target": "Vomiting",
		    "weight": 0.25
		  },
		  {
		    "source": "Abdominal pain upper",
		    "target": "Anxiety",
		    "weight": 0.2
		  },
		  {
		    "source": "Abdominal pain upper",
		    "target": "Attention deficit\/hyperactivity disorder",
		    "weight": 0.2
		  },
		  {
		    "source": "Abdominal pain upper",
		    "target": "Condition aggravated",
		    "weight": 0.2
		  },
		  {
		    "source": "Abdominal pain upper",
		    "target": "Decreased appetite",
		    "weight": 0.2
		  },
		  {
		    "source": "Abdominal pain upper",
		    "target": "Disturbance in social behaviour",
		    "weight": 0.2
		  },
		  {
		    "source": "Abdominal pain upper",
		    "target": "Drug dose omission",
		    "weight": 0.2
		  },
		  {
		    "source": "Abdominal pain upper",
		    "target": "Fatigue",
		    "weight": 0.2
		  },
		  {
		    "source": "Abdominal pain upper",
		    "target": "Gastroenteritis viral",
		    "weight": 0.2
		  },
		  {
		    "source": "Abdominal pain upper",
		    "target": "Headache",
		    "weight": 0.7
		  },
		  {
		    "source": "Abdominal pain upper",
		    "target": "Malaise",
		    "weight": 0.2
		  },
		  {
		    "source": "Abdominal pain upper",
		    "target": "Mania",
		    "weight": 0.2
		  },
		  {
		    "source": "Abdominal pain upper",
		    "target": "Therapy cessation",
		    "weight": 0.2
		  },
		  {
		    "source": "Abdominal tenderness",
		    "target": "Headache",
		    "weight": 0.2
		  },
		  {
		    "source": "Abdominal tenderness",
		    "target": "Hunger",
		    "weight": 0.2
		  },
		  {
		    "source": "Abdominal tenderness",
		    "target": "Insomnia",
		    "weight": 0.2
		  },
		  {
		    "source": "Abdominal tenderness",
		    "target": "Nausea",
		    "weight": 0.2
		  },
		  {
		    "source": "Abnormal behaviour",
		    "target": "Accidental overdose",
		    "weight": 0.1111
		  },
		  {
		    "source": "Abnormal behaviour",
		    "target": "Anxiety",
		    "weight": 0.1111
		  },
		  {
		    "source": "Abnormal behaviour",
		    "target": "Condition aggravated",
		    "weight": 0.2
		  },
		  {
		    "source": "Abnormal behaviour",
		    "target": "Depression",
		    "weight": 0.1111
		  },
		  {
		    "source": "Abnormal behaviour",
		    "target": "Disturbance in attention",
		    "weight": 0.3095
		  },
		  {
		    "source": "Abnormal behaviour",
		    "target": "Drug dose omission",
		    "weight": 0.75
		  },
		  {
		    "source": "Abnormal behaviour",
		    "target": "Drug effect decreased",
		    "weight": 0.3095
		  },
		  {
		    "source": "Abnormal behaviour",
		    "target": "Drug effect variable",
		    "weight": 0.5
		  },
		  {
		    "source": "Abnormal behaviour",
		    "target": "Drug ineffective",
		    "weight": 0.2
		  },
		  {
		    "source": "Abnormal behaviour",
		    "target": "Educational problem",
		    "weight": 0.3095
		  },
		  {
		    "source": "Abnormal behaviour",
		    "target": "Emotional disorder",
		    "weight": 0.1429
		  },
		  {
		    "source": "Abnormal behaviour",
		    "target": "Euphoric mood",
		    "weight": 0.1667
		  },
		  {
		    "source": "Abnormal behaviour",
		    "target": "Feeling abnormal",
		    "weight": 0.1111
		  },
		  {
		    "source": "Abnormal behaviour",
		    "target": "Impulsive behaviour",
		    "weight": 0.1667
		  },
		  {
		    "source": "Abnormal behaviour",
		    "target": "Infection",
		    "weight": 0.1429
		  },
		  {
		    "source": "Abnormal behaviour",
		    "target": "Laziness",
		    "weight": 0.1111
		  },
		  {
		    "source": "Abnormal behaviour",
		    "target": "Logorrhoea",
		    "weight": 0.1667
		  },
		  {
		    "source": "Abnormal behaviour",
		    "target": "Mania",
		    "weight": 0.1667
		  },
		  {
		    "source": "Abnormal behaviour",
		    "target": "Memory impairment",
		    "weight": 0.1111
		  },
		  {
		    "source": "Abnormal behaviour",
		    "target": "Mood swings",
		    "weight": 0.1667
		  },
		  {
		    "source": "Abnormal behaviour",
		    "target": "Panic attack",
		    "weight": 0.1111
		  },
		  {
		    "source": "Abnormal behaviour",
		    "target": "Product quality issue",
		    "weight": 1.5929
		  },
		  {
		    "source": "Abnormal behaviour",
		    "target": "Psychomotor hyperactivity",
		    "weight": 0.45
		  },
		  {
		    "source": "Abnormal behaviour",
		    "target": "Thinking abnormal",
		    "weight": 0.1667
		  },
		  {
		    "source": "Abnormal behaviour",
		    "target": "Type 2 diabetes mellitus",
		    "weight": 0.5
		  },
		  {
		    "source": "Abnormal behaviour",
		    "target": "Urinary incontinence",
		    "weight": 0.1667
		  },
		  {
		    "source": "Abnormal behaviour",
		    "target": "Weight decreased",
		    "weight": 0.1111
		  },
		  {
		    "source": "Abnormal loss of weight",
		    "target": "Agitation",
		    "weight": 0.0588
		  },
		  {
		    "source": "Abnormal loss of weight",
		    "target": "Anxiety",
		    "weight": 0.0476
		  },
		  {
		    "source": "Abnormal loss of weight",
		    "target": "Attention deficit\/hyperactivity disorder",
		    "weight": 0.0476
		  },
		  {
		    "source": "Abnormal loss of weight",
		    "target": "Blood glucose increased",
		    "weight": 0.1429
		  },
		  {
		    "source": "Abnormal loss of weight",
		    "target": "Bruxism",
		    "weight": 0.0476
		  },
		  {
		    "source": "Abnormal loss of weight",
		    "target": "Condition aggravated",
		    "weight": 0.1905
		  },
		  {
		    "source": "Abnormal loss of weight",
		    "target": "Decreased appetite",
		    "weight": 0.1064
		  },
		  {
		    "source": "Abnormal loss of weight",
		    "target": "Depression",
		    "weight": 0.0476
		  },
		  {
		    "source": "Abnormal loss of weight",
		    "target": "Dermatitis",
		    "weight": 0.0476
		  },
		  {
		    "source": "Abnormal loss of weight",
		    "target": "Discomfort",
		    "weight": 0.0588
		  },
		  {
		    "source": "Abnormal loss of weight",
		    "target": "Disturbance in attention",
		    "weight": 0.0588
		  },
		  {
		    "source": "Abnormal loss of weight",
		    "target": "Diverticulitis",
		    "weight": 0.0476
		  },
		  {
		    "source": "Abnormal loss of weight",
		    "target": "Drug ineffective",
		    "weight": 0.2017
		  },
		  {
		    "source": "Abnormal loss of weight",
		    "target": "Fatigue",
		    "weight": 0.0588
		  },
		  {
		    "source": "Abnormal loss of weight",
		    "target": "Feeding disorder",
		    "weight": 0.0476
		  },
		  {
		    "source": "Abnormal loss of weight",
		    "target": "Feeling abnormal",
		    "weight": 0.0588
		  },
		  {
		    "source": "Abnormal loss of weight",
		    "target": "Gastritis",
		    "weight": 0.0476
		  },
		  {
		    "source": "Abnormal loss of weight",
		    "target": "Hypersomnia",
		    "weight": 0.0588
		  },
		  {
		    "source": "Abnormal loss of weight",
		    "target": "Impaired work ability",
		    "weight": 0.0588
		  },
		  {
		    "source": "Abnormal loss of weight",
		    "target": "Incorrect dose administered",
		    "weight": 0.0588
		  },
		  {
		    "source": "Abnormal loss of weight",
		    "target": "Increased appetite",
		    "weight": 0.0476
		  },
		  {
		    "source": "Abnormal loss of weight",
		    "target": "Mental impairment",
		    "weight": 0.0588
		  },
		  {
		    "source": "Abnormal loss of weight",
		    "target": "Nightmare",
		    "weight": 0.0588
		  },
		  {
		    "source": "Abnormal loss of weight",
		    "target": "Osteoarthritis",
		    "weight": 0.0476
		  },
		  {
		    "source": "Abnormal loss of weight",
		    "target": "Pain",
		    "weight": 0.0476
		  },
		  {
		    "source": "Abnormal loss of weight",
		    "target": "Panic attack",
		    "weight": 0.0476
		  },
		  {
		    "source": "Abnormal loss of weight",
		    "target": "Poor quality sleep",
		    "weight": 0.0476
		  },
		  {
		    "source": "Abnormal loss of weight",
		    "target": "Product quality issue",
		    "weight": 0.1429
		  },
		  {
		    "source": "Abnormal loss of weight",
		    "target": "Psychotic disorder",
		    "weight": 0.0476
		  },
		  {
		    "source": "Abnormal loss of weight",
		    "target": "Rapid eye movements sleep abnormal",
		    "weight": 0.0588
		  },
		  {
		    "source": "Abnormal loss of weight",
		    "target": "Road traffic accident",
		    "weight": 0.0588
		  },
		  {
		    "source": "Abnormal loss of weight",
		    "target": "Scar",
		    "weight": 0.0476
		  },
		  {
		    "source": "Abnormal loss of weight",
		    "target": "Sleep disorder",
		    "weight": 0.1429
		  },
		  {
		    "source": "Abnormal loss of weight",
		    "target": "Tooth infection",
		    "weight": 0.0476
		  },
		  {
		    "source": "Abnormal loss of weight",
		    "target": "Tooth loss",
		    "weight": 0.0476
		  },
		  {
		    "source": "Abnormal loss of weight",
		    "target": "Toothache",
		    "weight": 0.0476
		  },
		  {
		    "source": "Abnormal loss of weight",
		    "target": "Underweight",
		    "weight": 0.0588
		  },
		  {
		    "source": "Abnormal loss of weight",
		    "target": "Weight increased",
		    "weight": 0.0588
		  },
		  {
		    "source": "Abnormal loss of weight",
		    "target": "Wrist fracture",
		    "weight": 0.1429
		  },
		  {
		    "source": "Accident",
		    "target": "Asthma",
		    "weight": 0.2
		  },
		  {
		    "source": "Accident",
		    "target": "Sinus disorder",
		    "weight": 0.2
		  },
		  {
		    "source": "Accident",
		    "target": "Sleep apnoea syndrome",
		    "weight": 0.2
		  },
		  {
		    "source": "Accident",
		    "target": "Upper-airway cough syndrome",
		    "weight": 0.2
		  },
		  {
		    "source": "Accidental overdose",
		    "target": "Anxiety",
		    "weight": 0.1111
		  },
		  {
		    "source": "Accidental overdose",
		    "target": "Depression",
		    "weight": 0.1111
		  },
		  {
		    "source": "Accidental overdose",
		    "target": "Drug effect decreased",
		    "weight": 0.25
		  },
		  {
		    "source": "Accidental overdose",
		    "target": "Drug ineffective",
		    "weight": 0.3333
		  },
		  {
		    "source": "Accidental overdose",
		    "target": "Feeling abnormal",
		    "weight": 0.1111
		  },
		  {
		    "source": "Accidental overdose",
		    "target": "Inappropriate schedule of drug administration",
		    "weight": 0.25
		  },
		  {
		    "source": "Accidental overdose",
		    "target": "Insomnia",
		    "weight": 0.25
		  },
		  {
		    "source": "Accidental overdose",
		    "target": "Laziness",
		    "weight": 0.1111
		  },
		  {
		    "source": "Accidental overdose",
		    "target": "Memory impairment",
		    "weight": 0.1111
		  },
		  {
		    "source": "Accidental overdose",
		    "target": "No adverse event",
		    "weight": 0.5
		  },
		  {
		    "source": "Accidental overdose",
		    "target": "Panic attack",
		    "weight": 0.1111
		  },
		  {
		    "source": "Accidental overdose",
		    "target": "Product quality issue",
		    "weight": 0.3333
		  },
		  {
		    "source": "Accidental overdose",
		    "target": "Weight decreased",
		    "weight": 0.1111
		  },
		  {
		    "source": "Activities of daily living impaired",
		    "target": "Anxiety",
		    "weight": 0.3095
		  },
		  {
		    "source": "Activities of daily living impaired",
		    "target": "Apathy",
		    "weight": 0.1667
		  },
		  {
		    "source": "Activities of daily living impaired",
		    "target": "Catatonia",
		    "weight": 0.1667
		  },
		  {
		    "source": "Activities of daily living impaired",
		    "target": "Depression",
		    "weight": 0.1429
		  },
		  {
		    "source": "Activities of daily living impaired",
		    "target": "Disturbance in attention",
		    "weight": 0.1429
		  },
		  {
		    "source": "Activities of daily living impaired",
		    "target": "Drug dose omission",
		    "weight": 0.1429
		  },
		  {
		    "source": "Activities of daily living impaired",
		    "target": "Fall",
		    "weight": 0.1
		  },
		  {
		    "source": "Activities of daily living impaired",
		    "target": "Feeling abnormal",
		    "weight": 0.3095
		  },
		  {
		    "source": "Activities of daily living impaired",
		    "target": "Impaired driving ability",
		    "weight": 0.1
		  },
		  {
		    "source": "Activities of daily living impaired",
		    "target": "Impaired work ability",
		    "weight": 0.1667
		  },
		  {
		    "source": "Activities of daily living impaired",
		    "target": "Insomnia",
		    "weight": 0.1
		  },
		  {
		    "source": "Activities of daily living impaired",
		    "target": "Logorrhoea",
		    "weight": 0.1429
		  },
		  {
		    "source": "Activities of daily living impaired",
		    "target": "Loss of control of legs",
		    "weight": 0.1
		  },
		  {
		    "source": "Activities of daily living impaired",
		    "target": "Memory impairment",
		    "weight": 0.1
		  },
		  {
		    "source": "Activities of daily living impaired",
		    "target": "Mental impairment",
		    "weight": 0.1
		  },
		  {
		    "source": "Activities of daily living impaired",
		    "target": "Pain",
		    "weight": 0.1
		  },
		  {
		    "source": "Activities of daily living impaired",
		    "target": "Pain in extremity",
		    "weight": 0.1
		  },
		  {
		    "source": "Activities of daily living impaired",
		    "target": "Road traffic accident",
		    "weight": 0.1
		  },
		  {
		    "source": "Adnexal torsion",
		    "target": "Blood pressure increased",
		    "weight": 0.3333
		  },
		  {
		    "source": "Adnexal torsion",
		    "target": "Palpitations",
		    "weight": 0.3333
		  },
		  {
		    "source": "Adverse drug reaction",
		    "target": "Anxiety",
		    "weight": 0.5
		  },
		  {
		    "source": "Adverse drug reaction",
		    "target": "Decreased appetite",
		    "weight": 0.1667
		  },
		  {
		    "source": "Adverse drug reaction",
		    "target": "Headache",
		    "weight": 0.1667
		  },
		  {
		    "source": "Adverse drug reaction",
		    "target": "Hypertension",
		    "weight": 0.3333
		  },
		  {
		    "source": "Adverse drug reaction",
		    "target": "Insomnia",
		    "weight": 0.1667
		  },
		  {
		    "source": "Adverse drug reaction",
		    "target": "Nausea",
		    "weight": 0.1667
		  },
		  {
		    "source": "Adverse drug reaction",
		    "target": "Product use issue",
		    "weight": 0.3333
		  },
		  {
		    "source": "Adverse drug reaction",
		    "target": "Weight decreased",
		    "weight": 0.1667
		  },
		  {
		    "source": "Adverse event",
		    "target": "Agitation",
		    "weight": 0.25
		  },
		  {
		    "source": "Adverse event",
		    "target": "Anxiety",
		    "weight": 0.2
		  },
		  {
		    "source": "Adverse event",
		    "target": "Attention deficit\/hyperactivity disorder",
		    "weight": 0.2
		  },
		  {
		    "source": "Adverse event",
		    "target": "Condition aggravated",
		    "weight": 0.2
		  },
		  {
		    "source": "Adverse event",
		    "target": "Crying",
		    "weight": 0.2
		  },
		  {
		    "source": "Adverse event",
		    "target": "Depression",
		    "weight": 0.45
		  },
		  {
		    "source": "Adverse event",
		    "target": "Drug dose omission",
		    "weight": 0.2
		  },
		  {
		    "source": "Adverse event",
		    "target": "Fatigue",
		    "weight": 0.3333
		  },
		  {
		    "source": "Adverse event",
		    "target": "Hospitalisation",
		    "weight": 0.3333
		  },
		  {
		    "source": "Adverse event",
		    "target": "Hot flush",
		    "weight": 0.2
		  },
		  {
		    "source": "Adverse event",
		    "target": "Incorrect dose administered",
		    "weight": 0.25
		  },
		  {
		    "source": "Adverse event",
		    "target": "Migraine",
		    "weight": 0.2
		  },
		  {
		    "source": "Adverse event",
		    "target": "Restlessness",
		    "weight": 0.25
		  },
		  {
		    "source": "Adverse event",
		    "target": "Underdose",
		    "weight": 0.25
		  },
		  {
		    "source": "Adverse event",
		    "target": "Wrong technique in product usage process",
		    "weight": 0.25
		  },
		  {
		    "source": "Affect lability",
		    "target": "Anaphylactic reaction",
		    "weight": 0.0455
		  },
		  {
		    "source": "Affect lability",
		    "target": "Anger",
		    "weight": 0.0455
		  },
		  {
		    "source": "Affect lability",
		    "target": "Anxiety",
		    "weight": 0.2455
		  },
		  {
		    "source": "Affect lability",
		    "target": "Apathy",
		    "weight": 0.0455
		  },
		  {
		    "source": "Affect lability",
		    "target": "Bipolar disorder",
		    "weight": 0.0455
		  },
		  {
		    "source": "Affect lability",
		    "target": "Depressed mood",
		    "weight": 0.2
		  },
		  {
		    "source": "Affect lability",
		    "target": "Depression",
		    "weight": 0.2121
		  },
		  {
		    "source": "Affect lability",
		    "target": "Drug dose omission",
		    "weight": 0.0455
		  },
		  {
		    "source": "Affect lability",
		    "target": "Drug effect decreased",
		    "weight": 0.0455
		  },
		  {
		    "source": "Affect lability",
		    "target": "Drug effect increased",
		    "weight": 0.0455
		  },
		  {
		    "source": "Affect lability",
		    "target": "Drug ineffective",
		    "weight": 0.0455
		  },
		  {
		    "source": "Affect lability",
		    "target": "Eye irritation",
		    "weight": 0.0455
		  },
		  {
		    "source": "Affect lability",
		    "target": "Fatigue",
		    "weight": 0.2455
		  },
		  {
		    "source": "Affect lability",
		    "target": "Fear",
		    "weight": 0.0455
		  },
		  {
		    "source": "Affect lability",
		    "target": "Feeling of relaxation",
		    "weight": 0.2
		  },
		  {
		    "source": "Affect lability",
		    "target": "Headache",
		    "weight": 0.0455
		  },
		  {
		    "source": "Affect lability",
		    "target": "Hypersomnia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Affect lability",
		    "target": "Intentional self-injury",
		    "weight": 0.1667
		  },
		  {
		    "source": "Affect lability",
		    "target": "Malaise",
		    "weight": 0.0455
		  },
		  {
		    "source": "Affect lability",
		    "target": "Migraine",
		    "weight": 0.0455
		  },
		  {
		    "source": "Affect lability",
		    "target": "Nasopharyngitis",
		    "weight": 0.0455
		  },
		  {
		    "source": "Affect lability",
		    "target": "Negative thoughts",
		    "weight": 0.1667
		  },
		  {
		    "source": "Affect lability",
		    "target": "Social phobia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Affect lability",
		    "target": "Suicidal ideation",
		    "weight": 0.1667
		  },
		  {
		    "source": "Affect lability",
		    "target": "Suicide attempt",
		    "weight": 0.1667
		  },
		  {
		    "source": "Affect lability",
		    "target": "Tachyphrenia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Affect lability",
		    "target": "Weight increased",
		    "weight": 0.0455
		  },
		  {
		    "source": "Affective disorder",
		    "target": "Aggression",
		    "weight": 0.1667
		  },
		  {
		    "source": "Affective disorder",
		    "target": "Agitation",
		    "weight": 0.1667
		  },
		  {
		    "source": "Affective disorder",
		    "target": "Drug dose omission",
		    "weight": 0.1667
		  },
		  {
		    "source": "Affective disorder",
		    "target": "Off label use",
		    "weight": 0.1667
		  },
		  {
		    "source": "Affective disorder",
		    "target": "Suicidal ideation",
		    "weight": 0.1667
		  },
		  {
		    "source": "Aggression",
		    "target": "Agitation",
		    "weight": 0.3056
		  },
		  {
		    "source": "Aggression",
		    "target": "Anxiety",
		    "weight": 0.2639
		  },
		  {
		    "source": "Aggression",
		    "target": "Constipation",
		    "weight": 0.0667
		  },
		  {
		    "source": "Aggression",
		    "target": "Contusion",
		    "weight": 0.1429
		  },
		  {
		    "source": "Aggression",
		    "target": "Crying",
		    "weight": 0.1389
		  },
		  {
		    "source": "Aggression",
		    "target": "Decreased appetite",
		    "weight": 0.4556
		  },
		  {
		    "source": "Aggression",
		    "target": "Derealisation",
		    "weight": 0.125
		  },
		  {
		    "source": "Aggression",
		    "target": "Device breakage",
		    "weight": 0.1429
		  },
		  {
		    "source": "Aggression",
		    "target": "Disturbance in attention",
		    "weight": 0.2667
		  },
		  {
		    "source": "Aggression",
		    "target": "Disturbance in social behaviour",
		    "weight": 0.2
		  },
		  {
		    "source": "Aggression",
		    "target": "Dizziness",
		    "weight": 0.0556
		  },
		  {
		    "source": "Aggression",
		    "target": "Drug administered to patient of inappropriate age",
		    "weight": 0.0667
		  },
		  {
		    "source": "Aggression",
		    "target": "Drug dose omission",
		    "weight": 0.3667
		  },
		  {
		    "source": "Aggression",
		    "target": "Drug effect decreased",
		    "weight": 0.2056
		  },
		  {
		    "source": "Aggression",
		    "target": "Drug ineffective",
		    "weight": 0.15
		  },
		  {
		    "source": "Aggression",
		    "target": "Drug withdrawal convulsions",
		    "weight": 0.0833
		  },
		  {
		    "source": "Aggression",
		    "target": "Eosinophilic oesophagitis",
		    "weight": 0.0667
		  },
		  {
		    "source": "Aggression",
		    "target": "Epistaxis",
		    "weight": 0.0556
		  },
		  {
		    "source": "Aggression",
		    "target": "Feeling abnormal",
		    "weight": 0.0667
		  },
		  {
		    "source": "Aggression",
		    "target": "Flat affect",
		    "weight": 0.0556
		  },
		  {
		    "source": "Aggression",
		    "target": "Growth accelerated",
		    "weight": 0.0667
		  },
		  {
		    "source": "Aggression",
		    "target": "Haemorrhoids",
		    "weight": 0.0667
		  },
		  {
		    "source": "Aggression",
		    "target": "Headache",
		    "weight": 0.0556
		  },
		  {
		    "source": "Aggression",
		    "target": "Hepatic enzyme increased",
		    "weight": 0.0667
		  },
		  {
		    "source": "Aggression",
		    "target": "Hostility",
		    "weight": 0.0833
		  },
		  {
		    "source": "Aggression",
		    "target": "Impulse-control disorder",
		    "weight": 0.3333
		  },
		  {
		    "source": "Aggression",
		    "target": "Increased appetite",
		    "weight": 0.0833
		  },
		  {
		    "source": "Aggression",
		    "target": "Insomnia",
		    "weight": 0.1806
		  },
		  {
		    "source": "Aggression",
		    "target": "Irritability",
		    "weight": 0.6984
		  },
		  {
		    "source": "Aggression",
		    "target": "Lactose intolerance",
		    "weight": 0.0667
		  },
		  {
		    "source": "Aggression",
		    "target": "Logorrhoea",
		    "weight": 0.0667
		  },
		  {
		    "source": "Aggression",
		    "target": "Malaise",
		    "weight": 0.1429
		  },
		  {
		    "source": "Aggression",
		    "target": "Mania",
		    "weight": 0.0833
		  },
		  {
		    "source": "Aggression",
		    "target": "Motor dysfunction",
		    "weight": 0.125
		  },
		  {
		    "source": "Aggression",
		    "target": "Myoclonic epilepsy",
		    "weight": 0.125
		  },
		  {
		    "source": "Aggression",
		    "target": "Nausea",
		    "weight": 0.0556
		  },
		  {
		    "source": "Aggression",
		    "target": "Obsessive thoughts",
		    "weight": 0.0556
		  },
		  {
		    "source": "Aggression",
		    "target": "Off label use",
		    "weight": 0.1667
		  },
		  {
		    "source": "Aggression",
		    "target": "Optic nerve neoplasm",
		    "weight": 0.0833
		  },
		  {
		    "source": "Aggression",
		    "target": "Panic disorder",
		    "weight": 0.125
		  },
		  {
		    "source": "Aggression",
		    "target": "Personality change",
		    "weight": 0.1429
		  },
		  {
		    "source": "Aggression",
		    "target": "Product substitution issue",
		    "weight": 0.3333
		  },
		  {
		    "source": "Aggression",
		    "target": "Product use issue",
		    "weight": 0.5
		  },
		  {
		    "source": "Aggression",
		    "target": "Sleep disorder",
		    "weight": 0.2
		  },
		  {
		    "source": "Aggression",
		    "target": "Social avoidant behaviour",
		    "weight": 0.0556
		  },
		  {
		    "source": "Aggression",
		    "target": "Somnolence",
		    "weight": 0.0833
		  },
		  {
		    "source": "Aggression",
		    "target": "Suicidal ideation",
		    "weight": 0.1667
		  },
		  {
		    "source": "Aggression",
		    "target": "Thinking abnormal",
		    "weight": 0.125
		  },
		  {
		    "source": "Aggression",
		    "target": "Tic",
		    "weight": 0.0556
		  },
		  {
		    "source": "Aggression",
		    "target": "Vomiting",
		    "weight": 0.0556
		  },
		  {
		    "source": "Aggression",
		    "target": "Weight decreased",
		    "weight": 0.2095
		  },
		  {
		    "source": "Agitation",
		    "target": "Anger",
		    "weight": 0.3333
		  },
		  {
		    "source": "Agitation",
		    "target": "Anxiety",
		    "weight": 0.3889
		  },
		  {
		    "source": "Agitation",
		    "target": "Blood pressure increased",
		    "weight": 0.1
		  },
		  {
		    "source": "Agitation",
		    "target": "Condition aggravated",
		    "weight": 0.25
		  },
		  {
		    "source": "Agitation",
		    "target": "Crying",
		    "weight": 0.1389
		  },
		  {
		    "source": "Agitation",
		    "target": "Decreased appetite",
		    "weight": 0.1144
		  },
		  {
		    "source": "Agitation",
		    "target": "Depression",
		    "weight": 0.5833
		  },
		  {
		    "source": "Agitation",
		    "target": "Discomfort",
		    "weight": 0.0588
		  },
		  {
		    "source": "Agitation",
		    "target": "Dissociation",
		    "weight": 0.1
		  },
		  {
		    "source": "Agitation",
		    "target": "Disturbance in attention",
		    "weight": 0.0588
		  },
		  {
		    "source": "Agitation",
		    "target": "Dizziness",
		    "weight": 0.0556
		  },
		  {
		    "source": "Agitation",
		    "target": "Drug dose omission",
		    "weight": 0.1667
		  },
		  {
		    "source": "Agitation",
		    "target": "Drug effect decreased",
		    "weight": 0.1389
		  },
		  {
		    "source": "Agitation",
		    "target": "Drug ineffective",
		    "weight": 0.1422
		  },
		  {
		    "source": "Agitation",
		    "target": "Drug interaction",
		    "weight": 0.1
		  },
		  {
		    "source": "Agitation",
		    "target": "Drug withdrawal convulsions",
		    "weight": 0.0833
		  },
		  {
		    "source": "Agitation",
		    "target": "Dyskinesia",
		    "weight": 0.1
		  },
		  {
		    "source": "Agitation",
		    "target": "Epistaxis",
		    "weight": 0.0556
		  },
		  {
		    "source": "Agitation",
		    "target": "Fatigue",
		    "weight": 0.2588
		  },
		  {
		    "source": "Agitation",
		    "target": "Feeling abnormal",
		    "weight": 0.0588
		  },
		  {
		    "source": "Agitation",
		    "target": "Flat affect",
		    "weight": 0.0556
		  },
		  {
		    "source": "Agitation",
		    "target": "Headache",
		    "weight": 0.2556
		  },
		  {
		    "source": "Agitation",
		    "target": "Hostility",
		    "weight": 0.0833
		  },
		  {
		    "source": "Agitation",
		    "target": "Hyperhidrosis",
		    "weight": 0.1
		  },
		  {
		    "source": "Agitation",
		    "target": "Hypersomnia",
		    "weight": 0.0588
		  },
		  {
		    "source": "Agitation",
		    "target": "Impaired work ability",
		    "weight": 0.0588
		  },
		  {
		    "source": "Agitation",
		    "target": "Incorrect dose administered",
		    "weight": 0.0588
		  },
		  {
		    "source": "Agitation",
		    "target": "Increased appetite",
		    "weight": 0.0833
		  },
		  {
		    "source": "Agitation",
		    "target": "Insomnia",
		    "weight": 0.0556
		  },
		  {
		    "source": "Agitation",
		    "target": "Irritability",
		    "weight": 0.3056
		  },
		  {
		    "source": "Agitation",
		    "target": "Mania",
		    "weight": 0.0833
		  },
		  {
		    "source": "Agitation",
		    "target": "Mental impairment",
		    "weight": 0.0588
		  },
		  {
		    "source": "Agitation",
		    "target": "Mood swings",
		    "weight": 0.2
		  },
		  {
		    "source": "Agitation",
		    "target": "Muscle spasms",
		    "weight": 0.1
		  },
		  {
		    "source": "Agitation",
		    "target": "Mydriasis",
		    "weight": 0.1
		  },
		  {
		    "source": "Agitation",
		    "target": "Nausea",
		    "weight": 0.0556
		  },
		  {
		    "source": "Agitation",
		    "target": "Nightmare",
		    "weight": 0.0588
		  },
		  {
		    "source": "Agitation",
		    "target": "Obsessive thoughts",
		    "weight": 0.0556
		  },
		  {
		    "source": "Agitation",
		    "target": "Off label use",
		    "weight": 0.1667
		  },
		  {
		    "source": "Agitation",
		    "target": "Optic nerve neoplasm",
		    "weight": 0.0833
		  },
		  {
		    "source": "Agitation",
		    "target": "Rapid eye movements sleep abnormal",
		    "weight": 0.0588
		  },
		  {
		    "source": "Agitation",
		    "target": "Restlessness",
		    "weight": 0.45
		  },
		  {
		    "source": "Agitation",
		    "target": "Road traffic accident",
		    "weight": 0.0588
		  },
		  {
		    "source": "Agitation",
		    "target": "Serotonin syndrome",
		    "weight": 0.1
		  },
		  {
		    "source": "Agitation",
		    "target": "Social avoidant behaviour",
		    "weight": 0.0556
		  },
		  {
		    "source": "Agitation",
		    "target": "Somnolence",
		    "weight": 0.0833
		  },
		  {
		    "source": "Agitation",
		    "target": "Suicidal ideation",
		    "weight": 0.1667
		  },
		  {
		    "source": "Agitation",
		    "target": "Tachyphrenia",
		    "weight": 0.1
		  },
		  {
		    "source": "Agitation",
		    "target": "Tic",
		    "weight": 0.0556
		  },
		  {
		    "source": "Agitation",
		    "target": "Underweight",
		    "weight": 0.0588
		  },
		  {
		    "source": "Agitation",
		    "target": "Vomiting",
		    "weight": 0.0556
		  },
		  {
		    "source": "Agitation",
		    "target": "Weight increased",
		    "weight": 0.0588
		  },
		  {
		    "source": "Akathisia",
		    "target": "Cough",
		    "weight": 0.0769
		  },
		  {
		    "source": "Akathisia",
		    "target": "Fatigue",
		    "weight": 0.0769
		  },
		  {
		    "source": "Akathisia",
		    "target": "Feeling abnormal",
		    "weight": 0.0769
		  },
		  {
		    "source": "Akathisia",
		    "target": "Growing pains",
		    "weight": 0.0769
		  },
		  {
		    "source": "Akathisia",
		    "target": "Hypersensitivity",
		    "weight": 0.0769
		  },
		  {
		    "source": "Akathisia",
		    "target": "Insomnia",
		    "weight": 0.0769
		  },
		  {
		    "source": "Akathisia",
		    "target": "Movement disorder",
		    "weight": 0.0769
		  },
		  {
		    "source": "Akathisia",
		    "target": "Nasopharyngitis",
		    "weight": 0.0769
		  },
		  {
		    "source": "Akathisia",
		    "target": "Off label use",
		    "weight": 0.0769
		  },
		  {
		    "source": "Akathisia",
		    "target": "Pneumonia",
		    "weight": 0.0769
		  },
		  {
		    "source": "Akathisia",
		    "target": "Restlessness",
		    "weight": 0.0769
		  },
		  {
		    "source": "Akathisia",
		    "target": "Thirst",
		    "weight": 0.0769
		  },
		  {
		    "source": "Alcohol abuse",
		    "target": "Blood pressure increased",
		    "weight": 0.25
		  },
		  {
		    "source": "Alcohol abuse",
		    "target": "Drug abuse",
		    "weight": 0.25
		  },
		  {
		    "source": "Alcohol abuse",
		    "target": "Tachycardia",
		    "weight": 0.25
		  },
		  {
		    "source": "Alopecia",
		    "target": "Incorrect dose administered",
		    "weight": 0.5
		  },
		  {
		    "source": "Amnesia",
		    "target": "Apathy",
		    "weight": 0.0714
		  },
		  {
		    "source": "Amnesia",
		    "target": "Asthenia",
		    "weight": 0.1
		  },
		  {
		    "source": "Amnesia",
		    "target": "Condition aggravated",
		    "weight": 0.0714
		  },
		  {
		    "source": "Amnesia",
		    "target": "Depression",
		    "weight": 0.1
		  },
		  {
		    "source": "Amnesia",
		    "target": "Disturbance in attention",
		    "weight": 0.4333
		  },
		  {
		    "source": "Amnesia",
		    "target": "Drug dose omission",
		    "weight": 0.3333
		  },
		  {
		    "source": "Amnesia",
		    "target": "Drug ineffective",
		    "weight": 0.0714
		  },
		  {
		    "source": "Amnesia",
		    "target": "Dyskinesia",
		    "weight": 0.0714
		  },
		  {
		    "source": "Amnesia",
		    "target": "Eye movement disorder",
		    "weight": 0.0714
		  },
		  {
		    "source": "Amnesia",
		    "target": "Fatigue",
		    "weight": 0.1
		  },
		  {
		    "source": "Amnesia",
		    "target": "Feeling abnormal",
		    "weight": 0.1
		  },
		  {
		    "source": "Amnesia",
		    "target": "Hyperphagia",
		    "weight": 0.0714
		  },
		  {
		    "source": "Amnesia",
		    "target": "Intentional self-injury",
		    "weight": 0.1
		  },
		  {
		    "source": "Amnesia",
		    "target": "Laziness",
		    "weight": 0.0714
		  },
		  {
		    "source": "Amnesia",
		    "target": "Memory impairment",
		    "weight": 0.1
		  },
		  {
		    "source": "Amnesia",
		    "target": "Mental disorder",
		    "weight": 0.1
		  },
		  {
		    "source": "Amnesia",
		    "target": "Mood altered",
		    "weight": 0.1
		  },
		  {
		    "source": "Amnesia",
		    "target": "Musculoskeletal stiffness",
		    "weight": 0.0714
		  },
		  {
		    "source": "Amnesia",
		    "target": "Social avoidant behaviour",
		    "weight": 0.0714
		  },
		  {
		    "source": "Amnesia",
		    "target": "Thirst",
		    "weight": 0.0714
		  },
		  {
		    "source": "Amnesia",
		    "target": "Victim of abuse",
		    "weight": 0.0714
		  },
		  {
		    "source": "Amnesia",
		    "target": "Victim of sexual abuse",
		    "weight": 0.0714
		  },
		  {
		    "source": "Amnesia",
		    "target": "Weight increased",
		    "weight": 0.0714
		  },
		  {
		    "source": "Amphetamines negative",
		    "target": "Drug abuse",
		    "weight": 0.3333
		  },
		  {
		    "source": "Amphetamines negative",
		    "target": "Drug diversion",
		    "weight": 0.3333
		  },
		  {
		    "source": "Anaphylactic reaction",
		    "target": "Anger",
		    "weight": 0.0455
		  },
		  {
		    "source": "Anaphylactic reaction",
		    "target": "Antibody test positive",
		    "weight": 0.1667
		  },
		  {
		    "source": "Anaphylactic reaction",
		    "target": "Anxiety",
		    "weight": 0.0455
		  },
		  {
		    "source": "Anaphylactic reaction",
		    "target": "Apathy",
		    "weight": 0.0455
		  },
		  {
		    "source": "Anaphylactic reaction",
		    "target": "Bipolar disorder",
		    "weight": 0.0455
		  },
		  {
		    "source": "Anaphylactic reaction",
		    "target": "Crohn's disease",
		    "weight": 0.1667
		  },
		  {
		    "source": "Anaphylactic reaction",
		    "target": "Depression",
		    "weight": 0.0455
		  },
		  {
		    "source": "Anaphylactic reaction",
		    "target": "Drug dose omission",
		    "weight": 0.0455
		  },
		  {
		    "source": "Anaphylactic reaction",
		    "target": "Drug effect decreased",
		    "weight": 0.2121
		  },
		  {
		    "source": "Anaphylactic reaction",
		    "target": "Drug effect increased",
		    "weight": 0.0455
		  },
		  {
		    "source": "Anaphylactic reaction",
		    "target": "Drug ineffective",
		    "weight": 0.0455
		  },
		  {
		    "source": "Anaphylactic reaction",
		    "target": "Eye irritation",
		    "weight": 0.0455
		  },
		  {
		    "source": "Anaphylactic reaction",
		    "target": "Fatigue",
		    "weight": 0.0455
		  },
		  {
		    "source": "Anaphylactic reaction",
		    "target": "Fear",
		    "weight": 0.0455
		  },
		  {
		    "source": "Anaphylactic reaction",
		    "target": "Headache",
		    "weight": 0.0455
		  },
		  {
		    "source": "Anaphylactic reaction",
		    "target": "Hypersomnia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Anaphylactic reaction",
		    "target": "Infusion related reaction",
		    "weight": 0.1667
		  },
		  {
		    "source": "Anaphylactic reaction",
		    "target": "Malaise",
		    "weight": 0.0455
		  },
		  {
		    "source": "Anaphylactic reaction",
		    "target": "Migraine",
		    "weight": 0.0455
		  },
		  {
		    "source": "Anaphylactic reaction",
		    "target": "Nasopharyngitis",
		    "weight": 0.0455
		  },
		  {
		    "source": "Anaphylactic reaction",
		    "target": "Social phobia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Anaphylactic reaction",
		    "target": "Tachyphrenia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Anaphylactic reaction",
		    "target": "Weight increased",
		    "weight": 0.2121
		  },
		  {
		    "source": "Anger",
		    "target": "Anxiety",
		    "weight": 0.0455
		  },
		  {
		    "source": "Anger",
		    "target": "Apathy",
		    "weight": 0.0455
		  },
		  {
		    "source": "Anger",
		    "target": "Bipolar disorder",
		    "weight": 0.0455
		  },
		  {
		    "source": "Anger",
		    "target": "Condition aggravated",
		    "weight": 0.25
		  },
		  {
		    "source": "Anger",
		    "target": "Confusional state",
		    "weight": 0.1429
		  },
		  {
		    "source": "Anger",
		    "target": "Crying",
		    "weight": 0.1429
		  },
		  {
		    "source": "Anger",
		    "target": "Depression",
		    "weight": 0.3788
		  },
		  {
		    "source": "Anger",
		    "target": "Disturbance in attention",
		    "weight": 0.1429
		  },
		  {
		    "source": "Anger",
		    "target": "Drug dose omission",
		    "weight": 0.0455
		  },
		  {
		    "source": "Anger",
		    "target": "Drug effect decreased",
		    "weight": 0.0455
		  },
		  {
		    "source": "Anger",
		    "target": "Drug effect increased",
		    "weight": 0.0455
		  },
		  {
		    "source": "Anger",
		    "target": "Drug ineffective",
		    "weight": 0.0455
		  },
		  {
		    "source": "Anger",
		    "target": "Emotional disorder",
		    "weight": 0.1429
		  },
		  {
		    "source": "Anger",
		    "target": "Eye irritation",
		    "weight": 0.0455
		  },
		  {
		    "source": "Anger",
		    "target": "Fatigue",
		    "weight": 0.0455
		  },
		  {
		    "source": "Anger",
		    "target": "Fear",
		    "weight": 0.0455
		  },
		  {
		    "source": "Anger",
		    "target": "Headache",
		    "weight": 0.0455
		  },
		  {
		    "source": "Anger",
		    "target": "Hypersomnia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Anger",
		    "target": "Increased appetite",
		    "weight": 0.25
		  },
		  {
		    "source": "Anger",
		    "target": "Malaise",
		    "weight": 0.0455
		  },
		  {
		    "source": "Anger",
		    "target": "Migraine",
		    "weight": 0.0455
		  },
		  {
		    "source": "Anger",
		    "target": "Nasopharyngitis",
		    "weight": 0.0455
		  },
		  {
		    "source": "Anger",
		    "target": "Personality change",
		    "weight": 0.25
		  },
		  {
		    "source": "Anger",
		    "target": "Self injurious behaviour",
		    "weight": 0.1429
		  },
		  {
		    "source": "Anger",
		    "target": "Social phobia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Anger",
		    "target": "Suicidal ideation",
		    "weight": 0.1429
		  },
		  {
		    "source": "Anger",
		    "target": "Tachyphrenia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Anger",
		    "target": "Weight increased",
		    "weight": 0.0455
		  },
		  {
		    "source": "Angioedema",
		    "target": "Drug hypersensitivity",
		    "weight": 0.2
		  },
		  {
		    "source": "Angioedema",
		    "target": "Local swelling",
		    "weight": 0.2
		  },
		  {
		    "source": "Angioedema",
		    "target": "Neck pain",
		    "weight": 0.2
		  },
		  {
		    "source": "Angioedema",
		    "target": "Urticaria",
		    "weight": 0.2
		  },
		  {
		    "source": "Anhedonia",
		    "target": "Anxiety",
		    "weight": 0.2019
		  },
		  {
		    "source": "Anhedonia",
		    "target": "Depression",
		    "weight": 0.125
		  },
		  {
		    "source": "Anhedonia",
		    "target": "Emotional distress",
		    "weight": 0.0769
		  },
		  {
		    "source": "Anhedonia",
		    "target": "Frustration",
		    "weight": 0.0769
		  },
		  {
		    "source": "Anhedonia",
		    "target": "General physical health deterioration",
		    "weight": 0.0769
		  },
		  {
		    "source": "Anhedonia",
		    "target": "Genital haemorrhage",
		    "weight": 0.0769
		  },
		  {
		    "source": "Anhedonia",
		    "target": "Injury",
		    "weight": 0.2019
		  },
		  {
		    "source": "Anhedonia",
		    "target": "Insomnia",
		    "weight": 0.125
		  },
		  {
		    "source": "Anhedonia",
		    "target": "Medical device discomfort",
		    "weight": 0.0769
		  },
		  {
		    "source": "Anhedonia",
		    "target": "Medical device pain",
		    "weight": 0.0769
		  },
		  {
		    "source": "Anhedonia",
		    "target": "Mental disorder",
		    "weight": 0.125
		  },
		  {
		    "source": "Anhedonia",
		    "target": "Pain",
		    "weight": 0.125
		  },
		  {
		    "source": "Anhedonia",
		    "target": "Post procedural discomfort",
		    "weight": 0.0769
		  },
		  {
		    "source": "Anhedonia",
		    "target": "Procedural pain",
		    "weight": 0.0769
		  },
		  {
		    "source": "Anhedonia",
		    "target": "Pulmonary embolism",
		    "weight": 0.125
		  },
		  {
		    "source": "Anhedonia",
		    "target": "Uterine perforation",
		    "weight": 0.0769
		  },
		  {
		    "source": "Anorgasmia",
		    "target": "Blood pressure increased",
		    "weight": 0.0769
		  },
		  {
		    "source": "Anorgasmia",
		    "target": "Chills",
		    "weight": 0.0769
		  },
		  {
		    "source": "Anorgasmia",
		    "target": "Decreased interest",
		    "weight": 0.25
		  },
		  {
		    "source": "Anorgasmia",
		    "target": "Drug effect decreased",
		    "weight": 0.25
		  },
		  {
		    "source": "Anorgasmia",
		    "target": "Drug ineffective",
		    "weight": 0.0769
		  },
		  {
		    "source": "Anorgasmia",
		    "target": "Fatigue",
		    "weight": 0.0769
		  },
		  {
		    "source": "Anorgasmia",
		    "target": "Increased appetite",
		    "weight": 0.0769
		  },
		  {
		    "source": "Anorgasmia",
		    "target": "Libido decreased",
		    "weight": 0.3269
		  },
		  {
		    "source": "Anorgasmia",
		    "target": "Muscle spasms",
		    "weight": 0.0769
		  },
		  {
		    "source": "Anorgasmia",
		    "target": "Nausea",
		    "weight": 0.0769
		  },
		  {
		    "source": "Anorgasmia",
		    "target": "Pain in jaw",
		    "weight": 0.0769
		  },
		  {
		    "source": "Anorgasmia",
		    "target": "Palpitations",
		    "weight": 0.0769
		  },
		  {
		    "source": "Anorgasmia",
		    "target": "Pyrexia",
		    "weight": 0.0769
		  },
		  {
		    "source": "Anorgasmia",
		    "target": "Vomiting",
		    "weight": 0.0769
		  },
		  {
		    "source": "Antibody test positive",
		    "target": "Crohn's disease",
		    "weight": 0.1667
		  },
		  {
		    "source": "Antibody test positive",
		    "target": "Drug effect decreased",
		    "weight": 0.1667
		  },
		  {
		    "source": "Antibody test positive",
		    "target": "Infusion related reaction",
		    "weight": 0.1667
		  },
		  {
		    "source": "Antibody test positive",
		    "target": "Weight increased",
		    "weight": 0.1667
		  },
		  {
		    "source": "Antisocial behaviour",
		    "target": "Blood iron abnormal",
		    "weight": 0.0833
		  },
		  {
		    "source": "Antisocial behaviour",
		    "target": "Condition aggravated",
		    "weight": 0.0833
		  },
		  {
		    "source": "Antisocial behaviour",
		    "target": "Depression",
		    "weight": 0.0833
		  },
		  {
		    "source": "Antisocial behaviour",
		    "target": "Drug ineffective",
		    "weight": 0.0833
		  },
		  {
		    "source": "Antisocial behaviour",
		    "target": "Formication",
		    "weight": 0.0833
		  },
		  {
		    "source": "Antisocial behaviour",
		    "target": "Hostility",
		    "weight": 0.0833
		  },
		  {
		    "source": "Antisocial behaviour",
		    "target": "Inappropriate schedule of drug administration",
		    "weight": 0.25
		  },
		  {
		    "source": "Antisocial behaviour",
		    "target": "Irritability",
		    "weight": 0.0833
		  },
		  {
		    "source": "Antisocial behaviour",
		    "target": "Malabsorption",
		    "weight": 0.0833
		  },
		  {
		    "source": "Antisocial behaviour",
		    "target": "Mood swings",
		    "weight": 0.0833
		  },
		  {
		    "source": "Antisocial behaviour",
		    "target": "Performance status decreased",
		    "weight": 0.25
		  },
		  {
		    "source": "Antisocial behaviour",
		    "target": "Prescribed overdose",
		    "weight": 0.25
		  },
		  {
		    "source": "Antisocial behaviour",
		    "target": "Vitamin D abnormal",
		    "weight": 0.0833
		  },
		  {
		    "source": "Antisocial behaviour",
		    "target": "Vitreous floaters",
		    "weight": 0.0833
		  },
		  {
		    "source": "Anxiety",
		    "target": "Apathy",
		    "weight": 0.2121
		  },
		  {
		    "source": "Anxiety",
		    "target": "Aphasia",
		    "weight": 0.0833
		  },
		  {
		    "source": "Anxiety",
		    "target": "Asthenia",
		    "weight": 0.1667
		  },
		  {
		    "source": "Anxiety",
		    "target": "Attention deficit\/hyperactivity disorder",
		    "weight": 0.0476
		  },
		  {
		    "source": "Anxiety",
		    "target": "Bipolar disorder",
		    "weight": 0.0455
		  },
		  {
		    "source": "Anxiety",
		    "target": "Blood pressure increased",
		    "weight": 0.25
		  },
		  {
		    "source": "Anxiety",
		    "target": "Bruxism",
		    "weight": 0.0476
		  },
		  {
		    "source": "Anxiety",
		    "target": "Calcinosis",
		    "weight": 0.2
		  },
		  {
		    "source": "Anxiety",
		    "target": "Catatonia",
		    "weight": 0.1667
		  },
		  {
		    "source": "Anxiety",
		    "target": "Chest pain",
		    "weight": 0.2
		  },
		  {
		    "source": "Anxiety",
		    "target": "Condition aggravated",
		    "weight": 0.2976
		  },
		  {
		    "source": "Anxiety",
		    "target": "Crying",
		    "weight": 0.3389
		  },
		  {
		    "source": "Anxiety",
		    "target": "Decreased appetite",
		    "weight": 0.3032
		  },
		  {
		    "source": "Anxiety",
		    "target": "Delusion",
		    "weight": 0.3333
		  },
		  {
		    "source": "Anxiety",
		    "target": "Depressed mood",
		    "weight": 0.2
		  },
		  {
		    "source": "Anxiety",
		    "target": "Depression",
		    "weight": 1.072
		  },
		  {
		    "source": "Anxiety",
		    "target": "Derealisation",
		    "weight": 0.125
		  },
		  {
		    "source": "Anxiety",
		    "target": "Dermatitis",
		    "weight": 0.0476
		  },
		  {
		    "source": "Anxiety",
		    "target": "Disability",
		    "weight": 0.2
		  },
		  {
		    "source": "Anxiety",
		    "target": "Disturbance in attention",
		    "weight": 0.2262
		  },
		  {
		    "source": "Anxiety",
		    "target": "Disturbance in social behaviour",
		    "weight": 0.25
		  },
		  {
		    "source": "Anxiety",
		    "target": "Diverticulitis",
		    "weight": 0.0476
		  },
		  {
		    "source": "Anxiety",
		    "target": "Dizziness",
		    "weight": 0.1389
		  },
		  {
		    "source": "Anxiety",
		    "target": "Drug abuse",
		    "weight": 0.2
		  },
		  {
		    "source": "Anxiety",
		    "target": "Drug diversion",
		    "weight": 0.1667
		  },
		  {
		    "source": "Anxiety",
		    "target": "Drug dose omission",
		    "weight": 0.605
		  },
		  {
		    "source": "Anxiety",
		    "target": "Drug effect decreased",
		    "weight": 0.5177
		  },
		  {
		    "source": "Anxiety",
		    "target": "Drug effect increased",
		    "weight": 0.3788
		  },
		  {
		    "source": "Anxiety",
		    "target": "Drug effect variable",
		    "weight": 0.25
		  },
		  {
		    "source": "Anxiety",
		    "target": "Drug ineffective",
		    "weight": 0.2121
		  },
		  {
		    "source": "Anxiety",
		    "target": "Drug withdrawal convulsions",
		    "weight": 0.0833
		  },
		  {
		    "source": "Anxiety",
		    "target": "Dysgraphia",
		    "weight": 0.0833
		  },
		  {
		    "source": "Anxiety",
		    "target": "Dyspnoea",
		    "weight": 0.0833
		  },
		  {
		    "source": "Anxiety",
		    "target": "Emotional distress",
		    "weight": 0.3269
		  },
		  {
		    "source": "Anxiety",
		    "target": "Epistaxis",
		    "weight": 0.0556
		  },
		  {
		    "source": "Anxiety",
		    "target": "Eye irritation",
		    "weight": 0.0455
		  },
		  {
		    "source": "Anxiety",
		    "target": "Fatigue",
		    "weight": 0.2455
		  },
		  {
		    "source": "Anxiety",
		    "target": "Fear",
		    "weight": 0.0455
		  },
		  {
		    "source": "Anxiety",
		    "target": "Feeding disorder",
		    "weight": 0.0476
		  },
		  {
		    "source": "Anxiety",
		    "target": "Feeling abnormal",
		    "weight": 0.504
		  },
		  {
		    "source": "Anxiety",
		    "target": "Feeling jittery",
		    "weight": 0.5
		  },
		  {
		    "source": "Anxiety",
		    "target": "Feeling of relaxation",
		    "weight": 0.2
		  },
		  {
		    "source": "Anxiety",
		    "target": "Flat affect",
		    "weight": 0.0556
		  },
		  {
		    "source": "Anxiety",
		    "target": "Frustration",
		    "weight": 0.1603
		  },
		  {
		    "source": "Anxiety",
		    "target": "Gastritis",
		    "weight": 0.0476
		  },
		  {
		    "source": "Anxiety",
		    "target": "Gastroenteritis viral",
		    "weight": 0.2
		  },
		  {
		    "source": "Anxiety",
		    "target": "Gastrooesophageal reflux disease",
		    "weight": 0.2
		  },
		  {
		    "source": "Anxiety",
		    "target": "General physical health deterioration",
		    "weight": 0.0769
		  },
		  {
		    "source": "Anxiety",
		    "target": "Genital haemorrhage",
		    "weight": 0.0769
		  },
		  {
		    "source": "Anxiety",
		    "target": "Hallucinations, mixed",
		    "weight": 0.0833
		  },
		  {
		    "source": "Anxiety",
		    "target": "Headache",
		    "weight": 1.301
		  },
		  {
		    "source": "Anxiety",
		    "target": "Heart rate irregular",
		    "weight": 0.2
		  },
		  {
		    "source": "Anxiety",
		    "target": "Hostility",
		    "weight": 0.0833
		  },
		  {
		    "source": "Anxiety",
		    "target": "Hot flush",
		    "weight": 0.2
		  },
		  {
		    "source": "Anxiety",
		    "target": "Hypersomnia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Anxiety",
		    "target": "Impaired work ability",
		    "weight": 0.1667
		  },
		  {
		    "source": "Anxiety",
		    "target": "Impulsive behaviour",
		    "weight": 0.0833
		  },
		  {
		    "source": "Anxiety",
		    "target": "Inappropriate schedule of drug administration",
		    "weight": 0.7
		  },
		  {
		    "source": "Anxiety",
		    "target": "Incoherent",
		    "weight": 0.0833
		  },
		  {
		    "source": "Anxiety",
		    "target": "Increased appetite",
		    "weight": 0.131
		  },
		  {
		    "source": "Anxiety",
		    "target": "Injury",
		    "weight": 0.2019
		  },
		  {
		    "source": "Anxiety",
		    "target": "Insomnia",
		    "weight": 0.8056
		  },
		  {
		    "source": "Anxiety",
		    "target": "Irritability",
		    "weight": 0.3056
		  },
		  {
		    "source": "Anxiety",
		    "target": "Laziness",
		    "weight": 0.1111
		  },
		  {
		    "source": "Anxiety",
		    "target": "Libido decreased",
		    "weight": 0.2
		  },
		  {
		    "source": "Anxiety",
		    "target": "Logorrhoea",
		    "weight": 0.1429
		  },
		  {
		    "source": "Anxiety",
		    "target": "Malaise",
		    "weight": 0.2121
		  },
		  {
		    "source": "Anxiety",
		    "target": "Mania",
		    "weight": 0.0833
		  },
		  {
		    "source": "Anxiety",
		    "target": "Medical device discomfort",
		    "weight": 0.0769
		  },
		  {
		    "source": "Anxiety",
		    "target": "Medical device pain",
		    "weight": 0.0769
		  },
		  {
		    "source": "Anxiety",
		    "target": "Memory impairment",
		    "weight": 0.1111
		  },
		  {
		    "source": "Anxiety",
		    "target": "Mental disorder",
		    "weight": 0.125
		  },
		  {
		    "source": "Anxiety",
		    "target": "Migraine",
		    "weight": 0.0455
		  },
		  {
		    "source": "Anxiety",
		    "target": "Motor dysfunction",
		    "weight": 0.125
		  },
		  {
		    "source": "Anxiety",
		    "target": "Myoclonic epilepsy",
		    "weight": 0.125
		  },
		  {
		    "source": "Anxiety",
		    "target": "Nasopharyngitis",
		    "weight": 0.0455
		  },
		  {
		    "source": "Anxiety",
		    "target": "Nausea",
		    "weight": 0.1389
		  },
		  {
		    "source": "Anxiety",
		    "target": "Nightmare",
		    "weight": 0.1667
		  },
		  {
		    "source": "Anxiety",
		    "target": "Obsessive thoughts",
		    "weight": 0.0556
		  },
		  {
		    "source": "Anxiety",
		    "target": "Obsessive-compulsive disorder",
		    "weight": 0.2
		  },
		  {
		    "source": "Anxiety",
		    "target": "Oesophagitis",
		    "weight": 0.0833
		  },
		  {
		    "source": "Anxiety",
		    "target": "Off label use",
		    "weight": 0.2
		  },
		  {
		    "source": "Anxiety",
		    "target": "Optic nerve neoplasm",
		    "weight": 0.0833
		  },
		  {
		    "source": "Anxiety",
		    "target": "Osteoarthritis",
		    "weight": 0.0476
		  },
		  {
		    "source": "Anxiety",
		    "target": "Pain",
		    "weight": 0.1726
		  },
		  {
		    "source": "Anxiety",
		    "target": "Palpitations",
		    "weight": 0.3333
		  },
		  {
		    "source": "Anxiety",
		    "target": "Panic attack",
		    "weight": 0.3587
		  },
		  {
		    "source": "Anxiety",
		    "target": "Panic disorder",
		    "weight": 0.125
		  },
		  {
		    "source": "Anxiety",
		    "target": "Panic reaction",
		    "weight": 0.25
		  },
		  {
		    "source": "Anxiety",
		    "target": "Poor quality sleep",
		    "weight": 0.0476
		  },
		  {
		    "source": "Anxiety",
		    "target": "Post procedural discomfort",
		    "weight": 0.0769
		  },
		  {
		    "source": "Anxiety",
		    "target": "Procedural pain",
		    "weight": 0.0769
		  },
		  {
		    "source": "Anxiety",
		    "target": "Psychomotor hyperactivity",
		    "weight": 0.0833
		  },
		  {
		    "source": "Anxiety",
		    "target": "Psychotic disorder",
		    "weight": 0.0476
		  },
		  {
		    "source": "Anxiety",
		    "target": "Pulmonary embolism",
		    "weight": 0.125
		  },
		  {
		    "source": "Anxiety",
		    "target": "Pyrexia",
		    "weight": 0.0833
		  },
		  {
		    "source": "Anxiety",
		    "target": "Scar",
		    "weight": 0.0476
		  },
		  {
		    "source": "Anxiety",
		    "target": "Seizure",
		    "weight": 0.0833
		  },
		  {
		    "source": "Anxiety",
		    "target": "Self-injurious ideation",
		    "weight": 0.1667
		  },
		  {
		    "source": "Anxiety",
		    "target": "Social avoidant behaviour",
		    "weight": 0.0556
		  },
		  {
		    "source": "Anxiety",
		    "target": "Social phobia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Anxiety",
		    "target": "Somnolence",
		    "weight": 0.0833
		  },
		  {
		    "source": "Anxiety",
		    "target": "Stress",
		    "weight": 0.3333
		  },
		  {
		    "source": "Anxiety",
		    "target": "Surgery",
		    "weight": 0.2
		  },
		  {
		    "source": "Anxiety",
		    "target": "Syncope",
		    "weight": 0.0833
		  },
		  {
		    "source": "Anxiety",
		    "target": "Tachyphrenia",
		    "weight": 0.2455
		  },
		  {
		    "source": "Anxiety",
		    "target": "Tension",
		    "weight": 0.2
		  },
		  {
		    "source": "Anxiety",
		    "target": "Thinking abnormal",
		    "weight": 0.125
		  },
		  {
		    "source": "Anxiety",
		    "target": "Tic",
		    "weight": 0.0556
		  },
		  {
		    "source": "Anxiety",
		    "target": "Tooth infection",
		    "weight": 0.0476
		  },
		  {
		    "source": "Anxiety",
		    "target": "Tooth loss",
		    "weight": 0.0476
		  },
		  {
		    "source": "Anxiety",
		    "target": "Toothache",
		    "weight": 0.0476
		  },
		  {
		    "source": "Anxiety",
		    "target": "Tourette's disorder",
		    "weight": 0.0833
		  },
		  {
		    "source": "Anxiety",
		    "target": "Unevaluable event",
		    "weight": 0.0833
		  },
		  {
		    "source": "Anxiety",
		    "target": "Uterine perforation",
		    "weight": 0.0769
		  },
		  {
		    "source": "Anxiety",
		    "target": "Vomiting",
		    "weight": 0.0556
		  },
		  {
		    "source": "Anxiety",
		    "target": "Weight decreased",
		    "weight": 0.1111
		  },
		  {
		    "source": "Anxiety",
		    "target": "Weight increased",
		    "weight": 0.1288
		  },
		  {
		    "source": "Anxiety",
		    "target": "Withdrawal syndrome",
		    "weight": 0.1667
		  },
		  {
		    "source": "Apathy",
		    "target": "Bipolar disorder",
		    "weight": 0.2455
		  },
		  {
		    "source": "Apathy",
		    "target": "Catatonia",
		    "weight": 0.1667
		  },
		  {
		    "source": "Apathy",
		    "target": "Condition aggravated",
		    "weight": 0.0714
		  },
		  {
		    "source": "Apathy",
		    "target": "Decreased appetite",
		    "weight": 0.2
		  },
		  {
		    "source": "Apathy",
		    "target": "Depression",
		    "weight": 0.2455
		  },
		  {
		    "source": "Apathy",
		    "target": "Drug dose omission",
		    "weight": 0.0455
		  },
		  {
		    "source": "Apathy",
		    "target": "Drug effect decreased",
		    "weight": 0.0455
		  },
		  {
		    "source": "Apathy",
		    "target": "Drug effect increased",
		    "weight": 0.0455
		  },
		  {
		    "source": "Apathy",
		    "target": "Drug ineffective",
		    "weight": 0.4502
		  },
		  {
		    "source": "Apathy",
		    "target": "Dyskinesia",
		    "weight": 0.0714
		  },
		  {
		    "source": "Apathy",
		    "target": "Eye irritation",
		    "weight": 0.0455
		  },
		  {
		    "source": "Apathy",
		    "target": "Eye movement disorder",
		    "weight": 0.0714
		  },
		  {
		    "source": "Apathy",
		    "target": "Fatigue",
		    "weight": 0.0455
		  },
		  {
		    "source": "Apathy",
		    "target": "Fear",
		    "weight": 0.0455
		  },
		  {
		    "source": "Apathy",
		    "target": "Feeling abnormal",
		    "weight": 0.1667
		  },
		  {
		    "source": "Apathy",
		    "target": "Feeling of despair",
		    "weight": 0.2
		  },
		  {
		    "source": "Apathy",
		    "target": "Headache",
		    "weight": 0.0455
		  },
		  {
		    "source": "Apathy",
		    "target": "Hyperphagia",
		    "weight": 0.0714
		  },
		  {
		    "source": "Apathy",
		    "target": "Hypersomnia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Apathy",
		    "target": "Impaired work ability",
		    "weight": 0.1667
		  },
		  {
		    "source": "Apathy",
		    "target": "Laziness",
		    "weight": 0.0714
		  },
		  {
		    "source": "Apathy",
		    "target": "Malaise",
		    "weight": 0.0455
		  },
		  {
		    "source": "Apathy",
		    "target": "Migraine",
		    "weight": 0.0455
		  },
		  {
		    "source": "Apathy",
		    "target": "Musculoskeletal stiffness",
		    "weight": 0.0714
		  },
		  {
		    "source": "Apathy",
		    "target": "Nasopharyngitis",
		    "weight": 0.0455
		  },
		  {
		    "source": "Apathy",
		    "target": "Product substitution issue",
		    "weight": 0.3333
		  },
		  {
		    "source": "Apathy",
		    "target": "Social avoidant behaviour",
		    "weight": 0.0714
		  },
		  {
		    "source": "Apathy",
		    "target": "Social phobia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Apathy",
		    "target": "Tachyphrenia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Apathy",
		    "target": "Thirst",
		    "weight": 0.0714
		  },
		  {
		    "source": "Apathy",
		    "target": "Victim of abuse",
		    "weight": 0.0714
		  },
		  {
		    "source": "Apathy",
		    "target": "Victim of sexual abuse",
		    "weight": 0.0714
		  },
		  {
		    "source": "Apathy",
		    "target": "Weight increased",
		    "weight": 0.1169
		  },
		  {
		    "source": "Aphasia",
		    "target": "Dizziness",
		    "weight": 0.0833
		  },
		  {
		    "source": "Aphasia",
		    "target": "Dyspnoea",
		    "weight": 0.0833
		  },
		  {
		    "source": "Aphasia",
		    "target": "Hallucinations, mixed",
		    "weight": 0.0833
		  },
		  {
		    "source": "Aphasia",
		    "target": "Incoherent",
		    "weight": 0.0833
		  },
		  {
		    "source": "Aphasia",
		    "target": "Nausea",
		    "weight": 0.0833
		  },
		  {
		    "source": "Aphasia",
		    "target": "Oesophagitis",
		    "weight": 0.0833
		  },
		  {
		    "source": "Aphasia",
		    "target": "Pyrexia",
		    "weight": 0.0833
		  },
		  {
		    "source": "Aphasia",
		    "target": "Seizure",
		    "weight": 0.0833
		  },
		  {
		    "source": "Aphasia",
		    "target": "Syncope",
		    "weight": 0.0833
		  },
		  {
		    "source": "Aphasia",
		    "target": "Unevaluable event",
		    "weight": 0.0833
		  },
		  {
		    "source": "Appendicitis",
		    "target": "Pyrexia",
		    "weight": 0.25
		  },
		  {
		    "source": "Appendicitis",
		    "target": "Vomiting",
		    "weight": 0.25
		  },
		  {
		    "source": "Appetite disorder",
		    "target": "Sleep disorder",
		    "weight": 0.5
		  },
		  {
		    "source": "Application site vesicles",
		    "target": "Rash",
		    "weight": 0.5
		  },
		  {
		    "source": "Arthralgia",
		    "target": "Arthritis",
		    "weight": 0.2
		  },
		  {
		    "source": "Arthralgia",
		    "target": "Arthropathy",
		    "weight": 0.2
		  },
		  {
		    "source": "Arthralgia",
		    "target": "Autoimmune disorder",
		    "weight": 0.2
		  },
		  {
		    "source": "Arthralgia",
		    "target": "Back disorder",
		    "weight": 0.2
		  },
		  {
		    "source": "Arthralgia",
		    "target": "Back pain",
		    "weight": 0.3429
		  },
		  {
		    "source": "Arthralgia",
		    "target": "Blood cholesterol increased",
		    "weight": 0.2
		  },
		  {
		    "source": "Arthralgia",
		    "target": "Blood glucose increased",
		    "weight": 0.1
		  },
		  {
		    "source": "Arthralgia",
		    "target": "Condition aggravated",
		    "weight": 0.2
		  },
		  {
		    "source": "Arthralgia",
		    "target": "Decreased interest",
		    "weight": 0.1
		  },
		  {
		    "source": "Arthralgia",
		    "target": "Dehydration",
		    "weight": 0.2
		  },
		  {
		    "source": "Arthralgia",
		    "target": "Depression",
		    "weight": 0.1
		  },
		  {
		    "source": "Arthralgia",
		    "target": "Disease progression",
		    "weight": 0.2
		  },
		  {
		    "source": "Arthralgia",
		    "target": "Drug dose omission",
		    "weight": 0.2
		  },
		  {
		    "source": "Arthralgia",
		    "target": "Drug ineffective",
		    "weight": 0.3333
		  },
		  {
		    "source": "Arthralgia",
		    "target": "Dysgeusia",
		    "weight": 0.1111
		  },
		  {
		    "source": "Arthralgia",
		    "target": "Fatigue",
		    "weight": 0.1111
		  },
		  {
		    "source": "Arthralgia",
		    "target": "General physical health deterioration",
		    "weight": 0.1111
		  },
		  {
		    "source": "Arthralgia",
		    "target": "Hypoaesthesia",
		    "weight": 0.1111
		  },
		  {
		    "source": "Arthralgia",
		    "target": "Impaired work ability",
		    "weight": 0.1429
		  },
		  {
		    "source": "Arthralgia",
		    "target": "Insomnia",
		    "weight": 0.1
		  },
		  {
		    "source": "Arthralgia",
		    "target": "Irritable bowel syndrome",
		    "weight": 0.1111
		  },
		  {
		    "source": "Arthralgia",
		    "target": "Joint stiffness",
		    "weight": 0.2
		  },
		  {
		    "source": "Arthralgia",
		    "target": "Meniscus injury",
		    "weight": 0.2
		  },
		  {
		    "source": "Arthralgia",
		    "target": "Muscle spasms",
		    "weight": 0.1111
		  },
		  {
		    "source": "Arthralgia",
		    "target": "Musculoskeletal disorder",
		    "weight": 0.1111
		  },
		  {
		    "source": "Arthralgia",
		    "target": "Musculoskeletal pain",
		    "weight": 0.1429
		  },
		  {
		    "source": "Arthralgia",
		    "target": "Neck pain",
		    "weight": 0.1429
		  },
		  {
		    "source": "Arthralgia",
		    "target": "No therapeutic response",
		    "weight": 0.1
		  },
		  {
		    "source": "Arthralgia",
		    "target": "Pain",
		    "weight": 0.1429
		  },
		  {
		    "source": "Arthralgia",
		    "target": "Pain in extremity",
		    "weight": 0.1
		  },
		  {
		    "source": "Arthralgia",
		    "target": "Paraesthesia",
		    "weight": 0.1
		  },
		  {
		    "source": "Arthralgia",
		    "target": "Product quality issue",
		    "weight": 0.3333
		  },
		  {
		    "source": "Arthralgia",
		    "target": "Product substitution issue",
		    "weight": 0.2429
		  },
		  {
		    "source": "Arthralgia",
		    "target": "Pyoderma gangrenosum",
		    "weight": 0.5
		  },
		  {
		    "source": "Arthralgia",
		    "target": "Syncope",
		    "weight": 0.1111
		  },
		  {
		    "source": "Arthralgia",
		    "target": "Vertigo",
		    "weight": 0.1
		  },
		  {
		    "source": "Arthritis",
		    "target": "Autoimmune disorder",
		    "weight": 0.2
		  },
		  {
		    "source": "Arthritis",
		    "target": "Disease progression",
		    "weight": 0.2
		  },
		  {
		    "source": "Arthritis",
		    "target": "Drug dose omission",
		    "weight": 0.2
		  },
		  {
		    "source": "Arthropathy",
		    "target": "Dehydration",
		    "weight": 0.2
		  },
		  {
		    "source": "Arthropathy",
		    "target": "Joint stiffness",
		    "weight": 0.2
		  },
		  {
		    "source": "Arthropathy",
		    "target": "Meniscus injury",
		    "weight": 0.2
		  },
		  {
		    "source": "Arthropathy",
		    "target": "Shoulder arthroplasty",
		    "weight": 0.5
		  },
		  {
		    "source": "Asthenia",
		    "target": "Balance disorder",
		    "weight": 0.0526
		  },
		  {
		    "source": "Asthenia",
		    "target": "Constipation",
		    "weight": 0.0526
		  },
		  {
		    "source": "Asthenia",
		    "target": "Crying",
		    "weight": 0.125
		  },
		  {
		    "source": "Asthenia",
		    "target": "Depression",
		    "weight": 0.1
		  },
		  {
		    "source": "Asthenia",
		    "target": "Disability",
		    "weight": 0.125
		  },
		  {
		    "source": "Asthenia",
		    "target": "Disturbance in attention",
		    "weight": 0.1
		  },
		  {
		    "source": "Asthenia",
		    "target": "Drug ineffective",
		    "weight": 0.125
		  },
		  {
		    "source": "Asthenia",
		    "target": "Epistaxis",
		    "weight": 0.0526
		  },
		  {
		    "source": "Asthenia",
		    "target": "Fatigue",
		    "weight": 0.3193
		  },
		  {
		    "source": "Asthenia",
		    "target": "Feeling abnormal",
		    "weight": 0.1
		  },
		  {
		    "source": "Asthenia",
		    "target": "Flushing",
		    "weight": 0.1667
		  },
		  {
		    "source": "Asthenia",
		    "target": "Gait disturbance",
		    "weight": 0.0526
		  },
		  {
		    "source": "Asthenia",
		    "target": "Headache",
		    "weight": 0.125
		  },
		  {
		    "source": "Asthenia",
		    "target": "Heart rate decreased",
		    "weight": 0.0526
		  },
		  {
		    "source": "Asthenia",
		    "target": "Hypoaesthesia",
		    "weight": 0.1667
		  },
		  {
		    "source": "Asthenia",
		    "target": "Hypotension",
		    "weight": 0.0526
		  },
		  {
		    "source": "Asthenia",
		    "target": "Impaired healing",
		    "weight": 0.0526
		  },
		  {
		    "source": "Asthenia",
		    "target": "Insomnia",
		    "weight": 0.2193
		  },
		  {
		    "source": "Asthenia",
		    "target": "Intentional self-injury",
		    "weight": 0.1
		  },
		  {
		    "source": "Asthenia",
		    "target": "Invasive ductal breast carcinoma",
		    "weight": 0.0526
		  },
		  {
		    "source": "Asthenia",
		    "target": "Malaise",
		    "weight": 0.1667
		  },
		  {
		    "source": "Asthenia",
		    "target": "Memory impairment",
		    "weight": 0.2667
		  },
		  {
		    "source": "Asthenia",
		    "target": "Mental disorder",
		    "weight": 0.1
		  },
		  {
		    "source": "Asthenia",
		    "target": "Mood altered",
		    "weight": 0.1
		  },
		  {
		    "source": "Asthenia",
		    "target": "Nightmare",
		    "weight": 0.1667
		  },
		  {
		    "source": "Asthenia",
		    "target": "Oral discomfort",
		    "weight": 0.1667
		  },
		  {
		    "source": "Asthenia",
		    "target": "Performance status decreased",
		    "weight": 0.125
		  },
		  {
		    "source": "Asthenia",
		    "target": "Pneumonia",
		    "weight": 0.0526
		  },
		  {
		    "source": "Asthenia",
		    "target": "Prescribed overdose",
		    "weight": 0.125
		  },
		  {
		    "source": "Asthenia",
		    "target": "Rash pruritic",
		    "weight": 0.0526
		  },
		  {
		    "source": "Asthenia",
		    "target": "Rash pustular",
		    "weight": 0.0526
		  },
		  {
		    "source": "Asthenia",
		    "target": "Self-injurious ideation",
		    "weight": 0.1667
		  },
		  {
		    "source": "Asthenia",
		    "target": "Skin mass",
		    "weight": 0.0526
		  },
		  {
		    "source": "Asthenia",
		    "target": "Suicidal ideation",
		    "weight": 0.5
		  },
		  {
		    "source": "Asthenia",
		    "target": "Therapy cessation",
		    "weight": 0.1776
		  },
		  {
		    "source": "Asthenia",
		    "target": "Urinary hesitation",
		    "weight": 0.0526
		  },
		  {
		    "source": "Asthenia",
		    "target": "Urinary retention",
		    "weight": 0.0526
		  },
		  {
		    "source": "Asthenia",
		    "target": "Vertigo",
		    "weight": 0.0526
		  },
		  {
		    "source": "Asthma",
		    "target": "Sinus disorder",
		    "weight": 0.2
		  },
		  {
		    "source": "Asthma",
		    "target": "Sleep apnoea syndrome",
		    "weight": 0.2
		  },
		  {
		    "source": "Asthma",
		    "target": "Upper-airway cough syndrome",
		    "weight": 0.2
		  },
		  {
		    "source": "Attention deficit\/hyperactivity disorder",
		    "target": "Bruxism",
		    "weight": 0.0476
		  },
		  {
		    "source": "Attention deficit\/hyperactivity disorder",
		    "target": "Condition aggravated",
		    "weight": 0.4476
		  },
		  {
		    "source": "Attention deficit\/hyperactivity disorder",
		    "target": "Decreased appetite",
		    "weight": 0.0476
		  },
		  {
		    "source": "Attention deficit\/hyperactivity disorder",
		    "target": "Depression",
		    "weight": 0.0476
		  },
		  {
		    "source": "Attention deficit\/hyperactivity disorder",
		    "target": "Dermatitis",
		    "weight": 0.0476
		  },
		  {
		    "source": "Attention deficit\/hyperactivity disorder",
		    "target": "Disturbance in attention",
		    "weight": 0.25
		  },
		  {
		    "source": "Attention deficit\/hyperactivity disorder",
		    "target": "Diverticulitis",
		    "weight": 0.0476
		  },
		  {
		    "source": "Attention deficit\/hyperactivity disorder",
		    "target": "Drug dose omission",
		    "weight": 0.2
		  },
		  {
		    "source": "Attention deficit\/hyperactivity disorder",
		    "target": "Feeding disorder",
		    "weight": 0.0476
		  },
		  {
		    "source": "Attention deficit\/hyperactivity disorder",
		    "target": "Gastritis",
		    "weight": 0.0476
		  },
		  {
		    "source": "Attention deficit\/hyperactivity disorder",
		    "target": "Increased appetite",
		    "weight": 0.0476
		  },
		  {
		    "source": "Attention deficit\/hyperactivity disorder",
		    "target": "Job dissatisfaction",
		    "weight": 0.25
		  },
		  {
		    "source": "Attention deficit\/hyperactivity disorder",
		    "target": "Mania",
		    "weight": 0.2
		  },
		  {
		    "source": "Attention deficit\/hyperactivity disorder",
		    "target": "Migraine",
		    "weight": 0.2
		  },
		  {
		    "source": "Attention deficit\/hyperactivity disorder",
		    "target": "Osteoarthritis",
		    "weight": 0.0476
		  },
		  {
		    "source": "Attention deficit\/hyperactivity disorder",
		    "target": "Pain",
		    "weight": 0.0476
		  },
		  {
		    "source": "Attention deficit\/hyperactivity disorder",
		    "target": "Panic attack",
		    "weight": 0.0476
		  },
		  {
		    "source": "Attention deficit\/hyperactivity disorder",
		    "target": "Poor quality sleep",
		    "weight": 0.0476
		  },
		  {
		    "source": "Attention deficit\/hyperactivity disorder",
		    "target": "Prescribed overdose",
		    "weight": 0.25
		  },
		  {
		    "source": "Attention deficit\/hyperactivity disorder",
		    "target": "Psychotic disorder",
		    "weight": 0.0476
		  },
		  {
		    "source": "Attention deficit\/hyperactivity disorder",
		    "target": "Scar",
		    "weight": 0.0476
		  },
		  {
		    "source": "Attention deficit\/hyperactivity disorder",
		    "target": "Therapy cessation",
		    "weight": 0.2
		  },
		  {
		    "source": "Attention deficit\/hyperactivity disorder",
		    "target": "Tooth infection",
		    "weight": 0.0476
		  },
		  {
		    "source": "Attention deficit\/hyperactivity disorder",
		    "target": "Tooth loss",
		    "weight": 0.0476
		  },
		  {
		    "source": "Attention deficit\/hyperactivity disorder",
		    "target": "Toothache",
		    "weight": 0.0476
		  },
		  {
		    "source": "Autoimmune disorder",
		    "target": "Disease progression",
		    "weight": 0.2
		  },
		  {
		    "source": "Autoimmune disorder",
		    "target": "Drug dose omission",
		    "weight": 0.2
		  },
		  {
		    "source": "Back disorder",
		    "target": "Back pain",
		    "weight": 0.2
		  },
		  {
		    "source": "Back disorder",
		    "target": "Blood cholesterol increased",
		    "weight": 0.2
		  },
		  {
		    "source": "Back disorder",
		    "target": "Condition aggravated",
		    "weight": 0.2
		  },
		  {
		    "source": "Back disorder",
		    "target": "Foot operation",
		    "weight": 0.125
		  },
		  {
		    "source": "Back disorder",
		    "target": "Inappropriate schedule of drug administration",
		    "weight": 0.125
		  },
		  {
		    "source": "Back disorder",
		    "target": "Intervertebral disc protrusion",
		    "weight": 0.125
		  },
		  {
		    "source": "Back disorder",
		    "target": "Knee operation",
		    "weight": 0.125
		  },
		  {
		    "source": "Back disorder",
		    "target": "Limb injury",
		    "weight": 0.125
		  },
		  {
		    "source": "Back disorder",
		    "target": "Pain",
		    "weight": 0.125
		  },
		  {
		    "source": "Back disorder",
		    "target": "Product use issue",
		    "weight": 0.125
		  },
		  {
		    "source": "Back pain",
		    "target": "Blood cholesterol increased",
		    "weight": 0.2
		  },
		  {
		    "source": "Back pain",
		    "target": "Condition aggravated",
		    "weight": 0.2
		  },
		  {
		    "source": "Back pain",
		    "target": "Impaired work ability",
		    "weight": 0.1429
		  },
		  {
		    "source": "Back pain",
		    "target": "Musculoskeletal pain",
		    "weight": 0.1429
		  },
		  {
		    "source": "Back pain",
		    "target": "Neck pain",
		    "weight": 0.1429
		  },
		  {
		    "source": "Back pain",
		    "target": "Pain",
		    "weight": 0.1429
		  },
		  {
		    "source": "Back pain",
		    "target": "Product substitution issue",
		    "weight": 0.1429
		  },
		  {
		    "source": "Balance disorder",
		    "target": "Constipation",
		    "weight": 0.0526
		  },
		  {
		    "source": "Balance disorder",
		    "target": "Epistaxis",
		    "weight": 0.0526
		  },
		  {
		    "source": "Balance disorder",
		    "target": "Fatigue",
		    "weight": 0.0526
		  },
		  {
		    "source": "Balance disorder",
		    "target": "Gait disturbance",
		    "weight": 0.0526
		  },
		  {
		    "source": "Balance disorder",
		    "target": "Heart rate decreased",
		    "weight": 0.0526
		  },
		  {
		    "source": "Balance disorder",
		    "target": "Hypotension",
		    "weight": 0.0526
		  },
		  {
		    "source": "Balance disorder",
		    "target": "Impaired healing",
		    "weight": 0.0526
		  },
		  {
		    "source": "Balance disorder",
		    "target": "Insomnia",
		    "weight": 0.0526
		  },
		  {
		    "source": "Balance disorder",
		    "target": "Invasive ductal breast carcinoma",
		    "weight": 0.0526
		  },
		  {
		    "source": "Balance disorder",
		    "target": "Pneumonia",
		    "weight": 0.0526
		  },
		  {
		    "source": "Balance disorder",
		    "target": "Rash pruritic",
		    "weight": 0.0526
		  },
		  {
		    "source": "Balance disorder",
		    "target": "Rash pustular",
		    "weight": 0.0526
		  },
		  {
		    "source": "Balance disorder",
		    "target": "Skin mass",
		    "weight": 0.0526
		  },
		  {
		    "source": "Balance disorder",
		    "target": "Therapy cessation",
		    "weight": 0.0526
		  },
		  {
		    "source": "Balance disorder",
		    "target": "Urinary hesitation",
		    "weight": 0.0526
		  },
		  {
		    "source": "Balance disorder",
		    "target": "Urinary retention",
		    "weight": 0.0526
		  },
		  {
		    "source": "Balance disorder",
		    "target": "Vertigo",
		    "weight": 0.0526
		  },
		  {
		    "source": "Bedridden",
		    "target": "Bipolar disorder",
		    "weight": 0.2
		  },
		  {
		    "source": "Bedridden",
		    "target": "Drug dose omission",
		    "weight": 0.2
		  },
		  {
		    "source": "Bedridden",
		    "target": "Off label use",
		    "weight": 0.2
		  },
		  {
		    "source": "Bedridden",
		    "target": "Weight increased",
		    "weight": 0.2
		  },
		  {
		    "source": "Benign intracranial hypertension",
		    "target": "Papilloedema",
		    "weight": 0.5
		  },
		  {
		    "source": "Benign neoplasm of thyroid gland",
		    "target": "Condition aggravated",
		    "weight": 0.3333
		  },
		  {
		    "source": "Benign neoplasm of thyroid gland",
		    "target": "House dust allergy",
		    "weight": 0.3333
		  },
		  {
		    "source": "Binge eating",
		    "target": "Condition aggravated",
		    "weight": 0.5
		  },
		  {
		    "source": "Binge eating",
		    "target": "Inappropriate schedule of drug administration",
		    "weight": 0.5
		  },
		  {
		    "source": "Bipolar disorder",
		    "target": "Decreased appetite",
		    "weight": 0.2
		  },
		  {
		    "source": "Bipolar disorder",
		    "target": "Depression",
		    "weight": 0.2455
		  },
		  {
		    "source": "Bipolar disorder",
		    "target": "Drug dose omission",
		    "weight": 0.2455
		  },
		  {
		    "source": "Bipolar disorder",
		    "target": "Drug effect decreased",
		    "weight": 0.0455
		  },
		  {
		    "source": "Bipolar disorder",
		    "target": "Drug effect increased",
		    "weight": 0.0455
		  },
		  {
		    "source": "Bipolar disorder",
		    "target": "Drug ineffective",
		    "weight": 0.0455
		  },
		  {
		    "source": "Bipolar disorder",
		    "target": "Eye irritation",
		    "weight": 0.0455
		  },
		  {
		    "source": "Bipolar disorder",
		    "target": "Fatigue",
		    "weight": 0.0455
		  },
		  {
		    "source": "Bipolar disorder",
		    "target": "Fear",
		    "weight": 0.0455
		  },
		  {
		    "source": "Bipolar disorder",
		    "target": "Feeling of despair",
		    "weight": 0.2
		  },
		  {
		    "source": "Bipolar disorder",
		    "target": "Headache",
		    "weight": 0.0455
		  },
		  {
		    "source": "Bipolar disorder",
		    "target": "Hypersomnia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Bipolar disorder",
		    "target": "Malaise",
		    "weight": 0.0455
		  },
		  {
		    "source": "Bipolar disorder",
		    "target": "Migraine",
		    "weight": 0.0455
		  },
		  {
		    "source": "Bipolar disorder",
		    "target": "Nasopharyngitis",
		    "weight": 0.0455
		  },
		  {
		    "source": "Bipolar disorder",
		    "target": "Off label use",
		    "weight": 0.2
		  },
		  {
		    "source": "Bipolar disorder",
		    "target": "Social phobia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Bipolar disorder",
		    "target": "Tachyphrenia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Bipolar disorder",
		    "target": "Weight increased",
		    "weight": 0.2455
		  },
		  {
		    "source": "Blindness unilateral",
		    "target": "Drug dose omission",
		    "weight": 0.3333
		  },
		  {
		    "source": "Blindness unilateral",
		    "target": "Migraine",
		    "weight": 0.3333
		  },
		  {
		    "source": "Blood cholesterol increased",
		    "target": "Condition aggravated",
		    "weight": 0.2
		  },
		  {
		    "source": "Blood creatine phosphokinase increased",
		    "target": "Intentional overdose",
		    "weight": 0.3333
		  },
		  {
		    "source": "Blood creatine phosphokinase increased",
		    "target": "Renal impairment",
		    "weight": 0.3333
		  },
		  {
		    "source": "Blood glucose decreased",
		    "target": "Blood pressure systolic increased",
		    "weight": 0.1
		  },
		  {
		    "source": "Blood glucose decreased",
		    "target": "Cystic fibrosis related diabetes",
		    "weight": 0.1
		  },
		  {
		    "source": "Blood glucose decreased",
		    "target": "Depressed mood",
		    "weight": 0.1
		  },
		  {
		    "source": "Blood glucose decreased",
		    "target": "Dyspepsia",
		    "weight": 0.1
		  },
		  {
		    "source": "Blood glucose decreased",
		    "target": "Mycobacterium test positive",
		    "weight": 0.1
		  },
		  {
		    "source": "Blood glucose decreased",
		    "target": "Obstructive airways disorder",
		    "weight": 0.1
		  },
		  {
		    "source": "Blood glucose decreased",
		    "target": "Pseudomonas infection",
		    "weight": 0.1
		  },
		  {
		    "source": "Blood glucose decreased",
		    "target": "Sinus disorder",
		    "weight": 0.1
		  },
		  {
		    "source": "Blood glucose decreased",
		    "target": "Weight increased",
		    "weight": 0.1
		  },
		  {
		    "source": "Blood glucose increased",
		    "target": "Condition aggravated",
		    "weight": 0.1429
		  },
		  {
		    "source": "Blood glucose increased",
		    "target": "Decreased interest",
		    "weight": 0.1
		  },
		  {
		    "source": "Blood glucose increased",
		    "target": "Depression",
		    "weight": 0.1
		  },
		  {
		    "source": "Blood glucose increased",
		    "target": "Drug hypersensitivity",
		    "weight": 0.2
		  },
		  {
		    "source": "Blood glucose increased",
		    "target": "Drug ineffective",
		    "weight": 0.1429
		  },
		  {
		    "source": "Blood glucose increased",
		    "target": "Fatigue",
		    "weight": 0.2
		  },
		  {
		    "source": "Blood glucose increased",
		    "target": "Headache",
		    "weight": 0.2
		  },
		  {
		    "source": "Blood glucose increased",
		    "target": "Insomnia",
		    "weight": 0.1
		  },
		  {
		    "source": "Blood glucose increased",
		    "target": "No therapeutic response",
		    "weight": 0.1
		  },
		  {
		    "source": "Blood glucose increased",
		    "target": "Pain in extremity",
		    "weight": 0.1
		  },
		  {
		    "source": "Blood glucose increased",
		    "target": "Paraesthesia",
		    "weight": 0.1
		  },
		  {
		    "source": "Blood glucose increased",
		    "target": "Product quality issue",
		    "weight": 0.1429
		  },
		  {
		    "source": "Blood glucose increased",
		    "target": "Product substitution issue",
		    "weight": 0.1
		  },
		  {
		    "source": "Blood glucose increased",
		    "target": "Pyrexia",
		    "weight": 0.2
		  },
		  {
		    "source": "Blood glucose increased",
		    "target": "Sleep disorder",
		    "weight": 0.1429
		  },
		  {
		    "source": "Blood glucose increased",
		    "target": "Vertigo",
		    "weight": 0.1
		  },
		  {
		    "source": "Blood glucose increased",
		    "target": "Wrist fracture",
		    "weight": 0.1429
		  },
		  {
		    "source": "Blood iron abnormal",
		    "target": "Condition aggravated",
		    "weight": 0.0833
		  },
		  {
		    "source": "Blood iron abnormal",
		    "target": "Depression",
		    "weight": 0.0833
		  },
		  {
		    "source": "Blood iron abnormal",
		    "target": "Drug ineffective",
		    "weight": 0.0833
		  },
		  {
		    "source": "Blood iron abnormal",
		    "target": "Formication",
		    "weight": 0.0833
		  },
		  {
		    "source": "Blood iron abnormal",
		    "target": "Hostility",
		    "weight": 0.0833
		  },
		  {
		    "source": "Blood iron abnormal",
		    "target": "Irritability",
		    "weight": 0.0833
		  },
		  {
		    "source": "Blood iron abnormal",
		    "target": "Malabsorption",
		    "weight": 0.0833
		  },
		  {
		    "source": "Blood iron abnormal",
		    "target": "Mood swings",
		    "weight": 0.0833
		  },
		  {
		    "source": "Blood iron abnormal",
		    "target": "Vitamin D abnormal",
		    "weight": 0.0833
		  },
		  {
		    "source": "Blood iron abnormal",
		    "target": "Vitreous floaters",
		    "weight": 0.0833
		  },
		  {
		    "source": "Blood oestrogen abnormal",
		    "target": "Hepatic enzyme increased",
		    "weight": 0.25
		  },
		  {
		    "source": "Blood oestrogen abnormal",
		    "target": "Lipids increased",
		    "weight": 0.25
		  },
		  {
		    "source": "Blood oestrogen abnormal",
		    "target": "Urinary tract infection",
		    "weight": 0.25
		  },
		  {
		    "source": "Blood pressure decreased",
		    "target": "Cervical spinal stenosis",
		    "weight": 0.25
		  },
		  {
		    "source": "Blood pressure decreased",
		    "target": "Spinal osteoarthritis",
		    "weight": 0.25
		  },
		  {
		    "source": "Blood pressure decreased",
		    "target": "Therapeutic response unexpected",
		    "weight": 0.25
		  },
		  {
		    "source": "Blood pressure increased",
		    "target": "Chest pain",
		    "weight": 0.25
		  },
		  {
		    "source": "Blood pressure increased",
		    "target": "Chills",
		    "weight": 0.0769
		  },
		  {
		    "source": "Blood pressure increased",
		    "target": "Dissociation",
		    "weight": 0.1
		  },
		  {
		    "source": "Blood pressure increased",
		    "target": "Drug abuse",
		    "weight": 0.25
		  },
		  {
		    "source": "Blood pressure increased",
		    "target": "Drug dose omission",
		    "weight": 0.25
		  },
		  {
		    "source": "Blood pressure increased",
		    "target": "Drug ineffective",
		    "weight": 0.0769
		  },
		  {
		    "source": "Blood pressure increased",
		    "target": "Drug interaction",
		    "weight": 0.1
		  },
		  {
		    "source": "Blood pressure increased",
		    "target": "Dyskinesia",
		    "weight": 0.1
		  },
		  {
		    "source": "Blood pressure increased",
		    "target": "Emotional distress",
		    "weight": 0.25
		  },
		  {
		    "source": "Blood pressure increased",
		    "target": "Fatigue",
		    "weight": 0.4103
		  },
		  {
		    "source": "Blood pressure increased",
		    "target": "Hyperhidrosis",
		    "weight": 0.1
		  },
		  {
		    "source": "Blood pressure increased",
		    "target": "Increased appetite",
		    "weight": 0.0769
		  },
		  {
		    "source": "Blood pressure increased",
		    "target": "Libido decreased",
		    "weight": 0.0769
		  },
		  {
		    "source": "Blood pressure increased",
		    "target": "Muscle spasms",
		    "weight": 0.1769
		  },
		  {
		    "source": "Blood pressure increased",
		    "target": "Mydriasis",
		    "weight": 0.1
		  },
		  {
		    "source": "Blood pressure increased",
		    "target": "Nausea",
		    "weight": 0.0769
		  },
		  {
		    "source": "Blood pressure increased",
		    "target": "Pain in extremity",
		    "weight": 0.25
		  },
		  {
		    "source": "Blood pressure increased",
		    "target": "Pain in jaw",
		    "weight": 0.0769
		  },
		  {
		    "source": "Blood pressure increased",
		    "target": "Palpitations",
		    "weight": 0.6603
		  },
		  {
		    "source": "Blood pressure increased",
		    "target": "Pyrexia",
		    "weight": 0.0769
		  },
		  {
		    "source": "Blood pressure increased",
		    "target": "Serotonin syndrome",
		    "weight": 0.1
		  },
		  {
		    "source": "Blood pressure increased",
		    "target": "Tachycardia",
		    "weight": 0.25
		  },
		  {
		    "source": "Blood pressure increased",
		    "target": "Tachyphrenia",
		    "weight": 0.1
		  },
		  {
		    "source": "Blood pressure increased",
		    "target": "Therapeutic response unexpected",
		    "weight": 0.3333
		  },
		  {
		    "source": "Blood pressure increased",
		    "target": "Vomiting",
		    "weight": 0.0769
		  },
		  {
		    "source": "Blood pressure systolic increased",
		    "target": "Cystic fibrosis related diabetes",
		    "weight": 0.1
		  },
		  {
		    "source": "Blood pressure systolic increased",
		    "target": "Depressed mood",
		    "weight": 0.1
		  },
		  {
		    "source": "Blood pressure systolic increased",
		    "target": "Dyspepsia",
		    "weight": 0.1
		  },
		  {
		    "source": "Blood pressure systolic increased",
		    "target": "Mycobacterium test positive",
		    "weight": 0.1
		  },
		  {
		    "source": "Blood pressure systolic increased",
		    "target": "Obstructive airways disorder",
		    "weight": 0.1
		  },
		  {
		    "source": "Blood pressure systolic increased",
		    "target": "Pseudomonas infection",
		    "weight": 0.1
		  },
		  {
		    "source": "Blood pressure systolic increased",
		    "target": "Sinus disorder",
		    "weight": 0.1
		  },
		  {
		    "source": "Blood pressure systolic increased",
		    "target": "Weight increased",
		    "weight": 0.1
		  },
		  {
		    "source": "Body temperature increased",
		    "target": "Diarrhoea",
		    "weight": 0.1
		  },
		  {
		    "source": "Body temperature increased",
		    "target": "Gastroenteritis viral",
		    "weight": 0.1
		  },
		  {
		    "source": "Body temperature increased",
		    "target": "Malaise",
		    "weight": 0.1
		  },
		  {
		    "source": "Body temperature increased",
		    "target": "Paranasal sinus hypersecretion",
		    "weight": 0.1
		  },
		  {
		    "source": "Body temperature increased",
		    "target": "Pharyngitis streptococcal",
		    "weight": 0.1
		  },
		  {
		    "source": "Body temperature increased",
		    "target": "Pyrexia",
		    "weight": 0.1
		  },
		  {
		    "source": "Body temperature increased",
		    "target": "Rales",
		    "weight": 0.1
		  },
		  {
		    "source": "Body temperature increased",
		    "target": "Upper respiratory tract infection",
		    "weight": 0.1
		  },
		  {
		    "source": "Body temperature increased",
		    "target": "Vomiting",
		    "weight": 0.1
		  },
		  {
		    "source": "Bone contusion",
		    "target": "Contusion",
		    "weight": 0.3333
		  },
		  {
		    "source": "Bone contusion",
		    "target": "Fall",
		    "weight": 0.3333
		  },
		  {
		    "source": "Brain injury",
		    "target": "Injury",
		    "weight": 0.2
		  },
		  {
		    "source": "Brain injury",
		    "target": "Neuralgia",
		    "weight": 0.2
		  },
		  {
		    "source": "Brain injury",
		    "target": "Road traffic accident",
		    "weight": 0.2
		  },
		  {
		    "source": "Brain injury",
		    "target": "Unevaluable event",
		    "weight": 0.2
		  },
		  {
		    "source": "Breakthrough pain",
		    "target": "Condition aggravated",
		    "weight": 0.2
		  },
		  {
		    "source": "Breakthrough pain",
		    "target": "Muscle injury",
		    "weight": 0.2
		  },
		  {
		    "source": "Breakthrough pain",
		    "target": "Musculoskeletal pain",
		    "weight": 0.2
		  },
		  {
		    "source": "Breakthrough pain",
		    "target": "Sinusitis",
		    "weight": 0.2
		  },
		  {
		    "source": "Breast cancer stage IV",
		    "target": "Malaise",
		    "weight": 0.5
		  },
		  {
		    "source": "Breast tenderness",
		    "target": "Fatigue",
		    "weight": 0.25
		  },
		  {
		    "source": "Breast tenderness",
		    "target": "Hot flush",
		    "weight": 0.5
		  },
		  {
		    "source": "Breast tenderness",
		    "target": "Nausea",
		    "weight": 0.25
		  },
		  {
		    "source": "Breast tenderness",
		    "target": "Vomiting",
		    "weight": 0.25
		  },
		  {
		    "source": "Breech presentation",
		    "target": "Drug withdrawal syndrome neonatal",
		    "weight": 0.1667
		  },
		  {
		    "source": "Breech presentation",
		    "target": "Foetal distress syndrome",
		    "weight": 0.1667
		  },
		  {
		    "source": "Breech presentation",
		    "target": "Foetal exposure during pregnancy",
		    "weight": 0.1667
		  },
		  {
		    "source": "Breech presentation",
		    "target": "Jaundice neonatal",
		    "weight": 0.1667
		  },
		  {
		    "source": "Breech presentation",
		    "target": "Premature baby",
		    "weight": 0.1667
		  },
		  {
		    "source": "Bruxism",
		    "target": "Condition aggravated",
		    "weight": 0.0476
		  },
		  {
		    "source": "Bruxism",
		    "target": "Decreased appetite",
		    "weight": 0.0476
		  },
		  {
		    "source": "Bruxism",
		    "target": "Depression",
		    "weight": 0.0476
		  },
		  {
		    "source": "Bruxism",
		    "target": "Dermatitis",
		    "weight": 0.0476
		  },
		  {
		    "source": "Bruxism",
		    "target": "Diverticulitis",
		    "weight": 0.0476
		  },
		  {
		    "source": "Bruxism",
		    "target": "Feeding disorder",
		    "weight": 0.0476
		  },
		  {
		    "source": "Bruxism",
		    "target": "Gastritis",
		    "weight": 0.0476
		  },
		  {
		    "source": "Bruxism",
		    "target": "Increased appetite",
		    "weight": 0.0476
		  },
		  {
		    "source": "Bruxism",
		    "target": "Osteoarthritis",
		    "weight": 0.0476
		  },
		  {
		    "source": "Bruxism",
		    "target": "Pain",
		    "weight": 0.0476
		  },
		  {
		    "source": "Bruxism",
		    "target": "Panic attack",
		    "weight": 0.0476
		  },
		  {
		    "source": "Bruxism",
		    "target": "Poor quality sleep",
		    "weight": 0.0476
		  },
		  {
		    "source": "Bruxism",
		    "target": "Psychotic disorder",
		    "weight": 0.0476
		  },
		  {
		    "source": "Bruxism",
		    "target": "Scar",
		    "weight": 0.0476
		  },
		  {
		    "source": "Bruxism",
		    "target": "Tooth infection",
		    "weight": 0.0476
		  },
		  {
		    "source": "Bruxism",
		    "target": "Tooth loss",
		    "weight": 0.0476
		  },
		  {
		    "source": "Bruxism",
		    "target": "Toothache",
		    "weight": 0.0476
		  },
		  {
		    "source": "Burning sensation",
		    "target": "Glossodynia",
		    "weight": 0.5
		  },
		  {
		    "source": "Burning sensation",
		    "target": "Headache",
		    "weight": 0.2
		  },
		  {
		    "source": "Burning sensation",
		    "target": "Nasal discomfort",
		    "weight": 0.2
		  },
		  {
		    "source": "Burning sensation",
		    "target": "Rhinalgia",
		    "weight": 0.2
		  },
		  {
		    "source": "Burning sensation",
		    "target": "Sinus headache",
		    "weight": 0.2
		  },
		  {
		    "source": "Burning sensation",
		    "target": "Swollen tongue",
		    "weight": 0.5
		  },
		  {
		    "source": "Caesarean section",
		    "target": "Maternal exposure during pregnancy",
		    "weight": 0.2
		  },
		  {
		    "source": "Caesarean section",
		    "target": "Premature delivery",
		    "weight": 0.2
		  },
		  {
		    "source": "Caesarean section",
		    "target": "Rhesus incompatibility",
		    "weight": 0.2
		  },
		  {
		    "source": "Caesarean section",
		    "target": "Transfusion",
		    "weight": 0.2
		  },
		  {
		    "source": "Calcinosis",
		    "target": "Chest pain",
		    "weight": 0.2
		  },
		  {
		    "source": "Calcinosis",
		    "target": "Gastrooesophageal reflux disease",
		    "weight": 0.2
		  },
		  {
		    "source": "Calcinosis",
		    "target": "Heart rate irregular",
		    "weight": 0.2
		  },
		  {
		    "source": "Cardiac arrest",
		    "target": "Seizure",
		    "weight": 0.5
		  },
		  {
		    "source": "Cardiac disorder",
		    "target": "Drug effect decreased",
		    "weight": 0.5
		  },
		  {
		    "source": "Cardiac failure congestive",
		    "target": "Cardiomyopathy",
		    "weight": 0.0769
		  },
		  {
		    "source": "Cardiac failure congestive",
		    "target": "Costochondritis",
		    "weight": 0.0769
		  },
		  {
		    "source": "Cardiac failure congestive",
		    "target": "Disease progression",
		    "weight": 0.1
		  },
		  {
		    "source": "Cardiac failure congestive",
		    "target": "Dyspnoea",
		    "weight": 0.1
		  },
		  {
		    "source": "Cardiac failure congestive",
		    "target": "Fluid overload",
		    "weight": 0.1
		  },
		  {
		    "source": "Cardiac failure congestive",
		    "target": "Gastrooesophageal reflux disease",
		    "weight": 0.0769
		  },
		  {
		    "source": "Cardiac failure congestive",
		    "target": "Grief reaction",
		    "weight": 0.0769
		  },
		  {
		    "source": "Cardiac failure congestive",
		    "target": "Nausea",
		    "weight": 0.0769
		  },
		  {
		    "source": "Cardiac failure congestive",
		    "target": "Oedema",
		    "weight": 0.1
		  },
		  {
		    "source": "Cardiac failure congestive",
		    "target": "Oedema peripheral",
		    "weight": 0.0769
		  },
		  {
		    "source": "Cardiac failure congestive",
		    "target": "Oxygen saturation decreased",
		    "weight": 0.1
		  },
		  {
		    "source": "Cardiac failure congestive",
		    "target": "Peripheral swelling",
		    "weight": 0.1
		  },
		  {
		    "source": "Cardiac failure congestive",
		    "target": "Pleural effusion",
		    "weight": 0.0769
		  },
		  {
		    "source": "Cardiac failure congestive",
		    "target": "Pulmonary arterial hypertension",
		    "weight": 0.1
		  },
		  {
		    "source": "Cardiac failure congestive",
		    "target": "Respiratory failure",
		    "weight": 0.1
		  },
		  {
		    "source": "Cardiac failure congestive",
		    "target": "Right ventricular failure",
		    "weight": 0.1
		  },
		  {
		    "source": "Cardiac failure congestive",
		    "target": "Severe acute respiratory syndrome",
		    "weight": 0.0769
		  },
		  {
		    "source": "Cardiac failure congestive",
		    "target": "Stress",
		    "weight": 0.0769
		  },
		  {
		    "source": "Cardiac failure congestive",
		    "target": "Tearfulness",
		    "weight": 0.0769
		  },
		  {
		    "source": "Cardiac failure congestive",
		    "target": "Viral infection",
		    "weight": 0.0769
		  },
		  {
		    "source": "Cardiac failure congestive",
		    "target": "Vomiting",
		    "weight": 0.0769
		  },
		  {
		    "source": "Cardiomegaly",
		    "target": "Chest pain",
		    "weight": 0.2
		  },
		  {
		    "source": "Cardiomegaly",
		    "target": "Drug interaction",
		    "weight": 0.2
		  },
		  {
		    "source": "Cardiomegaly",
		    "target": "Hypertension",
		    "weight": 0.2
		  },
		  {
		    "source": "Cardiomegaly",
		    "target": "Pain in extremity",
		    "weight": 0.2
		  },
		  {
		    "source": "Cardiomyopathy",
		    "target": "Costochondritis",
		    "weight": 0.0769
		  },
		  {
		    "source": "Cardiomyopathy",
		    "target": "Gastrooesophageal reflux disease",
		    "weight": 0.0769
		  },
		  {
		    "source": "Cardiomyopathy",
		    "target": "Grief reaction",
		    "weight": 0.0769
		  },
		  {
		    "source": "Cardiomyopathy",
		    "target": "Nausea",
		    "weight": 0.0769
		  },
		  {
		    "source": "Cardiomyopathy",
		    "target": "Oedema peripheral",
		    "weight": 0.0769
		  },
		  {
		    "source": "Cardiomyopathy",
		    "target": "Pleural effusion",
		    "weight": 0.0769
		  },
		  {
		    "source": "Cardiomyopathy",
		    "target": "Severe acute respiratory syndrome",
		    "weight": 0.0769
		  },
		  {
		    "source": "Cardiomyopathy",
		    "target": "Stress",
		    "weight": 0.0769
		  },
		  {
		    "source": "Cardiomyopathy",
		    "target": "Tearfulness",
		    "weight": 0.0769
		  },
		  {
		    "source": "Cardiomyopathy",
		    "target": "Viral infection",
		    "weight": 0.0769
		  },
		  {
		    "source": "Cardiomyopathy",
		    "target": "Vomiting",
		    "weight": 0.0769
		  },
		  {
		    "source": "Cardiovascular disorder",
		    "target": "Complex regional pain syndrome",
		    "weight": 0.0714
		  },
		  {
		    "source": "Cardiovascular disorder",
		    "target": "Hypoaesthesia",
		    "weight": 0.0714
		  },
		  {
		    "source": "Cardiovascular disorder",
		    "target": "Intervertebral disc protrusion",
		    "weight": 0.0714
		  },
		  {
		    "source": "Cardiovascular disorder",
		    "target": "Loss of consciousness",
		    "weight": 0.0714
		  },
		  {
		    "source": "Cardiovascular disorder",
		    "target": "Nerve injury",
		    "weight": 0.0714
		  },
		  {
		    "source": "Cardiovascular disorder",
		    "target": "Nonspecific reaction",
		    "weight": 0.0714
		  },
		  {
		    "source": "Cardiovascular disorder",
		    "target": "Pain",
		    "weight": 0.0714
		  },
		  {
		    "source": "Cardiovascular disorder",
		    "target": "Paraesthesia",
		    "weight": 0.0714
		  },
		  {
		    "source": "Cardiovascular disorder",
		    "target": "Product use issue",
		    "weight": 0.0714
		  },
		  {
		    "source": "Cardiovascular disorder",
		    "target": "Radiculitis brachial",
		    "weight": 0.0714
		  },
		  {
		    "source": "Cardiovascular disorder",
		    "target": "Sleep disorder",
		    "weight": 0.0714
		  },
		  {
		    "source": "Cardiovascular disorder",
		    "target": "Therapeutic response unexpected",
		    "weight": 0.0714
		  },
		  {
		    "source": "Cardiovascular disorder",
		    "target": "Thoracic outlet syndrome",
		    "weight": 0.0714
		  },
		  {
		    "source": "Catatonia",
		    "target": "Feeling abnormal",
		    "weight": 0.1667
		  },
		  {
		    "source": "Catatonia",
		    "target": "Impaired work ability",
		    "weight": 0.1667
		  },
		  {
		    "source": "Central nervous system lesion",
		    "target": "Prescribed underdose",
		    "weight": 0.3333
		  },
		  {
		    "source": "Central nervous system lesion",
		    "target": "White blood cell count increased",
		    "weight": 0.3333
		  },
		  {
		    "source": "Cerebrovascular accident",
		    "target": "Embolism arterial",
		    "weight": 0.5
		  },
		  {
		    "source": "Cervical spinal stenosis",
		    "target": "Spinal osteoarthritis",
		    "weight": 0.25
		  },
		  {
		    "source": "Cervical spinal stenosis",
		    "target": "Therapeutic response unexpected",
		    "weight": 0.25
		  },
		  {
		    "source": "Change in sustained attention",
		    "target": "Disturbance in attention",
		    "weight": 0.1667
		  },
		  {
		    "source": "Change in sustained attention",
		    "target": "Drug effect decreased",
		    "weight": 0.1667
		  },
		  {
		    "source": "Change in sustained attention",
		    "target": "Product quality issue",
		    "weight": 0.1667
		  },
		  {
		    "source": "Change in sustained attention",
		    "target": "Psychomotor hyperactivity",
		    "weight": 0.1667
		  },
		  {
		    "source": "Change in sustained attention",
		    "target": "Restlessness",
		    "weight": 0.1667
		  },
		  {
		    "source": "Chest discomfort",
		    "target": "Drug interaction",
		    "weight": 0.3333
		  },
		  {
		    "source": "Chest discomfort",
		    "target": "Feeling jittery",
		    "weight": 0.5
		  },
		  {
		    "source": "Chest pain",
		    "target": "Crying",
		    "weight": 0.3333
		  },
		  {
		    "source": "Chest pain",
		    "target": "Drug interaction",
		    "weight": 0.2
		  },
		  {
		    "source": "Chest pain",
		    "target": "Gastrooesophageal reflux disease",
		    "weight": 0.2
		  },
		  {
		    "source": "Chest pain",
		    "target": "Headache",
		    "weight": 0.3333
		  },
		  {
		    "source": "Chest pain",
		    "target": "Heart rate irregular",
		    "weight": 0.2
		  },
		  {
		    "source": "Chest pain",
		    "target": "Hypertension",
		    "weight": 0.2
		  },
		  {
		    "source": "Chest pain",
		    "target": "Mania",
		    "weight": 0.3333
		  },
		  {
		    "source": "Chest pain",
		    "target": "Pain in extremity",
		    "weight": 0.45
		  },
		  {
		    "source": "Chest pain",
		    "target": "Palpitations",
		    "weight": 0.25
		  },
		  {
		    "source": "Chest pain",
		    "target": "Paraesthesia",
		    "weight": 0.3333
		  },
		  {
		    "source": "Chills",
		    "target": "Drug ineffective",
		    "weight": 0.0769
		  },
		  {
		    "source": "Chills",
		    "target": "Drug withdrawal syndrome",
		    "weight": 0.3333
		  },
		  {
		    "source": "Chills",
		    "target": "Fatigue",
		    "weight": 0.0769
		  },
		  {
		    "source": "Chills",
		    "target": "Hot flush",
		    "weight": 0.3333
		  },
		  {
		    "source": "Chills",
		    "target": "Increased appetite",
		    "weight": 0.0769
		  },
		  {
		    "source": "Chills",
		    "target": "Libido decreased",
		    "weight": 0.0769
		  },
		  {
		    "source": "Chills",
		    "target": "Muscle spasms",
		    "weight": 0.0769
		  },
		  {
		    "source": "Chills",
		    "target": "Nausea",
		    "weight": 0.0769
		  },
		  {
		    "source": "Chills",
		    "target": "Nervousness",
		    "weight": 0.25
		  },
		  {
		    "source": "Chills",
		    "target": "Pain in jaw",
		    "weight": 0.0769
		  },
		  {
		    "source": "Chills",
		    "target": "Palpitations",
		    "weight": 0.0769
		  },
		  {
		    "source": "Chills",
		    "target": "Pruritus",
		    "weight": 0.25
		  },
		  {
		    "source": "Chills",
		    "target": "Pyrexia",
		    "weight": 0.0769
		  },
		  {
		    "source": "Chills",
		    "target": "Swelling face",
		    "weight": 0.25
		  },
		  {
		    "source": "Chills",
		    "target": "Vomiting",
		    "weight": 0.0769
		  },
		  {
		    "source": "Complex regional pain syndrome",
		    "target": "Hypoaesthesia",
		    "weight": 0.0714
		  },
		  {
		    "source": "Complex regional pain syndrome",
		    "target": "Intervertebral disc protrusion",
		    "weight": 0.0714
		  },
		  {
		    "source": "Complex regional pain syndrome",
		    "target": "Loss of consciousness",
		    "weight": 0.0714
		  },
		  {
		    "source": "Complex regional pain syndrome",
		    "target": "Nerve injury",
		    "weight": 0.0714
		  },
		  {
		    "source": "Complex regional pain syndrome",
		    "target": "Nonspecific reaction",
		    "weight": 0.0714
		  },
		  {
		    "source": "Complex regional pain syndrome",
		    "target": "Pain",
		    "weight": 0.0714
		  },
		  {
		    "source": "Complex regional pain syndrome",
		    "target": "Paraesthesia",
		    "weight": 0.0714
		  },
		  {
		    "source": "Complex regional pain syndrome",
		    "target": "Product use issue",
		    "weight": 0.0714
		  },
		  {
		    "source": "Complex regional pain syndrome",
		    "target": "Radiculitis brachial",
		    "weight": 0.0714
		  },
		  {
		    "source": "Complex regional pain syndrome",
		    "target": "Sleep disorder",
		    "weight": 0.0714
		  },
		  {
		    "source": "Complex regional pain syndrome",
		    "target": "Therapeutic response unexpected",
		    "weight": 0.0714
		  },
		  {
		    "source": "Complex regional pain syndrome",
		    "target": "Thoracic outlet syndrome",
		    "weight": 0.0714
		  },
		  {
		    "source": "Concussion",
		    "target": "Headache",
		    "weight": 0.2
		  },
		  {
		    "source": "Concussion",
		    "target": "Loss of consciousness",
		    "weight": 0.2
		  },
		  {
		    "source": "Concussion",
		    "target": "Post-traumatic neck syndrome",
		    "weight": 0.2
		  },
		  {
		    "source": "Concussion",
		    "target": "Road traffic accident",
		    "weight": 0.2
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Decreased appetite",
		    "weight": 0.0476
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Depression",
		    "weight": 0.4643
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Dermatitis",
		    "weight": 0.0476
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Diverticulitis",
		    "weight": 0.0476
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Drug dose omission",
		    "weight": 0.2
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Drug ineffective",
		    "weight": 0.4976
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Dyskinesia",
		    "weight": 0.0714
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Eye movement disorder",
		    "weight": 0.0714
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Feeding disorder",
		    "weight": 0.0476
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Fibromyalgia",
		    "weight": 0.2
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Formication",
		    "weight": 0.0833
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Gastritis",
		    "weight": 0.0476
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Haemophobia",
		    "weight": 0.5
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Headache",
		    "weight": 0.25
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Hostility",
		    "weight": 0.0833
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "House dust allergy",
		    "weight": 0.3333
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Hyperhidrosis",
		    "weight": 0.5
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Hyperphagia",
		    "weight": 0.0714
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Hypersensitivity",
		    "weight": 0.3333
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Increased appetite",
		    "weight": 0.2976
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Irritability",
		    "weight": 0.3333
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Laziness",
		    "weight": 0.0714
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Malabsorption",
		    "weight": 0.0833
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Mania",
		    "weight": 0.2
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Migraine",
		    "weight": 0.2
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Mood swings",
		    "weight": 0.0833
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Muscle injury",
		    "weight": 0.2
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Muscle spasms",
		    "weight": 0.2
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Musculoskeletal pain",
		    "weight": 0.2
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Musculoskeletal stiffness",
		    "weight": 0.0714
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Myalgia",
		    "weight": 0.2
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Nausea",
		    "weight": 0.25
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Osteoarthritis",
		    "weight": 0.0476
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Pain",
		    "weight": 0.0476
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Pain in extremity",
		    "weight": 0.25
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Panic attack",
		    "weight": 0.0476
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Personality change",
		    "weight": 0.25
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Poor quality sleep",
		    "weight": 0.0476
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Product quality issue",
		    "weight": 0.3429
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Psychomotor hyperactivity",
		    "weight": 0.2
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Psychotic disorder",
		    "weight": 0.0476
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Scar",
		    "weight": 0.0476
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Sinusitis",
		    "weight": 0.2
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Sjogren's syndrome",
		    "weight": 0.2
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Sleep disorder",
		    "weight": 0.1429
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Social avoidant behaviour",
		    "weight": 0.0714
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Therapy cessation",
		    "weight": 0.2
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Thirst",
		    "weight": 0.0714
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Tobacco user",
		    "weight": 0.5
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Tooth infection",
		    "weight": 0.0476
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Tooth loss",
		    "weight": 0.0476
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Toothache",
		    "weight": 0.0476
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Victim of abuse",
		    "weight": 0.0714
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Victim of sexual abuse",
		    "weight": 0.0714
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Vitamin D abnormal",
		    "weight": 0.0833
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Vitreous floaters",
		    "weight": 0.0833
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Weight increased",
		    "weight": 0.0714
		  },
		  {
		    "source": "Condition aggravated",
		    "target": "Wrist fracture",
		    "weight": 0.1429
		  },
		  {
		    "source": "Confusional state",
		    "target": "Crying",
		    "weight": 0.1429
		  },
		  {
		    "source": "Confusional state",
		    "target": "Disorientation",
		    "weight": 0.2
		  },
		  {
		    "source": "Confusional state",
		    "target": "Disturbance in attention",
		    "weight": 0.1429
		  },
		  {
		    "source": "Confusional state",
		    "target": "Disturbance in social behaviour",
		    "weight": 0.0769
		  },
		  {
		    "source": "Confusional state",
		    "target": "Dizziness",
		    "weight": 0.0769
		  },
		  {
		    "source": "Confusional state",
		    "target": "Emotional disorder",
		    "weight": 0.1429
		  },
		  {
		    "source": "Confusional state",
		    "target": "Fear",
		    "weight": 0.2
		  },
		  {
		    "source": "Confusional state",
		    "target": "Feeling abnormal",
		    "weight": 0.0769
		  },
		  {
		    "source": "Confusional state",
		    "target": "Hypothyroidism",
		    "weight": 0.0769
		  },
		  {
		    "source": "Confusional state",
		    "target": "Incorrect dose administered",
		    "weight": 0.0769
		  },
		  {
		    "source": "Confusional state",
		    "target": "Malaise",
		    "weight": 0.0769
		  },
		  {
		    "source": "Confusional state",
		    "target": "Memory impairment",
		    "weight": 0.2
		  },
		  {
		    "source": "Confusional state",
		    "target": "Mental impairment",
		    "weight": 0.0769
		  },
		  {
		    "source": "Confusional state",
		    "target": "Nausea",
		    "weight": 0.0769
		  },
		  {
		    "source": "Confusional state",
		    "target": "Performance status decreased",
		    "weight": 0.0769
		  },
		  {
		    "source": "Confusional state",
		    "target": "Product quality issue",
		    "weight": 0.2769
		  },
		  {
		    "source": "Confusional state",
		    "target": "Self injurious behaviour",
		    "weight": 0.1429
		  },
		  {
		    "source": "Confusional state",
		    "target": "Somnolence",
		    "weight": 0.0769
		  },
		  {
		    "source": "Confusional state",
		    "target": "Suicidal ideation",
		    "weight": 0.1429
		  },
		  {
		    "source": "Confusional state",
		    "target": "Wrong technique in product usage process",
		    "weight": 0.0769
		  },
		  {
		    "source": "Constipation",
		    "target": "Decreased appetite",
		    "weight": 0.0667
		  },
		  {
		    "source": "Constipation",
		    "target": "Disturbance in attention",
		    "weight": 0.0667
		  },
		  {
		    "source": "Constipation",
		    "target": "Drug administered to patient of inappropriate age",
		    "weight": 0.0667
		  },
		  {
		    "source": "Constipation",
		    "target": "Drug effect decreased",
		    "weight": 0.0667
		  },
		  {
		    "source": "Constipation",
		    "target": "Drug ineffective",
		    "weight": 0.0667
		  },
		  {
		    "source": "Constipation",
		    "target": "Eosinophilic oesophagitis",
		    "weight": 0.0667
		  },
		  {
		    "source": "Constipation",
		    "target": "Epistaxis",
		    "weight": 0.0526
		  },
		  {
		    "source": "Constipation",
		    "target": "Fatigue",
		    "weight": 0.0526
		  },
		  {
		    "source": "Constipation",
		    "target": "Feeling abnormal",
		    "weight": 0.0667
		  },
		  {
		    "source": "Constipation",
		    "target": "Gait disturbance",
		    "weight": 0.0526
		  },
		  {
		    "source": "Constipation",
		    "target": "Growth accelerated",
		    "weight": 0.0667
		  },
		  {
		    "source": "Constipation",
		    "target": "Haemorrhoids",
		    "weight": 0.0667
		  },
		  {
		    "source": "Constipation",
		    "target": "Headache",
		    "weight": 0.25
		  },
		  {
		    "source": "Constipation",
		    "target": "Heart rate decreased",
		    "weight": 0.0526
		  },
		  {
		    "source": "Constipation",
		    "target": "Hepatic enzyme increased",
		    "weight": 0.0667
		  },
		  {
		    "source": "Constipation",
		    "target": "Hypotension",
		    "weight": 0.0526
		  },
		  {
		    "source": "Constipation",
		    "target": "Impaired healing",
		    "weight": 0.0526
		  },
		  {
		    "source": "Constipation",
		    "target": "Insomnia",
		    "weight": 0.0526
		  },
		  {
		    "source": "Constipation",
		    "target": "Invasive ductal breast carcinoma",
		    "weight": 0.0526
		  },
		  {
		    "source": "Constipation",
		    "target": "Lactose intolerance",
		    "weight": 0.0667
		  },
		  {
		    "source": "Constipation",
		    "target": "Logorrhoea",
		    "weight": 0.0667
		  },
		  {
		    "source": "Constipation",
		    "target": "Pneumonia",
		    "weight": 0.0526
		  },
		  {
		    "source": "Constipation",
		    "target": "Product quality issue",
		    "weight": 0.25
		  },
		  {
		    "source": "Constipation",
		    "target": "Rash pruritic",
		    "weight": 0.0526
		  },
		  {
		    "source": "Constipation",
		    "target": "Rash pustular",
		    "weight": 0.0526
		  },
		  {
		    "source": "Constipation",
		    "target": "Skin mass",
		    "weight": 0.0526
		  },
		  {
		    "source": "Constipation",
		    "target": "Therapy cessation",
		    "weight": 0.0526
		  },
		  {
		    "source": "Constipation",
		    "target": "Urinary hesitation",
		    "weight": 0.0526
		  },
		  {
		    "source": "Constipation",
		    "target": "Urinary retention",
		    "weight": 0.0526
		  },
		  {
		    "source": "Constipation",
		    "target": "Vertigo",
		    "weight": 0.0526
		  },
		  {
		    "source": "Constipation",
		    "target": "Vitamin D deficiency",
		    "weight": 0.25
		  },
		  {
		    "source": "Constipation",
		    "target": "Weight decreased",
		    "weight": 0.0667
		  },
		  {
		    "source": "Contusion",
		    "target": "Device breakage",
		    "weight": 0.1429
		  },
		  {
		    "source": "Contusion",
		    "target": "Fall",
		    "weight": 0.3333
		  },
		  {
		    "source": "Contusion",
		    "target": "Irritability",
		    "weight": 0.1429
		  },
		  {
		    "source": "Contusion",
		    "target": "Malaise",
		    "weight": 0.1429
		  },
		  {
		    "source": "Contusion",
		    "target": "Personality change",
		    "weight": 0.1429
		  },
		  {
		    "source": "Contusion",
		    "target": "Weight decreased",
		    "weight": 0.1429
		  },
		  {
		    "source": "Costochondritis",
		    "target": "Gastrooesophageal reflux disease",
		    "weight": 0.0769
		  },
		  {
		    "source": "Costochondritis",
		    "target": "Grief reaction",
		    "weight": 0.0769
		  },
		  {
		    "source": "Costochondritis",
		    "target": "Nausea",
		    "weight": 0.0769
		  },
		  {
		    "source": "Costochondritis",
		    "target": "Oedema peripheral",
		    "weight": 0.0769
		  },
		  {
		    "source": "Costochondritis",
		    "target": "Pleural effusion",
		    "weight": 0.0769
		  },
		  {
		    "source": "Costochondritis",
		    "target": "Severe acute respiratory syndrome",
		    "weight": 0.0769
		  },
		  {
		    "source": "Costochondritis",
		    "target": "Stress",
		    "weight": 0.0769
		  },
		  {
		    "source": "Costochondritis",
		    "target": "Tearfulness",
		    "weight": 0.0769
		  },
		  {
		    "source": "Costochondritis",
		    "target": "Viral infection",
		    "weight": 0.0769
		  },
		  {
		    "source": "Costochondritis",
		    "target": "Vomiting",
		    "weight": 0.0769
		  },
		  {
		    "source": "Cough",
		    "target": "Dysphagia",
		    "weight": 0.5
		  },
		  {
		    "source": "Cough",
		    "target": "Fatigue",
		    "weight": 0.0769
		  },
		  {
		    "source": "Cough",
		    "target": "Feeling abnormal",
		    "weight": 0.0769
		  },
		  {
		    "source": "Cough",
		    "target": "Growing pains",
		    "weight": 0.0769
		  },
		  {
		    "source": "Cough",
		    "target": "Hypersensitivity",
		    "weight": 0.0769
		  },
		  {
		    "source": "Cough",
		    "target": "Insomnia",
		    "weight": 0.0769
		  },
		  {
		    "source": "Cough",
		    "target": "Movement disorder",
		    "weight": 0.0769
		  },
		  {
		    "source": "Cough",
		    "target": "Nasopharyngitis",
		    "weight": 0.0769
		  },
		  {
		    "source": "Cough",
		    "target": "Off label use",
		    "weight": 0.0769
		  },
		  {
		    "source": "Cough",
		    "target": "Pneumonia",
		    "weight": 0.0769
		  },
		  {
		    "source": "Cough",
		    "target": "Restlessness",
		    "weight": 0.0769
		  },
		  {
		    "source": "Cough",
		    "target": "Thirst",
		    "weight": 0.0769
		  },
		  {
		    "source": "Crohn's disease",
		    "target": "Drug effect decreased",
		    "weight": 0.1667
		  },
		  {
		    "source": "Crohn's disease",
		    "target": "Gastrointestinal stenosis",
		    "weight": 0.1667
		  },
		  {
		    "source": "Crohn's disease",
		    "target": "Infusion related reaction",
		    "weight": 0.1667
		  },
		  {
		    "source": "Crohn's disease",
		    "target": "Injection site pain",
		    "weight": 0.1667
		  },
		  {
		    "source": "Crohn's disease",
		    "target": "Intestinal obstruction",
		    "weight": 0.3333
		  },
		  {
		    "source": "Crohn's disease",
		    "target": "Intestinal polyp",
		    "weight": 0.1667
		  },
		  {
		    "source": "Crohn's disease",
		    "target": "Large intestinal stenosis",
		    "weight": 0.1667
		  },
		  {
		    "source": "Crohn's disease",
		    "target": "Nasopharyngitis",
		    "weight": 0.1667
		  },
		  {
		    "source": "Crohn's disease",
		    "target": "Weight increased",
		    "weight": 0.1667
		  },
		  {
		    "source": "Crying",
		    "target": "Decreased appetite",
		    "weight": 0.0556
		  },
		  {
		    "source": "Crying",
		    "target": "Depression",
		    "weight": 0.2769
		  },
		  {
		    "source": "Crying",
		    "target": "Diarrhoea",
		    "weight": 0.0769
		  },
		  {
		    "source": "Crying",
		    "target": "Disability",
		    "weight": 0.125
		  },
		  {
		    "source": "Crying",
		    "target": "Disturbance in attention",
		    "weight": 0.2198
		  },
		  {
		    "source": "Crying",
		    "target": "Disturbance in social behaviour",
		    "weight": 0.1
		  },
		  {
		    "source": "Crying",
		    "target": "Dizziness",
		    "weight": 0.0556
		  },
		  {
		    "source": "Crying",
		    "target": "Drug dose omission",
		    "weight": 0.1
		  },
		  {
		    "source": "Crying",
		    "target": "Drug effect decreased",
		    "weight": 0.3158
		  },
		  {
		    "source": "Crying",
		    "target": "Drug ineffective",
		    "weight": 0.4583
		  },
		  {
		    "source": "Crying",
		    "target": "Drug interaction",
		    "weight": 0.0769
		  },
		  {
		    "source": "Crying",
		    "target": "Drug withdrawal convulsions",
		    "weight": 0.0833
		  },
		  {
		    "source": "Crying",
		    "target": "Emotional disorder",
		    "weight": 0.1429
		  },
		  {
		    "source": "Crying",
		    "target": "Epistaxis",
		    "weight": 0.0556
		  },
		  {
		    "source": "Crying",
		    "target": "Fatigue",
		    "weight": 0.0769
		  },
		  {
		    "source": "Crying",
		    "target": "Fear",
		    "weight": 0.0769
		  },
		  {
		    "source": "Crying",
		    "target": "Flat affect",
		    "weight": 0.0556
		  },
		  {
		    "source": "Crying",
		    "target": "Formication",
		    "weight": 0.1
		  },
		  {
		    "source": "Crying",
		    "target": "Haemorrhagic diathesis",
		    "weight": 0.25
		  },
		  {
		    "source": "Crying",
		    "target": "Headache",
		    "weight": 0.1806
		  },
		  {
		    "source": "Crying",
		    "target": "Hostility",
		    "weight": 0.0833
		  },
		  {
		    "source": "Crying",
		    "target": "Hot flush",
		    "weight": 0.2
		  },
		  {
		    "source": "Crying",
		    "target": "Incorrect dose administered",
		    "weight": 0.0769
		  },
		  {
		    "source": "Crying",
		    "target": "Increased appetite",
		    "weight": 0.0833
		  },
		  {
		    "source": "Crying",
		    "target": "Insomnia",
		    "weight": 0.0556
		  },
		  {
		    "source": "Crying",
		    "target": "Irritability",
		    "weight": 0.0556
		  },
		  {
		    "source": "Crying",
		    "target": "Laziness",
		    "weight": 0.0769
		  },
		  {
		    "source": "Crying",
		    "target": "Malaise",
		    "weight": 0.0769
		  },
		  {
		    "source": "Crying",
		    "target": "Mania",
		    "weight": 0.4167
		  },
		  {
		    "source": "Crying",
		    "target": "Muscle twitching",
		    "weight": 0.1
		  },
		  {
		    "source": "Crying",
		    "target": "Myalgia",
		    "weight": 0.1
		  },
		  {
		    "source": "Crying",
		    "target": "Nausea",
		    "weight": 0.0556
		  },
		  {
		    "source": "Crying",
		    "target": "Obsessive thoughts",
		    "weight": 0.0556
		  },
		  {
		    "source": "Crying",
		    "target": "Optic nerve neoplasm",
		    "weight": 0.0833
		  },
		  {
		    "source": "Crying",
		    "target": "Pain",
		    "weight": 0.25
		  },
		  {
		    "source": "Crying",
		    "target": "Performance status decreased",
		    "weight": 0.125
		  },
		  {
		    "source": "Crying",
		    "target": "Prescribed overdose",
		    "weight": 0.125
		  },
		  {
		    "source": "Crying",
		    "target": "Psychomotor hyperactivity",
		    "weight": 0.0769
		  },
		  {
		    "source": "Crying",
		    "target": "Screaming",
		    "weight": 0.1
		  },
		  {
		    "source": "Crying",
		    "target": "Self injurious behaviour",
		    "weight": 0.1429
		  },
		  {
		    "source": "Crying",
		    "target": "Social avoidant behaviour",
		    "weight": 0.0556
		  },
		  {
		    "source": "Crying",
		    "target": "Somnolence",
		    "weight": 0.1603
		  },
		  {
		    "source": "Crying",
		    "target": "Suicidal ideation",
		    "weight": 0.1429
		  },
		  {
		    "source": "Crying",
		    "target": "Therapy cessation",
		    "weight": 0.125
		  },
		  {
		    "source": "Crying",
		    "target": "Tic",
		    "weight": 0.0556
		  },
		  {
		    "source": "Crying",
		    "target": "Tremor",
		    "weight": 0.1
		  },
		  {
		    "source": "Crying",
		    "target": "Vomiting",
		    "weight": 0.0556
		  },
		  {
		    "source": "Crying",
		    "target": "Wrong technique in product usage process",
		    "weight": 0.1
		  },
		  {
		    "source": "Cystic fibrosis related diabetes",
		    "target": "Depressed mood",
		    "weight": 0.1
		  },
		  {
		    "source": "Cystic fibrosis related diabetes",
		    "target": "Dyspepsia",
		    "weight": 0.1
		  },
		  {
		    "source": "Cystic fibrosis related diabetes",
		    "target": "Mycobacterium test positive",
		    "weight": 0.1
		  },
		  {
		    "source": "Cystic fibrosis related diabetes",
		    "target": "Obstructive airways disorder",
		    "weight": 0.1
		  },
		  {
		    "source": "Cystic fibrosis related diabetes",
		    "target": "Pseudomonas infection",
		    "weight": 0.1
		  },
		  {
		    "source": "Cystic fibrosis related diabetes",
		    "target": "Sinus disorder",
		    "weight": 0.1
		  },
		  {
		    "source": "Cystic fibrosis related diabetes",
		    "target": "Weight increased",
		    "weight": 0.1
		  },
		  {
		    "source": "Cytogenetic abnormality",
		    "target": "Drug dose omission",
		    "weight": 0.125
		  },
		  {
		    "source": "Cytogenetic abnormality",
		    "target": "Drug ineffective",
		    "weight": 0.125
		  },
		  {
		    "source": "Cytogenetic abnormality",
		    "target": "Drug tolerance",
		    "weight": 0.125
		  },
		  {
		    "source": "Cytogenetic abnormality",
		    "target": "Fatigue",
		    "weight": 0.125
		  },
		  {
		    "source": "Cytogenetic abnormality",
		    "target": "Inappropriate schedule of drug administration",
		    "weight": 0.125
		  },
		  {
		    "source": "Cytogenetic abnormality",
		    "target": "Prescribed overdose",
		    "weight": 0.125
		  },
		  {
		    "source": "Cytogenetic abnormality",
		    "target": "Product use issue",
		    "weight": 0.125
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Depression",
		    "weight": 0.2476
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Dermatitis",
		    "weight": 0.0476
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Discomfort",
		    "weight": 0.0588
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Disturbance in attention",
		    "weight": 0.1255
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Disturbance in social behaviour",
		    "weight": 0.2
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Diverticulitis",
		    "weight": 0.0476
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Dizziness",
		    "weight": 0.0556
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Drug administered to patient of inappropriate age",
		    "weight": 0.0667
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Drug effect decreased",
		    "weight": 0.3222
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Drug ineffective",
		    "weight": 0.5422
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Dry mouth",
		    "weight": 0.5333
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Emotional disorder",
		    "weight": 0.25
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Eosinophilic oesophagitis",
		    "weight": 0.0667
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Epistaxis",
		    "weight": 0.0556
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Fatigue",
		    "weight": 0.0588
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Feeding disorder",
		    "weight": 0.0476
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Feeling abnormal",
		    "weight": 0.1255
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Feeling of despair",
		    "weight": 0.2
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Flat affect",
		    "weight": 0.0556
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Gastritis",
		    "weight": 0.0476
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Gastroenteritis viral",
		    "weight": 0.2
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Growth accelerated",
		    "weight": 0.0667
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Haemorrhoids",
		    "weight": 0.0667
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Headache",
		    "weight": 0.4222
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Heart rate increased",
		    "weight": 0.2
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Hepatic enzyme increased",
		    "weight": 0.0667
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Hypersomnia",
		    "weight": 0.0588
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Impaired work ability",
		    "weight": 0.0588
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Inappropriate schedule of drug administration",
		    "weight": 0.2
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Incorrect dose administered",
		    "weight": 0.0588
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Increased appetite",
		    "weight": 0.2143
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Insomnia",
		    "weight": 0.6722
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Irritability",
		    "weight": 0.3889
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Lactose intolerance",
		    "weight": 0.0667
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Lethargy",
		    "weight": 0.1667
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Logorrhoea",
		    "weight": 0.0667
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Mental impairment",
		    "weight": 0.0588
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Nausea",
		    "weight": 0.2222
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Nightmare",
		    "weight": 0.0588
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Obsessive thoughts",
		    "weight": 0.0556
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Osteoarthritis",
		    "weight": 0.0476
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Pain",
		    "weight": 0.0476
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Panic attack",
		    "weight": 0.0476
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Poor quality sleep",
		    "weight": 0.0476
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Psychotic disorder",
		    "weight": 0.0476
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Rapid eye movements sleep abnormal",
		    "weight": 0.0588
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Rebound effect",
		    "weight": 0.1667
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Road traffic accident",
		    "weight": 0.0588
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Scar",
		    "weight": 0.0476
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Seizure",
		    "weight": 0.2
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Social avoidant behaviour",
		    "weight": 0.0556
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Somnolence",
		    "weight": 0.3667
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Tic",
		    "weight": 0.0556
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Tooth infection",
		    "weight": 0.0476
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Tooth loss",
		    "weight": 0.0476
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Toothache",
		    "weight": 0.0476
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Underweight",
		    "weight": 0.0588
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Vomiting",
		    "weight": 0.0556
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Weight decreased",
		    "weight": 0.2333
		  },
		  {
		    "source": "Decreased appetite",
		    "target": "Weight increased",
		    "weight": 0.0588
		  },
		  {
		    "source": "Decreased interest",
		    "target": "Depression",
		    "weight": 0.1
		  },
		  {
		    "source": "Decreased interest",
		    "target": "Drug effect decreased",
		    "weight": 0.25
		  },
		  {
		    "source": "Decreased interest",
		    "target": "Insomnia",
		    "weight": 0.1
		  },
		  {
		    "source": "Decreased interest",
		    "target": "Libido decreased",
		    "weight": 0.25
		  },
		  {
		    "source": "Decreased interest",
		    "target": "No therapeutic response",
		    "weight": 0.1
		  },
		  {
		    "source": "Decreased interest",
		    "target": "Pain in extremity",
		    "weight": 0.1
		  },
		  {
		    "source": "Decreased interest",
		    "target": "Paraesthesia",
		    "weight": 0.1
		  },
		  {
		    "source": "Decreased interest",
		    "target": "Product substitution issue",
		    "weight": 0.1
		  },
		  {
		    "source": "Decreased interest",
		    "target": "Vertigo",
		    "weight": 0.1
		  },
		  {
		    "source": "Dehydration",
		    "target": "Joint stiffness",
		    "weight": 0.2
		  },
		  {
		    "source": "Dehydration",
		    "target": "Meniscus injury",
		    "weight": 0.2
		  },
		  {
		    "source": "Delusion",
		    "target": "Stress",
		    "weight": 0.3333
		  },
		  {
		    "source": "Dental care",
		    "target": "Myalgia",
		    "weight": 0.5
		  },
		  {
		    "source": "Depressed level of consciousness",
		    "target": "Disturbance in attention",
		    "weight": 0.25
		  },
		  {
		    "source": "Depressed level of consciousness",
		    "target": "Performance status decreased",
		    "weight": 0.25
		  },
		  {
		    "source": "Depressed level of consciousness",
		    "target": "Product quality issue",
		    "weight": 0.25
		  },
		  {
		    "source": "Depressed mood",
		    "target": "Dyspepsia",
		    "weight": 0.1
		  },
		  {
		    "source": "Depressed mood",
		    "target": "Fatigue",
		    "weight": 0.2
		  },
		  {
		    "source": "Depressed mood",
		    "target": "Feeling of relaxation",
		    "weight": 0.2
		  },
		  {
		    "source": "Depressed mood",
		    "target": "Mycobacterium test positive",
		    "weight": 0.1
		  },
		  {
		    "source": "Depressed mood",
		    "target": "Obstructive airways disorder",
		    "weight": 0.1
		  },
		  {
		    "source": "Depressed mood",
		    "target": "Pseudomonas infection",
		    "weight": 0.1
		  },
		  {
		    "source": "Depressed mood",
		    "target": "Sinus disorder",
		    "weight": 0.1
		  },
		  {
		    "source": "Depressed mood",
		    "target": "Weight increased",
		    "weight": 0.1
		  },
		  {
		    "source": "Depression",
		    "target": "Dermatitis",
		    "weight": 0.0476
		  },
		  {
		    "source": "Depression",
		    "target": "Diarrhoea",
		    "weight": 0.0769
		  },
		  {
		    "source": "Depression",
		    "target": "Disability",
		    "weight": 0.2
		  },
		  {
		    "source": "Depression",
		    "target": "Disturbance in attention",
		    "weight": 0.3198
		  },
		  {
		    "source": "Depression",
		    "target": "Diverticulitis",
		    "weight": 0.0476
		  },
		  {
		    "source": "Depression",
		    "target": "Drug abuse",
		    "weight": 0.2
		  },
		  {
		    "source": "Depression",
		    "target": "Drug dose omission",
		    "weight": 0.1883
		  },
		  {
		    "source": "Depression",
		    "target": "Drug effect decreased",
		    "weight": 0.1224
		  },
		  {
		    "source": "Depression",
		    "target": "Drug effect increased",
		    "weight": 0.0455
		  },
		  {
		    "source": "Depression",
		    "target": "Drug ineffective",
		    "weight": 0.6288
		  },
		  {
		    "source": "Depression",
		    "target": "Drug interaction",
		    "weight": 0.0769
		  },
		  {
		    "source": "Depression",
		    "target": "Drug withdrawal syndrome",
		    "weight": 0.1667
		  },
		  {
		    "source": "Depression",
		    "target": "Eye irritation",
		    "weight": 0.0455
		  },
		  {
		    "source": "Depression",
		    "target": "Fatigue",
		    "weight": 0.5557
		  },
		  {
		    "source": "Depression",
		    "target": "Fear",
		    "weight": 0.1224
		  },
		  {
		    "source": "Depression",
		    "target": "Feeding disorder",
		    "weight": 0.0476
		  },
		  {
		    "source": "Depression",
		    "target": "Feeling abnormal",
		    "weight": 0.354
		  },
		  {
		    "source": "Depression",
		    "target": "Feeling of despair",
		    "weight": 0.2
		  },
		  {
		    "source": "Depression",
		    "target": "Formication",
		    "weight": 0.0833
		  },
		  {
		    "source": "Depression",
		    "target": "Gastritis",
		    "weight": 0.0476
		  },
		  {
		    "source": "Depression",
		    "target": "Headache",
		    "weight": 0.0455
		  },
		  {
		    "source": "Depression",
		    "target": "Hostility",
		    "weight": 0.0833
		  },
		  {
		    "source": "Depression",
		    "target": "Hot flush",
		    "weight": 0.2
		  },
		  {
		    "source": "Depression",
		    "target": "Hypersensitivity",
		    "weight": 0.3333
		  },
		  {
		    "source": "Depression",
		    "target": "Hypersomnia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Depression",
		    "target": "Incorrect dose administered",
		    "weight": 0.0769
		  },
		  {
		    "source": "Depression",
		    "target": "Increased appetite",
		    "weight": 0.0476
		  },
		  {
		    "source": "Depression",
		    "target": "Injury",
		    "weight": 0.125
		  },
		  {
		    "source": "Depression",
		    "target": "Insomnia",
		    "weight": 0.225
		  },
		  {
		    "source": "Depression",
		    "target": "Intentional self-injury",
		    "weight": 0.2667
		  },
		  {
		    "source": "Depression",
		    "target": "Irritability",
		    "weight": 0.0833
		  },
		  {
		    "source": "Depression",
		    "target": "Laziness",
		    "weight": 0.188
		  },
		  {
		    "source": "Depression",
		    "target": "Logorrhoea",
		    "weight": 0.1429
		  },
		  {
		    "source": "Depression",
		    "target": "Malabsorption",
		    "weight": 0.0833
		  },
		  {
		    "source": "Depression",
		    "target": "Malaise",
		    "weight": 0.1224
		  },
		  {
		    "source": "Depression",
		    "target": "Memory impairment",
		    "weight": 0.2111
		  },
		  {
		    "source": "Depression",
		    "target": "Mental disorder",
		    "weight": 0.225
		  },
		  {
		    "source": "Depression",
		    "target": "Migraine",
		    "weight": 0.0455
		  },
		  {
		    "source": "Depression",
		    "target": "Mood altered",
		    "weight": 0.1
		  },
		  {
		    "source": "Depression",
		    "target": "Mood swings",
		    "weight": 0.0833
		  },
		  {
		    "source": "Depression",
		    "target": "Nasopharyngitis",
		    "weight": 0.0455
		  },
		  {
		    "source": "Depression",
		    "target": "Negative thoughts",
		    "weight": 0.1667
		  },
		  {
		    "source": "Depression",
		    "target": "No therapeutic response",
		    "weight": 0.1
		  },
		  {
		    "source": "Depression",
		    "target": "Obsessive-compulsive disorder",
		    "weight": 0.2
		  },
		  {
		    "source": "Depression",
		    "target": "Off label use",
		    "weight": 0.2
		  },
		  {
		    "source": "Depression",
		    "target": "Osteoarthritis",
		    "weight": 0.0476
		  },
		  {
		    "source": "Depression",
		    "target": "Pain",
		    "weight": 0.1726
		  },
		  {
		    "source": "Depression",
		    "target": "Pain in extremity",
		    "weight": 0.1
		  },
		  {
		    "source": "Depression",
		    "target": "Panic attack",
		    "weight": 0.3587
		  },
		  {
		    "source": "Depression",
		    "target": "Paraesthesia",
		    "weight": 0.2667
		  },
		  {
		    "source": "Depression",
		    "target": "Poor quality sleep",
		    "weight": 0.0476
		  },
		  {
		    "source": "Depression",
		    "target": "Product quality issue",
		    "weight": 0.3333
		  },
		  {
		    "source": "Depression",
		    "target": "Product substitution issue",
		    "weight": 0.2667
		  },
		  {
		    "source": "Depression",
		    "target": "Psychomotor hyperactivity",
		    "weight": 0.0769
		  },
		  {
		    "source": "Depression",
		    "target": "Psychotic disorder",
		    "weight": 0.0476
		  },
		  {
		    "source": "Depression",
		    "target": "Pulmonary embolism",
		    "weight": 0.125
		  },
		  {
		    "source": "Depression",
		    "target": "Restlessness",
		    "weight": 0.25
		  },
		  {
		    "source": "Depression",
		    "target": "Scar",
		    "weight": 0.0476
		  },
		  {
		    "source": "Depression",
		    "target": "Social phobia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Depression",
		    "target": "Somnolence",
		    "weight": 0.0769
		  },
		  {
		    "source": "Depression",
		    "target": "Stress",
		    "weight": 0.3333
		  },
		  {
		    "source": "Depression",
		    "target": "Suicidal ideation",
		    "weight": 0.1667
		  },
		  {
		    "source": "Depression",
		    "target": "Suicide attempt",
		    "weight": 0.1667
		  },
		  {
		    "source": "Depression",
		    "target": "Surgery",
		    "weight": 0.2
		  },
		  {
		    "source": "Depression",
		    "target": "Tachyphrenia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Depression",
		    "target": "Tinnitus",
		    "weight": 0.1667
		  },
		  {
		    "source": "Depression",
		    "target": "Tooth infection",
		    "weight": 0.0476
		  },
		  {
		    "source": "Depression",
		    "target": "Tooth loss",
		    "weight": 0.0476
		  },
		  {
		    "source": "Depression",
		    "target": "Toothache",
		    "weight": 0.0476
		  },
		  {
		    "source": "Depression",
		    "target": "Vertigo",
		    "weight": 0.1
		  },
		  {
		    "source": "Depression",
		    "target": "Vitamin D abnormal",
		    "weight": 0.0833
		  },
		  {
		    "source": "Depression",
		    "target": "Vitreous floaters",
		    "weight": 0.0833
		  },
		  {
		    "source": "Depression",
		    "target": "Weight decreased",
		    "weight": 0.1111
		  },
		  {
		    "source": "Depression",
		    "target": "Weight increased",
		    "weight": 0.0455
		  },
		  {
		    "source": "Derealisation",
		    "target": "Insomnia",
		    "weight": 0.125
		  },
		  {
		    "source": "Derealisation",
		    "target": "Motor dysfunction",
		    "weight": 0.125
		  },
		  {
		    "source": "Derealisation",
		    "target": "Myoclonic epilepsy",
		    "weight": 0.125
		  },
		  {
		    "source": "Derealisation",
		    "target": "Panic disorder",
		    "weight": 0.125
		  },
		  {
		    "source": "Derealisation",
		    "target": "Thinking abnormal",
		    "weight": 0.125
		  },
		  {
		    "source": "Dermatitis",
		    "target": "Diverticulitis",
		    "weight": 0.0476
		  },
		  {
		    "source": "Dermatitis",
		    "target": "Feeding disorder",
		    "weight": 0.0476
		  },
		  {
		    "source": "Dermatitis",
		    "target": "Gastritis",
		    "weight": 0.0476
		  },
		  {
		    "source": "Dermatitis",
		    "target": "Increased appetite",
		    "weight": 0.0476
		  },
		  {
		    "source": "Dermatitis",
		    "target": "Osteoarthritis",
		    "weight": 0.0476
		  },
		  {
		    "source": "Dermatitis",
		    "target": "Pain",
		    "weight": 0.0476
		  },
		  {
		    "source": "Dermatitis",
		    "target": "Panic attack",
		    "weight": 0.0476
		  },
		  {
		    "source": "Dermatitis",
		    "target": "Poor quality sleep",
		    "weight": 0.0476
		  },
		  {
		    "source": "Dermatitis",
		    "target": "Psychotic disorder",
		    "weight": 0.0476
		  },
		  {
		    "source": "Dermatitis",
		    "target": "Scar",
		    "weight": 0.0476
		  },
		  {
		    "source": "Dermatitis",
		    "target": "Tooth infection",
		    "weight": 0.0476
		  },
		  {
		    "source": "Dermatitis",
		    "target": "Tooth loss",
		    "weight": 0.0476
		  },
		  {
		    "source": "Dermatitis",
		    "target": "Toothache",
		    "weight": 0.0476
		  },
		  {
		    "source": "Device breakage",
		    "target": "Irritability",
		    "weight": 0.1429
		  },
		  {
		    "source": "Device breakage",
		    "target": "Malaise",
		    "weight": 0.1429
		  },
		  {
		    "source": "Device breakage",
		    "target": "Personality change",
		    "weight": 0.1429
		  },
		  {
		    "source": "Device breakage",
		    "target": "Weight decreased",
		    "weight": 0.1429
		  },
		  {
		    "source": "Diabetes mellitus",
		    "target": "Pre-existing condition improved",
		    "weight": 0.3333
		  },
		  {
		    "source": "Diabetes mellitus",
		    "target": "Therapeutic response unexpected",
		    "weight": 0.3333
		  },
		  {
		    "source": "Diarrhoea",
		    "target": "Disturbance in attention",
		    "weight": 0.0769
		  },
		  {
		    "source": "Diarrhoea",
		    "target": "Drug effect decreased",
		    "weight": 0.0769
		  },
		  {
		    "source": "Diarrhoea",
		    "target": "Drug interaction",
		    "weight": 0.0769
		  },
		  {
		    "source": "Diarrhoea",
		    "target": "Fatigue",
		    "weight": 0.0769
		  },
		  {
		    "source": "Diarrhoea",
		    "target": "Fear",
		    "weight": 0.0769
		  },
		  {
		    "source": "Diarrhoea",
		    "target": "Gastroenteritis viral",
		    "weight": 0.1
		  },
		  {
		    "source": "Diarrhoea",
		    "target": "Hyperventilation",
		    "weight": 0.2
		  },
		  {
		    "source": "Diarrhoea",
		    "target": "Incorrect dose administered",
		    "weight": 0.0769
		  },
		  {
		    "source": "Diarrhoea",
		    "target": "Influenza like illness",
		    "weight": 0.3333
		  },
		  {
		    "source": "Diarrhoea",
		    "target": "Laziness",
		    "weight": 0.0769
		  },
		  {
		    "source": "Diarrhoea",
		    "target": "Malaise",
		    "weight": 0.1769
		  },
		  {
		    "source": "Diarrhoea",
		    "target": "Paranasal sinus hypersecretion",
		    "weight": 0.1
		  },
		  {
		    "source": "Diarrhoea",
		    "target": "Pharyngitis streptococcal",
		    "weight": 0.1
		  },
		  {
		    "source": "Diarrhoea",
		    "target": "Psychomotor hyperactivity",
		    "weight": 0.0769
		  },
		  {
		    "source": "Diarrhoea",
		    "target": "Pyrexia",
		    "weight": 0.1
		  },
		  {
		    "source": "Diarrhoea",
		    "target": "Rales",
		    "weight": 0.1
		  },
		  {
		    "source": "Diarrhoea",
		    "target": "Retching",
		    "weight": 0.2
		  },
		  {
		    "source": "Diarrhoea",
		    "target": "Somnolence",
		    "weight": 0.0769
		  },
		  {
		    "source": "Diarrhoea",
		    "target": "Trismus",
		    "weight": 0.2
		  },
		  {
		    "source": "Diarrhoea",
		    "target": "Upper respiratory tract infection",
		    "weight": 0.1
		  },
		  {
		    "source": "Diarrhoea",
		    "target": "Vomiting",
		    "weight": 0.3
		  },
		  {
		    "source": "Disability",
		    "target": "Drug ineffective",
		    "weight": 0.125
		  },
		  {
		    "source": "Disability",
		    "target": "Headache",
		    "weight": 0.125
		  },
		  {
		    "source": "Disability",
		    "target": "Obsessive-compulsive disorder",
		    "weight": 0.2
		  },
		  {
		    "source": "Disability",
		    "target": "Off label use",
		    "weight": 0.2
		  },
		  {
		    "source": "Disability",
		    "target": "Performance status decreased",
		    "weight": 0.125
		  },
		  {
		    "source": "Disability",
		    "target": "Prescribed overdose",
		    "weight": 0.125
		  },
		  {
		    "source": "Disability",
		    "target": "Psychomotor hyperactivity",
		    "weight": 0.5
		  },
		  {
		    "source": "Disability",
		    "target": "Therapy cessation",
		    "weight": 0.125
		  },
		  {
		    "source": "Discomfort",
		    "target": "Disturbance in attention",
		    "weight": 0.0588
		  },
		  {
		    "source": "Discomfort",
		    "target": "Drug ineffective",
		    "weight": 0.0588
		  },
		  {
		    "source": "Discomfort",
		    "target": "Fatigue",
		    "weight": 0.0588
		  },
		  {
		    "source": "Discomfort",
		    "target": "Feeling abnormal",
		    "weight": 0.0588
		  },
		  {
		    "source": "Discomfort",
		    "target": "Hypersomnia",
		    "weight": 0.0588
		  },
		  {
		    "source": "Discomfort",
		    "target": "Impaired work ability",
		    "weight": 0.0588
		  },
		  {
		    "source": "Discomfort",
		    "target": "Incorrect dose administered",
		    "weight": 0.0588
		  },
		  {
		    "source": "Discomfort",
		    "target": "Mental impairment",
		    "weight": 0.0588
		  },
		  {
		    "source": "Discomfort",
		    "target": "Nightmare",
		    "weight": 0.0588
		  },
		  {
		    "source": "Discomfort",
		    "target": "Rapid eye movements sleep abnormal",
		    "weight": 0.0588
		  },
		  {
		    "source": "Discomfort",
		    "target": "Road traffic accident",
		    "weight": 0.0588
		  },
		  {
		    "source": "Discomfort",
		    "target": "Underweight",
		    "weight": 0.0588
		  },
		  {
		    "source": "Discomfort",
		    "target": "Weight increased",
		    "weight": 0.0588
		  },
		  {
		    "source": "Disease progression",
		    "target": "Drug dose omission",
		    "weight": 0.2
		  },
		  {
		    "source": "Disease progression",
		    "target": "Dyspnoea",
		    "weight": 0.1
		  },
		  {
		    "source": "Disease progression",
		    "target": "Fluid overload",
		    "weight": 0.1
		  },
		  {
		    "source": "Disease progression",
		    "target": "Oedema",
		    "weight": 0.1
		  },
		  {
		    "source": "Disease progression",
		    "target": "Oxygen saturation decreased",
		    "weight": 0.1
		  },
		  {
		    "source": "Disease progression",
		    "target": "Peripheral swelling",
		    "weight": 0.1
		  },
		  {
		    "source": "Disease progression",
		    "target": "Pulmonary arterial hypertension",
		    "weight": 0.1
		  },
		  {
		    "source": "Disease progression",
		    "target": "Respiratory failure",
		    "weight": 0.1
		  },
		  {
		    "source": "Disease progression",
		    "target": "Right ventricular failure",
		    "weight": 0.1
		  },
		  {
		    "source": "Disorganised speech",
		    "target": "Drug effect decreased",
		    "weight": 0.1667
		  },
		  {
		    "source": "Disorganised speech",
		    "target": "Feeling abnormal",
		    "weight": 0.1667
		  },
		  {
		    "source": "Disorganised speech",
		    "target": "Headache",
		    "weight": 0.1667
		  },
		  {
		    "source": "Disorganised speech",
		    "target": "Memory impairment",
		    "weight": 0.1667
		  },
		  {
		    "source": "Disorganised speech",
		    "target": "Product quality issue",
		    "weight": 0.1667
		  },
		  {
		    "source": "Disorientation",
		    "target": "Fear",
		    "weight": 0.2
		  },
		  {
		    "source": "Disorientation",
		    "target": "Memory impairment",
		    "weight": 0.2
		  },
		  {
		    "source": "Disorientation",
		    "target": "Product quality issue",
		    "weight": 0.2
		  },
		  {
		    "source": "Dissociation",
		    "target": "Drug interaction",
		    "weight": 0.1
		  },
		  {
		    "source": "Dissociation",
		    "target": "Dyskinesia",
		    "weight": 0.1
		  },
		  {
		    "source": "Dissociation",
		    "target": "Hyperhidrosis",
		    "weight": 0.1
		  },
		  {
		    "source": "Dissociation",
		    "target": "Muscle spasms",
		    "weight": 0.1
		  },
		  {
		    "source": "Dissociation",
		    "target": "Mydriasis",
		    "weight": 0.1
		  },
		  {
		    "source": "Dissociation",
		    "target": "Serotonin syndrome",
		    "weight": 0.1
		  },
		  {
		    "source": "Dissociation",
		    "target": "Tachyphrenia",
		    "weight": 0.1
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Disturbance in social behaviour",
		    "weight": 0.7833
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Drug administered to patient of inappropriate age",
		    "weight": 0.0667
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Drug dose omission",
		    "weight": 1.7929
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Drug effect decreased",
		    "weight": 0.9607
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Drug effect increased",
		    "weight": 0.1667
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Drug ineffective",
		    "weight": 0.8831
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Drug interaction",
		    "weight": 0.0769
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Drug tolerance",
		    "weight": 0.0909
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Drug withdrawal syndrome",
		    "weight": 0.3333
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Dysgraphia",
		    "weight": 0.0833
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Educational problem",
		    "weight": 0.5595
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Emotional disorder",
		    "weight": 0.2857
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Eosinophilic oesophagitis",
		    "weight": 0.0667
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Fatigue",
		    "weight": 0.8191
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Fear",
		    "weight": 0.0769
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Feeling abnormal",
		    "weight": 1.4517
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Flat affect",
		    "weight": 0.3333
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Food hoarding",
		    "weight": 0.2
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Frustration",
		    "weight": 0.0833
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Growth accelerated",
		    "weight": 0.0667
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Haemorrhoids",
		    "weight": 0.0667
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Headache",
		    "weight": 0.25
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Hepatic enzyme increased",
		    "weight": 0.0667
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Hunger",
		    "weight": 0.25
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Hypersomnia",
		    "weight": 0.0588
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Hypertension",
		    "weight": 0.3333
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Impaired work ability",
		    "weight": 0.0588
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Impulsive behaviour",
		    "weight": 0.0833
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Inappropriate schedule of drug administration",
		    "weight": 0.0909
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Incorrect dose administered",
		    "weight": 0.4767
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Increased appetite",
		    "weight": 0.2
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Infection",
		    "weight": 0.1429
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Influenza like illness",
		    "weight": 0.3333
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Intentional self-injury",
		    "weight": 0.1
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Job dissatisfaction",
		    "weight": 0.25
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Lactose intolerance",
		    "weight": 0.0667
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Laziness",
		    "weight": 0.0769
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Logorrhoea",
		    "weight": 0.2095
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Loss of consciousness",
		    "weight": 0.3333
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Malaise",
		    "weight": 0.0769
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Memory impairment",
		    "weight": 0.1
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Mental disorder",
		    "weight": 0.1
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Mental impairment",
		    "weight": 0.0588
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Mood altered",
		    "weight": 0.1
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Mood swings",
		    "weight": 0.1667
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Nightmare",
		    "weight": 0.0588
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Performance status decreased",
		    "weight": 0.5
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Prescribed overdose",
		    "weight": 0.25
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Product quality issue",
		    "weight": 1.9838
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Psychomotor hyperactivity",
		    "weight": 0.3269
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Rapid eye movements sleep abnormal",
		    "weight": 0.0588
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Restlessness",
		    "weight": 0.4167
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Road traffic accident",
		    "weight": 0.0588
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Self injurious behaviour",
		    "weight": 0.1429
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Sleep disorder",
		    "weight": 0.2
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Somnolence",
		    "weight": 0.3345
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Stress",
		    "weight": 0.0909
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Suicidal ideation",
		    "weight": 0.3929
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Therapeutic response unexpected",
		    "weight": 0.25
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Tourette's disorder",
		    "weight": 0.0833
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Underweight",
		    "weight": 0.0588
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Urinary incontinence",
		    "weight": 0.1667
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Weight decreased",
		    "weight": 0.0667
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Weight increased",
		    "weight": 0.3422
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Wrong technique in product usage process",
		    "weight": 0.0909
		  },
		  {
		    "source": "Disturbance in attention",
		    "target": "Yawning",
		    "weight": 0.0909
		  },
		  {
		    "source": "Disturbance in social behaviour",
		    "target": "Dizziness",
		    "weight": 0.0769
		  },
		  {
		    "source": "Disturbance in social behaviour",
		    "target": "Drug administered to patient of inappropriate age",
		    "weight": 0.325
		  },
		  {
		    "source": "Disturbance in social behaviour",
		    "target": "Drug diversion",
		    "weight": 0.1667
		  },
		  {
		    "source": "Disturbance in social behaviour",
		    "target": "Drug dose omission",
		    "weight": 1.125
		  },
		  {
		    "source": "Disturbance in social behaviour",
		    "target": "Drug effect decreased",
		    "weight": 0.1833
		  },
		  {
		    "source": "Disturbance in social behaviour",
		    "target": "Drug effect delayed",
		    "weight": 0.125
		  },
		  {
		    "source": "Disturbance in social behaviour",
		    "target": "Drug ineffective",
		    "weight": 0.5512
		  },
		  {
		    "source": "Disturbance in social behaviour",
		    "target": "Dysgraphia",
		    "weight": 0.0833
		  },
		  {
		    "source": "Disturbance in social behaviour",
		    "target": "Fatigue",
		    "weight": 0.2
		  },
		  {
		    "source": "Disturbance in social behaviour",
		    "target": "Feeling abnormal",
		    "weight": 0.1603
		  },
		  {
		    "source": "Disturbance in social behaviour",
		    "target": "Formication",
		    "weight": 0.1
		  },
		  {
		    "source": "Disturbance in social behaviour",
		    "target": "Frustration",
		    "weight": 0.0833
		  },
		  {
		    "source": "Disturbance in social behaviour",
		    "target": "Headache",
		    "weight": 0.125
		  },
		  {
		    "source": "Disturbance in social behaviour",
		    "target": "Heart rate increased",
		    "weight": 0.2
		  },
		  {
		    "source": "Disturbance in social behaviour",
		    "target": "Hypothyroidism",
		    "weight": 0.0769
		  },
		  {
		    "source": "Disturbance in social behaviour",
		    "target": "Impulsive behaviour",
		    "weight": 0.0833
		  },
		  {
		    "source": "Disturbance in social behaviour",
		    "target": "Inappropriate schedule of drug administration",
		    "weight": 0.1667
		  },
		  {
		    "source": "Disturbance in social behaviour",
		    "target": "Incorrect dose administered",
		    "weight": 0.0769
		  },
		  {
		    "source": "Disturbance in social behaviour",
		    "target": "Insomnia",
		    "weight": 0.325
		  },
		  {
		    "source": "Disturbance in social behaviour",
		    "target": "Intentional overdose",
		    "weight": 0.1429
		  },
		  {
		    "source": "Disturbance in social behaviour",
		    "target": "Malaise",
		    "weight": 0.6198
		  },
		  {
		    "source": "Disturbance in social behaviour",
		    "target": "Mental impairment",
		    "weight": 0.0769
		  },
		  {
		    "source": "Disturbance in social behaviour",
		    "target": "Muscle twitching",
		    "weight": 0.1
		  },
		  {
		    "source": "Disturbance in social behaviour",
		    "target": "Myalgia",
		    "weight": 0.1
		  },
		  {
		    "source": "Disturbance in social behaviour",
		    "target": "Nausea",
		    "weight": 0.2769
		  },
		  {
		    "source": "Disturbance in social behaviour",
		    "target": "Oral administration complication",
		    "weight": 0.2
		  },
		  {
		    "source": "Disturbance in social behaviour",
		    "target": "Performance status decreased",
		    "weight": 0.0769
		  },
		  {
		    "source": "Disturbance in social behaviour",
		    "target": "Product quality issue",
		    "weight": 1.5781
		  },
		  {
		    "source": "Disturbance in social behaviour",
		    "target": "Product use issue",
		    "weight": 0.1429
		  },
		  {
		    "source": "Disturbance in social behaviour",
		    "target": "Psychomotor hyperactivity",
		    "weight": 0.0833
		  },
		  {
		    "source": "Disturbance in social behaviour",
		    "target": "Screaming",
		    "weight": 0.1
		  },
		  {
		    "source": "Disturbance in social behaviour",
		    "target": "Seizure",
		    "weight": 0.2
		  },
		  {
		    "source": "Disturbance in social behaviour",
		    "target": "Sleep disorder",
		    "weight": 0.2
		  },
		  {
		    "source": "Disturbance in social behaviour",
		    "target": "Somnambulism",
		    "weight": 0.2
		  },
		  {
		    "source": "Disturbance in social behaviour",
		    "target": "Somnolence",
		    "weight": 0.0769
		  },
		  {
		    "source": "Disturbance in social behaviour",
		    "target": "Tourette's disorder",
		    "weight": 0.0833
		  },
		  {
		    "source": "Disturbance in social behaviour",
		    "target": "Tremor",
		    "weight": 0.1
		  },
		  {
		    "source": "Disturbance in social behaviour",
		    "target": "Weight increased",
		    "weight": 0.0833
		  },
		  {
		    "source": "Disturbance in social behaviour",
		    "target": "Withdrawal syndrome",
		    "weight": 0.1667
		  },
		  {
		    "source": "Disturbance in social behaviour",
		    "target": "Wrong technique in product usage process",
		    "weight": 0.3198
		  },
		  {
		    "source": "Diverticulitis",
		    "target": "Feeding disorder",
		    "weight": 0.0476
		  },
		  {
		    "source": "Diverticulitis",
		    "target": "Gastritis",
		    "weight": 0.0476
		  },
		  {
		    "source": "Diverticulitis",
		    "target": "Increased appetite",
		    "weight": 0.0476
		  },
		  {
		    "source": "Diverticulitis",
		    "target": "Osteoarthritis",
		    "weight": 0.0476
		  },
		  {
		    "source": "Diverticulitis",
		    "target": "Pain",
		    "weight": 0.0476
		  },
		  {
		    "source": "Diverticulitis",
		    "target": "Panic attack",
		    "weight": 0.0476
		  },
		  {
		    "source": "Diverticulitis",
		    "target": "Poor quality sleep",
		    "weight": 0.0476
		  },
		  {
		    "source": "Diverticulitis",
		    "target": "Psychotic disorder",
		    "weight": 0.0476
		  },
		  {
		    "source": "Diverticulitis",
		    "target": "Scar",
		    "weight": 0.0476
		  },
		  {
		    "source": "Diverticulitis",
		    "target": "Tooth infection",
		    "weight": 0.0476
		  },
		  {
		    "source": "Diverticulitis",
		    "target": "Tooth loss",
		    "weight": 0.0476
		  },
		  {
		    "source": "Diverticulitis",
		    "target": "Toothache",
		    "weight": 0.0476
		  },
		  {
		    "source": "Dizziness",
		    "target": "Drug effect decreased",
		    "weight": 0.0556
		  },
		  {
		    "source": "Dizziness",
		    "target": "Dyspnoea",
		    "weight": 0.0833
		  },
		  {
		    "source": "Dizziness",
		    "target": "Epistaxis",
		    "weight": 0.0556
		  },
		  {
		    "source": "Dizziness",
		    "target": "Feeling abnormal",
		    "weight": 0.0769
		  },
		  {
		    "source": "Dizziness",
		    "target": "Flat affect",
		    "weight": 0.0556
		  },
		  {
		    "source": "Dizziness",
		    "target": "Hallucinations, mixed",
		    "weight": 0.0833
		  },
		  {
		    "source": "Dizziness",
		    "target": "Headache",
		    "weight": 0.0556
		  },
		  {
		    "source": "Dizziness",
		    "target": "Hypothyroidism",
		    "weight": 0.0769
		  },
		  {
		    "source": "Dizziness",
		    "target": "Incoherent",
		    "weight": 0.0833
		  },
		  {
		    "source": "Dizziness",
		    "target": "Incorrect dose administered",
		    "weight": 0.0769
		  },
		  {
		    "source": "Dizziness",
		    "target": "Insomnia",
		    "weight": 0.0556
		  },
		  {
		    "source": "Dizziness",
		    "target": "Irritability",
		    "weight": 0.0556
		  },
		  {
		    "source": "Dizziness",
		    "target": "Limb discomfort",
		    "weight": 0.3333
		  },
		  {
		    "source": "Dizziness",
		    "target": "Malaise",
		    "weight": 0.0769
		  },
		  {
		    "source": "Dizziness",
		    "target": "Mental impairment",
		    "weight": 0.0769
		  },
		  {
		    "source": "Dizziness",
		    "target": "Nausea",
		    "weight": 0.2158
		  },
		  {
		    "source": "Dizziness",
		    "target": "Obsessive thoughts",
		    "weight": 0.0556
		  },
		  {
		    "source": "Dizziness",
		    "target": "Oesophagitis",
		    "weight": 0.0833
		  },
		  {
		    "source": "Dizziness",
		    "target": "Pallor",
		    "weight": 0.3333
		  },
		  {
		    "source": "Dizziness",
		    "target": "Performance status decreased",
		    "weight": 0.0769
		  },
		  {
		    "source": "Dizziness",
		    "target": "Product quality issue",
		    "weight": 0.0769
		  },
		  {
		    "source": "Dizziness",
		    "target": "Pyrexia",
		    "weight": 0.0833
		  },
		  {
		    "source": "Dizziness",
		    "target": "Seizure",
		    "weight": 0.0833
		  },
		  {
		    "source": "Dizziness",
		    "target": "Social avoidant behaviour",
		    "weight": 0.0556
		  },
		  {
		    "source": "Dizziness",
		    "target": "Somnolence",
		    "weight": 0.0769
		  },
		  {
		    "source": "Dizziness",
		    "target": "Syncope",
		    "weight": 0.0833
		  },
		  {
		    "source": "Dizziness",
		    "target": "Tic",
		    "weight": 0.0556
		  },
		  {
		    "source": "Dizziness",
		    "target": "Unevaluable event",
		    "weight": 0.0833
		  },
		  {
		    "source": "Dizziness",
		    "target": "Vomiting",
		    "weight": 0.0556
		  },
		  {
		    "source": "Dizziness",
		    "target": "Wrong technique in product usage process",
		    "weight": 0.0769
		  },
		  {
		    "source": "Drug abuse",
		    "target": "Drug diversion",
		    "weight": 0.3333
		  },
		  {
		    "source": "Drug abuse",
		    "target": "Panic attack",
		    "weight": 0.2
		  },
		  {
		    "source": "Drug abuse",
		    "target": "Surgery",
		    "weight": 0.2
		  },
		  {
		    "source": "Drug abuse",
		    "target": "Tachycardia",
		    "weight": 0.25
		  },
		  {
		    "source": "Drug administered at inappropriate site",
		    "target": "Hair colour changes",
		    "weight": 0.3333
		  },
		  {
		    "source": "Drug administered at inappropriate site",
		    "target": "Hair texture abnormal",
		    "weight": 0.3333
		  },
		  {
		    "source": "Drug administered to patient of inappropriate age",
		    "target": "Drug dose omission",
		    "weight": 0.125
		  },
		  {
		    "source": "Drug administered to patient of inappropriate age",
		    "target": "Drug effect decreased",
		    "weight": 0.0667
		  },
		  {
		    "source": "Drug administered to patient of inappropriate age",
		    "target": "Drug effect delayed",
		    "weight": 0.125
		  },
		  {
		    "source": "Drug administered to patient of inappropriate age",
		    "target": "Drug ineffective",
		    "weight": 0.3028
		  },
		  {
		    "source": "Drug administered to patient of inappropriate age",
		    "target": "Eosinophilic oesophagitis",
		    "weight": 0.0667
		  },
		  {
		    "source": "Drug administered to patient of inappropriate age",
		    "target": "Eye swelling",
		    "weight": 0.1429
		  },
		  {
		    "source": "Drug administered to patient of inappropriate age",
		    "target": "Feeling abnormal",
		    "weight": 0.0667
		  },
		  {
		    "source": "Drug administered to patient of inappropriate age",
		    "target": "Flight of ideas",
		    "weight": 0.1111
		  },
		  {
		    "source": "Drug administered to patient of inappropriate age",
		    "target": "Growth accelerated",
		    "weight": 0.0667
		  },
		  {
		    "source": "Drug administered to patient of inappropriate age",
		    "target": "Haemorrhoids",
		    "weight": 0.0667
		  },
		  {
		    "source": "Drug administered to patient of inappropriate age",
		    "target": "Headache",
		    "weight": 0.125
		  },
		  {
		    "source": "Drug administered to patient of inappropriate age",
		    "target": "Hepatic enzyme increased",
		    "weight": 0.0667
		  },
		  {
		    "source": "Drug administered to patient of inappropriate age",
		    "target": "Hypersensitivity",
		    "weight": 0.1429
		  },
		  {
		    "source": "Drug administered to patient of inappropriate age",
		    "target": "Hypoaesthesia oral",
		    "weight": 0.1429
		  },
		  {
		    "source": "Drug administered to patient of inappropriate age",
		    "target": "Initial insomnia",
		    "weight": 0.1111
		  },
		  {
		    "source": "Drug administered to patient of inappropriate age",
		    "target": "Insomnia",
		    "weight": 0.125
		  },
		  {
		    "source": "Drug administered to patient of inappropriate age",
		    "target": "Lactose intolerance",
		    "weight": 0.0667
		  },
		  {
		    "source": "Drug administered to patient of inappropriate age",
		    "target": "Learning disorder",
		    "weight": 0.5
		  },
		  {
		    "source": "Drug administered to patient of inappropriate age",
		    "target": "Lip swelling",
		    "weight": 0.1429
		  },
		  {
		    "source": "Drug administered to patient of inappropriate age",
		    "target": "Logorrhoea",
		    "weight": 0.0667
		  },
		  {
		    "source": "Drug administered to patient of inappropriate age",
		    "target": "Neck pain",
		    "weight": 0.1429
		  },
		  {
		    "source": "Drug administered to patient of inappropriate age",
		    "target": "No adverse event",
		    "weight": 1.5
		  },
		  {
		    "source": "Drug administered to patient of inappropriate age",
		    "target": "Oral administration complication",
		    "weight": 0.3111
		  },
		  {
		    "source": "Drug administered to patient of inappropriate age",
		    "target": "Paranoia",
		    "weight": 0.1111
		  },
		  {
		    "source": "Drug administered to patient of inappropriate age",
		    "target": "Personality change",
		    "weight": 0.5
		  },
		  {
		    "source": "Drug administered to patient of inappropriate age",
		    "target": "Product quality issue",
		    "weight": 0.4361
		  },
		  {
		    "source": "Drug administered to patient of inappropriate age",
		    "target": "Psychomotor hyperactivity",
		    "weight": 0.1111
		  },
		  {
		    "source": "Drug administered to patient of inappropriate age",
		    "target": "Rash",
		    "weight": 0.1429
		  },
		  {
		    "source": "Drug administered to patient of inappropriate age",
		    "target": "Restlessness",
		    "weight": 0.1111
		  },
		  {
		    "source": "Drug administered to patient of inappropriate age",
		    "target": "Somnambulism",
		    "weight": 0.2
		  },
		  {
		    "source": "Drug administered to patient of inappropriate age",
		    "target": "Weight decreased",
		    "weight": 0.0667
		  },
		  {
		    "source": "Drug dispensing error",
		    "target": "Drug ineffective",
		    "weight": 0.5
		  },
		  {
		    "source": "Drug diversion",
		    "target": "Drug dose omission",
		    "weight": 0.1667
		  },
		  {
		    "source": "Drug diversion",
		    "target": "Drug ineffective",
		    "weight": 0.8333
		  },
		  {
		    "source": "Drug diversion",
		    "target": "Inappropriate schedule of drug administration",
		    "weight": 0.1667
		  },
		  {
		    "source": "Drug diversion",
		    "target": "Intentional overdose",
		    "weight": 0.3333
		  },
		  {
		    "source": "Drug diversion",
		    "target": "Intentional product misuse",
		    "weight": 0.3333
		  },
		  {
		    "source": "Drug diversion",
		    "target": "Vomiting",
		    "weight": 0.3333
		  },
		  {
		    "source": "Drug diversion",
		    "target": "Withdrawal syndrome",
		    "weight": 0.1667
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Drug effect decreased",
		    "weight": 0.1455
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Drug effect delayed",
		    "weight": 0.125
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Drug effect increased",
		    "weight": 0.0455
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Drug ineffective",
		    "weight": 0.2955
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Drug screen negative",
		    "weight": 0.5
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Drug tolerance",
		    "weight": 0.125
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Drug withdrawal syndrome",
		    "weight": 0.8333
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Dysgeusia",
		    "weight": 0.5
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Educational problem",
		    "weight": 0.8333
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Emotional distress",
		    "weight": 0.25
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Eye irritation",
		    "weight": 0.0455
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Family stress",
		    "weight": 0.3333
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Fatigue",
		    "weight": 0.3705
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Fear",
		    "weight": 0.0455
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Feeling abnormal",
		    "weight": 0.3929
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Food hoarding",
		    "weight": 0.2
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Foot fracture",
		    "weight": 0.25
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Formication",
		    "weight": 0.1
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Headache",
		    "weight": 0.9205
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Hypersomnia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Hypertension",
		    "weight": 0.3333
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Inappropriate schedule of drug administration",
		    "weight": 0.2917
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Increased appetite",
		    "weight": 0.2
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Insomnia",
		    "weight": 0.125
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Logorrhoea",
		    "weight": 0.1429
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Malaise",
		    "weight": 0.2455
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Migraine",
		    "weight": 0.5788
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Muscle twitching",
		    "weight": 0.1
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Myalgia",
		    "weight": 0.1
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Nasopharyngitis",
		    "weight": 0.0455
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Off label use",
		    "weight": 0.3667
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Prescribed overdose",
		    "weight": 0.125
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Product quality issue",
		    "weight": 0.7083
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Product use issue",
		    "weight": 0.125
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Pruritus",
		    "weight": 0.3333
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Psychomotor hyperactivity",
		    "weight": 0.25
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Screaming",
		    "weight": 0.1
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Sinusitis",
		    "weight": 0.5
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Sleep disorder",
		    "weight": 0.2
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Social phobia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Suicidal ideation",
		    "weight": 0.1667
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Tachyphrenia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Tearfulness",
		    "weight": 0.3333
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Therapeutic response unexpected",
		    "weight": 0.25
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Tremor",
		    "weight": 0.1
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Urine amphetamine negative",
		    "weight": 0.5
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Weight increased",
		    "weight": 0.4455
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Withdrawal syndrome",
		    "weight": 0.1667
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Wrist fracture",
		    "weight": 0.25
		  },
		  {
		    "source": "Drug dose omission",
		    "target": "Wrong technique in product usage process",
		    "weight": 0.1
		  },
		  {
		    "source": "Drug dose titration not performed",
		    "target": "Drug ineffective",
		    "weight": 0.3333
		  },
		  {
		    "source": "Drug dose titration not performed",
		    "target": "Product use issue",
		    "weight": 0.3333
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Drug effect increased",
		    "weight": 0.3371
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Drug effect variable",
		    "weight": 0.25
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Drug ineffective",
		    "weight": 0.6197
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Drug interaction",
		    "weight": 0.0769
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Drug tolerance",
		    "weight": 0.0909
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Drug withdrawal convulsions",
		    "weight": 0.0833
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Dry mouth",
		    "weight": 0.2
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Dysgraphia",
		    "weight": 0.0833
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Educational problem",
		    "weight": 0.3095
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Emotional disorder",
		    "weight": 0.2679
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Eosinophilic oesophagitis",
		    "weight": 0.0667
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Epistaxis",
		    "weight": 0.0556
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Eye irritation",
		    "weight": 0.0455
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Fatigue",
		    "weight": 0.1224
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Fear",
		    "weight": 0.1224
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Feeling abnormal",
		    "weight": 0.6083
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Flat affect",
		    "weight": 0.0556
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Formication",
		    "weight": 0.1
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Frustration",
		    "weight": 0.0833
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Growth accelerated",
		    "weight": 0.0667
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Haemorrhoids",
		    "weight": 0.0667
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Headache",
		    "weight": 0.2677
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Hepatic enzyme increased",
		    "weight": 0.0667
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Hostility",
		    "weight": 0.0833
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Hypersomnia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Impulsive behaviour",
		    "weight": 0.0833
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Inappropriate schedule of drug administration",
		    "weight": 2.8742
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Incorrect dose administered",
		    "weight": 0.7512
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Increased appetite",
		    "weight": 0.0833
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Infection",
		    "weight": 0.1429
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Infusion related reaction",
		    "weight": 0.1667
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Insomnia",
		    "weight": 0.6389
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Irritability",
		    "weight": 0.0556
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Job dissatisfaction",
		    "weight": 0.25
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Lactose intolerance",
		    "weight": 0.0667
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Laziness",
		    "weight": 0.0769
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Lethargy",
		    "weight": 0.125
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Libido decreased",
		    "weight": 0.25
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Logorrhoea",
		    "weight": 0.0667
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Malaise",
		    "weight": 0.1224
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Mania",
		    "weight": 0.0833
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Memory impairment",
		    "weight": 0.1667
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Migraine",
		    "weight": 0.0455
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Mood swings",
		    "weight": 0.1667
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Muscle twitching",
		    "weight": 0.1
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Myalgia",
		    "weight": 0.1
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Nasopharyngitis",
		    "weight": 0.0455
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Nausea",
		    "weight": 0.0556
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Obsessive thoughts",
		    "weight": 0.0556
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Off label use",
		    "weight": 0.3333
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Optic nerve neoplasm",
		    "weight": 0.0833
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Overdose",
		    "weight": 0.5
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Panic reaction",
		    "weight": 0.25
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Prescribed overdose",
		    "weight": 0.3333
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Product quality issue",
		    "weight": 3.2754
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Product tampering",
		    "weight": 0.25
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Psychiatric symptom",
		    "weight": 0.125
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Psychomotor hyperactivity",
		    "weight": 0.3269
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Restlessness",
		    "weight": 0.1667
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Screaming",
		    "weight": 0.1
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Social avoidant behaviour",
		    "weight": 0.0556
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Social phobia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Somnolence",
		    "weight": 0.6178
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Stress",
		    "weight": 0.0909
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Tachyphrenia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Tic",
		    "weight": 0.0556
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Tourette's disorder",
		    "weight": 0.0833
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Tremor",
		    "weight": 0.1
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Urinary incontinence",
		    "weight": 0.1667
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Vomiting",
		    "weight": 0.0556
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Weight decreased",
		    "weight": 0.0667
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Weight increased",
		    "weight": 0.2955
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Wrong technique in product usage process",
		    "weight": 0.8992
		  },
		  {
		    "source": "Drug effect decreased",
		    "target": "Yawning",
		    "weight": 0.0909
		  },
		  {
		    "source": "Drug effect delayed",
		    "target": "Drug ineffective",
		    "weight": 0.125
		  },
		  {
		    "source": "Drug effect delayed",
		    "target": "Headache",
		    "weight": 0.125
		  },
		  {
		    "source": "Drug effect delayed",
		    "target": "Impulsive behaviour",
		    "weight": 0.5
		  },
		  {
		    "source": "Drug effect delayed",
		    "target": "Insomnia",
		    "weight": 0.125
		  },
		  {
		    "source": "Drug effect delayed",
		    "target": "Product quality issue",
		    "weight": 0.125
		  },
		  {
		    "source": "Drug effect incomplete",
		    "target": "Drug effect increased",
		    "weight": 0.2
		  },
		  {
		    "source": "Drug effect incomplete",
		    "target": "Drug ineffective",
		    "weight": 0.2
		  },
		  {
		    "source": "Drug effect incomplete",
		    "target": "Product quality issue",
		    "weight": 0.2
		  },
		  {
		    "source": "Drug effect incomplete",
		    "target": "Psychomotor hyperactivity",
		    "weight": 0.2
		  },
		  {
		    "source": "Drug effect increased",
		    "target": "Drug effect variable",
		    "weight": 0.1667
		  },
		  {
		    "source": "Drug effect increased",
		    "target": "Drug ineffective",
		    "weight": 0.4121
		  },
		  {
		    "source": "Drug effect increased",
		    "target": "Emotional disorder",
		    "weight": 0.125
		  },
		  {
		    "source": "Drug effect increased",
		    "target": "Eye irritation",
		    "weight": 0.0455
		  },
		  {
		    "source": "Drug effect increased",
		    "target": "Fatigue",
		    "weight": 0.0455
		  },
		  {
		    "source": "Drug effect increased",
		    "target": "Fear",
		    "weight": 0.0455
		  },
		  {
		    "source": "Drug effect increased",
		    "target": "Feeling abnormal",
		    "weight": 0.2917
		  },
		  {
		    "source": "Drug effect increased",
		    "target": "Feeling jittery",
		    "weight": 0.1667
		  },
		  {
		    "source": "Drug effect increased",
		    "target": "Headache",
		    "weight": 0.0455
		  },
		  {
		    "source": "Drug effect increased",
		    "target": "Hypersomnia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Drug effect increased",
		    "target": "Lethargy",
		    "weight": 0.125
		  },
		  {
		    "source": "Drug effect increased",
		    "target": "Malaise",
		    "weight": 0.0455
		  },
		  {
		    "source": "Drug effect increased",
		    "target": "Migraine",
		    "weight": 0.0455
		  },
		  {
		    "source": "Drug effect increased",
		    "target": "Nasopharyngitis",
		    "weight": 0.0455
		  },
		  {
		    "source": "Drug effect increased",
		    "target": "Palpitations",
		    "weight": 0.3333
		  },
		  {
		    "source": "Drug effect increased",
		    "target": "Product quality issue",
		    "weight": 0.6583
		  },
		  {
		    "source": "Drug effect increased",
		    "target": "Psychiatric symptom",
		    "weight": 0.125
		  },
		  {
		    "source": "Drug effect increased",
		    "target": "Psychomotor hyperactivity",
		    "weight": 0.2
		  },
		  {
		    "source": "Drug effect increased",
		    "target": "Social phobia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Drug effect increased",
		    "target": "Somnolence",
		    "weight": 0.3333
		  },
		  {
		    "source": "Drug effect increased",
		    "target": "Tachyphrenia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Drug effect increased",
		    "target": "Weight increased",
		    "weight": 0.0455
		  },
		  {
		    "source": "Drug effect increased",
		    "target": "Wrong technique in product usage process",
		    "weight": 0.125
		  },
		  {
		    "source": "Drug effect variable",
		    "target": "Drug ineffective",
		    "weight": 0.3667
		  },
		  {
		    "source": "Drug effect variable",
		    "target": "Feeling abnormal",
		    "weight": 0.2
		  },
		  {
		    "source": "Drug effect variable",
		    "target": "Feeling jittery",
		    "weight": 0.1667
		  },
		  {
		    "source": "Drug effect variable",
		    "target": "Insomnia",
		    "weight": 0.2
		  },
		  {
		    "source": "Drug effect variable",
		    "target": "Panic reaction",
		    "weight": 0.25
		  },
		  {
		    "source": "Drug effect variable",
		    "target": "Product quality issue",
		    "weight": 1.3667
		  },
		  {
		    "source": "Drug effect variable",
		    "target": "Somnolence",
		    "weight": 0.1667
		  },
		  {
		    "source": "Drug hypersensitivity",
		    "target": "Fatigue",
		    "weight": 0.2
		  },
		  {
		    "source": "Drug hypersensitivity",
		    "target": "Headache",
		    "weight": 0.2
		  },
		  {
		    "source": "Drug hypersensitivity",
		    "target": "Local swelling",
		    "weight": 0.2
		  },
		  {
		    "source": "Drug hypersensitivity",
		    "target": "Neck pain",
		    "weight": 0.2
		  },
		  {
		    "source": "Drug hypersensitivity",
		    "target": "Pyrexia",
		    "weight": 0.2
		  },
		  {
		    "source": "Drug hypersensitivity",
		    "target": "Urticaria",
		    "weight": 0.2
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Drug screen negative",
		    "weight": 0.5
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Drug tolerance",
		    "weight": 0.7159
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Drug withdrawal convulsions",
		    "weight": 0.0833
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Drug withdrawal syndrome",
		    "weight": 0.1667
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Dysgraphia",
		    "weight": 0.0833
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Dyskinesia",
		    "weight": 0.0714
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Emotional disorder",
		    "weight": 0.25
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Eosinophilic oesophagitis",
		    "weight": 0.0667
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Eye irritation",
		    "weight": 0.0455
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Eye movement disorder",
		    "weight": 0.0714
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Fatigue",
		    "weight": 0.5562
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Fear",
		    "weight": 0.0455
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Feeling abnormal",
		    "weight": 0.6588
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Feeling jittery",
		    "weight": 0.5
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Feeling of despair",
		    "weight": 0.25
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Flight of ideas",
		    "weight": 0.1111
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Formication",
		    "weight": 0.0833
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Frustration",
		    "weight": 0.0833
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Growth accelerated",
		    "weight": 0.0667
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Haemorrhagic diathesis",
		    "weight": 0.25
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Haemorrhoids",
		    "weight": 0.0667
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Headache",
		    "weight": 0.7955
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Hepatic enzyme increased",
		    "weight": 0.0667
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Hostility",
		    "weight": 0.1667
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Hunger",
		    "weight": 0.25
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Hyperphagia",
		    "weight": 0.0714
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Hypersomnia",
		    "weight": 0.1043
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Impaired work ability",
		    "weight": 0.0588
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Impulsive behaviour",
		    "weight": 0.5833
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Inappropriate schedule of drug administration",
		    "weight": 1.0492
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Incorrect dose administered",
		    "weight": 0.1497
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Increased appetite",
		    "weight": 0.3269
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Initial insomnia",
		    "weight": 0.1111
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Insomnia",
		    "weight": 0.575
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Intentional overdose",
		    "weight": 0.4762
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Irritability",
		    "weight": 0.0833
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Job dissatisfaction",
		    "weight": 0.25
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Lactose intolerance",
		    "weight": 0.0667
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Laziness",
		    "weight": 0.0714
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Lethargy",
		    "weight": 0.1667
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Libido decreased",
		    "weight": 0.0769
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Logorrhoea",
		    "weight": 0.0667
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Malabsorption",
		    "weight": 0.0833
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Malaise",
		    "weight": 0.3883
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Mania",
		    "weight": 0.0833
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Mental impairment",
		    "weight": 0.0588
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Migraine",
		    "weight": 0.0455
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Mood altered",
		    "weight": 0.25
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Mood swings",
		    "weight": 0.0833
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Muscle spasms",
		    "weight": 0.0769
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Musculoskeletal stiffness",
		    "weight": 0.0714
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Nasopharyngitis",
		    "weight": 0.0455
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Nausea",
		    "weight": 0.2769
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Nervousness",
		    "weight": 0.3333
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Nightmare",
		    "weight": 0.0588
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Off label use",
		    "weight": 0.3333
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Optic nerve neoplasm",
		    "weight": 0.0833
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Oral administration complication",
		    "weight": 0.1111
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Pain",
		    "weight": 0.25
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Pain in jaw",
		    "weight": 0.0769
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Palpitations",
		    "weight": 0.0769
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Paraesthesia",
		    "weight": 0.6667
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Paranoia",
		    "weight": 0.1111
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Performance status decreased",
		    "weight": 0.125
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Prescribed overdose",
		    "weight": 1.0833
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Product quality issue",
		    "weight": 12.1627
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Product substitution issue",
		    "weight": 0.5
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Product tampering",
		    "weight": 0.5833
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Product use issue",
		    "weight": 0.6012
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Psychomotor hyperactivity",
		    "weight": 0.5944
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Pyrexia",
		    "weight": 0.0769
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Rapid eye movements sleep abnormal",
		    "weight": 0.0588
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Rash",
		    "weight": 0.25
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Rebound effect",
		    "weight": 0.1667
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Respiratory tract infection",
		    "weight": 0.25
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Restlessness",
		    "weight": 0.3611
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Road traffic accident",
		    "weight": 0.0588
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Sleep disorder",
		    "weight": 0.1429
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Sluggishness",
		    "weight": 0.25
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Social avoidant behaviour",
		    "weight": 0.0714
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Social phobia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Somnolence",
		    "weight": 0.5076
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Stress",
		    "weight": 0.0909
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Tachyphrenia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Therapy cessation",
		    "weight": 0.125
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Thirst",
		    "weight": 0.0714
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Tinnitus",
		    "weight": 0.1667
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Tourette's disorder",
		    "weight": 0.0833
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Toxicity to various agents",
		    "weight": 0.25
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Underweight",
		    "weight": 0.0588
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Victim of abuse",
		    "weight": 0.0714
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Victim of sexual abuse",
		    "weight": 0.0714
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Vitamin D abnormal",
		    "weight": 0.0833
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Vitreous floaters",
		    "weight": 0.0833
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Vomiting",
		    "weight": 0.0769
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Weight decreased",
		    "weight": 0.0667
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Weight increased",
		    "weight": 0.759
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Wrist fracture",
		    "weight": 0.1429
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Wrong technique in product usage process",
		    "weight": 0.5671
		  },
		  {
		    "source": "Drug ineffective",
		    "target": "Yawning",
		    "weight": 0.0909
		  },
		  {
		    "source": "Drug interaction",
		    "target": "Dyskinesia",
		    "weight": 0.1
		  },
		  {
		    "source": "Drug interaction",
		    "target": "Fatigue",
		    "weight": 0.0769
		  },
		  {
		    "source": "Drug interaction",
		    "target": "Fear",
		    "weight": 0.0769
		  },
		  {
		    "source": "Drug interaction",
		    "target": "Hyperhidrosis",
		    "weight": 0.1
		  },
		  {
		    "source": "Drug interaction",
		    "target": "Hypertension",
		    "weight": 0.2
		  },
		  {
		    "source": "Drug interaction",
		    "target": "Incorrect dose administered",
		    "weight": 0.0769
		  },
		  {
		    "source": "Drug interaction",
		    "target": "Laziness",
		    "weight": 0.0769
		  },
		  {
		    "source": "Drug interaction",
		    "target": "Malaise",
		    "weight": 0.0769
		  },
		  {
		    "source": "Drug interaction",
		    "target": "Muscle spasms",
		    "weight": 0.1
		  },
		  {
		    "source": "Drug interaction",
		    "target": "Mydriasis",
		    "weight": 0.1
		  },
		  {
		    "source": "Drug interaction",
		    "target": "No adverse event",
		    "weight": 0.5
		  },
		  {
		    "source": "Drug interaction",
		    "target": "Pain in extremity",
		    "weight": 0.2
		  },
		  {
		    "source": "Drug interaction",
		    "target": "Psychomotor hyperactivity",
		    "weight": 0.0769
		  },
		  {
		    "source": "Drug interaction",
		    "target": "Serotonin syndrome",
		    "weight": 0.1
		  },
		  {
		    "source": "Drug interaction",
		    "target": "Somnolence",
		    "weight": 0.0769
		  },
		  {
		    "source": "Drug interaction",
		    "target": "Tachyphrenia",
		    "weight": 0.1
		  },
		  {
		    "source": "Drug prescribing error",
		    "target": "No adverse event",
		    "weight": 1
		  },
		  {
		    "source": "Drug screen false positive",
		    "target": "Hepatitis C",
		    "weight": 0.5
		  },
		  {
		    "source": "Drug tolerance",
		    "target": "Fatigue",
		    "weight": 0.125
		  },
		  {
		    "source": "Drug tolerance",
		    "target": "Inappropriate schedule of drug administration",
		    "weight": 0.2159
		  },
		  {
		    "source": "Drug tolerance",
		    "target": "Incorrect dose administered",
		    "weight": 0.0909
		  },
		  {
		    "source": "Drug tolerance",
		    "target": "Prescribed overdose",
		    "weight": 0.125
		  },
		  {
		    "source": "Drug tolerance",
		    "target": "Product quality issue",
		    "weight": 0.0909
		  },
		  {
		    "source": "Drug tolerance",
		    "target": "Product use issue",
		    "weight": 0.125
		  },
		  {
		    "source": "Drug tolerance",
		    "target": "Somnolence",
		    "weight": 0.0909
		  },
		  {
		    "source": "Drug tolerance",
		    "target": "Stress",
		    "weight": 0.0909
		  },
		  {
		    "source": "Drug tolerance",
		    "target": "Wrong technique in product usage process",
		    "weight": 0.0909
		  },
		  {
		    "source": "Drug tolerance",
		    "target": "Yawning",
		    "weight": 0.0909
		  },
		  {
		    "source": "Drug withdrawal convulsions",
		    "target": "Hostility",
		    "weight": 0.0833
		  },
		  {
		    "source": "Drug withdrawal convulsions",
		    "target": "Increased appetite",
		    "weight": 0.0833
		  },
		  {
		    "source": "Drug withdrawal convulsions",
		    "target": "Mania",
		    "weight": 0.0833
		  },
		  {
		    "source": "Drug withdrawal convulsions",
		    "target": "Optic nerve neoplasm",
		    "weight": 0.0833
		  },
		  {
		    "source": "Drug withdrawal convulsions",
		    "target": "Somnolence",
		    "weight": 0.0833
		  },
		  {
		    "source": "Drug withdrawal syndrome",
		    "target": "Hot flush",
		    "weight": 0.3333
		  },
		  {
		    "source": "Drug withdrawal syndrome",
		    "target": "Impulsive behaviour",
		    "weight": 0.25
		  },
		  {
		    "source": "Drug withdrawal syndrome",
		    "target": "Malaise",
		    "weight": 0.5
		  },
		  {
		    "source": "Drug withdrawal syndrome",
		    "target": "Paraesthesia",
		    "weight": 0.1667
		  },
		  {
		    "source": "Drug withdrawal syndrome",
		    "target": "Product substitution issue",
		    "weight": 0.1667
		  },
		  {
		    "source": "Drug withdrawal syndrome",
		    "target": "Restlessness",
		    "weight": 0.25
		  },
		  {
		    "source": "Drug withdrawal syndrome",
		    "target": "Sleep disorder",
		    "weight": 0.25
		  },
		  {
		    "source": "Drug withdrawal syndrome",
		    "target": "Tinnitus",
		    "weight": 0.1667
		  },
		  {
		    "source": "Drug withdrawal syndrome neonatal",
		    "target": "Foetal distress syndrome",
		    "weight": 0.1667
		  },
		  {
		    "source": "Drug withdrawal syndrome neonatal",
		    "target": "Foetal exposure during pregnancy",
		    "weight": 0.1667
		  },
		  {
		    "source": "Drug withdrawal syndrome neonatal",
		    "target": "Jaundice neonatal",
		    "weight": 0.1667
		  },
		  {
		    "source": "Drug withdrawal syndrome neonatal",
		    "target": "Premature baby",
		    "weight": 0.1667
		  },
		  {
		    "source": "Dry mouth",
		    "target": "Dry skin",
		    "weight": 0.0909
		  },
		  {
		    "source": "Dry mouth",
		    "target": "Dysgeusia",
		    "weight": 0.5
		  },
		  {
		    "source": "Dry mouth",
		    "target": "Dyspareunia",
		    "weight": 0.0909
		  },
		  {
		    "source": "Dry mouth",
		    "target": "Fungal infection",
		    "weight": 0.0909
		  },
		  {
		    "source": "Dry mouth",
		    "target": "Hormone level abnormal",
		    "weight": 0.0909
		  },
		  {
		    "source": "Dry mouth",
		    "target": "Inappropriate schedule of drug administration",
		    "weight": 0.2
		  },
		  {
		    "source": "Dry mouth",
		    "target": "Somnolence",
		    "weight": 0.2
		  },
		  {
		    "source": "Dry mouth",
		    "target": "Vaginal discharge",
		    "weight": 0.0909
		  },
		  {
		    "source": "Dry mouth",
		    "target": "Vaginal pH increased",
		    "weight": 0.0909
		  },
		  {
		    "source": "Dry mouth",
		    "target": "Vulvovaginal dryness",
		    "weight": 0.0909
		  },
		  {
		    "source": "Dry mouth",
		    "target": "Vulvovaginal erythema",
		    "weight": 0.0909
		  },
		  {
		    "source": "Dry mouth",
		    "target": "Vulvovaginal pain",
		    "weight": 0.0909
		  },
		  {
		    "source": "Dry mouth",
		    "target": "Vulvovaginal swelling",
		    "weight": 0.0909
		  },
		  {
		    "source": "Dry skin",
		    "target": "Dyspareunia",
		    "weight": 0.0909
		  },
		  {
		    "source": "Dry skin",
		    "target": "Fungal infection",
		    "weight": 0.0909
		  },
		  {
		    "source": "Dry skin",
		    "target": "Hormone level abnormal",
		    "weight": 0.0909
		  },
		  {
		    "source": "Dry skin",
		    "target": "Vaginal discharge",
		    "weight": 0.0909
		  },
		  {
		    "source": "Dry skin",
		    "target": "Vaginal pH increased",
		    "weight": 0.0909
		  },
		  {
		    "source": "Dry skin",
		    "target": "Vulvovaginal dryness",
		    "weight": 0.0909
		  },
		  {
		    "source": "Dry skin",
		    "target": "Vulvovaginal erythema",
		    "weight": 0.0909
		  },
		  {
		    "source": "Dry skin",
		    "target": "Vulvovaginal pain",
		    "weight": 0.0909
		  },
		  {
		    "source": "Dry skin",
		    "target": "Vulvovaginal swelling",
		    "weight": 0.0909
		  },
		  {
		    "source": "Dysgeusia",
		    "target": "Fatigue",
		    "weight": 0.1111
		  },
		  {
		    "source": "Dysgeusia",
		    "target": "General physical health deterioration",
		    "weight": 0.1111
		  },
		  {
		    "source": "Dysgeusia",
		    "target": "Hypoaesthesia",
		    "weight": 0.1111
		  },
		  {
		    "source": "Dysgeusia",
		    "target": "Irritable bowel syndrome",
		    "weight": 0.1111
		  },
		  {
		    "source": "Dysgeusia",
		    "target": "Muscle spasms",
		    "weight": 0.1111
		  },
		  {
		    "source": "Dysgeusia",
		    "target": "Musculoskeletal disorder",
		    "weight": 0.1111
		  },
		  {
		    "source": "Dysgeusia",
		    "target": "Syncope",
		    "weight": 0.1111
		  },
		  {
		    "source": "Dysgraphia",
		    "target": "Feeling abnormal",
		    "weight": 0.0833
		  },
		  {
		    "source": "Dysgraphia",
		    "target": "Frustration",
		    "weight": 0.0833
		  },
		  {
		    "source": "Dysgraphia",
		    "target": "Impulsive behaviour",
		    "weight": 0.0833
		  },
		  {
		    "source": "Dysgraphia",
		    "target": "Psychomotor hyperactivity",
		    "weight": 0.0833
		  },
		  {
		    "source": "Dysgraphia",
		    "target": "Tourette's disorder",
		    "weight": 0.0833
		  },
		  {
		    "source": "Dysgraphia",
		    "target": "Weight increased",
		    "weight": 0.0833
		  },
		  {
		    "source": "Dyskinesia",
		    "target": "Eye movement disorder",
		    "weight": 0.0714
		  },
		  {
		    "source": "Dyskinesia",
		    "target": "Hyperhidrosis",
		    "weight": 0.1
		  },
		  {
		    "source": "Dyskinesia",
		    "target": "Hyperphagia",
		    "weight": 0.0714
		  },
		  {
		    "source": "Dyskinesia",
		    "target": "Laziness",
		    "weight": 0.0714
		  },
		  {
		    "source": "Dyskinesia",
		    "target": "Muscle spasms",
		    "weight": 0.1
		  },
		  {
		    "source": "Dyskinesia",
		    "target": "Musculoskeletal stiffness",
		    "weight": 0.0714
		  },
		  {
		    "source": "Dyskinesia",
		    "target": "Mydriasis",
		    "weight": 0.1
		  },
		  {
		    "source": "Dyskinesia",
		    "target": "Serotonin syndrome",
		    "weight": 0.1
		  },
		  {
		    "source": "Dyskinesia",
		    "target": "Social avoidant behaviour",
		    "weight": 0.0714
		  },
		  {
		    "source": "Dyskinesia",
		    "target": "Tachyphrenia",
		    "weight": 0.1
		  },
		  {
		    "source": "Dyskinesia",
		    "target": "Thirst",
		    "weight": 0.0714
		  },
		  {
		    "source": "Dyskinesia",
		    "target": "Victim of abuse",
		    "weight": 0.0714
		  },
		  {
		    "source": "Dyskinesia",
		    "target": "Victim of sexual abuse",
		    "weight": 0.0714
		  },
		  {
		    "source": "Dyskinesia",
		    "target": "Weight increased",
		    "weight": 0.0714
		  },
		  {
		    "source": "Dyspareunia",
		    "target": "Fungal infection",
		    "weight": 0.0909
		  },
		  {
		    "source": "Dyspareunia",
		    "target": "Hormone level abnormal",
		    "weight": 0.0909
		  },
		  {
		    "source": "Dyspareunia",
		    "target": "Vaginal discharge",
		    "weight": 0.0909
		  },
		  {
		    "source": "Dyspareunia",
		    "target": "Vaginal pH increased",
		    "weight": 0.0909
		  },
		  {
		    "source": "Dyspareunia",
		    "target": "Vulvovaginal dryness",
		    "weight": 0.0909
		  },
		  {
		    "source": "Dyspareunia",
		    "target": "Vulvovaginal erythema",
		    "weight": 0.0909
		  },
		  {
		    "source": "Dyspareunia",
		    "target": "Vulvovaginal pain",
		    "weight": 0.0909
		  },
		  {
		    "source": "Dyspareunia",
		    "target": "Vulvovaginal swelling",
		    "weight": 0.0909
		  },
		  {
		    "source": "Dyspepsia",
		    "target": "Mycobacterium test positive",
		    "weight": 0.1
		  },
		  {
		    "source": "Dyspepsia",
		    "target": "Obstructive airways disorder",
		    "weight": 0.1
		  },
		  {
		    "source": "Dyspepsia",
		    "target": "Pseudomonas infection",
		    "weight": 0.1
		  },
		  {
		    "source": "Dyspepsia",
		    "target": "Sinus disorder",
		    "weight": 0.1
		  },
		  {
		    "source": "Dyspepsia",
		    "target": "Weight increased",
		    "weight": 0.1
		  },
		  {
		    "source": "Dyspnoea",
		    "target": "Fluid overload",
		    "weight": 0.1
		  },
		  {
		    "source": "Dyspnoea",
		    "target": "Hallucinations, mixed",
		    "weight": 0.0833
		  },
		  {
		    "source": "Dyspnoea",
		    "target": "Incoherent",
		    "weight": 0.0833
		  },
		  {
		    "source": "Dyspnoea",
		    "target": "Insomnia",
		    "weight": 0.5
		  },
		  {
		    "source": "Dyspnoea",
		    "target": "Irregular breathing",
		    "weight": 0.5
		  },
		  {
		    "source": "Dyspnoea",
		    "target": "Nausea",
		    "weight": 0.0833
		  },
		  {
		    "source": "Dyspnoea",
		    "target": "Oedema",
		    "weight": 0.1
		  },
		  {
		    "source": "Dyspnoea",
		    "target": "Oesophagitis",
		    "weight": 0.0833
		  },
		  {
		    "source": "Dyspnoea",
		    "target": "Oxygen saturation decreased",
		    "weight": 0.1
		  },
		  {
		    "source": "Dyspnoea",
		    "target": "Peripheral swelling",
		    "weight": 0.1
		  },
		  {
		    "source": "Dyspnoea",
		    "target": "Pulmonary arterial hypertension",
		    "weight": 0.1
		  },
		  {
		    "source": "Dyspnoea",
		    "target": "Pyrexia",
		    "weight": 0.0833
		  },
		  {
		    "source": "Dyspnoea",
		    "target": "Respiratory failure",
		    "weight": 0.1
		  },
		  {
		    "source": "Dyspnoea",
		    "target": "Right ventricular failure",
		    "weight": 0.1
		  },
		  {
		    "source": "Dyspnoea",
		    "target": "Seizure",
		    "weight": 0.0833
		  },
		  {
		    "source": "Dyspnoea",
		    "target": "Syncope",
		    "weight": 0.0833
		  },
		  {
		    "source": "Dyspnoea",
		    "target": "Unevaluable event",
		    "weight": 0.0833
		  },
		  {
		    "source": "Dysuria",
		    "target": "Headache",
		    "weight": 0.2
		  },
		  {
		    "source": "Dysuria",
		    "target": "Migraine",
		    "weight": 0.2
		  },
		  {
		    "source": "Dysuria",
		    "target": "Vision blurred",
		    "weight": 0.2
		  },
		  {
		    "source": "Dysuria",
		    "target": "Visual acuity reduced",
		    "weight": 0.2
		  },
		  {
		    "source": "Educational problem",
		    "target": "Emotional disorder",
		    "weight": 0.1429
		  },
		  {
		    "source": "Educational problem",
		    "target": "Family stress",
		    "weight": 0.3333
		  },
		  {
		    "source": "Educational problem",
		    "target": "Feeling abnormal",
		    "weight": 0.25
		  },
		  {
		    "source": "Educational problem",
		    "target": "Infection",
		    "weight": 0.1429
		  },
		  {
		    "source": "Educational problem",
		    "target": "Mood swings",
		    "weight": 0.1667
		  },
		  {
		    "source": "Educational problem",
		    "target": "Product quality issue",
		    "weight": 0.6429
		  },
		  {
		    "source": "Educational problem",
		    "target": "Suicidal ideation",
		    "weight": 0.25
		  },
		  {
		    "source": "Educational problem",
		    "target": "Urinary incontinence",
		    "weight": 0.1667
		  },
		  {
		    "source": "Emotional disorder",
		    "target": "Feeling abnormal",
		    "weight": 0.125
		  },
		  {
		    "source": "Emotional disorder",
		    "target": "Gynaecomastia",
		    "weight": 0.2
		  },
		  {
		    "source": "Emotional disorder",
		    "target": "Infection",
		    "weight": 0.1429
		  },
		  {
		    "source": "Emotional disorder",
		    "target": "Insomnia",
		    "weight": 0.25
		  },
		  {
		    "source": "Emotional disorder",
		    "target": "Lethargy",
		    "weight": 0.125
		  },
		  {
		    "source": "Emotional disorder",
		    "target": "Off label use",
		    "weight": 0.2
		  },
		  {
		    "source": "Emotional disorder",
		    "target": "Product quality issue",
		    "weight": 0.2679
		  },
		  {
		    "source": "Emotional disorder",
		    "target": "Product use issue",
		    "weight": 0.2
		  },
		  {
		    "source": "Emotional disorder",
		    "target": "Psychiatric symptom",
		    "weight": 0.125
		  },
		  {
		    "source": "Emotional disorder",
		    "target": "Self injurious behaviour",
		    "weight": 0.1429
		  },
		  {
		    "source": "Emotional disorder",
		    "target": "Suicidal ideation",
		    "weight": 0.1429
		  },
		  {
		    "source": "Emotional disorder",
		    "target": "Weight increased",
		    "weight": 0.2
		  },
		  {
		    "source": "Emotional disorder",
		    "target": "Wrong technique in product usage process",
		    "weight": 0.125
		  },
		  {
		    "source": "Emotional distress",
		    "target": "Frustration",
		    "weight": 0.0769
		  },
		  {
		    "source": "Emotional distress",
		    "target": "General physical health deterioration",
		    "weight": 0.0769
		  },
		  {
		    "source": "Emotional distress",
		    "target": "Genital haemorrhage",
		    "weight": 0.0769
		  },
		  {
		    "source": "Emotional distress",
		    "target": "Injury",
		    "weight": 0.0769
		  },
		  {
		    "source": "Emotional distress",
		    "target": "Medical device discomfort",
		    "weight": 0.0769
		  },
		  {
		    "source": "Emotional distress",
		    "target": "Medical device pain",
		    "weight": 0.0769
		  },
		  {
		    "source": "Emotional distress",
		    "target": "Post procedural discomfort",
		    "weight": 0.0769
		  },
		  {
		    "source": "Emotional distress",
		    "target": "Procedural pain",
		    "weight": 0.0769
		  },
		  {
		    "source": "Emotional distress",
		    "target": "Uterine perforation",
		    "weight": 0.0769
		  },
		  {
		    "source": "Eosinophilic oesophagitis",
		    "target": "Feeling abnormal",
		    "weight": 0.0667
		  },
		  {
		    "source": "Eosinophilic oesophagitis",
		    "target": "Growth accelerated",
		    "weight": 0.0667
		  },
		  {
		    "source": "Eosinophilic oesophagitis",
		    "target": "Haemorrhoids",
		    "weight": 0.0667
		  },
		  {
		    "source": "Eosinophilic oesophagitis",
		    "target": "Hepatic enzyme increased",
		    "weight": 0.0667
		  },
		  {
		    "source": "Eosinophilic oesophagitis",
		    "target": "Lactose intolerance",
		    "weight": 0.0667
		  },
		  {
		    "source": "Eosinophilic oesophagitis",
		    "target": "Logorrhoea",
		    "weight": 0.0667
		  },
		  {
		    "source": "Eosinophilic oesophagitis",
		    "target": "Weight decreased",
		    "weight": 0.0667
		  },
		  {
		    "source": "Epistaxis",
		    "target": "Fatigue",
		    "weight": 0.0526
		  },
		  {
		    "source": "Epistaxis",
		    "target": "Flat affect",
		    "weight": 0.0556
		  },
		  {
		    "source": "Epistaxis",
		    "target": "Gait disturbance",
		    "weight": 0.0526
		  },
		  {
		    "source": "Epistaxis",
		    "target": "Headache",
		    "weight": 0.0556
		  },
		  {
		    "source": "Epistaxis",
		    "target": "Heart rate decreased",
		    "weight": 0.0526
		  },
		  {
		    "source": "Epistaxis",
		    "target": "Hypotension",
		    "weight": 0.0526
		  },
		  {
		    "source": "Epistaxis",
		    "target": "Impaired healing",
		    "weight": 0.0526
		  },
		  {
		    "source": "Epistaxis",
		    "target": "Insomnia",
		    "weight": 0.1082
		  },
		  {
		    "source": "Epistaxis",
		    "target": "Invasive ductal breast carcinoma",
		    "weight": 0.0526
		  },
		  {
		    "source": "Epistaxis",
		    "target": "Irritability",
		    "weight": 0.0556
		  },
		  {
		    "source": "Epistaxis",
		    "target": "Nausea",
		    "weight": 0.0556
		  },
		  {
		    "source": "Epistaxis",
		    "target": "Obsessive thoughts",
		    "weight": 0.0556
		  },
		  {
		    "source": "Epistaxis",
		    "target": "Pneumonia",
		    "weight": 0.0526
		  },
		  {
		    "source": "Epistaxis",
		    "target": "Rash pruritic",
		    "weight": 0.0526
		  },
		  {
		    "source": "Epistaxis",
		    "target": "Rash pustular",
		    "weight": 0.0526
		  },
		  {
		    "source": "Epistaxis",
		    "target": "Skin mass",
		    "weight": 0.0526
		  },
		  {
		    "source": "Epistaxis",
		    "target": "Social avoidant behaviour",
		    "weight": 0.0556
		  },
		  {
		    "source": "Epistaxis",
		    "target": "Therapy cessation",
		    "weight": 0.0526
		  },
		  {
		    "source": "Epistaxis",
		    "target": "Tic",
		    "weight": 0.0556
		  },
		  {
		    "source": "Epistaxis",
		    "target": "Urinary hesitation",
		    "weight": 0.0526
		  },
		  {
		    "source": "Epistaxis",
		    "target": "Urinary retention",
		    "weight": 0.0526
		  },
		  {
		    "source": "Epistaxis",
		    "target": "Vertigo",
		    "weight": 0.0526
		  },
		  {
		    "source": "Epistaxis",
		    "target": "Vomiting",
		    "weight": 0.0556
		  },
		  {
		    "source": "Erythema",
		    "target": "Hypoaesthesia",
		    "weight": 0.2
		  },
		  {
		    "source": "Erythema",
		    "target": "Paraesthesia",
		    "weight": 0.2
		  },
		  {
		    "source": "Erythema",
		    "target": "Skin discolouration",
		    "weight": 0.2
		  },
		  {
		    "source": "Erythema",
		    "target": "Yellow skin",
		    "weight": 0.2
		  },
		  {
		    "source": "Euphoric mood",
		    "target": "Impulsive behaviour",
		    "weight": 0.1667
		  },
		  {
		    "source": "Euphoric mood",
		    "target": "Logorrhoea",
		    "weight": 0.1667
		  },
		  {
		    "source": "Euphoric mood",
		    "target": "Mania",
		    "weight": 0.1667
		  },
		  {
		    "source": "Euphoric mood",
		    "target": "Thinking abnormal",
		    "weight": 0.1667
		  },
		  {
		    "source": "Eye irritation",
		    "target": "Fatigue",
		    "weight": 0.0455
		  },
		  {
		    "source": "Eye irritation",
		    "target": "Fear",
		    "weight": 0.0455
		  },
		  {
		    "source": "Eye irritation",
		    "target": "Headache",
		    "weight": 0.0455
		  },
		  {
		    "source": "Eye irritation",
		    "target": "Hypersomnia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Eye irritation",
		    "target": "Malaise",
		    "weight": 0.0455
		  },
		  {
		    "source": "Eye irritation",
		    "target": "Migraine",
		    "weight": 0.0455
		  },
		  {
		    "source": "Eye irritation",
		    "target": "Nasopharyngitis",
		    "weight": 0.0455
		  },
		  {
		    "source": "Eye irritation",
		    "target": "Social phobia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Eye irritation",
		    "target": "Tachyphrenia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Eye irritation",
		    "target": "Weight increased",
		    "weight": 0.0455
		  },
		  {
		    "source": "Eye movement disorder",
		    "target": "Hyperphagia",
		    "weight": 0.0714
		  },
		  {
		    "source": "Eye movement disorder",
		    "target": "Laziness",
		    "weight": 0.0714
		  },
		  {
		    "source": "Eye movement disorder",
		    "target": "Musculoskeletal stiffness",
		    "weight": 0.0714
		  },
		  {
		    "source": "Eye movement disorder",
		    "target": "Social avoidant behaviour",
		    "weight": 0.0714
		  },
		  {
		    "source": "Eye movement disorder",
		    "target": "Thirst",
		    "weight": 0.0714
		  },
		  {
		    "source": "Eye movement disorder",
		    "target": "Victim of abuse",
		    "weight": 0.0714
		  },
		  {
		    "source": "Eye movement disorder",
		    "target": "Victim of sexual abuse",
		    "weight": 0.0714
		  },
		  {
		    "source": "Eye movement disorder",
		    "target": "Weight increased",
		    "weight": 0.0714
		  },
		  {
		    "source": "Eye swelling",
		    "target": "Hypersensitivity",
		    "weight": 0.1429
		  },
		  {
		    "source": "Eye swelling",
		    "target": "Hypoaesthesia oral",
		    "weight": 0.1429
		  },
		  {
		    "source": "Eye swelling",
		    "target": "Lip swelling",
		    "weight": 0.1429
		  },
		  {
		    "source": "Eye swelling",
		    "target": "Neck pain",
		    "weight": 0.1429
		  },
		  {
		    "source": "Eye swelling",
		    "target": "Rash",
		    "weight": 0.1429
		  },
		  {
		    "source": "Faecal incontinence",
		    "target": "Flatulence",
		    "weight": 0.3333
		  },
		  {
		    "source": "Faecal incontinence",
		    "target": "Product use issue",
		    "weight": 0.3333
		  },
		  {
		    "source": "Fall",
		    "target": "Feeling jittery",
		    "weight": 0.1667
		  },
		  {
		    "source": "Fall",
		    "target": "Hospitalisation",
		    "weight": 0.1667
		  },
		  {
		    "source": "Fall",
		    "target": "Impaired driving ability",
		    "weight": 0.1
		  },
		  {
		    "source": "Fall",
		    "target": "Inappropriate schedule of drug administration",
		    "weight": 0.1667
		  },
		  {
		    "source": "Fall",
		    "target": "Insomnia",
		    "weight": 0.2667
		  },
		  {
		    "source": "Fall",
		    "target": "Loss of control of legs",
		    "weight": 0.1
		  },
		  {
		    "source": "Fall",
		    "target": "Memory impairment",
		    "weight": 0.2667
		  },
		  {
		    "source": "Fall",
		    "target": "Mental impairment",
		    "weight": 0.1
		  },
		  {
		    "source": "Fall",
		    "target": "Pain",
		    "weight": 0.2667
		  },
		  {
		    "source": "Fall",
		    "target": "Pain in extremity",
		    "weight": 0.2667
		  },
		  {
		    "source": "Fall",
		    "target": "Prescribed overdose",
		    "weight": 0.1667
		  },
		  {
		    "source": "Fall",
		    "target": "Road traffic accident",
		    "weight": 0.2667
		  },
		  {
		    "source": "Fall",
		    "target": "Seizure",
		    "weight": 0.1667
		  },
		  {
		    "source": "Fatigue",
		    "target": "Fear",
		    "weight": 0.1224
		  },
		  {
		    "source": "Fatigue",
		    "target": "Feeling abnormal",
		    "weight": 0.4857
		  },
		  {
		    "source": "Fatigue",
		    "target": "Feeling of relaxation",
		    "weight": 0.2
		  },
		  {
		    "source": "Fatigue",
		    "target": "Flushing",
		    "weight": 0.1667
		  },
		  {
		    "source": "Fatigue",
		    "target": "Gait disturbance",
		    "weight": 0.0526
		  },
		  {
		    "source": "Fatigue",
		    "target": "General physical health deterioration",
		    "weight": 0.1111
		  },
		  {
		    "source": "Fatigue",
		    "target": "Growing pains",
		    "weight": 0.0769
		  },
		  {
		    "source": "Fatigue",
		    "target": "Headache",
		    "weight": 0.4455
		  },
		  {
		    "source": "Fatigue",
		    "target": "Heart rate decreased",
		    "weight": 0.0526
		  },
		  {
		    "source": "Fatigue",
		    "target": "Hospitalisation",
		    "weight": 0.3333
		  },
		  {
		    "source": "Fatigue",
		    "target": "Hypersensitivity",
		    "weight": 0.0769
		  },
		  {
		    "source": "Fatigue",
		    "target": "Hypersomnia",
		    "weight": 0.1043
		  },
		  {
		    "source": "Fatigue",
		    "target": "Hypoaesthesia",
		    "weight": 0.2778
		  },
		  {
		    "source": "Fatigue",
		    "target": "Hypotension",
		    "weight": 0.0526
		  },
		  {
		    "source": "Fatigue",
		    "target": "Impaired healing",
		    "weight": 0.0526
		  },
		  {
		    "source": "Fatigue",
		    "target": "Impaired work ability",
		    "weight": 0.0588
		  },
		  {
		    "source": "Fatigue",
		    "target": "Inappropriate schedule of drug administration",
		    "weight": 0.125
		  },
		  {
		    "source": "Fatigue",
		    "target": "Incorrect dose administered",
		    "weight": 0.1357
		  },
		  {
		    "source": "Fatigue",
		    "target": "Increased appetite",
		    "weight": 0.0769
		  },
		  {
		    "source": "Fatigue",
		    "target": "Influenza like illness",
		    "weight": 0.3333
		  },
		  {
		    "source": "Fatigue",
		    "target": "Insomnia",
		    "weight": 0.1296
		  },
		  {
		    "source": "Fatigue",
		    "target": "Intentional self-injury",
		    "weight": 0.1
		  },
		  {
		    "source": "Fatigue",
		    "target": "Invasive ductal breast carcinoma",
		    "weight": 0.0526
		  },
		  {
		    "source": "Fatigue",
		    "target": "Irritable bowel syndrome",
		    "weight": 0.1111
		  },
		  {
		    "source": "Fatigue",
		    "target": "Laziness",
		    "weight": 0.0769
		  },
		  {
		    "source": "Fatigue",
		    "target": "Libido decreased",
		    "weight": 0.0769
		  },
		  {
		    "source": "Fatigue",
		    "target": "Malaise",
		    "weight": 0.3224
		  },
		  {
		    "source": "Fatigue",
		    "target": "Memory impairment",
		    "weight": 0.2667
		  },
		  {
		    "source": "Fatigue",
		    "target": "Mental disorder",
		    "weight": 0.1
		  },
		  {
		    "source": "Fatigue",
		    "target": "Mental impairment",
		    "weight": 0.0588
		  },
		  {
		    "source": "Fatigue",
		    "target": "Migraine",
		    "weight": 0.0455
		  },
		  {
		    "source": "Fatigue",
		    "target": "Mood altered",
		    "weight": 0.1
		  },
		  {
		    "source": "Fatigue",
		    "target": "Mood swings",
		    "weight": 0.2
		  },
		  {
		    "source": "Fatigue",
		    "target": "Movement disorder",
		    "weight": 0.0769
		  },
		  {
		    "source": "Fatigue",
		    "target": "Muscle spasms",
		    "weight": 0.188
		  },
		  {
		    "source": "Fatigue",
		    "target": "Musculoskeletal disorder",
		    "weight": 0.1111
		  },
		  {
		    "source": "Fatigue",
		    "target": "Nasopharyngitis",
		    "weight": 0.1224
		  },
		  {
		    "source": "Fatigue",
		    "target": "Nausea",
		    "weight": 0.3269
		  },
		  {
		    "source": "Fatigue",
		    "target": "Nightmare",
		    "weight": 0.0588
		  },
		  {
		    "source": "Fatigue",
		    "target": "Off label use",
		    "weight": 0.5769
		  },
		  {
		    "source": "Fatigue",
		    "target": "Oral discomfort",
		    "weight": 0.1667
		  },
		  {
		    "source": "Fatigue",
		    "target": "Pain in jaw",
		    "weight": 0.0769
		  },
		  {
		    "source": "Fatigue",
		    "target": "Palpitations",
		    "weight": 0.0769
		  },
		  {
		    "source": "Fatigue",
		    "target": "Pneumonia",
		    "weight": 0.1296
		  },
		  {
		    "source": "Fatigue",
		    "target": "Prescribed overdose",
		    "weight": 0.125
		  },
		  {
		    "source": "Fatigue",
		    "target": "Product quality issue",
		    "weight": 0.5
		  },
		  {
		    "source": "Fatigue",
		    "target": "Product use issue",
		    "weight": 0.125
		  },
		  {
		    "source": "Fatigue",
		    "target": "Psychomotor hyperactivity",
		    "weight": 0.0769
		  },
		  {
		    "source": "Fatigue",
		    "target": "Pyrexia",
		    "weight": 0.2769
		  },
		  {
		    "source": "Fatigue",
		    "target": "Rapid eye movements sleep abnormal",
		    "weight": 0.0588
		  },
		  {
		    "source": "Fatigue",
		    "target": "Rash pruritic",
		    "weight": 0.0526
		  },
		  {
		    "source": "Fatigue",
		    "target": "Rash pustular",
		    "weight": 0.0526
		  },
		  {
		    "source": "Fatigue",
		    "target": "Restlessness",
		    "weight": 0.2769
		  },
		  {
		    "source": "Fatigue",
		    "target": "Road traffic accident",
		    "weight": 0.0588
		  },
		  {
		    "source": "Fatigue",
		    "target": "Skin mass",
		    "weight": 0.0526
		  },
		  {
		    "source": "Fatigue",
		    "target": "Sluggishness",
		    "weight": 0.25
		  },
		  {
		    "source": "Fatigue",
		    "target": "Social phobia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Fatigue",
		    "target": "Somnolence",
		    "weight": 0.0769
		  },
		  {
		    "source": "Fatigue",
		    "target": "Stress",
		    "weight": 0.3333
		  },
		  {
		    "source": "Fatigue",
		    "target": "Syncope",
		    "weight": 0.1111
		  },
		  {
		    "source": "Fatigue",
		    "target": "Tachyphrenia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Fatigue",
		    "target": "Therapeutic response unexpected",
		    "weight": 0.3333
		  },
		  {
		    "source": "Fatigue",
		    "target": "Therapy cessation",
		    "weight": 0.0526
		  },
		  {
		    "source": "Fatigue",
		    "target": "Thirst",
		    "weight": 0.0769
		  },
		  {
		    "source": "Fatigue",
		    "target": "Underweight",
		    "weight": 0.0588
		  },
		  {
		    "source": "Fatigue",
		    "target": "Urinary hesitation",
		    "weight": 0.0526
		  },
		  {
		    "source": "Fatigue",
		    "target": "Urinary retention",
		    "weight": 0.0526
		  },
		  {
		    "source": "Fatigue",
		    "target": "Vertigo",
		    "weight": 0.0526
		  },
		  {
		    "source": "Fatigue",
		    "target": "Vomiting",
		    "weight": 0.3269
		  },
		  {
		    "source": "Fatigue",
		    "target": "Weight increased",
		    "weight": 0.1043
		  },
		  {
		    "source": "Fear",
		    "target": "Headache",
		    "weight": 0.0455
		  },
		  {
		    "source": "Fear",
		    "target": "Hypersomnia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Fear",
		    "target": "Incorrect dose administered",
		    "weight": 0.0769
		  },
		  {
		    "source": "Fear",
		    "target": "Laziness",
		    "weight": 0.0769
		  },
		  {
		    "source": "Fear",
		    "target": "Loss of employment",
		    "weight": 0.25
		  },
		  {
		    "source": "Fear",
		    "target": "Malaise",
		    "weight": 0.1224
		  },
		  {
		    "source": "Fear",
		    "target": "Memory impairment",
		    "weight": 0.2
		  },
		  {
		    "source": "Fear",
		    "target": "Migraine",
		    "weight": 0.0455
		  },
		  {
		    "source": "Fear",
		    "target": "Nasopharyngitis",
		    "weight": 0.0455
		  },
		  {
		    "source": "Fear",
		    "target": "Nervousness",
		    "weight": 0.25
		  },
		  {
		    "source": "Fear",
		    "target": "Panic attack",
		    "weight": 0.25
		  },
		  {
		    "source": "Fear",
		    "target": "Product quality issue",
		    "weight": 0.2
		  },
		  {
		    "source": "Fear",
		    "target": "Psychomotor hyperactivity",
		    "weight": 0.0769
		  },
		  {
		    "source": "Fear",
		    "target": "Social phobia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Fear",
		    "target": "Somnolence",
		    "weight": 0.0769
		  },
		  {
		    "source": "Fear",
		    "target": "Tachyphrenia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Fear",
		    "target": "Weight increased",
		    "weight": 0.0455
		  },
		  {
		    "source": "Feeding disorder",
		    "target": "Gastritis",
		    "weight": 0.0476
		  },
		  {
		    "source": "Feeding disorder",
		    "target": "Increased appetite",
		    "weight": 0.0476
		  },
		  {
		    "source": "Feeding disorder",
		    "target": "Osteoarthritis",
		    "weight": 0.0476
		  },
		  {
		    "source": "Feeding disorder",
		    "target": "Pain",
		    "weight": 0.0476
		  },
		  {
		    "source": "Feeding disorder",
		    "target": "Panic attack",
		    "weight": 0.0476
		  },
		  {
		    "source": "Feeding disorder",
		    "target": "Poor quality sleep",
		    "weight": 0.0476
		  },
		  {
		    "source": "Feeding disorder",
		    "target": "Psychotic disorder",
		    "weight": 0.0476
		  },
		  {
		    "source": "Feeding disorder",
		    "target": "Scar",
		    "weight": 0.0476
		  },
		  {
		    "source": "Feeding disorder",
		    "target": "Tooth infection",
		    "weight": 0.0476
		  },
		  {
		    "source": "Feeding disorder",
		    "target": "Tooth loss",
		    "weight": 0.0476
		  },
		  {
		    "source": "Feeding disorder",
		    "target": "Toothache",
		    "weight": 0.0476
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Feeling of despair",
		    "weight": 0.25
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Foot fracture",
		    "weight": 0.25
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Frustration",
		    "weight": 0.0833
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Growing pains",
		    "weight": 0.0769
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Growth accelerated",
		    "weight": 0.0667
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Haemorrhoids",
		    "weight": 0.0667
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Headache",
		    "weight": 0.1667
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Hepatic enzyme increased",
		    "weight": 0.0667
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Hypersensitivity",
		    "weight": 0.0769
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Hypersomnia",
		    "weight": 0.0588
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Hypothyroidism",
		    "weight": 0.0769
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Impaired work ability",
		    "weight": 0.2255
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Impulsive behaviour",
		    "weight": 0.0833
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Incorrect dose administered",
		    "weight": 0.3857
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Insomnia",
		    "weight": 0.2769
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Intentional self-injury",
		    "weight": 0.1
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Lactose intolerance",
		    "weight": 0.0667
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Laziness",
		    "weight": 0.1111
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Lethargy",
		    "weight": 0.125
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Logorrhoea",
		    "weight": 0.2095
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Malaise",
		    "weight": 0.0769
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Memory impairment",
		    "weight": 0.3778
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Mental disorder",
		    "weight": 0.1
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Mental impairment",
		    "weight": 0.1357
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Mood altered",
		    "weight": 0.35
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Movement disorder",
		    "weight": 0.0769
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Nasopharyngitis",
		    "weight": 0.0769
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Nausea",
		    "weight": 0.0769
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Nightmare",
		    "weight": 0.0588
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Off label use",
		    "weight": 0.0769
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Panic attack",
		    "weight": 0.1111
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Performance status decreased",
		    "weight": 0.0769
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Pneumonia",
		    "weight": 0.0769
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Product quality issue",
		    "weight": 1.6519
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Psychiatric symptom",
		    "weight": 0.125
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Psychomotor hyperactivity",
		    "weight": 0.0833
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Rapid eye movements sleep abnormal",
		    "weight": 0.0588
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Restlessness",
		    "weight": 0.0769
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Road traffic accident",
		    "weight": 0.0588
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Sensory loss",
		    "weight": 0.25
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Somnolence",
		    "weight": 0.5769
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Stereotypy",
		    "weight": 0.3333
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Suicidal ideation",
		    "weight": 0.25
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Thirst",
		    "weight": 0.0769
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Tic",
		    "weight": 0.3333
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Tourette's disorder",
		    "weight": 0.0833
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Tremor",
		    "weight": 0.25
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Underweight",
		    "weight": 0.0588
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Weight decreased",
		    "weight": 0.1778
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Weight increased",
		    "weight": 0.1422
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Wrist fracture",
		    "weight": 0.25
		  },
		  {
		    "source": "Feeling abnormal",
		    "target": "Wrong technique in product usage process",
		    "weight": 0.2019
		  },
		  {
		    "source": "Feeling hot",
		    "target": "Hypoaesthesia",
		    "weight": 0.3333
		  },
		  {
		    "source": "Feeling hot",
		    "target": "Pain in extremity",
		    "weight": 0.3333
		  },
		  {
		    "source": "Feeling jittery",
		    "target": "Hospitalisation",
		    "weight": 0.1667
		  },
		  {
		    "source": "Feeling jittery",
		    "target": "Inappropriate schedule of drug administration",
		    "weight": 0.1667
		  },
		  {
		    "source": "Feeling jittery",
		    "target": "Nervousness",
		    "weight": 0.3333
		  },
		  {
		    "source": "Feeling jittery",
		    "target": "Prescribed overdose",
		    "weight": 0.1667
		  },
		  {
		    "source": "Feeling jittery",
		    "target": "Product quality issue",
		    "weight": 0.1667
		  },
		  {
		    "source": "Feeling jittery",
		    "target": "Seizure",
		    "weight": 0.1667
		  },
		  {
		    "source": "Feeling jittery",
		    "target": "Somnolence",
		    "weight": 0.1667
		  },
		  {
		    "source": "Feeling of despair",
		    "target": "Mood altered",
		    "weight": 0.25
		  },
		  {
		    "source": "Fibromyalgia",
		    "target": "Muscle spasms",
		    "weight": 0.2
		  },
		  {
		    "source": "Fibromyalgia",
		    "target": "Myalgia",
		    "weight": 0.2
		  },
		  {
		    "source": "Fibromyalgia",
		    "target": "Sjogren's syndrome",
		    "weight": 0.2
		  },
		  {
		    "source": "Flat affect",
		    "target": "Headache",
		    "weight": 0.0556
		  },
		  {
		    "source": "Flat affect",
		    "target": "Insomnia",
		    "weight": 0.0556
		  },
		  {
		    "source": "Flat affect",
		    "target": "Irritability",
		    "weight": 0.0556
		  },
		  {
		    "source": "Flat affect",
		    "target": "Loss of consciousness",
		    "weight": 0.3333
		  },
		  {
		    "source": "Flat affect",
		    "target": "Nausea",
		    "weight": 0.0556
		  },
		  {
		    "source": "Flat affect",
		    "target": "Obsessive thoughts",
		    "weight": 0.0556
		  },
		  {
		    "source": "Flat affect",
		    "target": "Social avoidant behaviour",
		    "weight": 0.0556
		  },
		  {
		    "source": "Flat affect",
		    "target": "Tic",
		    "weight": 0.0556
		  },
		  {
		    "source": "Flat affect",
		    "target": "Vomiting",
		    "weight": 0.0556
		  },
		  {
		    "source": "Flatulence",
		    "target": "Product use issue",
		    "weight": 0.3333
		  },
		  {
		    "source": "Flight of ideas",
		    "target": "Initial insomnia",
		    "weight": 0.1111
		  },
		  {
		    "source": "Flight of ideas",
		    "target": "Oral administration complication",
		    "weight": 0.1111
		  },
		  {
		    "source": "Flight of ideas",
		    "target": "Paranoia",
		    "weight": 0.1111
		  },
		  {
		    "source": "Flight of ideas",
		    "target": "Product quality issue",
		    "weight": 0.1111
		  },
		  {
		    "source": "Flight of ideas",
		    "target": "Psychomotor hyperactivity",
		    "weight": 0.1111
		  },
		  {
		    "source": "Flight of ideas",
		    "target": "Restlessness",
		    "weight": 0.1111
		  },
		  {
		    "source": "Fluid overload",
		    "target": "Oedema",
		    "weight": 0.1
		  },
		  {
		    "source": "Fluid overload",
		    "target": "Oxygen saturation decreased",
		    "weight": 0.1
		  },
		  {
		    "source": "Fluid overload",
		    "target": "Peripheral swelling",
		    "weight": 0.1
		  },
		  {
		    "source": "Fluid overload",
		    "target": "Pulmonary arterial hypertension",
		    "weight": 0.1
		  },
		  {
		    "source": "Fluid overload",
		    "target": "Respiratory failure",
		    "weight": 0.1
		  },
		  {
		    "source": "Fluid overload",
		    "target": "Right ventricular failure",
		    "weight": 0.1
		  },
		  {
		    "source": "Flushing",
		    "target": "Gastritis",
		    "weight": 0.25
		  },
		  {
		    "source": "Flushing",
		    "target": "Hyperhidrosis",
		    "weight": 0.25
		  },
		  {
		    "source": "Flushing",
		    "target": "Hypoaesthesia",
		    "weight": 0.1667
		  },
		  {
		    "source": "Flushing",
		    "target": "Memory impairment",
		    "weight": 0.1667
		  },
		  {
		    "source": "Flushing",
		    "target": "Multiple sclerosis",
		    "weight": 0.25
		  },
		  {
		    "source": "Flushing",
		    "target": "Oral discomfort",
		    "weight": 0.1667
		  },
		  {
		    "source": "Flushing",
		    "target": "Palpitations",
		    "weight": 0.25
		  },
		  {
		    "source": "Flushing",
		    "target": "Product use issue",
		    "weight": 0.25
		  },
		  {
		    "source": "Foetal distress syndrome",
		    "target": "Foetal exposure during pregnancy",
		    "weight": 0.1667
		  },
		  {
		    "source": "Foetal distress syndrome",
		    "target": "Jaundice neonatal",
		    "weight": 0.1667
		  },
		  {
		    "source": "Foetal distress syndrome",
		    "target": "Premature baby",
		    "weight": 0.1667
		  },
		  {
		    "source": "Foetal exposure during pregnancy",
		    "target": "Jaundice neonatal",
		    "weight": 0.1667
		  },
		  {
		    "source": "Foetal exposure during pregnancy",
		    "target": "Premature baby",
		    "weight": 0.1667
		  },
		  {
		    "source": "Food craving",
		    "target": "Product use issue",
		    "weight": 0.5
		  },
		  {
		    "source": "Food hoarding",
		    "target": "Increased appetite",
		    "weight": 0.2
		  },
		  {
		    "source": "Food hoarding",
		    "target": "Weight increased",
		    "weight": 0.2
		  },
		  {
		    "source": "Foot fracture",
		    "target": "Wrist fracture",
		    "weight": 0.25
		  },
		  {
		    "source": "Foot operation",
		    "target": "Inappropriate schedule of drug administration",
		    "weight": 0.125
		  },
		  {
		    "source": "Foot operation",
		    "target": "Intervertebral disc protrusion",
		    "weight": 0.125
		  },
		  {
		    "source": "Foot operation",
		    "target": "Knee operation",
		    "weight": 0.125
		  },
		  {
		    "source": "Foot operation",
		    "target": "Limb injury",
		    "weight": 0.125
		  },
		  {
		    "source": "Foot operation",
		    "target": "Pain",
		    "weight": 0.125
		  },
		  {
		    "source": "Foot operation",
		    "target": "Product use issue",
		    "weight": 0.125
		  },
		  {
		    "source": "Foreign body",
		    "target": "Legal problem",
		    "weight": 0.3333
		  },
		  {
		    "source": "Foreign body",
		    "target": "Wrong technique in product usage process",
		    "weight": 0.3333
		  },
		  {
		    "source": "Formication",
		    "target": "Hostility",
		    "weight": 0.0833
		  },
		  {
		    "source": "Formication",
		    "target": "Irritability",
		    "weight": 0.0833
		  },
		  {
		    "source": "Formication",
		    "target": "Malabsorption",
		    "weight": 0.0833
		  },
		  {
		    "source": "Formication",
		    "target": "Mood swings",
		    "weight": 0.0833
		  },
		  {
		    "source": "Formication",
		    "target": "Muscle twitching",
		    "weight": 0.1
		  },
		  {
		    "source": "Formication",
		    "target": "Myalgia",
		    "weight": 0.1
		  },
		  {
		    "source": "Formication",
		    "target": "Screaming",
		    "weight": 0.1
		  },
		  {
		    "source": "Formication",
		    "target": "Tremor",
		    "weight": 0.1
		  },
		  {
		    "source": "Formication",
		    "target": "Vitamin D abnormal",
		    "weight": 0.0833
		  },
		  {
		    "source": "Formication",
		    "target": "Vitreous floaters",
		    "weight": 0.0833
		  },
		  {
		    "source": "Formication",
		    "target": "Wrong technique in product usage process",
		    "weight": 0.1
		  },
		  {
		    "source": "Frustration",
		    "target": "General physical health deterioration",
		    "weight": 0.0769
		  },
		  {
		    "source": "Frustration",
		    "target": "Genital haemorrhage",
		    "weight": 0.0769
		  },
		  {
		    "source": "Frustration",
		    "target": "Impulsive behaviour",
		    "weight": 0.0833
		  },
		  {
		    "source": "Frustration",
		    "target": "Injury",
		    "weight": 0.0769
		  },
		  {
		    "source": "Frustration",
		    "target": "Medical device discomfort",
		    "weight": 0.0769
		  },
		  {
		    "source": "Frustration",
		    "target": "Medical device pain",
		    "weight": 0.0769
		  },
		  {
		    "source": "Frustration",
		    "target": "Post procedural discomfort",
		    "weight": 0.0769
		  },
		  {
		    "source": "Frustration",
		    "target": "Procedural pain",
		    "weight": 0.0769
		  },
		  {
		    "source": "Frustration",
		    "target": "Psychomotor hyperactivity",
		    "weight": 0.0833
		  },
		  {
		    "source": "Frustration",
		    "target": "Tourette's disorder",
		    "weight": 0.0833
		  },
		  {
		    "source": "Frustration",
		    "target": "Uterine perforation",
		    "weight": 0.0769
		  },
		  {
		    "source": "Frustration",
		    "target": "Weight increased",
		    "weight": 0.0833
		  },
		  {
		    "source": "Fungal infection",
		    "target": "Hormone level abnormal",
		    "weight": 0.0909
		  },
		  {
		    "source": "Fungal infection",
		    "target": "Vaginal discharge",
		    "weight": 0.0909
		  },
		  {
		    "source": "Fungal infection",
		    "target": "Vaginal pH increased",
		    "weight": 0.0909
		  },
		  {
		    "source": "Fungal infection",
		    "target": "Vulvovaginal dryness",
		    "weight": 0.0909
		  },
		  {
		    "source": "Fungal infection",
		    "target": "Vulvovaginal erythema",
		    "weight": 0.0909
		  },
		  {
		    "source": "Fungal infection",
		    "target": "Vulvovaginal pain",
		    "weight": 0.0909
		  },
		  {
		    "source": "Fungal infection",
		    "target": "Vulvovaginal swelling",
		    "weight": 0.0909
		  },
		  {
		    "source": "Gait disturbance",
		    "target": "Heart rate decreased",
		    "weight": 0.0526
		  },
		  {
		    "source": "Gait disturbance",
		    "target": "Hypotension",
		    "weight": 0.0526
		  },
		  {
		    "source": "Gait disturbance",
		    "target": "Impaired healing",
		    "weight": 0.0526
		  },
		  {
		    "source": "Gait disturbance",
		    "target": "Insomnia",
		    "weight": 0.0526
		  },
		  {
		    "source": "Gait disturbance",
		    "target": "Invasive ductal breast carcinoma",
		    "weight": 0.0526
		  },
		  {
		    "source": "Gait disturbance",
		    "target": "Pneumonia",
		    "weight": 0.0526
		  },
		  {
		    "source": "Gait disturbance",
		    "target": "Rash pruritic",
		    "weight": 0.0526
		  },
		  {
		    "source": "Gait disturbance",
		    "target": "Rash pustular",
		    "weight": 0.0526
		  },
		  {
		    "source": "Gait disturbance",
		    "target": "Skin mass",
		    "weight": 0.0526
		  },
		  {
		    "source": "Gait disturbance",
		    "target": "Therapy cessation",
		    "weight": 0.0526
		  },
		  {
		    "source": "Gait disturbance",
		    "target": "Urinary hesitation",
		    "weight": 0.0526
		  },
		  {
		    "source": "Gait disturbance",
		    "target": "Urinary retention",
		    "weight": 0.0526
		  },
		  {
		    "source": "Gait disturbance",
		    "target": "Vertigo",
		    "weight": 0.0526
		  },
		  {
		    "source": "Gastritis",
		    "target": "Hyperhidrosis",
		    "weight": 0.25
		  },
		  {
		    "source": "Gastritis",
		    "target": "Increased appetite",
		    "weight": 0.0476
		  },
		  {
		    "source": "Gastritis",
		    "target": "Osteoarthritis",
		    "weight": 0.0476
		  },
		  {
		    "source": "Gastritis",
		    "target": "Pain",
		    "weight": 0.0476
		  },
		  {
		    "source": "Gastritis",
		    "target": "Panic attack",
		    "weight": 0.0476
		  },
		  {
		    "source": "Gastritis",
		    "target": "Poor quality sleep",
		    "weight": 0.0476
		  },
		  {
		    "source": "Gastritis",
		    "target": "Psychotic disorder",
		    "weight": 0.0476
		  },
		  {
		    "source": "Gastritis",
		    "target": "Scar",
		    "weight": 0.0476
		  },
		  {
		    "source": "Gastritis",
		    "target": "Tooth infection",
		    "weight": 0.0476
		  },
		  {
		    "source": "Gastritis",
		    "target": "Tooth loss",
		    "weight": 0.0476
		  },
		  {
		    "source": "Gastritis",
		    "target": "Toothache",
		    "weight": 0.0476
		  },
		  {
		    "source": "Gastroenteritis viral",
		    "target": "Headache",
		    "weight": 0.2
		  },
		  {
		    "source": "Gastroenteritis viral",
		    "target": "Malaise",
		    "weight": 0.1
		  },
		  {
		    "source": "Gastroenteritis viral",
		    "target": "Paranasal sinus hypersecretion",
		    "weight": 0.1
		  },
		  {
		    "source": "Gastroenteritis viral",
		    "target": "Pharyngitis streptococcal",
		    "weight": 0.1
		  },
		  {
		    "source": "Gastroenteritis viral",
		    "target": "Pyrexia",
		    "weight": 0.1
		  },
		  {
		    "source": "Gastroenteritis viral",
		    "target": "Rales",
		    "weight": 0.1
		  },
		  {
		    "source": "Gastroenteritis viral",
		    "target": "Upper respiratory tract infection",
		    "weight": 0.1
		  },
		  {
		    "source": "Gastroenteritis viral",
		    "target": "Vomiting",
		    "weight": 0.1
		  },
		  {
		    "source": "Gastrointestinal stenosis",
		    "target": "Injection site pain",
		    "weight": 0.1667
		  },
		  {
		    "source": "Gastrointestinal stenosis",
		    "target": "Intestinal polyp",
		    "weight": 0.1667
		  },
		  {
		    "source": "Gastrointestinal stenosis",
		    "target": "Large intestinal stenosis",
		    "weight": 0.1667
		  },
		  {
		    "source": "Gastrointestinal stenosis",
		    "target": "Nasopharyngitis",
		    "weight": 0.1667
		  },
		  {
		    "source": "Gastrooesophageal reflux disease",
		    "target": "Grief reaction",
		    "weight": 0.0769
		  },
		  {
		    "source": "Gastrooesophageal reflux disease",
		    "target": "Heart rate irregular",
		    "weight": 0.2
		  },
		  {
		    "source": "Gastrooesophageal reflux disease",
		    "target": "Nausea",
		    "weight": 0.0769
		  },
		  {
		    "source": "Gastrooesophageal reflux disease",
		    "target": "Oedema peripheral",
		    "weight": 0.0769
		  },
		  {
		    "source": "Gastrooesophageal reflux disease",
		    "target": "Pleural effusion",
		    "weight": 0.0769
		  },
		  {
		    "source": "Gastrooesophageal reflux disease",
		    "target": "Severe acute respiratory syndrome",
		    "weight": 0.0769
		  },
		  {
		    "source": "Gastrooesophageal reflux disease",
		    "target": "Stress",
		    "weight": 0.0769
		  },
		  {
		    "source": "Gastrooesophageal reflux disease",
		    "target": "Tearfulness",
		    "weight": 0.0769
		  },
		  {
		    "source": "Gastrooesophageal reflux disease",
		    "target": "Viral infection",
		    "weight": 0.0769
		  },
		  {
		    "source": "Gastrooesophageal reflux disease",
		    "target": "Vomiting",
		    "weight": 0.0769
		  },
		  {
		    "source": "General physical health deterioration",
		    "target": "Genital haemorrhage",
		    "weight": 0.0769
		  },
		  {
		    "source": "General physical health deterioration",
		    "target": "Hypoaesthesia",
		    "weight": 0.1111
		  },
		  {
		    "source": "General physical health deterioration",
		    "target": "Injury",
		    "weight": 0.0769
		  },
		  {
		    "source": "General physical health deterioration",
		    "target": "Irritable bowel syndrome",
		    "weight": 0.1111
		  },
		  {
		    "source": "General physical health deterioration",
		    "target": "Medical device discomfort",
		    "weight": 0.0769
		  },
		  {
		    "source": "General physical health deterioration",
		    "target": "Medical device pain",
		    "weight": 0.0769
		  },
		  {
		    "source": "General physical health deterioration",
		    "target": "Muscle spasms",
		    "weight": 0.1111
		  },
		  {
		    "source": "General physical health deterioration",
		    "target": "Musculoskeletal disorder",
		    "weight": 0.1111
		  },
		  {
		    "source": "General physical health deterioration",
		    "target": "Post procedural discomfort",
		    "weight": 0.0769
		  },
		  {
		    "source": "General physical health deterioration",
		    "target": "Procedural pain",
		    "weight": 0.0769
		  },
		  {
		    "source": "General physical health deterioration",
		    "target": "Syncope",
		    "weight": 0.1111
		  },
		  {
		    "source": "General physical health deterioration",
		    "target": "Uterine perforation",
		    "weight": 0.0769
		  },
		  {
		    "source": "Genital haemorrhage",
		    "target": "Injury",
		    "weight": 0.0769
		  },
		  {
		    "source": "Genital haemorrhage",
		    "target": "Medical device discomfort",
		    "weight": 0.0769
		  },
		  {
		    "source": "Genital haemorrhage",
		    "target": "Medical device pain",
		    "weight": 0.0769
		  },
		  {
		    "source": "Genital haemorrhage",
		    "target": "Post procedural discomfort",
		    "weight": 0.0769
		  },
		  {
		    "source": "Genital haemorrhage",
		    "target": "Procedural pain",
		    "weight": 0.0769
		  },
		  {
		    "source": "Genital haemorrhage",
		    "target": "Uterine perforation",
		    "weight": 0.0769
		  },
		  {
		    "source": "Glucose tolerance impaired",
		    "target": "Stress urinary incontinence",
		    "weight": 0.5
		  },
		  {
		    "source": "Grief reaction",
		    "target": "Nausea",
		    "weight": 0.0769
		  },
		  {
		    "source": "Grief reaction",
		    "target": "Oedema peripheral",
		    "weight": 0.0769
		  },
		  {
		    "source": "Grief reaction",
		    "target": "Pleural effusion",
		    "weight": 0.0769
		  },
		  {
		    "source": "Grief reaction",
		    "target": "Severe acute respiratory syndrome",
		    "weight": 0.0769
		  },
		  {
		    "source": "Grief reaction",
		    "target": "Stress",
		    "weight": 0.0769
		  },
		  {
		    "source": "Grief reaction",
		    "target": "Tearfulness",
		    "weight": 0.0769
		  },
		  {
		    "source": "Grief reaction",
		    "target": "Viral infection",
		    "weight": 0.0769
		  },
		  {
		    "source": "Grief reaction",
		    "target": "Vomiting",
		    "weight": 0.0769
		  },
		  {
		    "source": "Growing pains",
		    "target": "Hypersensitivity",
		    "weight": 0.0769
		  },
		  {
		    "source": "Growing pains",
		    "target": "Insomnia",
		    "weight": 0.0769
		  },
		  {
		    "source": "Growing pains",
		    "target": "Movement disorder",
		    "weight": 0.0769
		  },
		  {
		    "source": "Growing pains",
		    "target": "Nasopharyngitis",
		    "weight": 0.0769
		  },
		  {
		    "source": "Growing pains",
		    "target": "Off label use",
		    "weight": 0.0769
		  },
		  {
		    "source": "Growing pains",
		    "target": "Pneumonia",
		    "weight": 0.0769
		  },
		  {
		    "source": "Growing pains",
		    "target": "Restlessness",
		    "weight": 0.0769
		  },
		  {
		    "source": "Growing pains",
		    "target": "Thirst",
		    "weight": 0.0769
		  },
		  {
		    "source": "Growth accelerated",
		    "target": "Haemorrhoids",
		    "weight": 0.0667
		  },
		  {
		    "source": "Growth accelerated",
		    "target": "Hepatic enzyme increased",
		    "weight": 0.0667
		  },
		  {
		    "source": "Growth accelerated",
		    "target": "Lactose intolerance",
		    "weight": 0.0667
		  },
		  {
		    "source": "Growth accelerated",
		    "target": "Logorrhoea",
		    "weight": 0.0667
		  },
		  {
		    "source": "Growth accelerated",
		    "target": "Weight decreased",
		    "weight": 0.0667
		  },
		  {
		    "source": "Gynaecomastia",
		    "target": "Off label use",
		    "weight": 0.2
		  },
		  {
		    "source": "Gynaecomastia",
		    "target": "Product use issue",
		    "weight": 0.2
		  },
		  {
		    "source": "Gynaecomastia",
		    "target": "Weight increased",
		    "weight": 0.2
		  },
		  {
		    "source": "Haemorrhagic diathesis",
		    "target": "Pain",
		    "weight": 0.25
		  },
		  {
		    "source": "Haemorrhoids",
		    "target": "Hepatic enzyme increased",
		    "weight": 0.0667
		  },
		  {
		    "source": "Haemorrhoids",
		    "target": "Lactose intolerance",
		    "weight": 0.0667
		  },
		  {
		    "source": "Haemorrhoids",
		    "target": "Logorrhoea",
		    "weight": 0.0667
		  },
		  {
		    "source": "Haemorrhoids",
		    "target": "Weight decreased",
		    "weight": 0.0667
		  },
		  {
		    "source": "Hair colour changes",
		    "target": "Hair texture abnormal",
		    "weight": 0.3333
		  },
		  {
		    "source": "Hallucination",
		    "target": "Product use issue",
		    "weight": 0.5
		  },
		  {
		    "source": "Hallucinations, mixed",
		    "target": "Incoherent",
		    "weight": 0.0833
		  },
		  {
		    "source": "Hallucinations, mixed",
		    "target": "Nausea",
		    "weight": 0.0833
		  },
		  {
		    "source": "Hallucinations, mixed",
		    "target": "Oesophagitis",
		    "weight": 0.0833
		  },
		  {
		    "source": "Hallucinations, mixed",
		    "target": "Pyrexia",
		    "weight": 0.0833
		  },
		  {
		    "source": "Hallucinations, mixed",
		    "target": "Seizure",
		    "weight": 0.0833
		  },
		  {
		    "source": "Hallucinations, mixed",
		    "target": "Syncope",
		    "weight": 0.0833
		  },
		  {
		    "source": "Hallucinations, mixed",
		    "target": "Unevaluable event",
		    "weight": 0.0833
		  },
		  {
		    "source": "Hangover",
		    "target": "Psychomotor hyperactivity",
		    "weight": 0.5
		  },
		  {
		    "source": "Headache",
		    "target": "Hunger",
		    "weight": 0.2
		  },
		  {
		    "source": "Headache",
		    "target": "Hypersomnia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Headache",
		    "target": "Insomnia",
		    "weight": 0.5472
		  },
		  {
		    "source": "Headache",
		    "target": "Irritability",
		    "weight": 0.0556
		  },
		  {
		    "source": "Headache",
		    "target": "Loss of consciousness",
		    "weight": 0.2
		  },
		  {
		    "source": "Headache",
		    "target": "Malaise",
		    "weight": 0.0455
		  },
		  {
		    "source": "Headache",
		    "target": "Memory impairment",
		    "weight": 0.1667
		  },
		  {
		    "source": "Headache",
		    "target": "Migraine",
		    "weight": 0.2455
		  },
		  {
		    "source": "Headache",
		    "target": "Mood swings",
		    "weight": 0.2
		  },
		  {
		    "source": "Headache",
		    "target": "Nasal discomfort",
		    "weight": 0.2
		  },
		  {
		    "source": "Headache",
		    "target": "Nasopharyngitis",
		    "weight": 0.0455
		  },
		  {
		    "source": "Headache",
		    "target": "Nausea",
		    "weight": 0.6722
		  },
		  {
		    "source": "Headache",
		    "target": "Obsessive thoughts",
		    "weight": 0.0556
		  },
		  {
		    "source": "Headache",
		    "target": "Pain in extremity",
		    "weight": 0.25
		  },
		  {
		    "source": "Headache",
		    "target": "Paraesthesia",
		    "weight": 0.3333
		  },
		  {
		    "source": "Headache",
		    "target": "Performance status decreased",
		    "weight": 0.125
		  },
		  {
		    "source": "Headache",
		    "target": "Post-traumatic neck syndrome",
		    "weight": 0.2
		  },
		  {
		    "source": "Headache",
		    "target": "Prescribed overdose",
		    "weight": 0.125
		  },
		  {
		    "source": "Headache",
		    "target": "Product quality issue",
		    "weight": 0.5417
		  },
		  {
		    "source": "Headache",
		    "target": "Pyrexia",
		    "weight": 0.2
		  },
		  {
		    "source": "Headache",
		    "target": "Restlessness",
		    "weight": 0.2
		  },
		  {
		    "source": "Headache",
		    "target": "Rhinalgia",
		    "weight": 0.2
		  },
		  {
		    "source": "Headache",
		    "target": "Road traffic accident",
		    "weight": 0.2
		  },
		  {
		    "source": "Headache",
		    "target": "Sinus headache",
		    "weight": 0.2
		  },
		  {
		    "source": "Headache",
		    "target": "Social avoidant behaviour",
		    "weight": 0.0556
		  },
		  {
		    "source": "Headache",
		    "target": "Social phobia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Headache",
		    "target": "Tachyphrenia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Headache",
		    "target": "Therapeutic response unexpected",
		    "weight": 0.25
		  },
		  {
		    "source": "Headache",
		    "target": "Therapy cessation",
		    "weight": 0.125
		  },
		  {
		    "source": "Headache",
		    "target": "Tic",
		    "weight": 0.0556
		  },
		  {
		    "source": "Headache",
		    "target": "Vision blurred",
		    "weight": 0.2
		  },
		  {
		    "source": "Headache",
		    "target": "Visual acuity reduced",
		    "weight": 0.2
		  },
		  {
		    "source": "Headache",
		    "target": "Vitamin D deficiency",
		    "weight": 0.25
		  },
		  {
		    "source": "Headache",
		    "target": "Vomiting",
		    "weight": 0.0556
		  },
		  {
		    "source": "Headache",
		    "target": "Weight decreased",
		    "weight": 0.1667
		  },
		  {
		    "source": "Headache",
		    "target": "Weight increased",
		    "weight": 0.0455
		  },
		  {
		    "source": "Heart rate decreased",
		    "target": "Hypotension",
		    "weight": 0.0526
		  },
		  {
		    "source": "Heart rate decreased",
		    "target": "Impaired healing",
		    "weight": 0.0526
		  },
		  {
		    "source": "Heart rate decreased",
		    "target": "Insomnia",
		    "weight": 0.0526
		  },
		  {
		    "source": "Heart rate decreased",
		    "target": "Invasive ductal breast carcinoma",
		    "weight": 0.0526
		  },
		  {
		    "source": "Heart rate decreased",
		    "target": "Pneumonia",
		    "weight": 0.0526
		  },
		  {
		    "source": "Heart rate decreased",
		    "target": "Rash pruritic",
		    "weight": 0.0526
		  },
		  {
		    "source": "Heart rate decreased",
		    "target": "Rash pustular",
		    "weight": 0.0526
		  },
		  {
		    "source": "Heart rate decreased",
		    "target": "Skin mass",
		    "weight": 0.0526
		  },
		  {
		    "source": "Heart rate decreased",
		    "target": "Therapy cessation",
		    "weight": 0.0526
		  },
		  {
		    "source": "Heart rate decreased",
		    "target": "Urinary hesitation",
		    "weight": 0.0526
		  },
		  {
		    "source": "Heart rate decreased",
		    "target": "Urinary retention",
		    "weight": 0.0526
		  },
		  {
		    "source": "Heart rate decreased",
		    "target": "Vertigo",
		    "weight": 0.0526
		  },
		  {
		    "source": "Heart rate increased",
		    "target": "Insomnia",
		    "weight": 0.2
		  },
		  {
		    "source": "Heart rate increased",
		    "target": "Seizure",
		    "weight": 0.2
		  },
		  {
		    "source": "Hepatic enzyme increased",
		    "target": "Lactose intolerance",
		    "weight": 0.0667
		  },
		  {
		    "source": "Hepatic enzyme increased",
		    "target": "Lipids increased",
		    "weight": 0.25
		  },
		  {
		    "source": "Hepatic enzyme increased",
		    "target": "Logorrhoea",
		    "weight": 0.0667
		  },
		  {
		    "source": "Hepatic enzyme increased",
		    "target": "Urinary tract infection",
		    "weight": 0.25
		  },
		  {
		    "source": "Hepatic enzyme increased",
		    "target": "Weight decreased",
		    "weight": 0.0667
		  },
		  {
		    "source": "Hernia",
		    "target": "Implant tissue necrosis",
		    "weight": 0.5
		  },
		  {
		    "source": "Hormone level abnormal",
		    "target": "Vaginal discharge",
		    "weight": 0.0909
		  },
		  {
		    "source": "Hormone level abnormal",
		    "target": "Vaginal pH increased",
		    "weight": 0.0909
		  },
		  {
		    "source": "Hormone level abnormal",
		    "target": "Vulvovaginal dryness",
		    "weight": 0.0909
		  },
		  {
		    "source": "Hormone level abnormal",
		    "target": "Vulvovaginal erythema",
		    "weight": 0.0909
		  },
		  {
		    "source": "Hormone level abnormal",
		    "target": "Vulvovaginal pain",
		    "weight": 0.0909
		  },
		  {
		    "source": "Hormone level abnormal",
		    "target": "Vulvovaginal swelling",
		    "weight": 0.0909
		  },
		  {
		    "source": "Hospitalisation",
		    "target": "Inappropriate schedule of drug administration",
		    "weight": 0.1667
		  },
		  {
		    "source": "Hospitalisation",
		    "target": "Narcolepsy",
		    "weight": 0.3333
		  },
		  {
		    "source": "Hospitalisation",
		    "target": "Prescribed overdose",
		    "weight": 0.1667
		  },
		  {
		    "source": "Hospitalisation",
		    "target": "Seizure",
		    "weight": 0.5
		  },
		  {
		    "source": "Hospitalisation",
		    "target": "Withdrawal syndrome",
		    "weight": 0.5
		  },
		  {
		    "source": "Hostility",
		    "target": "Increased appetite",
		    "weight": 0.0833
		  },
		  {
		    "source": "Hostility",
		    "target": "Irritability",
		    "weight": 0.0833
		  },
		  {
		    "source": "Hostility",
		    "target": "Malabsorption",
		    "weight": 0.0833
		  },
		  {
		    "source": "Hostility",
		    "target": "Mania",
		    "weight": 0.0833
		  },
		  {
		    "source": "Hostility",
		    "target": "Mood swings",
		    "weight": 0.0833
		  },
		  {
		    "source": "Hostility",
		    "target": "Optic nerve neoplasm",
		    "weight": 0.0833
		  },
		  {
		    "source": "Hostility",
		    "target": "Somnolence",
		    "weight": 0.0833
		  },
		  {
		    "source": "Hostility",
		    "target": "Vitamin D abnormal",
		    "weight": 0.0833
		  },
		  {
		    "source": "Hostility",
		    "target": "Vitreous floaters",
		    "weight": 0.0833
		  },
		  {
		    "source": "Hunger",
		    "target": "Insomnia",
		    "weight": 0.2
		  },
		  {
		    "source": "Hunger",
		    "target": "Nausea",
		    "weight": 0.2
		  },
		  {
		    "source": "Hunger",
		    "target": "Restlessness",
		    "weight": 0.25
		  },
		  {
		    "source": "Hyperhidrosis",
		    "target": "Muscle spasms",
		    "weight": 0.1
		  },
		  {
		    "source": "Hyperhidrosis",
		    "target": "Mydriasis",
		    "weight": 0.1
		  },
		  {
		    "source": "Hyperhidrosis",
		    "target": "Serotonin syndrome",
		    "weight": 0.1
		  },
		  {
		    "source": "Hyperhidrosis",
		    "target": "Tachyphrenia",
		    "weight": 0.1
		  },
		  {
		    "source": "Hyperphagia",
		    "target": "Laziness",
		    "weight": 0.0714
		  },
		  {
		    "source": "Hyperphagia",
		    "target": "Musculoskeletal stiffness",
		    "weight": 0.0714
		  },
		  {
		    "source": "Hyperphagia",
		    "target": "Social avoidant behaviour",
		    "weight": 0.0714
		  },
		  {
		    "source": "Hyperphagia",
		    "target": "Thirst",
		    "weight": 0.0714
		  },
		  {
		    "source": "Hyperphagia",
		    "target": "Victim of abuse",
		    "weight": 0.0714
		  },
		  {
		    "source": "Hyperphagia",
		    "target": "Victim of sexual abuse",
		    "weight": 0.0714
		  },
		  {
		    "source": "Hyperphagia",
		    "target": "Weight increased",
		    "weight": 0.0714
		  },
		  {
		    "source": "Hypersensitivity",
		    "target": "Hypoaesthesia oral",
		    "weight": 0.1429
		  },
		  {
		    "source": "Hypersensitivity",
		    "target": "Insomnia",
		    "weight": 0.0769
		  },
		  {
		    "source": "Hypersensitivity",
		    "target": "Lip swelling",
		    "weight": 0.1429
		  },
		  {
		    "source": "Hypersensitivity",
		    "target": "Movement disorder",
		    "weight": 0.0769
		  },
		  {
		    "source": "Hypersensitivity",
		    "target": "Nasopharyngitis",
		    "weight": 0.0769
		  },
		  {
		    "source": "Hypersensitivity",
		    "target": "Neck pain",
		    "weight": 0.1429
		  },
		  {
		    "source": "Hypersensitivity",
		    "target": "Off label use",
		    "weight": 0.0769
		  },
		  {
		    "source": "Hypersensitivity",
		    "target": "Pneumonia",
		    "weight": 0.0769
		  },
		  {
		    "source": "Hypersensitivity",
		    "target": "Rash",
		    "weight": 0.1429
		  },
		  {
		    "source": "Hypersensitivity",
		    "target": "Rash macular",
		    "weight": 0.5
		  },
		  {
		    "source": "Hypersensitivity",
		    "target": "Restlessness",
		    "weight": 0.0769
		  },
		  {
		    "source": "Hypersensitivity",
		    "target": "Swollen tongue",
		    "weight": 0.5
		  },
		  {
		    "source": "Hypersensitivity",
		    "target": "Thirst",
		    "weight": 0.0769
		  },
		  {
		    "source": "Hypersomnia",
		    "target": "Impaired work ability",
		    "weight": 0.0588
		  },
		  {
		    "source": "Hypersomnia",
		    "target": "Incorrect dose administered",
		    "weight": 0.0588
		  },
		  {
		    "source": "Hypersomnia",
		    "target": "Malaise",
		    "weight": 0.0455
		  },
		  {
		    "source": "Hypersomnia",
		    "target": "Mental impairment",
		    "weight": 0.0588
		  },
		  {
		    "source": "Hypersomnia",
		    "target": "Migraine",
		    "weight": 0.0455
		  },
		  {
		    "source": "Hypersomnia",
		    "target": "Nasopharyngitis",
		    "weight": 0.0455
		  },
		  {
		    "source": "Hypersomnia",
		    "target": "Nightmare",
		    "weight": 0.0588
		  },
		  {
		    "source": "Hypersomnia",
		    "target": "Rapid eye movements sleep abnormal",
		    "weight": 0.0588
		  },
		  {
		    "source": "Hypersomnia",
		    "target": "Road traffic accident",
		    "weight": 0.0588
		  },
		  {
		    "source": "Hypersomnia",
		    "target": "Social phobia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Hypersomnia",
		    "target": "Tachyphrenia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Hypersomnia",
		    "target": "Underweight",
		    "weight": 0.0588
		  },
		  {
		    "source": "Hypersomnia",
		    "target": "Weight increased",
		    "weight": 0.1043
		  },
		  {
		    "source": "Hypertension",
		    "target": "Pain in extremity",
		    "weight": 0.2
		  },
		  {
		    "source": "Hypertension",
		    "target": "Product use issue",
		    "weight": 0.3333
		  },
		  {
		    "source": "Hyperventilation",
		    "target": "Retching",
		    "weight": 0.2
		  },
		  {
		    "source": "Hyperventilation",
		    "target": "Trismus",
		    "weight": 0.2
		  },
		  {
		    "source": "Hyperventilation",
		    "target": "Vomiting",
		    "weight": 0.2
		  },
		  {
		    "source": "Hypoaesthesia",
		    "target": "Hypoaesthesia oral",
		    "weight": 0.25
		  },
		  {
		    "source": "Hypoaesthesia",
		    "target": "Intervertebral disc protrusion",
		    "weight": 0.0714
		  },
		  {
		    "source": "Hypoaesthesia",
		    "target": "Irritable bowel syndrome",
		    "weight": 0.1111
		  },
		  {
		    "source": "Hypoaesthesia",
		    "target": "Loss of consciousness",
		    "weight": 0.0714
		  },
		  {
		    "source": "Hypoaesthesia",
		    "target": "Memory impairment",
		    "weight": 0.1667
		  },
		  {
		    "source": "Hypoaesthesia",
		    "target": "Muscle spasms",
		    "weight": 0.1111
		  },
		  {
		    "source": "Hypoaesthesia",
		    "target": "Musculoskeletal disorder",
		    "weight": 0.1111
		  },
		  {
		    "source": "Hypoaesthesia",
		    "target": "Nerve injury",
		    "weight": 0.0714
		  },
		  {
		    "source": "Hypoaesthesia",
		    "target": "Nonspecific reaction",
		    "weight": 0.0714
		  },
		  {
		    "source": "Hypoaesthesia",
		    "target": "Oral discomfort",
		    "weight": 0.1667
		  },
		  {
		    "source": "Hypoaesthesia",
		    "target": "Pain",
		    "weight": 0.0714
		  },
		  {
		    "source": "Hypoaesthesia",
		    "target": "Pain in extremity",
		    "weight": 0.3333
		  },
		  {
		    "source": "Hypoaesthesia",
		    "target": "Paraesthesia",
		    "weight": 0.5214
		  },
		  {
		    "source": "Hypoaesthesia",
		    "target": "Paraesthesia oral",
		    "weight": 0.25
		  },
		  {
		    "source": "Hypoaesthesia",
		    "target": "Product use issue",
		    "weight": 0.0714
		  },
		  {
		    "source": "Hypoaesthesia",
		    "target": "Radiculitis brachial",
		    "weight": 0.0714
		  },
		  {
		    "source": "Hypoaesthesia",
		    "target": "Skin discolouration",
		    "weight": 0.2
		  },
		  {
		    "source": "Hypoaesthesia",
		    "target": "Sleep disorder",
		    "weight": 0.0714
		  },
		  {
		    "source": "Hypoaesthesia",
		    "target": "Syncope",
		    "weight": 0.1111
		  },
		  {
		    "source": "Hypoaesthesia",
		    "target": "Therapeutic response unexpected",
		    "weight": 0.0714
		  },
		  {
		    "source": "Hypoaesthesia",
		    "target": "Thoracic outlet syndrome",
		    "weight": 0.0714
		  },
		  {
		    "source": "Hypoaesthesia",
		    "target": "Yellow skin",
		    "weight": 0.2
		  },
		  {
		    "source": "Hypoaesthesia oral",
		    "target": "Lip swelling",
		    "weight": 0.1429
		  },
		  {
		    "source": "Hypoaesthesia oral",
		    "target": "Neck pain",
		    "weight": 0.1429
		  },
		  {
		    "source": "Hypoaesthesia oral",
		    "target": "Paraesthesia",
		    "weight": 0.25
		  },
		  {
		    "source": "Hypoaesthesia oral",
		    "target": "Paraesthesia oral",
		    "weight": 0.25
		  },
		  {
		    "source": "Hypoaesthesia oral",
		    "target": "Rash",
		    "weight": 0.1429
		  },
		  {
		    "source": "Hypokinesia",
		    "target": "Musculoskeletal stiffness",
		    "weight": 0.3333
		  },
		  {
		    "source": "Hypokinesia",
		    "target": "Tremor",
		    "weight": 0.3333
		  },
		  {
		    "source": "Hypophagia",
		    "target": "Logorrhoea",
		    "weight": 0.5
		  },
		  {
		    "source": "Hypotension",
		    "target": "Impaired healing",
		    "weight": 0.0526
		  },
		  {
		    "source": "Hypotension",
		    "target": "Insomnia",
		    "weight": 0.0526
		  },
		  {
		    "source": "Hypotension",
		    "target": "Invasive ductal breast carcinoma",
		    "weight": 0.0526
		  },
		  {
		    "source": "Hypotension",
		    "target": "Pneumonia",
		    "weight": 0.0526
		  },
		  {
		    "source": "Hypotension",
		    "target": "Rash pruritic",
		    "weight": 0.0526
		  },
		  {
		    "source": "Hypotension",
		    "target": "Rash pustular",
		    "weight": 0.0526
		  },
		  {
		    "source": "Hypotension",
		    "target": "Skin mass",
		    "weight": 0.0526
		  },
		  {
		    "source": "Hypotension",
		    "target": "Therapy cessation",
		    "weight": 0.0526
		  },
		  {
		    "source": "Hypotension",
		    "target": "Urinary hesitation",
		    "weight": 0.0526
		  },
		  {
		    "source": "Hypotension",
		    "target": "Urinary retention",
		    "weight": 0.0526
		  },
		  {
		    "source": "Hypotension",
		    "target": "Vertigo",
		    "weight": 0.0526
		  },
		  {
		    "source": "Hypothyroidism",
		    "target": "Incorrect dose administered",
		    "weight": 0.0769
		  },
		  {
		    "source": "Hypothyroidism",
		    "target": "Malaise",
		    "weight": 0.0769
		  },
		  {
		    "source": "Hypothyroidism",
		    "target": "Mental impairment",
		    "weight": 0.0769
		  },
		  {
		    "source": "Hypothyroidism",
		    "target": "Nausea",
		    "weight": 0.0769
		  },
		  {
		    "source": "Hypothyroidism",
		    "target": "Performance status decreased",
		    "weight": 0.0769
		  },
		  {
		    "source": "Hypothyroidism",
		    "target": "Product quality issue",
		    "weight": 0.0769
		  },
		  {
		    "source": "Hypothyroidism",
		    "target": "Somnolence",
		    "weight": 0.0769
		  },
		  {
		    "source": "Hypothyroidism",
		    "target": "Wrong technique in product usage process",
		    "weight": 0.0769
		  },
		  {
		    "source": "Impaired driving ability",
		    "target": "Insomnia",
		    "weight": 0.1
		  },
		  {
		    "source": "Impaired driving ability",
		    "target": "Loss of control of legs",
		    "weight": 0.1
		  },
		  {
		    "source": "Impaired driving ability",
		    "target": "Memory impairment",
		    "weight": 0.1
		  },
		  {
		    "source": "Impaired driving ability",
		    "target": "Mental impairment",
		    "weight": 0.1
		  },
		  {
		    "source": "Impaired driving ability",
		    "target": "Pain",
		    "weight": 0.1
		  },
		  {
		    "source": "Impaired driving ability",
		    "target": "Pain in extremity",
		    "weight": 0.1
		  },
		  {
		    "source": "Impaired driving ability",
		    "target": "Road traffic accident",
		    "weight": 0.1
		  },
		  {
		    "source": "Impaired healing",
		    "target": "Insomnia",
		    "weight": 0.0526
		  },
		  {
		    "source": "Impaired healing",
		    "target": "Invasive ductal breast carcinoma",
		    "weight": 0.0526
		  },
		  {
		    "source": "Impaired healing",
		    "target": "Pneumonia",
		    "weight": 0.0526
		  },
		  {
		    "source": "Impaired healing",
		    "target": "Rash pruritic",
		    "weight": 0.0526
		  },
		  {
		    "source": "Impaired healing",
		    "target": "Rash pustular",
		    "weight": 0.0526
		  },
		  {
		    "source": "Impaired healing",
		    "target": "Skin mass",
		    "weight": 0.0526
		  },
		  {
		    "source": "Impaired healing",
		    "target": "Therapy cessation",
		    "weight": 0.0526
		  },
		  {
		    "source": "Impaired healing",
		    "target": "Urinary hesitation",
		    "weight": 0.0526
		  },
		  {
		    "source": "Impaired healing",
		    "target": "Urinary retention",
		    "weight": 0.0526
		  },
		  {
		    "source": "Impaired healing",
		    "target": "Vertigo",
		    "weight": 0.0526
		  },
		  {
		    "source": "Impaired work ability",
		    "target": "Incorrect dose administered",
		    "weight": 0.0588
		  },
		  {
		    "source": "Impaired work ability",
		    "target": "Mental impairment",
		    "weight": 0.0588
		  },
		  {
		    "source": "Impaired work ability",
		    "target": "Musculoskeletal pain",
		    "weight": 0.1429
		  },
		  {
		    "source": "Impaired work ability",
		    "target": "Neck pain",
		    "weight": 0.1429
		  },
		  {
		    "source": "Impaired work ability",
		    "target": "Nightmare",
		    "weight": 0.0588
		  },
		  {
		    "source": "Impaired work ability",
		    "target": "Pain",
		    "weight": 0.1429
		  },
		  {
		    "source": "Impaired work ability",
		    "target": "Product substitution issue",
		    "weight": 0.1429
		  },
		  {
		    "source": "Impaired work ability",
		    "target": "Rapid eye movements sleep abnormal",
		    "weight": 0.0588
		  },
		  {
		    "source": "Impaired work ability",
		    "target": "Road traffic accident",
		    "weight": 0.0588
		  },
		  {
		    "source": "Impaired work ability",
		    "target": "Underweight",
		    "weight": 0.0588
		  },
		  {
		    "source": "Impaired work ability",
		    "target": "Weight increased",
		    "weight": 0.0588
		  },
		  {
		    "source": "Impulse-control disorder",
		    "target": "Product substitution issue",
		    "weight": 0.3333
		  },
		  {
		    "source": "Impulsive behaviour",
		    "target": "Logorrhoea",
		    "weight": 0.1667
		  },
		  {
		    "source": "Impulsive behaviour",
		    "target": "Mania",
		    "weight": 0.1667
		  },
		  {
		    "source": "Impulsive behaviour",
		    "target": "Psychomotor hyperactivity",
		    "weight": 0.0833
		  },
		  {
		    "source": "Impulsive behaviour",
		    "target": "Restlessness",
		    "weight": 0.25
		  },
		  {
		    "source": "Impulsive behaviour",
		    "target": "Sleep disorder",
		    "weight": 0.25
		  },
		  {
		    "source": "Impulsive behaviour",
		    "target": "Thinking abnormal",
		    "weight": 0.1667
		  },
		  {
		    "source": "Impulsive behaviour",
		    "target": "Tourette's disorder",
		    "weight": 0.0833
		  },
		  {
		    "source": "Impulsive behaviour",
		    "target": "Weight increased",
		    "weight": 0.0833
		  },
		  {
		    "source": "Inappropriate schedule of drug administration",
		    "target": "Incorrect dose administered",
		    "weight": 0.0909
		  },
		  {
		    "source": "Inappropriate schedule of drug administration",
		    "target": "Increased appetite",
		    "weight": 0.25
		  },
		  {
		    "source": "Inappropriate schedule of drug administration",
		    "target": "Insomnia",
		    "weight": 0.5833
		  },
		  {
		    "source": "Inappropriate schedule of drug administration",
		    "target": "Intentional overdose",
		    "weight": 0.25
		  },
		  {
		    "source": "Inappropriate schedule of drug administration",
		    "target": "Intervertebral disc protrusion",
		    "weight": 0.125
		  },
		  {
		    "source": "Inappropriate schedule of drug administration",
		    "target": "Knee operation",
		    "weight": 0.125
		  },
		  {
		    "source": "Inappropriate schedule of drug administration",
		    "target": "Libido decreased",
		    "weight": 0.2
		  },
		  {
		    "source": "Inappropriate schedule of drug administration",
		    "target": "Limb injury",
		    "weight": 0.125
		  },
		  {
		    "source": "Inappropriate schedule of drug administration",
		    "target": "No adverse event",
		    "weight": 2.75
		  },
		  {
		    "source": "Inappropriate schedule of drug administration",
		    "target": "Overdose",
		    "weight": 0.25
		  },
		  {
		    "source": "Inappropriate schedule of drug administration",
		    "target": "Pain",
		    "weight": 0.125
		  },
		  {
		    "source": "Inappropriate schedule of drug administration",
		    "target": "Paranoia",
		    "weight": 0.25
		  },
		  {
		    "source": "Inappropriate schedule of drug administration",
		    "target": "Performance status decreased",
		    "weight": 0.25
		  },
		  {
		    "source": "Inappropriate schedule of drug administration",
		    "target": "Prescribed overdose",
		    "weight": 3.0417
		  },
		  {
		    "source": "Inappropriate schedule of drug administration",
		    "target": "Product quality issue",
		    "weight": 1.0076
		  },
		  {
		    "source": "Inappropriate schedule of drug administration",
		    "target": "Product use issue",
		    "weight": 0.25
		  },
		  {
		    "source": "Inappropriate schedule of drug administration",
		    "target": "Psychomotor hyperactivity",
		    "weight": 0.5
		  },
		  {
		    "source": "Inappropriate schedule of drug administration",
		    "target": "Psychotic disorder",
		    "weight": 0.25
		  },
		  {
		    "source": "Inappropriate schedule of drug administration",
		    "target": "Seizure",
		    "weight": 0.6667
		  },
		  {
		    "source": "Inappropriate schedule of drug administration",
		    "target": "Somnolence",
		    "weight": 0.2909
		  },
		  {
		    "source": "Inappropriate schedule of drug administration",
		    "target": "Stress",
		    "weight": 0.0909
		  },
		  {
		    "source": "Inappropriate schedule of drug administration",
		    "target": "Tachyphrenia",
		    "weight": 0.2
		  },
		  {
		    "source": "Inappropriate schedule of drug administration",
		    "target": "Tension",
		    "weight": 0.2
		  },
		  {
		    "source": "Inappropriate schedule of drug administration",
		    "target": "Vaginal haemorrhage",
		    "weight": 0.5
		  },
		  {
		    "source": "Inappropriate schedule of drug administration",
		    "target": "Weight increased",
		    "weight": 0.25
		  },
		  {
		    "source": "Inappropriate schedule of drug administration",
		    "target": "Withdrawal syndrome",
		    "weight": 0.1667
		  },
		  {
		    "source": "Inappropriate schedule of drug administration",
		    "target": "Wrong technique in product usage process",
		    "weight": 0.3409
		  },
		  {
		    "source": "Inappropriate schedule of drug administration",
		    "target": "Yawning",
		    "weight": 0.0909
		  },
		  {
		    "source": "Incoherent",
		    "target": "Nausea",
		    "weight": 0.0833
		  },
		  {
		    "source": "Incoherent",
		    "target": "Oesophagitis",
		    "weight": 0.0833
		  },
		  {
		    "source": "Incoherent",
		    "target": "Pyrexia",
		    "weight": 0.0833
		  },
		  {
		    "source": "Incoherent",
		    "target": "Seizure",
		    "weight": 0.0833
		  },
		  {
		    "source": "Incoherent",
		    "target": "Syncope",
		    "weight": 0.0833
		  },
		  {
		    "source": "Incoherent",
		    "target": "Unevaluable event",
		    "weight": 0.0833
		  },
		  {
		    "source": "Incorrect dose administered",
		    "target": "Insomnia",
		    "weight": 0.3333
		  },
		  {
		    "source": "Incorrect dose administered",
		    "target": "Laziness",
		    "weight": 0.0769
		  },
		  {
		    "source": "Incorrect dose administered",
		    "target": "Malaise",
		    "weight": 0.1538
		  },
		  {
		    "source": "Incorrect dose administered",
		    "target": "Mental impairment",
		    "weight": 0.1357
		  },
		  {
		    "source": "Incorrect dose administered",
		    "target": "Nausea",
		    "weight": 0.0769
		  },
		  {
		    "source": "Incorrect dose administered",
		    "target": "Nightmare",
		    "weight": 0.0588
		  },
		  {
		    "source": "Incorrect dose administered",
		    "target": "No adverse event",
		    "weight": 0.3333
		  },
		  {
		    "source": "Incorrect dose administered",
		    "target": "Performance status decreased",
		    "weight": 0.3269
		  },
		  {
		    "source": "Incorrect dose administered",
		    "target": "Product quality issue",
		    "weight": 1.3345
		  },
		  {
		    "source": "Incorrect dose administered",
		    "target": "Psychomotor hyperactivity",
		    "weight": 0.0769
		  },
		  {
		    "source": "Incorrect dose administered",
		    "target": "Rapid eye movements sleep abnormal",
		    "weight": 0.0588
		  },
		  {
		    "source": "Incorrect dose administered",
		    "target": "Road traffic accident",
		    "weight": 0.0588
		  },
		  {
		    "source": "Incorrect dose administered",
		    "target": "Sensory loss",
		    "weight": 0.25
		  },
		  {
		    "source": "Incorrect dose administered",
		    "target": "Somnolence",
		    "weight": 0.2448
		  },
		  {
		    "source": "Incorrect dose administered",
		    "target": "Stress",
		    "weight": 0.0909
		  },
		  {
		    "source": "Incorrect dose administered",
		    "target": "Tremor",
		    "weight": 0.25
		  },
		  {
		    "source": "Incorrect dose administered",
		    "target": "Underdose",
		    "weight": 0.25
		  },
		  {
		    "source": "Incorrect dose administered",
		    "target": "Underweight",
		    "weight": 0.0588
		  },
		  {
		    "source": "Incorrect dose administered",
		    "target": "Weight increased",
		    "weight": 0.0588
		  },
		  {
		    "source": "Incorrect dose administered",
		    "target": "Wrong technique in product usage process",
		    "weight": 1.0012
		  },
		  {
		    "source": "Incorrect dose administered",
		    "target": "Yawning",
		    "weight": 0.0909
		  },
		  {
		    "source": "Increased appetite",
		    "target": "Lethargy",
		    "weight": 0.1667
		  },
		  {
		    "source": "Increased appetite",
		    "target": "Libido decreased",
		    "weight": 0.0769
		  },
		  {
		    "source": "Increased appetite",
		    "target": "Mania",
		    "weight": 0.0833
		  },
		  {
		    "source": "Increased appetite",
		    "target": "Muscle spasms",
		    "weight": 0.0769
		  },
		  {
		    "source": "Increased appetite",
		    "target": "Nausea",
		    "weight": 0.0769
		  },
		  {
		    "source": "Increased appetite",
		    "target": "Optic nerve neoplasm",
		    "weight": 0.0833
		  },
		  {
		    "source": "Increased appetite",
		    "target": "Osteoarthritis",
		    "weight": 0.0476
		  },
		  {
		    "source": "Increased appetite",
		    "target": "Overdose",
		    "weight": 0.25
		  },
		  {
		    "source": "Increased appetite",
		    "target": "Pain",
		    "weight": 0.0476
		  },
		  {
		    "source": "Increased appetite",
		    "target": "Pain in jaw",
		    "weight": 0.0769
		  },
		  {
		    "source": "Increased appetite",
		    "target": "Palpitations",
		    "weight": 0.0769
		  },
		  {
		    "source": "Increased appetite",
		    "target": "Panic attack",
		    "weight": 0.0476
		  },
		  {
		    "source": "Increased appetite",
		    "target": "Personality change",
		    "weight": 0.25
		  },
		  {
		    "source": "Increased appetite",
		    "target": "Poor quality sleep",
		    "weight": 0.0476
		  },
		  {
		    "source": "Increased appetite",
		    "target": "Psychotic disorder",
		    "weight": 0.0476
		  },
		  {
		    "source": "Increased appetite",
		    "target": "Pyrexia",
		    "weight": 0.0769
		  },
		  {
		    "source": "Increased appetite",
		    "target": "Rebound effect",
		    "weight": 0.1667
		  },
		  {
		    "source": "Increased appetite",
		    "target": "Scar",
		    "weight": 0.0476
		  },
		  {
		    "source": "Increased appetite",
		    "target": "Somnolence",
		    "weight": 0.25
		  },
		  {
		    "source": "Increased appetite",
		    "target": "Tooth infection",
		    "weight": 0.0476
		  },
		  {
		    "source": "Increased appetite",
		    "target": "Tooth loss",
		    "weight": 0.0476
		  },
		  {
		    "source": "Increased appetite",
		    "target": "Toothache",
		    "weight": 0.0476
		  },
		  {
		    "source": "Increased appetite",
		    "target": "Vomiting",
		    "weight": 0.0769
		  },
		  {
		    "source": "Increased appetite",
		    "target": "Weight increased",
		    "weight": 0.45
		  },
		  {
		    "source": "Infection",
		    "target": "Product quality issue",
		    "weight": 0.1429
		  },
		  {
		    "source": "Infusion related reaction",
		    "target": "Weight increased",
		    "weight": 0.1667
		  },
		  {
		    "source": "Initial insomnia",
		    "target": "Oral administration complication",
		    "weight": 0.1111
		  },
		  {
		    "source": "Initial insomnia",
		    "target": "Paranoia",
		    "weight": 0.1111
		  },
		  {
		    "source": "Initial insomnia",
		    "target": "Product quality issue",
		    "weight": 0.1111
		  },
		  {
		    "source": "Initial insomnia",
		    "target": "Psychomotor hyperactivity",
		    "weight": 0.1111
		  },
		  {
		    "source": "Initial insomnia",
		    "target": "Restlessness",
		    "weight": 0.1111
		  },
		  {
		    "source": "Injection site bruising",
		    "target": "Injection site pain",
		    "weight": 0.25
		  },
		  {
		    "source": "Injection site bruising",
		    "target": "Injection site reaction",
		    "weight": 0.25
		  },
		  {
		    "source": "Injection site bruising",
		    "target": "Injection site swelling",
		    "weight": 0.25
		  },
		  {
		    "source": "Injection site pain",
		    "target": "Injection site reaction",
		    "weight": 0.25
		  },
		  {
		    "source": "Injection site pain",
		    "target": "Injection site swelling",
		    "weight": 0.25
		  },
		  {
		    "source": "Injection site pain",
		    "target": "Intestinal polyp",
		    "weight": 0.1667
		  },
		  {
		    "source": "Injection site pain",
		    "target": "Large intestinal stenosis",
		    "weight": 0.1667
		  },
		  {
		    "source": "Injection site pain",
		    "target": "Nasopharyngitis",
		    "weight": 0.1667
		  },
		  {
		    "source": "Injection site reaction",
		    "target": "Injection site swelling",
		    "weight": 0.25
		  },
		  {
		    "source": "Injury",
		    "target": "Insomnia",
		    "weight": 0.125
		  },
		  {
		    "source": "Injury",
		    "target": "Medical device discomfort",
		    "weight": 0.0769
		  },
		  {
		    "source": "Injury",
		    "target": "Medical device pain",
		    "weight": 0.0769
		  },
		  {
		    "source": "Injury",
		    "target": "Mental disorder",
		    "weight": 0.125
		  },
		  {
		    "source": "Injury",
		    "target": "Neuralgia",
		    "weight": 0.2
		  },
		  {
		    "source": "Injury",
		    "target": "Pain",
		    "weight": 0.125
		  },
		  {
		    "source": "Injury",
		    "target": "Post procedural discomfort",
		    "weight": 0.0769
		  },
		  {
		    "source": "Injury",
		    "target": "Procedural pain",
		    "weight": 0.0769
		  },
		  {
		    "source": "Injury",
		    "target": "Pulmonary embolism",
		    "weight": 0.125
		  },
		  {
		    "source": "Injury",
		    "target": "Road traffic accident",
		    "weight": 0.2
		  },
		  {
		    "source": "Injury",
		    "target": "Unevaluable event",
		    "weight": 0.2
		  },
		  {
		    "source": "Injury",
		    "target": "Uterine perforation",
		    "weight": 0.0769
		  },
		  {
		    "source": "Insomnia",
		    "target": "Invasive ductal breast carcinoma",
		    "weight": 0.0526
		  },
		  {
		    "source": "Insomnia",
		    "target": "Irritability",
		    "weight": 0.0556
		  },
		  {
		    "source": "Insomnia",
		    "target": "Loss of control of legs",
		    "weight": 0.1
		  },
		  {
		    "source": "Insomnia",
		    "target": "Malaise",
		    "weight": 0.1667
		  },
		  {
		    "source": "Insomnia",
		    "target": "Memory impairment",
		    "weight": 0.2667
		  },
		  {
		    "source": "Insomnia",
		    "target": "Mental disorder",
		    "weight": 0.125
		  },
		  {
		    "source": "Insomnia",
		    "target": "Mental impairment",
		    "weight": 0.1
		  },
		  {
		    "source": "Insomnia",
		    "target": "Motor dysfunction",
		    "weight": 0.125
		  },
		  {
		    "source": "Insomnia",
		    "target": "Movement disorder",
		    "weight": 0.0769
		  },
		  {
		    "source": "Insomnia",
		    "target": "Myoclonic epilepsy",
		    "weight": 0.125
		  },
		  {
		    "source": "Insomnia",
		    "target": "Nasopharyngitis",
		    "weight": 0.0769
		  },
		  {
		    "source": "Insomnia",
		    "target": "Nausea",
		    "weight": 0.4222
		  },
		  {
		    "source": "Insomnia",
		    "target": "Nightmare",
		    "weight": 0.1667
		  },
		  {
		    "source": "Insomnia",
		    "target": "No therapeutic response",
		    "weight": 0.1
		  },
		  {
		    "source": "Insomnia",
		    "target": "Obsessive thoughts",
		    "weight": 0.0556
		  },
		  {
		    "source": "Insomnia",
		    "target": "Off label use",
		    "weight": 0.4103
		  },
		  {
		    "source": "Insomnia",
		    "target": "Pain",
		    "weight": 0.3917
		  },
		  {
		    "source": "Insomnia",
		    "target": "Pain in extremity",
		    "weight": 0.3667
		  },
		  {
		    "source": "Insomnia",
		    "target": "Panic disorder",
		    "weight": 0.125
		  },
		  {
		    "source": "Insomnia",
		    "target": "Paraesthesia",
		    "weight": 0.1
		  },
		  {
		    "source": "Insomnia",
		    "target": "Pneumonia",
		    "weight": 0.1296
		  },
		  {
		    "source": "Insomnia",
		    "target": "Product quality issue",
		    "weight": 0.325
		  },
		  {
		    "source": "Insomnia",
		    "target": "Product substitution issue",
		    "weight": 0.1
		  },
		  {
		    "source": "Insomnia",
		    "target": "Pulmonary embolism",
		    "weight": 0.125
		  },
		  {
		    "source": "Insomnia",
		    "target": "Rash pruritic",
		    "weight": 0.0526
		  },
		  {
		    "source": "Insomnia",
		    "target": "Rash pustular",
		    "weight": 0.0526
		  },
		  {
		    "source": "Insomnia",
		    "target": "Restlessness",
		    "weight": 0.0769
		  },
		  {
		    "source": "Insomnia",
		    "target": "Road traffic accident",
		    "weight": 0.2667
		  },
		  {
		    "source": "Insomnia",
		    "target": "Seizure",
		    "weight": 0.2
		  },
		  {
		    "source": "Insomnia",
		    "target": "Self-injurious ideation",
		    "weight": 0.1667
		  },
		  {
		    "source": "Insomnia",
		    "target": "Sexual dysfunction",
		    "weight": 0.5
		  },
		  {
		    "source": "Insomnia",
		    "target": "Skin mass",
		    "weight": 0.0526
		  },
		  {
		    "source": "Insomnia",
		    "target": "Social avoidant behaviour",
		    "weight": 0.0556
		  },
		  {
		    "source": "Insomnia",
		    "target": "Somnolence",
		    "weight": 0.5
		  },
		  {
		    "source": "Insomnia",
		    "target": "Therapy cessation",
		    "weight": 0.0526
		  },
		  {
		    "source": "Insomnia",
		    "target": "Thinking abnormal",
		    "weight": 0.125
		  },
		  {
		    "source": "Insomnia",
		    "target": "Thirst",
		    "weight": 0.0769
		  },
		  {
		    "source": "Insomnia",
		    "target": "Tic",
		    "weight": 0.0556
		  },
		  {
		    "source": "Insomnia",
		    "target": "Tremor",
		    "weight": 0.5
		  },
		  {
		    "source": "Insomnia",
		    "target": "Urinary hesitation",
		    "weight": 0.0526
		  },
		  {
		    "source": "Insomnia",
		    "target": "Urinary retention",
		    "weight": 0.0526
		  },
		  {
		    "source": "Insomnia",
		    "target": "Vertigo",
		    "weight": 0.1526
		  },
		  {
		    "source": "Insomnia",
		    "target": "Vomiting",
		    "weight": 0.0556
		  },
		  {
		    "source": "Insomnia",
		    "target": "Weight decreased",
		    "weight": 0.1667
		  },
		  {
		    "source": "Insomnia",
		    "target": "Wrong technique in product usage process",
		    "weight": 0.3333
		  },
		  {
		    "source": "Intentional overdose",
		    "target": "Malaise",
		    "weight": 0.1429
		  },
		  {
		    "source": "Intentional overdose",
		    "target": "Paranoia",
		    "weight": 0.25
		  },
		  {
		    "source": "Intentional overdose",
		    "target": "Product quality issue",
		    "weight": 0.1429
		  },
		  {
		    "source": "Intentional overdose",
		    "target": "Product use issue",
		    "weight": 0.1429
		  },
		  {
		    "source": "Intentional overdose",
		    "target": "Psychotic disorder",
		    "weight": 0.25
		  },
		  {
		    "source": "Intentional overdose",
		    "target": "Renal impairment",
		    "weight": 0.3333
		  },
		  {
		    "source": "Intentional overdose",
		    "target": "Wrong technique in product usage process",
		    "weight": 0.1429
		  },
		  {
		    "source": "Intentional product misuse",
		    "target": "Vomiting",
		    "weight": 0.3333
		  },
		  {
		    "source": "Intentional self-injury",
		    "target": "Memory impairment",
		    "weight": 0.1
		  },
		  {
		    "source": "Intentional self-injury",
		    "target": "Mental disorder",
		    "weight": 0.1
		  },
		  {
		    "source": "Intentional self-injury",
		    "target": "Mood altered",
		    "weight": 0.1
		  },
		  {
		    "source": "Intentional self-injury",
		    "target": "Negative thoughts",
		    "weight": 0.1667
		  },
		  {
		    "source": "Intentional self-injury",
		    "target": "Suicidal ideation",
		    "weight": 0.1667
		  },
		  {
		    "source": "Intentional self-injury",
		    "target": "Suicide attempt",
		    "weight": 0.1667
		  },
		  {
		    "source": "Intervertebral disc protrusion",
		    "target": "Knee operation",
		    "weight": 0.125
		  },
		  {
		    "source": "Intervertebral disc protrusion",
		    "target": "Limb injury",
		    "weight": 0.125
		  },
		  {
		    "source": "Intervertebral disc protrusion",
		    "target": "Loss of consciousness",
		    "weight": 0.0714
		  },
		  {
		    "source": "Intervertebral disc protrusion",
		    "target": "Nerve injury",
		    "weight": 0.0714
		  },
		  {
		    "source": "Intervertebral disc protrusion",
		    "target": "Nonspecific reaction",
		    "weight": 0.0714
		  },
		  {
		    "source": "Intervertebral disc protrusion",
		    "target": "Pain",
		    "weight": 0.1964
		  },
		  {
		    "source": "Intervertebral disc protrusion",
		    "target": "Paraesthesia",
		    "weight": 0.0714
		  },
		  {
		    "source": "Intervertebral disc protrusion",
		    "target": "Product use issue",
		    "weight": 0.1964
		  },
		  {
		    "source": "Intervertebral disc protrusion",
		    "target": "Radiculitis brachial",
		    "weight": 0.0714
		  },
		  {
		    "source": "Intervertebral disc protrusion",
		    "target": "Sleep disorder",
		    "weight": 0.0714
		  },
		  {
		    "source": "Intervertebral disc protrusion",
		    "target": "Therapeutic response unexpected",
		    "weight": 0.0714
		  },
		  {
		    "source": "Intervertebral disc protrusion",
		    "target": "Thoracic outlet syndrome",
		    "weight": 0.0714
		  },
		  {
		    "source": "Intestinal polyp",
		    "target": "Large intestinal stenosis",
		    "weight": 0.1667
		  },
		  {
		    "source": "Intestinal polyp",
		    "target": "Nasopharyngitis",
		    "weight": 0.1667
		  },
		  {
		    "source": "Invasive ductal breast carcinoma",
		    "target": "Pneumonia",
		    "weight": 0.0526
		  },
		  {
		    "source": "Invasive ductal breast carcinoma",
		    "target": "Rash pruritic",
		    "weight": 0.0526
		  },
		  {
		    "source": "Invasive ductal breast carcinoma",
		    "target": "Rash pustular",
		    "weight": 0.0526
		  },
		  {
		    "source": "Invasive ductal breast carcinoma",
		    "target": "Skin mass",
		    "weight": 0.0526
		  },
		  {
		    "source": "Invasive ductal breast carcinoma",
		    "target": "Therapy cessation",
		    "weight": 0.0526
		  },
		  {
		    "source": "Invasive ductal breast carcinoma",
		    "target": "Urinary hesitation",
		    "weight": 0.0526
		  },
		  {
		    "source": "Invasive ductal breast carcinoma",
		    "target": "Urinary retention",
		    "weight": 0.0526
		  },
		  {
		    "source": "Invasive ductal breast carcinoma",
		    "target": "Vertigo",
		    "weight": 0.0526
		  },
		  {
		    "source": "Irritability",
		    "target": "Malabsorption",
		    "weight": 0.0833
		  },
		  {
		    "source": "Irritability",
		    "target": "Malaise",
		    "weight": 0.1429
		  },
		  {
		    "source": "Irritability",
		    "target": "Mood swings",
		    "weight": 0.5833
		  },
		  {
		    "source": "Irritability",
		    "target": "Nausea",
		    "weight": 0.0556
		  },
		  {
		    "source": "Irritability",
		    "target": "Obsessive thoughts",
		    "weight": 0.0556
		  },
		  {
		    "source": "Irritability",
		    "target": "Personality change",
		    "weight": 0.1429
		  },
		  {
		    "source": "Irritability",
		    "target": "Social avoidant behaviour",
		    "weight": 0.0556
		  },
		  {
		    "source": "Irritability",
		    "target": "Tic",
		    "weight": 0.0556
		  },
		  {
		    "source": "Irritability",
		    "target": "Vitamin D abnormal",
		    "weight": 0.0833
		  },
		  {
		    "source": "Irritability",
		    "target": "Vitreous floaters",
		    "weight": 0.0833
		  },
		  {
		    "source": "Irritability",
		    "target": "Vomiting",
		    "weight": 0.0556
		  },
		  {
		    "source": "Irritability",
		    "target": "Weight decreased",
		    "weight": 0.1429
		  },
		  {
		    "source": "Irritable bowel syndrome",
		    "target": "Muscle spasms",
		    "weight": 0.1111
		  },
		  {
		    "source": "Irritable bowel syndrome",
		    "target": "Musculoskeletal disorder",
		    "weight": 0.1111
		  },
		  {
		    "source": "Irritable bowel syndrome",
		    "target": "Syncope",
		    "weight": 0.1111
		  },
		  {
		    "source": "Jaundice neonatal",
		    "target": "Premature baby",
		    "weight": 0.1667
		  },
		  {
		    "source": "Job dissatisfaction",
		    "target": "Prescribed overdose",
		    "weight": 0.25
		  },
		  {
		    "source": "Job dissatisfaction",
		    "target": "Product tampering",
		    "weight": 0.25
		  },
		  {
		    "source": "Joint stiffness",
		    "target": "Meniscus injury",
		    "weight": 0.2
		  },
		  {
		    "source": "Knee operation",
		    "target": "Limb injury",
		    "weight": 0.125
		  },
		  {
		    "source": "Knee operation",
		    "target": "Pain",
		    "weight": 0.125
		  },
		  {
		    "source": "Knee operation",
		    "target": "Product use issue",
		    "weight": 0.125
		  },
		  {
		    "source": "Lactose intolerance",
		    "target": "Logorrhoea",
		    "weight": 0.0667
		  },
		  {
		    "source": "Lactose intolerance",
		    "target": "Weight decreased",
		    "weight": 0.0667
		  },
		  {
		    "source": "Large intestinal stenosis",
		    "target": "Nasopharyngitis",
		    "weight": 0.1667
		  },
		  {
		    "source": "Laziness",
		    "target": "Malaise",
		    "weight": 0.0769
		  },
		  {
		    "source": "Laziness",
		    "target": "Memory impairment",
		    "weight": 0.1111
		  },
		  {
		    "source": "Laziness",
		    "target": "Musculoskeletal stiffness",
		    "weight": 0.0714
		  },
		  {
		    "source": "Laziness",
		    "target": "Panic attack",
		    "weight": 0.1111
		  },
		  {
		    "source": "Laziness",
		    "target": "Psychomotor hyperactivity",
		    "weight": 0.0769
		  },
		  {
		    "source": "Laziness",
		    "target": "Social avoidant behaviour",
		    "weight": 0.0714
		  },
		  {
		    "source": "Laziness",
		    "target": "Somnolence",
		    "weight": 0.0769
		  },
		  {
		    "source": "Laziness",
		    "target": "Thirst",
		    "weight": 0.0714
		  },
		  {
		    "source": "Laziness",
		    "target": "Victim of abuse",
		    "weight": 0.0714
		  },
		  {
		    "source": "Laziness",
		    "target": "Victim of sexual abuse",
		    "weight": 0.0714
		  },
		  {
		    "source": "Laziness",
		    "target": "Weight decreased",
		    "weight": 0.1111
		  },
		  {
		    "source": "Laziness",
		    "target": "Weight increased",
		    "weight": 0.0714
		  },
		  {
		    "source": "Legal problem",
		    "target": "Wrong technique in product usage process",
		    "weight": 0.3333
		  },
		  {
		    "source": "Lethargy",
		    "target": "Product quality issue",
		    "weight": 0.125
		  },
		  {
		    "source": "Lethargy",
		    "target": "Psychiatric symptom",
		    "weight": 0.125
		  },
		  {
		    "source": "Lethargy",
		    "target": "Rebound effect",
		    "weight": 0.1667
		  },
		  {
		    "source": "Lethargy",
		    "target": "Somnolence",
		    "weight": 0.1667
		  },
		  {
		    "source": "Lethargy",
		    "target": "Wrong technique in product usage process",
		    "weight": 0.125
		  },
		  {
		    "source": "Leukopenia",
		    "target": "Neutropenia",
		    "weight": 0.5
		  },
		  {
		    "source": "Libido decreased",
		    "target": "Muscle spasms",
		    "weight": 0.0769
		  },
		  {
		    "source": "Libido decreased",
		    "target": "Nausea",
		    "weight": 0.0769
		  },
		  {
		    "source": "Libido decreased",
		    "target": "Pain in jaw",
		    "weight": 0.0769
		  },
		  {
		    "source": "Libido decreased",
		    "target": "Palpitations",
		    "weight": 0.0769
		  },
		  {
		    "source": "Libido decreased",
		    "target": "Pyrexia",
		    "weight": 0.0769
		  },
		  {
		    "source": "Libido decreased",
		    "target": "Tachyphrenia",
		    "weight": 0.2
		  },
		  {
		    "source": "Libido decreased",
		    "target": "Tension",
		    "weight": 0.2
		  },
		  {
		    "source": "Libido decreased",
		    "target": "Vomiting",
		    "weight": 0.0769
		  },
		  {
		    "source": "Limb discomfort",
		    "target": "Pallor",
		    "weight": 0.3333
		  },
		  {
		    "source": "Limb injury",
		    "target": "Pain",
		    "weight": 0.125
		  },
		  {
		    "source": "Limb injury",
		    "target": "Product use issue",
		    "weight": 0.125
		  },
		  {
		    "source": "Lip exfoliation",
		    "target": "Lip haemorrhage",
		    "weight": 0.2
		  },
		  {
		    "source": "Lip exfoliation",
		    "target": "Lip swelling",
		    "weight": 0.2
		  },
		  {
		    "source": "Lip exfoliation",
		    "target": "Mouth swelling",
		    "weight": 0.2
		  },
		  {
		    "source": "Lip exfoliation",
		    "target": "Pruritus",
		    "weight": 0.2
		  },
		  {
		    "source": "Lip haemorrhage",
		    "target": "Lip swelling",
		    "weight": 0.2
		  },
		  {
		    "source": "Lip haemorrhage",
		    "target": "Mouth swelling",
		    "weight": 0.2
		  },
		  {
		    "source": "Lip haemorrhage",
		    "target": "Pruritus",
		    "weight": 0.2
		  },
		  {
		    "source": "Lip swelling",
		    "target": "Mouth swelling",
		    "weight": 0.2
		  },
		  {
		    "source": "Lip swelling",
		    "target": "Neck pain",
		    "weight": 0.1429
		  },
		  {
		    "source": "Lip swelling",
		    "target": "Pruritus",
		    "weight": 0.2
		  },
		  {
		    "source": "Lip swelling",
		    "target": "Rash",
		    "weight": 0.1429
		  },
		  {
		    "source": "Lipids increased",
		    "target": "Urinary tract infection",
		    "weight": 0.25
		  },
		  {
		    "source": "Local swelling",
		    "target": "Neck pain",
		    "weight": 0.2
		  },
		  {
		    "source": "Local swelling",
		    "target": "Urticaria",
		    "weight": 0.2
		  },
		  {
		    "source": "Logorrhoea",
		    "target": "Mania",
		    "weight": 0.1667
		  },
		  {
		    "source": "Logorrhoea",
		    "target": "Thinking abnormal",
		    "weight": 0.1667
		  },
		  {
		    "source": "Logorrhoea",
		    "target": "Weight decreased",
		    "weight": 0.0667
		  },
		  {
		    "source": "Loss of consciousness",
		    "target": "Nerve injury",
		    "weight": 0.0714
		  },
		  {
		    "source": "Loss of consciousness",
		    "target": "Nonspecific reaction",
		    "weight": 0.0714
		  },
		  {
		    "source": "Loss of consciousness",
		    "target": "Pain",
		    "weight": 0.0714
		  },
		  {
		    "source": "Loss of consciousness",
		    "target": "Paraesthesia",
		    "weight": 0.0714
		  },
		  {
		    "source": "Loss of consciousness",
		    "target": "Post-traumatic neck syndrome",
		    "weight": 0.2
		  },
		  {
		    "source": "Loss of consciousness",
		    "target": "Product use issue",
		    "weight": 0.0714
		  },
		  {
		    "source": "Loss of consciousness",
		    "target": "Radiculitis brachial",
		    "weight": 0.0714
		  },
		  {
		    "source": "Loss of consciousness",
		    "target": "Road traffic accident",
		    "weight": 0.2
		  },
		  {
		    "source": "Loss of consciousness",
		    "target": "Sleep disorder",
		    "weight": 0.0714
		  },
		  {
		    "source": "Loss of consciousness",
		    "target": "Therapeutic response unexpected",
		    "weight": 0.0714
		  },
		  {
		    "source": "Loss of consciousness",
		    "target": "Thoracic outlet syndrome",
		    "weight": 0.0714
		  },
		  {
		    "source": "Loss of control of legs",
		    "target": "Memory impairment",
		    "weight": 0.1
		  },
		  {
		    "source": "Loss of control of legs",
		    "target": "Mental impairment",
		    "weight": 0.1
		  },
		  {
		    "source": "Loss of control of legs",
		    "target": "Pain",
		    "weight": 0.1
		  },
		  {
		    "source": "Loss of control of legs",
		    "target": "Pain in extremity",
		    "weight": 0.1
		  },
		  {
		    "source": "Loss of control of legs",
		    "target": "Road traffic accident",
		    "weight": 0.1
		  },
		  {
		    "source": "Loss of employment",
		    "target": "Nervousness",
		    "weight": 0.25
		  },
		  {
		    "source": "Loss of employment",
		    "target": "Panic attack",
		    "weight": 0.25
		  },
		  {
		    "source": "Malabsorption",
		    "target": "Mood swings",
		    "weight": 0.0833
		  },
		  {
		    "source": "Malabsorption",
		    "target": "Vitamin D abnormal",
		    "weight": 0.0833
		  },
		  {
		    "source": "Malabsorption",
		    "target": "Vitreous floaters",
		    "weight": 0.0833
		  },
		  {
		    "source": "Malaise",
		    "target": "Mental impairment",
		    "weight": 0.0769
		  },
		  {
		    "source": "Malaise",
		    "target": "Migraine",
		    "weight": 0.0455
		  },
		  {
		    "source": "Malaise",
		    "target": "Nasopharyngitis",
		    "weight": 0.0455
		  },
		  {
		    "source": "Malaise",
		    "target": "Nausea",
		    "weight": 0.2769
		  },
		  {
		    "source": "Malaise",
		    "target": "Nightmare",
		    "weight": 0.1667
		  },
		  {
		    "source": "Malaise",
		    "target": "Paranasal sinus hypersecretion",
		    "weight": 0.1
		  },
		  {
		    "source": "Malaise",
		    "target": "Performance status decreased",
		    "weight": 0.0769
		  },
		  {
		    "source": "Malaise",
		    "target": "Personality change",
		    "weight": 0.1429
		  },
		  {
		    "source": "Malaise",
		    "target": "Pharyngitis streptococcal",
		    "weight": 0.1
		  },
		  {
		    "source": "Malaise",
		    "target": "Product quality issue",
		    "weight": 0.4198
		  },
		  {
		    "source": "Malaise",
		    "target": "Product use issue",
		    "weight": 0.1429
		  },
		  {
		    "source": "Malaise",
		    "target": "Psychomotor hyperactivity",
		    "weight": 0.0769
		  },
		  {
		    "source": "Malaise",
		    "target": "Pyrexia",
		    "weight": 0.1
		  },
		  {
		    "source": "Malaise",
		    "target": "Rales",
		    "weight": 0.1
		  },
		  {
		    "source": "Malaise",
		    "target": "Self-injurious ideation",
		    "weight": 0.1667
		  },
		  {
		    "source": "Malaise",
		    "target": "Social phobia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Malaise",
		    "target": "Somnolence",
		    "weight": 0.1538
		  },
		  {
		    "source": "Malaise",
		    "target": "Tachyphrenia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Malaise",
		    "target": "Upper respiratory tract infection",
		    "weight": 0.1
		  },
		  {
		    "source": "Malaise",
		    "target": "Vomiting",
		    "weight": 0.1
		  },
		  {
		    "source": "Malaise",
		    "target": "Weight decreased",
		    "weight": 0.1429
		  },
		  {
		    "source": "Malaise",
		    "target": "Weight increased",
		    "weight": 0.0455
		  },
		  {
		    "source": "Malaise",
		    "target": "Wrong technique in product usage process",
		    "weight": 0.2198
		  },
		  {
		    "source": "Mania",
		    "target": "Optic nerve neoplasm",
		    "weight": 0.0833
		  },
		  {
		    "source": "Mania",
		    "target": "Somnolence",
		    "weight": 0.0833
		  },
		  {
		    "source": "Mania",
		    "target": "Therapy cessation",
		    "weight": 0.2
		  },
		  {
		    "source": "Mania",
		    "target": "Thinking abnormal",
		    "weight": 0.1667
		  },
		  {
		    "source": "Maternal exposure during pregnancy",
		    "target": "Premature delivery",
		    "weight": 0.2
		  },
		  {
		    "source": "Maternal exposure during pregnancy",
		    "target": "Rhesus incompatibility",
		    "weight": 0.2
		  },
		  {
		    "source": "Maternal exposure during pregnancy",
		    "target": "Transfusion",
		    "weight": 0.2
		  },
		  {
		    "source": "Medical device discomfort",
		    "target": "Medical device pain",
		    "weight": 0.0769
		  },
		  {
		    "source": "Medical device discomfort",
		    "target": "Post procedural discomfort",
		    "weight": 0.0769
		  },
		  {
		    "source": "Medical device discomfort",
		    "target": "Procedural pain",
		    "weight": 0.0769
		  },
		  {
		    "source": "Medical device discomfort",
		    "target": "Uterine perforation",
		    "weight": 0.0769
		  },
		  {
		    "source": "Medical device pain",
		    "target": "Post procedural discomfort",
		    "weight": 0.0769
		  },
		  {
		    "source": "Medical device pain",
		    "target": "Procedural pain",
		    "weight": 0.0769
		  },
		  {
		    "source": "Medical device pain",
		    "target": "Uterine perforation",
		    "weight": 0.0769
		  },
		  {
		    "source": "Memory impairment",
		    "target": "Mental disorder",
		    "weight": 0.1
		  },
		  {
		    "source": "Memory impairment",
		    "target": "Mental impairment",
		    "weight": 0.1
		  },
		  {
		    "source": "Memory impairment",
		    "target": "Mood altered",
		    "weight": 0.1
		  },
		  {
		    "source": "Memory impairment",
		    "target": "Oral discomfort",
		    "weight": 0.1667
		  },
		  {
		    "source": "Memory impairment",
		    "target": "Pain",
		    "weight": 0.2667
		  },
		  {
		    "source": "Memory impairment",
		    "target": "Pain in extremity",
		    "weight": 0.2667
		  },
		  {
		    "source": "Memory impairment",
		    "target": "Panic attack",
		    "weight": 0.1111
		  },
		  {
		    "source": "Memory impairment",
		    "target": "Product quality issue",
		    "weight": 0.3667
		  },
		  {
		    "source": "Memory impairment",
		    "target": "Road traffic accident",
		    "weight": 0.2667
		  },
		  {
		    "source": "Memory impairment",
		    "target": "Weight decreased",
		    "weight": 0.1111
		  },
		  {
		    "source": "Menorrhagia",
		    "target": "Metrorrhagia",
		    "weight": 0.5
		  },
		  {
		    "source": "Mental disorder",
		    "target": "Mood altered",
		    "weight": 0.1
		  },
		  {
		    "source": "Mental disorder",
		    "target": "Off label use",
		    "weight": 0.5
		  },
		  {
		    "source": "Mental disorder",
		    "target": "Pain",
		    "weight": 0.125
		  },
		  {
		    "source": "Mental disorder",
		    "target": "Pulmonary embolism",
		    "weight": 0.125
		  },
		  {
		    "source": "Mental impairment",
		    "target": "Nausea",
		    "weight": 0.0769
		  },
		  {
		    "source": "Mental impairment",
		    "target": "Nightmare",
		    "weight": 0.0588
		  },
		  {
		    "source": "Mental impairment",
		    "target": "Pain",
		    "weight": 0.1
		  },
		  {
		    "source": "Mental impairment",
		    "target": "Pain in extremity",
		    "weight": 0.1
		  },
		  {
		    "source": "Mental impairment",
		    "target": "Performance status decreased",
		    "weight": 0.0769
		  },
		  {
		    "source": "Mental impairment",
		    "target": "Product quality issue",
		    "weight": 0.0769
		  },
		  {
		    "source": "Mental impairment",
		    "target": "Rapid eye movements sleep abnormal",
		    "weight": 0.0588
		  },
		  {
		    "source": "Mental impairment",
		    "target": "Road traffic accident",
		    "weight": 0.1588
		  },
		  {
		    "source": "Mental impairment",
		    "target": "Somnolence",
		    "weight": 0.0769
		  },
		  {
		    "source": "Mental impairment",
		    "target": "Underweight",
		    "weight": 0.0588
		  },
		  {
		    "source": "Mental impairment",
		    "target": "Weight increased",
		    "weight": 0.0588
		  },
		  {
		    "source": "Mental impairment",
		    "target": "Wrong technique in product usage process",
		    "weight": 0.0769
		  },
		  {
		    "source": "Micturition urgency",
		    "target": "Pollakiuria",
		    "weight": 0.5
		  },
		  {
		    "source": "Migraine",
		    "target": "Nasopharyngitis",
		    "weight": 0.0455
		  },
		  {
		    "source": "Migraine",
		    "target": "Social phobia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Migraine",
		    "target": "Tachyphrenia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Migraine",
		    "target": "Vision blurred",
		    "weight": 0.2
		  },
		  {
		    "source": "Migraine",
		    "target": "Visual acuity reduced",
		    "weight": 0.2
		  },
		  {
		    "source": "Migraine",
		    "target": "Weight increased",
		    "weight": 0.0455
		  },
		  {
		    "source": "Mood swings",
		    "target": "Restlessness",
		    "weight": 0.2
		  },
		  {
		    "source": "Mood swings",
		    "target": "Urinary incontinence",
		    "weight": 0.1667
		  },
		  {
		    "source": "Mood swings",
		    "target": "Vitamin D abnormal",
		    "weight": 0.0833
		  },
		  {
		    "source": "Mood swings",
		    "target": "Vitreous floaters",
		    "weight": 0.0833
		  },
		  {
		    "source": "Motor dysfunction",
		    "target": "Myoclonic epilepsy",
		    "weight": 0.125
		  },
		  {
		    "source": "Motor dysfunction",
		    "target": "Panic disorder",
		    "weight": 0.125
		  },
		  {
		    "source": "Motor dysfunction",
		    "target": "Thinking abnormal",
		    "weight": 0.125
		  },
		  {
		    "source": "Mouth swelling",
		    "target": "Pruritus",
		    "weight": 0.2
		  },
		  {
		    "source": "Movement disorder",
		    "target": "Nasopharyngitis",
		    "weight": 0.0769
		  },
		  {
		    "source": "Movement disorder",
		    "target": "Off label use",
		    "weight": 0.0769
		  },
		  {
		    "source": "Movement disorder",
		    "target": "Pneumonia",
		    "weight": 0.0769
		  },
		  {
		    "source": "Movement disorder",
		    "target": "Restlessness",
		    "weight": 0.0769
		  },
		  {
		    "source": "Movement disorder",
		    "target": "Thirst",
		    "weight": 0.0769
		  },
		  {
		    "source": "Multiple sclerosis",
		    "target": "Palpitations",
		    "weight": 0.25
		  },
		  {
		    "source": "Multiple sclerosis",
		    "target": "Product use issue",
		    "weight": 0.25
		  },
		  {
		    "source": "Muscle injury",
		    "target": "Musculoskeletal pain",
		    "weight": 0.2
		  },
		  {
		    "source": "Muscle injury",
		    "target": "Sinusitis",
		    "weight": 0.2
		  },
		  {
		    "source": "Muscle spasms",
		    "target": "Musculoskeletal disorder",
		    "weight": 0.1111
		  },
		  {
		    "source": "Muscle spasms",
		    "target": "Myalgia",
		    "weight": 0.2
		  },
		  {
		    "source": "Muscle spasms",
		    "target": "Mydriasis",
		    "weight": 0.1
		  },
		  {
		    "source": "Muscle spasms",
		    "target": "Nausea",
		    "weight": 0.0769
		  },
		  {
		    "source": "Muscle spasms",
		    "target": "Pain in jaw",
		    "weight": 0.0769
		  },
		  {
		    "source": "Muscle spasms",
		    "target": "Palpitations",
		    "weight": 0.0769
		  },
		  {
		    "source": "Muscle spasms",
		    "target": "Peripheral vascular disorder",
		    "weight": 0.5
		  },
		  {
		    "source": "Muscle spasms",
		    "target": "Pyrexia",
		    "weight": 0.0769
		  },
		  {
		    "source": "Muscle spasms",
		    "target": "Serotonin syndrome",
		    "weight": 0.1
		  },
		  {
		    "source": "Muscle spasms",
		    "target": "Sjogren's syndrome",
		    "weight": 0.2
		  },
		  {
		    "source": "Muscle spasms",
		    "target": "Syncope",
		    "weight": 0.1111
		  },
		  {
		    "source": "Muscle spasms",
		    "target": "Tachyphrenia",
		    "weight": 0.1
		  },
		  {
		    "source": "Muscle spasms",
		    "target": "Vomiting",
		    "weight": 0.0769
		  },
		  {
		    "source": "Muscle twitching",
		    "target": "Myalgia",
		    "weight": 0.1
		  },
		  {
		    "source": "Muscle twitching",
		    "target": "Screaming",
		    "weight": 0.1
		  },
		  {
		    "source": "Muscle twitching",
		    "target": "Tremor",
		    "weight": 0.1
		  },
		  {
		    "source": "Muscle twitching",
		    "target": "Wrong technique in product usage process",
		    "weight": 0.1
		  },
		  {
		    "source": "Musculoskeletal disorder",
		    "target": "Syncope",
		    "weight": 0.1111
		  },
		  {
		    "source": "Musculoskeletal pain",
		    "target": "Neck pain",
		    "weight": 0.1429
		  },
		  {
		    "source": "Musculoskeletal pain",
		    "target": "Pain",
		    "weight": 0.1429
		  },
		  {
		    "source": "Musculoskeletal pain",
		    "target": "Product substitution issue",
		    "weight": 0.1429
		  },
		  {
		    "source": "Musculoskeletal pain",
		    "target": "Sinusitis",
		    "weight": 0.2
		  },
		  {
		    "source": "Musculoskeletal stiffness",
		    "target": "Social avoidant behaviour",
		    "weight": 0.0714
		  },
		  {
		    "source": "Musculoskeletal stiffness",
		    "target": "Thirst",
		    "weight": 0.0714
		  },
		  {
		    "source": "Musculoskeletal stiffness",
		    "target": "Tremor",
		    "weight": 0.3333
		  },
		  {
		    "source": "Musculoskeletal stiffness",
		    "target": "Victim of abuse",
		    "weight": 0.0714
		  },
		  {
		    "source": "Musculoskeletal stiffness",
		    "target": "Victim of sexual abuse",
		    "weight": 0.0714
		  },
		  {
		    "source": "Musculoskeletal stiffness",
		    "target": "Weight increased",
		    "weight": 0.0714
		  },
		  {
		    "source": "Myalgia",
		    "target": "Screaming",
		    "weight": 0.1
		  },
		  {
		    "source": "Myalgia",
		    "target": "Sjogren's syndrome",
		    "weight": 0.2
		  },
		  {
		    "source": "Myalgia",
		    "target": "Tremor",
		    "weight": 0.1
		  },
		  {
		    "source": "Myalgia",
		    "target": "Wrong technique in product usage process",
		    "weight": 0.1
		  },
		  {
		    "source": "Mycobacterium test positive",
		    "target": "Obstructive airways disorder",
		    "weight": 0.1
		  },
		  {
		    "source": "Mycobacterium test positive",
		    "target": "Pseudomonas infection",
		    "weight": 0.1
		  },
		  {
		    "source": "Mycobacterium test positive",
		    "target": "Sinus disorder",
		    "weight": 0.1
		  },
		  {
		    "source": "Mycobacterium test positive",
		    "target": "Weight increased",
		    "weight": 0.1
		  },
		  {
		    "source": "Mydriasis",
		    "target": "Serotonin syndrome",
		    "weight": 0.1
		  },
		  {
		    "source": "Mydriasis",
		    "target": "Somnolence",
		    "weight": 0.5
		  },
		  {
		    "source": "Mydriasis",
		    "target": "Tachyphrenia",
		    "weight": 0.1
		  },
		  {
		    "source": "Mydriasis",
		    "target": "Thyroid disorder",
		    "weight": 0.3333
		  },
		  {
		    "source": "Mydriasis",
		    "target": "Vision blurred",
		    "weight": 0.3333
		  },
		  {
		    "source": "Myoclonic epilepsy",
		    "target": "Panic disorder",
		    "weight": 0.125
		  },
		  {
		    "source": "Myoclonic epilepsy",
		    "target": "Thinking abnormal",
		    "weight": 0.125
		  },
		  {
		    "source": "Narcolepsy",
		    "target": "Seizure",
		    "weight": 0.3333
		  },
		  {
		    "source": "Nasal discomfort",
		    "target": "Rhinalgia",
		    "weight": 0.2
		  },
		  {
		    "source": "Nasal discomfort",
		    "target": "Sinus headache",
		    "weight": 0.2
		  },
		  {
		    "source": "Nasopharyngitis",
		    "target": "Off label use",
		    "weight": 0.0769
		  },
		  {
		    "source": "Nasopharyngitis",
		    "target": "Pneumonia",
		    "weight": 0.0769
		  },
		  {
		    "source": "Nasopharyngitis",
		    "target": "Restlessness",
		    "weight": 0.0769
		  },
		  {
		    "source": "Nasopharyngitis",
		    "target": "Social phobia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Nasopharyngitis",
		    "target": "Tachyphrenia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Nasopharyngitis",
		    "target": "Thirst",
		    "weight": 0.0769
		  },
		  {
		    "source": "Nasopharyngitis",
		    "target": "Weight increased",
		    "weight": 0.0455
		  },
		  {
		    "source": "Nausea",
		    "target": "Obsessive thoughts",
		    "weight": 0.0556
		  },
		  {
		    "source": "Nausea",
		    "target": "Oedema peripheral",
		    "weight": 0.0769
		  },
		  {
		    "source": "Nausea",
		    "target": "Oesophagitis",
		    "weight": 0.0833
		  },
		  {
		    "source": "Nausea",
		    "target": "Pain in extremity",
		    "weight": 0.25
		  },
		  {
		    "source": "Nausea",
		    "target": "Pain in jaw",
		    "weight": 0.0769
		  },
		  {
		    "source": "Nausea",
		    "target": "Palpitations",
		    "weight": 0.0769
		  },
		  {
		    "source": "Nausea",
		    "target": "Performance status decreased",
		    "weight": 0.0769
		  },
		  {
		    "source": "Nausea",
		    "target": "Pleural effusion",
		    "weight": 0.0769
		  },
		  {
		    "source": "Nausea",
		    "target": "Product quality issue",
		    "weight": 0.2769
		  },
		  {
		    "source": "Nausea",
		    "target": "Pyrexia",
		    "weight": 0.1603
		  },
		  {
		    "source": "Nausea",
		    "target": "Seizure",
		    "weight": 0.0833
		  },
		  {
		    "source": "Nausea",
		    "target": "Severe acute respiratory syndrome",
		    "weight": 0.0769
		  },
		  {
		    "source": "Nausea",
		    "target": "Social avoidant behaviour",
		    "weight": 0.0556
		  },
		  {
		    "source": "Nausea",
		    "target": "Somnolence",
		    "weight": 0.0769
		  },
		  {
		    "source": "Nausea",
		    "target": "Stress",
		    "weight": 0.0769
		  },
		  {
		    "source": "Nausea",
		    "target": "Syncope",
		    "weight": 0.0833
		  },
		  {
		    "source": "Nausea",
		    "target": "Tearfulness",
		    "weight": 0.0769
		  },
		  {
		    "source": "Nausea",
		    "target": "Tic",
		    "weight": 0.0556
		  },
		  {
		    "source": "Nausea",
		    "target": "Unevaluable event",
		    "weight": 0.0833
		  },
		  {
		    "source": "Nausea",
		    "target": "Viral infection",
		    "weight": 0.0769
		  },
		  {
		    "source": "Nausea",
		    "target": "Vomiting",
		    "weight": 0.4594
		  },
		  {
		    "source": "Nausea",
		    "target": "Weight decreased",
		    "weight": 0.1667
		  },
		  {
		    "source": "Nausea",
		    "target": "Wrong technique in product usage process",
		    "weight": 0.0769
		  },
		  {
		    "source": "Neck pain",
		    "target": "Pain",
		    "weight": 0.1429
		  },
		  {
		    "source": "Neck pain",
		    "target": "Product substitution issue",
		    "weight": 0.1429
		  },
		  {
		    "source": "Neck pain",
		    "target": "Rash",
		    "weight": 0.1429
		  },
		  {
		    "source": "Neck pain",
		    "target": "Urticaria",
		    "weight": 0.2
		  },
		  {
		    "source": "Negative thoughts",
		    "target": "Suicidal ideation",
		    "weight": 0.1667
		  },
		  {
		    "source": "Negative thoughts",
		    "target": "Suicide attempt",
		    "weight": 0.1667
		  },
		  {
		    "source": "Nerve injury",
		    "target": "Nonspecific reaction",
		    "weight": 0.0714
		  },
		  {
		    "source": "Nerve injury",
		    "target": "Pain",
		    "weight": 0.0714
		  },
		  {
		    "source": "Nerve injury",
		    "target": "Paraesthesia",
		    "weight": 0.0714
		  },
		  {
		    "source": "Nerve injury",
		    "target": "Product use issue",
		    "weight": 0.0714
		  },
		  {
		    "source": "Nerve injury",
		    "target": "Radiculitis brachial",
		    "weight": 0.0714
		  },
		  {
		    "source": "Nerve injury",
		    "target": "Sleep disorder",
		    "weight": 0.0714
		  },
		  {
		    "source": "Nerve injury",
		    "target": "Therapeutic response unexpected",
		    "weight": 0.0714
		  },
		  {
		    "source": "Nerve injury",
		    "target": "Thoracic outlet syndrome",
		    "weight": 0.0714
		  },
		  {
		    "source": "Nervousness",
		    "target": "Panic attack",
		    "weight": 0.25
		  },
		  {
		    "source": "Nervousness",
		    "target": "Pruritus",
		    "weight": 0.25
		  },
		  {
		    "source": "Nervousness",
		    "target": "Swelling face",
		    "weight": 0.25
		  },
		  {
		    "source": "Neuralgia",
		    "target": "Road traffic accident",
		    "weight": 0.2
		  },
		  {
		    "source": "Neuralgia",
		    "target": "Unevaluable event",
		    "weight": 0.2
		  },
		  {
		    "source": "Nightmare",
		    "target": "Rapid eye movements sleep abnormal",
		    "weight": 0.0588
		  },
		  {
		    "source": "Nightmare",
		    "target": "Road traffic accident",
		    "weight": 0.0588
		  },
		  {
		    "source": "Nightmare",
		    "target": "Self-injurious ideation",
		    "weight": 0.1667
		  },
		  {
		    "source": "Nightmare",
		    "target": "Underweight",
		    "weight": 0.0588
		  },
		  {
		    "source": "Nightmare",
		    "target": "Weight increased",
		    "weight": 0.0588
		  },
		  {
		    "source": "No adverse event",
		    "target": "Prescribed overdose",
		    "weight": 2.6667
		  },
		  {
		    "source": "No adverse event",
		    "target": "Product quality issue",
		    "weight": 1.5833
		  },
		  {
		    "source": "No adverse event",
		    "target": "Product use issue",
		    "weight": 1
		  },
		  {
		    "source": "No adverse event",
		    "target": "Treatment noncompliance",
		    "weight": 0.5
		  },
		  {
		    "source": "No adverse event",
		    "target": "Wrong technique in product usage process",
		    "weight": 2.4167
		  },
		  {
		    "source": "No therapeutic response",
		    "target": "Pain in extremity",
		    "weight": 0.1
		  },
		  {
		    "source": "No therapeutic response",
		    "target": "Paraesthesia",
		    "weight": 0.1
		  },
		  {
		    "source": "No therapeutic response",
		    "target": "Product substitution issue",
		    "weight": 0.1
		  },
		  {
		    "source": "No therapeutic response",
		    "target": "Vertigo",
		    "weight": 0.1
		  },
		  {
		    "source": "Nonspecific reaction",
		    "target": "Pain",
		    "weight": 0.0714
		  },
		  {
		    "source": "Nonspecific reaction",
		    "target": "Paraesthesia",
		    "weight": 0.0714
		  },
		  {
		    "source": "Nonspecific reaction",
		    "target": "Product use issue",
		    "weight": 0.0714
		  },
		  {
		    "source": "Nonspecific reaction",
		    "target": "Radiculitis brachial",
		    "weight": 0.0714
		  },
		  {
		    "source": "Nonspecific reaction",
		    "target": "Sleep disorder",
		    "weight": 0.0714
		  },
		  {
		    "source": "Nonspecific reaction",
		    "target": "Therapeutic response unexpected",
		    "weight": 0.0714
		  },
		  {
		    "source": "Nonspecific reaction",
		    "target": "Thoracic outlet syndrome",
		    "weight": 0.0714
		  },
		  {
		    "source": "Obsessive thoughts",
		    "target": "Social avoidant behaviour",
		    "weight": 0.0556
		  },
		  {
		    "source": "Obsessive thoughts",
		    "target": "Tic",
		    "weight": 0.0556
		  },
		  {
		    "source": "Obsessive thoughts",
		    "target": "Vomiting",
		    "weight": 0.0556
		  },
		  {
		    "source": "Obsessive-compulsive disorder",
		    "target": "Off label use",
		    "weight": 0.2
		  },
		  {
		    "source": "Obstructive airways disorder",
		    "target": "Pseudomonas infection",
		    "weight": 0.1
		  },
		  {
		    "source": "Obstructive airways disorder",
		    "target": "Sinus disorder",
		    "weight": 0.1
		  },
		  {
		    "source": "Obstructive airways disorder",
		    "target": "Weight increased",
		    "weight": 0.1
		  },
		  {
		    "source": "Oedema",
		    "target": "Oxygen saturation decreased",
		    "weight": 0.1
		  },
		  {
		    "source": "Oedema",
		    "target": "Peripheral swelling",
		    "weight": 0.1
		  },
		  {
		    "source": "Oedema",
		    "target": "Pulmonary arterial hypertension",
		    "weight": 0.1
		  },
		  {
		    "source": "Oedema",
		    "target": "Respiratory failure",
		    "weight": 0.1
		  },
		  {
		    "source": "Oedema",
		    "target": "Right ventricular failure",
		    "weight": 0.1
		  },
		  {
		    "source": "Oedema peripheral",
		    "target": "Pleural effusion",
		    "weight": 0.0769
		  },
		  {
		    "source": "Oedema peripheral",
		    "target": "Severe acute respiratory syndrome",
		    "weight": 0.0769
		  },
		  {
		    "source": "Oedema peripheral",
		    "target": "Stress",
		    "weight": 0.0769
		  },
		  {
		    "source": "Oedema peripheral",
		    "target": "Tearfulness",
		    "weight": 0.0769
		  },
		  {
		    "source": "Oedema peripheral",
		    "target": "Viral infection",
		    "weight": 0.0769
		  },
		  {
		    "source": "Oedema peripheral",
		    "target": "Vomiting",
		    "weight": 0.0769
		  },
		  {
		    "source": "Oesophagitis",
		    "target": "Pyrexia",
		    "weight": 0.0833
		  },
		  {
		    "source": "Oesophagitis",
		    "target": "Seizure",
		    "weight": 0.0833
		  },
		  {
		    "source": "Oesophagitis",
		    "target": "Syncope",
		    "weight": 0.0833
		  },
		  {
		    "source": "Oesophagitis",
		    "target": "Unevaluable event",
		    "weight": 0.0833
		  },
		  {
		    "source": "Off label use",
		    "target": "Pneumonia",
		    "weight": 0.0769
		  },
		  {
		    "source": "Off label use",
		    "target": "Prescribed overdose",
		    "weight": 0.3333
		  },
		  {
		    "source": "Off label use",
		    "target": "Product use issue",
		    "weight": 0.2
		  },
		  {
		    "source": "Off label use",
		    "target": "Restlessness",
		    "weight": 0.0769
		  },
		  {
		    "source": "Off label use",
		    "target": "Suicidal ideation",
		    "weight": 0.1667
		  },
		  {
		    "source": "Off label use",
		    "target": "Thirst",
		    "weight": 0.0769
		  },
		  {
		    "source": "Off label use",
		    "target": "Weight increased",
		    "weight": 0.4
		  },
		  {
		    "source": "Optic nerve neoplasm",
		    "target": "Somnolence",
		    "weight": 0.0833
		  },
		  {
		    "source": "Oral administration complication",
		    "target": "Paranoia",
		    "weight": 0.1111
		  },
		  {
		    "source": "Oral administration complication",
		    "target": "Product quality issue",
		    "weight": 0.8111
		  },
		  {
		    "source": "Oral administration complication",
		    "target": "Psychomotor hyperactivity",
		    "weight": 0.1111
		  },
		  {
		    "source": "Oral administration complication",
		    "target": "Restlessness",
		    "weight": 0.1111
		  },
		  {
		    "source": "Oral administration complication",
		    "target": "Somnambulism",
		    "weight": 0.2
		  },
		  {
		    "source": "Oral candidiasis",
		    "target": "Skin candida",
		    "weight": 0.3333
		  },
		  {
		    "source": "Osteoarthritis",
		    "target": "Pain",
		    "weight": 0.0476
		  },
		  {
		    "source": "Osteoarthritis",
		    "target": "Panic attack",
		    "weight": 0.0476
		  },
		  {
		    "source": "Osteoarthritis",
		    "target": "Poor quality sleep",
		    "weight": 0.0476
		  },
		  {
		    "source": "Osteoarthritis",
		    "target": "Psychotic disorder",
		    "weight": 0.0476
		  },
		  {
		    "source": "Osteoarthritis",
		    "target": "Scar",
		    "weight": 0.0476
		  },
		  {
		    "source": "Osteoarthritis",
		    "target": "Tooth infection",
		    "weight": 0.0476
		  },
		  {
		    "source": "Osteoarthritis",
		    "target": "Tooth loss",
		    "weight": 0.0476
		  },
		  {
		    "source": "Osteoarthritis",
		    "target": "Toothache",
		    "weight": 0.0476
		  },
		  {
		    "source": "Overdose",
		    "target": "Weight increased",
		    "weight": 0.25
		  },
		  {
		    "source": "Oxygen saturation decreased",
		    "target": "Peripheral swelling",
		    "weight": 0.1
		  },
		  {
		    "source": "Oxygen saturation decreased",
		    "target": "Pulmonary arterial hypertension",
		    "weight": 0.1
		  },
		  {
		    "source": "Oxygen saturation decreased",
		    "target": "Respiratory failure",
		    "weight": 0.1
		  },
		  {
		    "source": "Oxygen saturation decreased",
		    "target": "Right ventricular failure",
		    "weight": 0.1
		  },
		  {
		    "source": "Pain",
		    "target": "Pain in extremity",
		    "weight": 0.2667
		  },
		  {
		    "source": "Pain",
		    "target": "Panic attack",
		    "weight": 0.0476
		  },
		  {
		    "source": "Pain",
		    "target": "Paraesthesia",
		    "weight": 0.0714
		  },
		  {
		    "source": "Pain",
		    "target": "Poor quality sleep",
		    "weight": 0.0476
		  },
		  {
		    "source": "Pain",
		    "target": "Product substitution issue",
		    "weight": 0.1429
		  },
		  {
		    "source": "Pain",
		    "target": "Product use issue",
		    "weight": 0.1964
		  },
		  {
		    "source": "Pain",
		    "target": "Psychotic disorder",
		    "weight": 0.0476
		  },
		  {
		    "source": "Pain",
		    "target": "Pulmonary embolism",
		    "weight": 0.125
		  },
		  {
		    "source": "Pain",
		    "target": "Radiculitis brachial",
		    "weight": 0.0714
		  },
		  {
		    "source": "Pain",
		    "target": "Road traffic accident",
		    "weight": 0.2667
		  },
		  {
		    "source": "Pain",
		    "target": "Scar",
		    "weight": 0.0476
		  },
		  {
		    "source": "Pain",
		    "target": "Sleep disorder",
		    "weight": 0.0714
		  },
		  {
		    "source": "Pain",
		    "target": "Therapeutic response unexpected",
		    "weight": 0.0714
		  },
		  {
		    "source": "Pain",
		    "target": "Thoracic outlet syndrome",
		    "weight": 0.0714
		  },
		  {
		    "source": "Pain",
		    "target": "Tooth infection",
		    "weight": 0.0476
		  },
		  {
		    "source": "Pain",
		    "target": "Tooth loss",
		    "weight": 0.0476
		  },
		  {
		    "source": "Pain",
		    "target": "Toothache",
		    "weight": 0.0476
		  },
		  {
		    "source": "Pain in extremity",
		    "target": "Palpitations",
		    "weight": 0.25
		  },
		  {
		    "source": "Pain in extremity",
		    "target": "Paraesthesia",
		    "weight": 0.1
		  },
		  {
		    "source": "Pain in extremity",
		    "target": "Product substitution issue",
		    "weight": 0.1
		  },
		  {
		    "source": "Pain in extremity",
		    "target": "Road traffic accident",
		    "weight": 0.2667
		  },
		  {
		    "source": "Pain in extremity",
		    "target": "Vertigo",
		    "weight": 0.1
		  },
		  {
		    "source": "Pain in jaw",
		    "target": "Palpitations",
		    "weight": 0.0769
		  },
		  {
		    "source": "Pain in jaw",
		    "target": "Pyrexia",
		    "weight": 0.0769
		  },
		  {
		    "source": "Pain in jaw",
		    "target": "Vomiting",
		    "weight": 0.0769
		  },
		  {
		    "source": "Palpitations",
		    "target": "Product use issue",
		    "weight": 0.25
		  },
		  {
		    "source": "Palpitations",
		    "target": "Pyrexia",
		    "weight": 0.0769
		  },
		  {
		    "source": "Palpitations",
		    "target": "Vomiting",
		    "weight": 0.0769
		  },
		  {
		    "source": "Panic attack",
		    "target": "Poor quality sleep",
		    "weight": 0.0476
		  },
		  {
		    "source": "Panic attack",
		    "target": "Psychotic disorder",
		    "weight": 0.0476
		  },
		  {
		    "source": "Panic attack",
		    "target": "Scar",
		    "weight": 0.0476
		  },
		  {
		    "source": "Panic attack",
		    "target": "Surgery",
		    "weight": 0.2
		  },
		  {
		    "source": "Panic attack",
		    "target": "Tooth infection",
		    "weight": 0.0476
		  },
		  {
		    "source": "Panic attack",
		    "target": "Tooth loss",
		    "weight": 0.0476
		  },
		  {
		    "source": "Panic attack",
		    "target": "Toothache",
		    "weight": 0.0476
		  },
		  {
		    "source": "Panic attack",
		    "target": "Weight decreased",
		    "weight": 0.1111
		  },
		  {
		    "source": "Panic disorder",
		    "target": "Thinking abnormal",
		    "weight": 0.125
		  },
		  {
		    "source": "Paraesthesia",
		    "target": "Paraesthesia oral",
		    "weight": 0.25
		  },
		  {
		    "source": "Paraesthesia",
		    "target": "Product substitution issue",
		    "weight": 0.2667
		  },
		  {
		    "source": "Paraesthesia",
		    "target": "Product use issue",
		    "weight": 0.0714
		  },
		  {
		    "source": "Paraesthesia",
		    "target": "Radiculitis brachial",
		    "weight": 0.0714
		  },
		  {
		    "source": "Paraesthesia",
		    "target": "Sensory loss",
		    "weight": 0.5
		  },
		  {
		    "source": "Paraesthesia",
		    "target": "Skin discolouration",
		    "weight": 0.2
		  },
		  {
		    "source": "Paraesthesia",
		    "target": "Sleep disorder",
		    "weight": 0.0714
		  },
		  {
		    "source": "Paraesthesia",
		    "target": "Therapeutic response unexpected",
		    "weight": 0.0714
		  },
		  {
		    "source": "Paraesthesia",
		    "target": "Thoracic outlet syndrome",
		    "weight": 0.0714
		  },
		  {
		    "source": "Paraesthesia",
		    "target": "Tinnitus",
		    "weight": 0.1667
		  },
		  {
		    "source": "Paraesthesia",
		    "target": "Vertigo",
		    "weight": 0.1
		  },
		  {
		    "source": "Paraesthesia",
		    "target": "Yellow skin",
		    "weight": 0.2
		  },
		  {
		    "source": "Paranasal sinus hypersecretion",
		    "target": "Pharyngitis streptococcal",
		    "weight": 0.1
		  },
		  {
		    "source": "Paranasal sinus hypersecretion",
		    "target": "Pyrexia",
		    "weight": 0.1
		  },
		  {
		    "source": "Paranasal sinus hypersecretion",
		    "target": "Rales",
		    "weight": 0.1
		  },
		  {
		    "source": "Paranasal sinus hypersecretion",
		    "target": "Upper respiratory tract infection",
		    "weight": 0.1
		  },
		  {
		    "source": "Paranasal sinus hypersecretion",
		    "target": "Vomiting",
		    "weight": 0.1
		  },
		  {
		    "source": "Paranoia",
		    "target": "Product quality issue",
		    "weight": 0.1111
		  },
		  {
		    "source": "Paranoia",
		    "target": "Psychomotor hyperactivity",
		    "weight": 0.1111
		  },
		  {
		    "source": "Paranoia",
		    "target": "Psychotic disorder",
		    "weight": 0.25
		  },
		  {
		    "source": "Paranoia",
		    "target": "Restlessness",
		    "weight": 0.1111
		  },
		  {
		    "source": "Performance status decreased",
		    "target": "Prescribed overdose",
		    "weight": 0.375
		  },
		  {
		    "source": "Performance status decreased",
		    "target": "Product quality issue",
		    "weight": 0.5769
		  },
		  {
		    "source": "Performance status decreased",
		    "target": "Somnolence",
		    "weight": 0.0769
		  },
		  {
		    "source": "Performance status decreased",
		    "target": "Therapy cessation",
		    "weight": 0.125
		  },
		  {
		    "source": "Performance status decreased",
		    "target": "Wrong technique in product usage process",
		    "weight": 0.0769
		  },
		  {
		    "source": "Peripheral swelling",
		    "target": "Pulmonary arterial hypertension",
		    "weight": 0.1
		  },
		  {
		    "source": "Peripheral swelling",
		    "target": "Respiratory failure",
		    "weight": 0.1
		  },
		  {
		    "source": "Peripheral swelling",
		    "target": "Right ventricular failure",
		    "weight": 0.1
		  },
		  {
		    "source": "Personality change",
		    "target": "Weight decreased",
		    "weight": 0.1429
		  },
		  {
		    "source": "Pharyngitis streptococcal",
		    "target": "Pyrexia",
		    "weight": 0.1
		  },
		  {
		    "source": "Pharyngitis streptococcal",
		    "target": "Rales",
		    "weight": 0.1
		  },
		  {
		    "source": "Pharyngitis streptococcal",
		    "target": "Upper respiratory tract infection",
		    "weight": 0.1
		  },
		  {
		    "source": "Pharyngitis streptococcal",
		    "target": "Vomiting",
		    "weight": 0.1
		  },
		  {
		    "source": "Pleural effusion",
		    "target": "Severe acute respiratory syndrome",
		    "weight": 0.0769
		  },
		  {
		    "source": "Pleural effusion",
		    "target": "Stress",
		    "weight": 0.0769
		  },
		  {
		    "source": "Pleural effusion",
		    "target": "Tearfulness",
		    "weight": 0.0769
		  },
		  {
		    "source": "Pleural effusion",
		    "target": "Viral infection",
		    "weight": 0.0769
		  },
		  {
		    "source": "Pleural effusion",
		    "target": "Vomiting",
		    "weight": 0.0769
		  },
		  {
		    "source": "Pneumonia",
		    "target": "Rash pruritic",
		    "weight": 0.0526
		  },
		  {
		    "source": "Pneumonia",
		    "target": "Rash pustular",
		    "weight": 0.0526
		  },
		  {
		    "source": "Pneumonia",
		    "target": "Restlessness",
		    "weight": 0.0769
		  },
		  {
		    "source": "Pneumonia",
		    "target": "Skin mass",
		    "weight": 0.0526
		  },
		  {
		    "source": "Pneumonia",
		    "target": "Therapy cessation",
		    "weight": 0.0526
		  },
		  {
		    "source": "Pneumonia",
		    "target": "Thirst",
		    "weight": 0.0769
		  },
		  {
		    "source": "Pneumonia",
		    "target": "Urinary hesitation",
		    "weight": 0.0526
		  },
		  {
		    "source": "Pneumonia",
		    "target": "Urinary retention",
		    "weight": 0.0526
		  },
		  {
		    "source": "Pneumonia",
		    "target": "Vertigo",
		    "weight": 0.0526
		  },
		  {
		    "source": "Poor quality sleep",
		    "target": "Psychotic disorder",
		    "weight": 0.0476
		  },
		  {
		    "source": "Poor quality sleep",
		    "target": "Scar",
		    "weight": 0.0476
		  },
		  {
		    "source": "Poor quality sleep",
		    "target": "Tooth infection",
		    "weight": 0.0476
		  },
		  {
		    "source": "Poor quality sleep",
		    "target": "Tooth loss",
		    "weight": 0.0476
		  },
		  {
		    "source": "Poor quality sleep",
		    "target": "Toothache",
		    "weight": 0.0476
		  },
		  {
		    "source": "Post procedural discomfort",
		    "target": "Procedural pain",
		    "weight": 0.0769
		  },
		  {
		    "source": "Post procedural discomfort",
		    "target": "Uterine perforation",
		    "weight": 0.0769
		  },
		  {
		    "source": "Post-traumatic neck syndrome",
		    "target": "Road traffic accident",
		    "weight": 0.2
		  },
		  {
		    "source": "Pre-existing condition improved",
		    "target": "Therapeutic response unexpected",
		    "weight": 0.3333
		  },
		  {
		    "source": "Premature delivery",
		    "target": "Rhesus incompatibility",
		    "weight": 0.2
		  },
		  {
		    "source": "Premature delivery",
		    "target": "Transfusion",
		    "weight": 0.2
		  },
		  {
		    "source": "Prescribed overdose",
		    "target": "Product use issue",
		    "weight": 0.125
		  },
		  {
		    "source": "Prescribed overdose",
		    "target": "Seizure",
		    "weight": 0.1667
		  },
		  {
		    "source": "Prescribed overdose",
		    "target": "Therapeutic response unexpected",
		    "weight": 0.5
		  },
		  {
		    "source": "Prescribed overdose",
		    "target": "Therapy cessation",
		    "weight": 0.125
		  },
		  {
		    "source": "Prescribed underdose",
		    "target": "White blood cell count increased",
		    "weight": 0.3333
		  },
		  {
		    "source": "Procedural pain",
		    "target": "Uterine perforation",
		    "weight": 0.0769
		  },
		  {
		    "source": "Product quality issue",
		    "target": "Product tampering",
		    "weight": 0.3333
		  },
		  {
		    "source": "Product quality issue",
		    "target": "Product use issue",
		    "weight": 0.1429
		  },
		  {
		    "source": "Product quality issue",
		    "target": "Psychiatric symptom",
		    "weight": 0.125
		  },
		  {
		    "source": "Product quality issue",
		    "target": "Psychomotor hyperactivity",
		    "weight": 0.9278
		  },
		  {
		    "source": "Product quality issue",
		    "target": "Restlessness",
		    "weight": 0.2778
		  },
		  {
		    "source": "Product quality issue",
		    "target": "Sleep disorder",
		    "weight": 0.1429
		  },
		  {
		    "source": "Product quality issue",
		    "target": "Sluggishness",
		    "weight": 0.25
		  },
		  {
		    "source": "Product quality issue",
		    "target": "Somnambulism",
		    "weight": 0.2
		  },
		  {
		    "source": "Product quality issue",
		    "target": "Somnolence",
		    "weight": 0.8345
		  },
		  {
		    "source": "Product quality issue",
		    "target": "Stress",
		    "weight": 0.0909
		  },
		  {
		    "source": "Product quality issue",
		    "target": "Vitamin D deficiency",
		    "weight": 0.25
		  },
		  {
		    "source": "Product quality issue",
		    "target": "Wrist fracture",
		    "weight": 0.1429
		  },
		  {
		    "source": "Product quality issue",
		    "target": "Wrong technique in product usage process",
		    "weight": 3.269
		  },
		  {
		    "source": "Product quality issue",
		    "target": "Yawning",
		    "weight": 0.0909
		  },
		  {
		    "source": "Product substitution issue",
		    "target": "Therapeutic product ineffective",
		    "weight": 0.5
		  },
		  {
		    "source": "Product substitution issue",
		    "target": "Tinnitus",
		    "weight": 0.1667
		  },
		  {
		    "source": "Product substitution issue",
		    "target": "Vertigo",
		    "weight": 0.1
		  },
		  {
		    "source": "Product use issue",
		    "target": "Radiculitis brachial",
		    "weight": 0.0714
		  },
		  {
		    "source": "Product use issue",
		    "target": "Sleep disorder",
		    "weight": 0.0714
		  },
		  {
		    "source": "Product use issue",
		    "target": "Therapeutic response unexpected",
		    "weight": 0.0714
		  },
		  {
		    "source": "Product use issue",
		    "target": "Thoracic outlet syndrome",
		    "weight": 0.0714
		  },
		  {
		    "source": "Product use issue",
		    "target": "Weight increased",
		    "weight": 0.2
		  },
		  {
		    "source": "Product use issue",
		    "target": "Wrong technique in product usage process",
		    "weight": 0.1429
		  },
		  {
		    "source": "Pruritus",
		    "target": "Rash",
		    "weight": 0.5
		  },
		  {
		    "source": "Pruritus",
		    "target": "Scab",
		    "weight": 0.25
		  },
		  {
		    "source": "Pruritus",
		    "target": "Swelling face",
		    "weight": 0.25
		  },
		  {
		    "source": "Pruritus",
		    "target": "Tearfulness",
		    "weight": 0.3333
		  },
		  {
		    "source": "Pruritus",
		    "target": "Urticaria",
		    "weight": 0.25
		  },
		  {
		    "source": "Pruritus",
		    "target": "Wrong technique in product usage process",
		    "weight": 0.25
		  },
		  {
		    "source": "Pruritus generalised",
		    "target": "Skin exfoliation",
		    "weight": 0.5
		  },
		  {
		    "source": "Pseudomonas infection",
		    "target": "Sinus disorder",
		    "weight": 0.1
		  },
		  {
		    "source": "Pseudomonas infection",
		    "target": "Weight increased",
		    "weight": 0.1
		  },
		  {
		    "source": "Psychiatric symptom",
		    "target": "Wrong technique in product usage process",
		    "weight": 0.125
		  },
		  {
		    "source": "Psychomotor hyperactivity",
		    "target": "Restlessness",
		    "weight": 0.2778
		  },
		  {
		    "source": "Psychomotor hyperactivity",
		    "target": "Somnolence",
		    "weight": 0.0769
		  },
		  {
		    "source": "Psychomotor hyperactivity",
		    "target": "Tourette's disorder",
		    "weight": 0.0833
		  },
		  {
		    "source": "Psychomotor hyperactivity",
		    "target": "Weight increased",
		    "weight": 0.0833
		  },
		  {
		    "source": "Psychotic disorder",
		    "target": "Scar",
		    "weight": 0.0476
		  },
		  {
		    "source": "Psychotic disorder",
		    "target": "Tooth infection",
		    "weight": 0.0476
		  },
		  {
		    "source": "Psychotic disorder",
		    "target": "Tooth loss",
		    "weight": 0.0476
		  },
		  {
		    "source": "Psychotic disorder",
		    "target": "Toothache",
		    "weight": 0.0476
		  },
		  {
		    "source": "Pulmonary arterial hypertension",
		    "target": "Respiratory failure",
		    "weight": 0.1
		  },
		  {
		    "source": "Pulmonary arterial hypertension",
		    "target": "Right ventricular failure",
		    "weight": 0.1
		  },
		  {
		    "source": "Pulmonary mass",
		    "target": "Sarcoidosis",
		    "weight": 0.5
		  },
		  {
		    "source": "Pyrexia",
		    "target": "Rales",
		    "weight": 0.1
		  },
		  {
		    "source": "Pyrexia",
		    "target": "Seizure",
		    "weight": 0.0833
		  },
		  {
		    "source": "Pyrexia",
		    "target": "Syncope",
		    "weight": 0.0833
		  },
		  {
		    "source": "Pyrexia",
		    "target": "Unevaluable event",
		    "weight": 0.0833
		  },
		  {
		    "source": "Pyrexia",
		    "target": "Upper respiratory tract infection",
		    "weight": 0.1
		  },
		  {
		    "source": "Pyrexia",
		    "target": "Vomiting",
		    "weight": 0.4269
		  },
		  {
		    "source": "Radiculitis brachial",
		    "target": "Sleep disorder",
		    "weight": 0.0714
		  },
		  {
		    "source": "Radiculitis brachial",
		    "target": "Therapeutic response unexpected",
		    "weight": 0.0714
		  },
		  {
		    "source": "Radiculitis brachial",
		    "target": "Thoracic outlet syndrome",
		    "weight": 0.0714
		  },
		  {
		    "source": "Rales",
		    "target": "Upper respiratory tract infection",
		    "weight": 0.1
		  },
		  {
		    "source": "Rales",
		    "target": "Vomiting",
		    "weight": 0.1
		  },
		  {
		    "source": "Rapid eye movements sleep abnormal",
		    "target": "Road traffic accident",
		    "weight": 0.0588
		  },
		  {
		    "source": "Rapid eye movements sleep abnormal",
		    "target": "Underweight",
		    "weight": 0.0588
		  },
		  {
		    "source": "Rapid eye movements sleep abnormal",
		    "target": "Weight increased",
		    "weight": 0.0588
		  },
		  {
		    "source": "Rash",
		    "target": "Respiratory tract infection",
		    "weight": 0.25
		  },
		  {
		    "source": "Rash",
		    "target": "Toxicity to various agents",
		    "weight": 0.25
		  },
		  {
		    "source": "Rash erythematous",
		    "target": "Rash macular",
		    "weight": 0.3333
		  },
		  {
		    "source": "Rash erythematous",
		    "target": "Rash pruritic",
		    "weight": 0.3333
		  },
		  {
		    "source": "Rash macular",
		    "target": "Rash pruritic",
		    "weight": 0.3333
		  },
		  {
		    "source": "Rash pruritic",
		    "target": "Rash pustular",
		    "weight": 0.0526
		  },
		  {
		    "source": "Rash pruritic",
		    "target": "Skin mass",
		    "weight": 0.0526
		  },
		  {
		    "source": "Rash pruritic",
		    "target": "Therapy cessation",
		    "weight": 0.0526
		  },
		  {
		    "source": "Rash pruritic",
		    "target": "Urinary hesitation",
		    "weight": 0.0526
		  },
		  {
		    "source": "Rash pruritic",
		    "target": "Urinary retention",
		    "weight": 0.0526
		  },
		  {
		    "source": "Rash pruritic",
		    "target": "Vertigo",
		    "weight": 0.0526
		  },
		  {
		    "source": "Rash pustular",
		    "target": "Skin mass",
		    "weight": 0.0526
		  },
		  {
		    "source": "Rash pustular",
		    "target": "Therapy cessation",
		    "weight": 0.0526
		  },
		  {
		    "source": "Rash pustular",
		    "target": "Urinary hesitation",
		    "weight": 0.0526
		  },
		  {
		    "source": "Rash pustular",
		    "target": "Urinary retention",
		    "weight": 0.0526
		  },
		  {
		    "source": "Rash pustular",
		    "target": "Vertigo",
		    "weight": 0.0526
		  },
		  {
		    "source": "Rebound effect",
		    "target": "Somnolence",
		    "weight": 0.1667
		  },
		  {
		    "source": "Respiratory failure",
		    "target": "Right ventricular failure",
		    "weight": 0.1
		  },
		  {
		    "source": "Respiratory tract infection",
		    "target": "Toxicity to various agents",
		    "weight": 0.25
		  },
		  {
		    "source": "Restlessness",
		    "target": "Sleep disorder",
		    "weight": 0.25
		  },
		  {
		    "source": "Restlessness",
		    "target": "Thirst",
		    "weight": 0.0769
		  },
		  {
		    "source": "Retching",
		    "target": "Trismus",
		    "weight": 0.2
		  },
		  {
		    "source": "Retching",
		    "target": "Vomiting",
		    "weight": 0.2
		  },
		  {
		    "source": "Rhesus incompatibility",
		    "target": "Transfusion",
		    "weight": 0.2
		  },
		  {
		    "source": "Rhinalgia",
		    "target": "Sinus headache",
		    "weight": 0.2
		  },
		  {
		    "source": "Road traffic accident",
		    "target": "Underweight",
		    "weight": 0.0588
		  },
		  {
		    "source": "Road traffic accident",
		    "target": "Unevaluable event",
		    "weight": 0.2
		  },
		  {
		    "source": "Road traffic accident",
		    "target": "Weight increased",
		    "weight": 0.0588
		  },
		  {
		    "source": "Scab",
		    "target": "Urticaria",
		    "weight": 0.25
		  },
		  {
		    "source": "Scab",
		    "target": "Wrong technique in product usage process",
		    "weight": 0.25
		  },
		  {
		    "source": "Scar",
		    "target": "Tooth infection",
		    "weight": 0.0476
		  },
		  {
		    "source": "Scar",
		    "target": "Tooth loss",
		    "weight": 0.0476
		  },
		  {
		    "source": "Scar",
		    "target": "Toothache",
		    "weight": 0.0476
		  },
		  {
		    "source": "Screaming",
		    "target": "Tremor",
		    "weight": 0.1
		  },
		  {
		    "source": "Screaming",
		    "target": "Wrong technique in product usage process",
		    "weight": 0.1
		  },
		  {
		    "source": "Seizure",
		    "target": "Syncope",
		    "weight": 0.0833
		  },
		  {
		    "source": "Seizure",
		    "target": "Unevaluable event",
		    "weight": 0.0833
		  },
		  {
		    "source": "Self injurious behaviour",
		    "target": "Suicidal ideation",
		    "weight": 0.1429
		  },
		  {
		    "source": "Sensory loss",
		    "target": "Tremor",
		    "weight": 0.25
		  },
		  {
		    "source": "Serotonin syndrome",
		    "target": "Tachyphrenia",
		    "weight": 0.1
		  },
		  {
		    "source": "Severe acute respiratory syndrome",
		    "target": "Stress",
		    "weight": 0.0769
		  },
		  {
		    "source": "Severe acute respiratory syndrome",
		    "target": "Tearfulness",
		    "weight": 0.0769
		  },
		  {
		    "source": "Severe acute respiratory syndrome",
		    "target": "Viral infection",
		    "weight": 0.0769
		  },
		  {
		    "source": "Severe acute respiratory syndrome",
		    "target": "Vomiting",
		    "weight": 0.0769
		  },
		  {
		    "source": "Sinus disorder",
		    "target": "Sleep apnoea syndrome",
		    "weight": 0.2
		  },
		  {
		    "source": "Sinus disorder",
		    "target": "Upper-airway cough syndrome",
		    "weight": 0.2
		  },
		  {
		    "source": "Sinus disorder",
		    "target": "Weight increased",
		    "weight": 0.1
		  },
		  {
		    "source": "Skin discolouration",
		    "target": "Yellow skin",
		    "weight": 0.2
		  },
		  {
		    "source": "Skin mass",
		    "target": "Therapy cessation",
		    "weight": 0.0526
		  },
		  {
		    "source": "Skin mass",
		    "target": "Urinary hesitation",
		    "weight": 0.0526
		  },
		  {
		    "source": "Skin mass",
		    "target": "Urinary retention",
		    "weight": 0.0526
		  },
		  {
		    "source": "Skin mass",
		    "target": "Vertigo",
		    "weight": 0.0526
		  },
		  {
		    "source": "Sleep apnoea syndrome",
		    "target": "Upper-airway cough syndrome",
		    "weight": 0.2
		  },
		  {
		    "source": "Sleep disorder",
		    "target": "Therapeutic response unexpected",
		    "weight": 0.0714
		  },
		  {
		    "source": "Sleep disorder",
		    "target": "Thoracic outlet syndrome",
		    "weight": 0.0714
		  },
		  {
		    "source": "Sleep disorder",
		    "target": "Wrist fracture",
		    "weight": 0.1429
		  },
		  {
		    "source": "Social avoidant behaviour",
		    "target": "Thirst",
		    "weight": 0.0714
		  },
		  {
		    "source": "Social avoidant behaviour",
		    "target": "Tic",
		    "weight": 0.0556
		  },
		  {
		    "source": "Social avoidant behaviour",
		    "target": "Victim of abuse",
		    "weight": 0.0714
		  },
		  {
		    "source": "Social avoidant behaviour",
		    "target": "Victim of sexual abuse",
		    "weight": 0.0714
		  },
		  {
		    "source": "Social avoidant behaviour",
		    "target": "Vomiting",
		    "weight": 0.0556
		  },
		  {
		    "source": "Social avoidant behaviour",
		    "target": "Weight increased",
		    "weight": 0.0714
		  },
		  {
		    "source": "Social phobia",
		    "target": "Tachyphrenia",
		    "weight": 0.0455
		  },
		  {
		    "source": "Social phobia",
		    "target": "Weight increased",
		    "weight": 0.0455
		  },
		  {
		    "source": "Somnolence",
		    "target": "Stress",
		    "weight": 0.0909
		  },
		  {
		    "source": "Somnolence",
		    "target": "Wrong technique in product usage process",
		    "weight": 0.1678
		  },
		  {
		    "source": "Somnolence",
		    "target": "Yawning",
		    "weight": 0.0909
		  },
		  {
		    "source": "Spinal osteoarthritis",
		    "target": "Therapeutic response unexpected",
		    "weight": 0.25
		  },
		  {
		    "source": "Stereotypy",
		    "target": "Tic",
		    "weight": 0.3333
		  },
		  {
		    "source": "Stress",
		    "target": "Tearfulness",
		    "weight": 0.0769
		  },
		  {
		    "source": "Stress",
		    "target": "Viral infection",
		    "weight": 0.0769
		  },
		  {
		    "source": "Stress",
		    "target": "Vomiting",
		    "weight": 0.0769
		  },
		  {
		    "source": "Stress",
		    "target": "Wrong technique in product usage process",
		    "weight": 0.0909
		  },
		  {
		    "source": "Stress",
		    "target": "Yawning",
		    "weight": 0.0909
		  },
		  {
		    "source": "Suicidal ideation",
		    "target": "Suicide attempt",
		    "weight": 0.1667
		  },
		  {
		    "source": "Syncope",
		    "target": "Unevaluable event",
		    "weight": 0.0833
		  },
		  {
		    "source": "Syncope",
		    "target": "Weight decreased",
		    "weight": 0.5
		  },
		  {
		    "source": "Syringe issue",
		    "target": "Underweight",
		    "weight": 0.5
		  },
		  {
		    "source": "Tachyphrenia",
		    "target": "Tension",
		    "weight": 0.2
		  },
		  {
		    "source": "Tachyphrenia",
		    "target": "Weight increased",
		    "weight": 0.0455
		  },
		  {
		    "source": "Tearfulness",
		    "target": "Viral infection",
		    "weight": 0.0769
		  },
		  {
		    "source": "Tearfulness",
		    "target": "Vomiting",
		    "weight": 0.0769
		  },
		  {
		    "source": "Therapeutic response unexpected",
		    "target": "Thoracic outlet syndrome",
		    "weight": 0.0714
		  },
		  {
		    "source": "Therapy cessation",
		    "target": "Urinary hesitation",
		    "weight": 0.0526
		  },
		  {
		    "source": "Therapy cessation",
		    "target": "Urinary retention",
		    "weight": 0.0526
		  },
		  {
		    "source": "Therapy cessation",
		    "target": "Vertigo",
		    "weight": 0.0526
		  },
		  {
		    "source": "Thirst",
		    "target": "Victim of abuse",
		    "weight": 0.0714
		  },
		  {
		    "source": "Thirst",
		    "target": "Victim of sexual abuse",
		    "weight": 0.0714
		  },
		  {
		    "source": "Thirst",
		    "target": "Weight increased",
		    "weight": 0.0714
		  },
		  {
		    "source": "Thyroid disorder",
		    "target": "Vision blurred",
		    "weight": 0.3333
		  },
		  {
		    "source": "Tic",
		    "target": "Vomiting",
		    "weight": 0.0556
		  },
		  {
		    "source": "Tooth infection",
		    "target": "Tooth loss",
		    "weight": 0.0476
		  },
		  {
		    "source": "Tooth infection",
		    "target": "Toothache",
		    "weight": 0.0476
		  },
		  {
		    "source": "Tooth loss",
		    "target": "Toothache",
		    "weight": 0.0476
		  },
		  {
		    "source": "Tourette's disorder",
		    "target": "Weight increased",
		    "weight": 0.0833
		  },
		  {
		    "source": "Tremor",
		    "target": "Wrong technique in product usage process",
		    "weight": 0.1
		  },
		  {
		    "source": "Trismus",
		    "target": "Vomiting",
		    "weight": 0.2
		  },
		  {
		    "source": "Underdose",
		    "target": "Wrong technique in product usage process",
		    "weight": 0.25
		  },
		  {
		    "source": "Underweight",
		    "target": "Weight increased",
		    "weight": 0.0588
		  },
		  {
		    "source": "Upper respiratory tract infection",
		    "target": "Vomiting",
		    "weight": 0.1
		  },
		  {
		    "source": "Urinary hesitation",
		    "target": "Urinary retention",
		    "weight": 0.0526
		  },
		  {
		    "source": "Urinary hesitation",
		    "target": "Vertigo",
		    "weight": 0.0526
		  },
		  {
		    "source": "Urinary retention",
		    "target": "Vertigo",
		    "weight": 0.0526
		  },
		  {
		    "source": "Urticaria",
		    "target": "Wrong technique in product usage process",
		    "weight": 0.25
		  },
		  {
		    "source": "Vaginal discharge",
		    "target": "Vaginal pH increased",
		    "weight": 0.0909
		  },
		  {
		    "source": "Vaginal discharge",
		    "target": "Vulvovaginal dryness",
		    "weight": 0.0909
		  },
		  {
		    "source": "Vaginal discharge",
		    "target": "Vulvovaginal erythema",
		    "weight": 0.0909
		  },
		  {
		    "source": "Vaginal discharge",
		    "target": "Vulvovaginal pain",
		    "weight": 0.0909
		  },
		  {
		    "source": "Vaginal discharge",
		    "target": "Vulvovaginal swelling",
		    "weight": 0.0909
		  },
		  {
		    "source": "Vaginal pH increased",
		    "target": "Vulvovaginal dryness",
		    "weight": 0.0909
		  },
		  {
		    "source": "Vaginal pH increased",
		    "target": "Vulvovaginal erythema",
		    "weight": 0.0909
		  },
		  {
		    "source": "Vaginal pH increased",
		    "target": "Vulvovaginal pain",
		    "weight": 0.0909
		  },
		  {
		    "source": "Vaginal pH increased",
		    "target": "Vulvovaginal swelling",
		    "weight": 0.0909
		  },
		  {
		    "source": "Victim of abuse",
		    "target": "Victim of sexual abuse",
		    "weight": 0.0714
		  },
		  {
		    "source": "Victim of abuse",
		    "target": "Weight increased",
		    "weight": 0.0714
		  },
		  {
		    "source": "Victim of sexual abuse",
		    "target": "Weight increased",
		    "weight": 0.0714
		  },
		  {
		    "source": "Viral infection",
		    "target": "Vomiting",
		    "weight": 0.0769
		  },
		  {
		    "source": "Vision blurred",
		    "target": "Visual acuity reduced",
		    "weight": 0.2
		  },
		  {
		    "source": "Vitamin D abnormal",
		    "target": "Vitreous floaters",
		    "weight": 0.0833
		  },
		  {
		    "source": "Vulvovaginal dryness",
		    "target": "Vulvovaginal erythema",
		    "weight": 0.0909
		  },
		  {
		    "source": "Vulvovaginal dryness",
		    "target": "Vulvovaginal pain",
		    "weight": 0.0909
		  },
		  {
		    "source": "Vulvovaginal dryness",
		    "target": "Vulvovaginal swelling",
		    "weight": 0.0909
		  },
		  {
		    "source": "Vulvovaginal erythema",
		    "target": "Vulvovaginal pain",
		    "weight": 0.0909
		  },
		  {
		    "source": "Vulvovaginal erythema",
		    "target": "Vulvovaginal swelling",
		    "weight": 0.0909
		  },
		  {
		    "source": "Vulvovaginal pain",
		    "target": "Vulvovaginal swelling",
		    "weight": 0.0909
		  },
		  {
		    "source": "Wrong technique in product usage process",
		    "target": "Yawning",
		    "weight": 0.0909
		  }
  ]
};

function networkGraph(location, nodeSub, linkSub){
const r = 3;

var svg = d3.select(location),
    width = +svg.attr("width"),
    height = +svg.attr("height");

var color = d3.scaleOrdinal(d3.schemeCategory20);

var simulation = d3.forceSimulation()
    .force("link", d3.forceLink().id(function(d) { return d.id; }))
    .force("charge", d3.forceManyBody().strength(-1))
    .force("center", d3.forceCenter(width / 2, height / 2))
    ;

  var link = svg.append("g")
      .attr("class", "links")
      .selectAll("line")
      .data(linkSub)
      .enter().append("line")
      .attr("stroke-width", function(d) { return Math.sqrt(d.weight); });

  var node = svg.append("g")
      .attr("class", "nodes")
      .selectAll("circle")
      .data(nodeSub)
      .enter().append("circle")
      .attr("r", r)
      .attr("fill", function(d) { return color(d.group); })
      .call(d3.drag()
          .on("start", dragstarted)
          .on("drag", dragged)
          .on("end", dragended));

  node.append("title")
      .text(function(d) { return d.id; });

  simulation
      .nodes(nodeSub)
      .on("tick", ticked);

  simulation.force("link")
      .links(linkSub);

  function ticked() {
    link
        .attr("x1", function(d) { return d.source.x; })
        .attr("y1", function(d) { return d.source.y; })
        .attr("x2", function(d) { return d.target.x; })
        .attr("y2", function(d) { return d.target.y; });

    node
         .attr("cx", function(d) { return d.x = Math.max(r, Math.min(width - r, d.x)); }) 
         .attr("cy", function(d) { return d.y = Math.max(r, Math.min(height - r, d.y)); });
  };

function dragstarted(d) {
  if (!d3.event.active) simulation.alphaTarget(0.3).restart();
  d.fx = d.x;
  d.fy = d.y;
}

function dragged(d) {
  d.fx = d3.event.x;
  d.fy = d3.event.y;
}

function dragended(d) {
  if (!d3.event.active) simulation.alphaTarget(0);
  d.fx = null;
  d.fy = null;
}
}

networkGraph("#Comorb", graph.nodes, graph.links);

</script>


</div>
</p>


