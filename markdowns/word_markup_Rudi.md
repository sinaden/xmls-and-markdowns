



# Motivation
  
**For what purpose was the dataset created?**  
  
Infections are the leading cause of mortality in CLL. Risk of Infection is increased upon CLL treatment and currently we have no model that is able to predict risk of infection upon CLL treatment. The dataset created puts together various sources of time-series electronic health records on CLL patients in Denmark. This also includes outcome on death, treatment and infection. Using this data set we aim to both model risk of infection upon CLL treatment and uncover risk factors responsible for low immune function and duration of treatment response upon different treatment regimens   
  
**Who created the dataset (e.g., which team, research group) and on behalf of which entity (e.g., company, institution, organization)?**  
  
Dataset was created by the CLL Laboratory at Rigshospitalet, Copenhagen University Hospital using data from the national CLL registry and PERSIMUNE data warehouse.  
  
**Who funded the creation of the dataset?**  
  
Novo Nordisk Foundation (grant NNF16OC0019302) and Danish Cancer Society  
  
**Any other comments?**  
  
 <i> not answered </i>  

# Composition
  
**What do the instances that comprise the dataset represent (e.g., samples, images, people)?**  
  
Dataset represents electronic health record data from various data sources collected on CLL Patients in Denmark. Baseline: Each instance is a single CLL patient and their set of CLL prognostic factor variables taken around time of CLL diagnosis
CLL Registry: Each instance is a single CLL patient and extracted from the National CLL Registry that contains information on several clinically relevant outcome like treatment and death. Treatment Outcome data contains information on line of CLL treatment and type of CLL treatment. Each instance is a line of treatment – hence multiple instances for patients with multiple lines of treatment. For the following each instance is one patient event – hence multiple instances for patients with multiple events – where events are a diagnosis, pathology, laboratory test, prescription, lab culture. Diagnosis: Historical data on previous patient diagnosis - not necessarily those related to CLL. Laboratory: Laboratory tests – not necessarily related to CLL. Pathology: Historical data on previous patient pathology - not necessarily related to CLL. Laboratory Cultures: data for different type of cultures taken for a given patient – thereby holding information on CLL related infections. Medications: Historical data on prescribed medications - not necessarily related to CLL
  
  
**How many instances are there in total?**  
  
Baseline: 4999 (each instance is a unique patient)
CLL Registry:4999 (each instance is a unique patient)
Treatment Outcome:1996 (No, or multiple instances for each patient possible)
Diagnosis:147197 (No, or multiple instances for each patient possible)
Laboratory:4226248 (No, or multiple instances for each patient possible)
Pathology:199337 (No, or multiple instances for each patient possible)
Laboratory Cultures:84299 (No, or multiple instances for each patient possible)
Medications:1098273 (No, or multiple instances for each patient possible)
  
  
**Does the dataset contain all possible instances or is it a sample (not necessarily random) of instances from a larger set?**  
  
CLL Registry contains data on all CLL patient in Denmark. Remaining datasets have missingness both at random and not at random.  
  
**What data does each instance consist of?**  
  
Each data instance is an instance of a patient record – hence raw data. A single patient is therefore spread across several instances in different datasets.  For example, a particular laboratory test, or a single prescription of a medication, will hold an instance each. Features must then be derived from these raw data to generate just a single-row for each patient as is typical in a machine learning dataset.  
  
**Is there a label, target, or outcome (e.g., mortality) associated with each instance?**  
  
No, as each instance is raw data. Outcomes may be derived from CLL Registry, Treatment Outcome, and Laboratory Cultures datasets.  
  
**Is any information missing from individual instances?**  
  
No information has been redacted. Missing information can be missing at random and not at random.  
  
**Are relationships between individual instances made explicit (e.g., familial links, or samples derived from the same patient or same exposure)?**  
  
Yes. The patient id links different instances in a given dataset to a single patient, and similarly instances from other datasets related to the same patient.  
  
**Are there recommended data splits (e.g., training, development/validation, testing)?**  
  
No  
  
**Are there any errors, sources of noise, or redundancies in the dataset?**  
  
Yes. There are potential duplicates and some of the dates and times may also have errors. Errors may also be present in laboratory values.  
  
**Is the dataset self-contained, or does it link to or otherwise rely on external resources (e.g., websites, public databases, other datasets and/or private silos)?**  
  
Yes. Datasets is extracted from the National CLL registry and PERSIMUNE data warehouse and continuously updated.  
  
**Does the dataset contain data that might be considered confidential (e.g., data that is protected by legal privilege or by doctor-patient confidentiality, data that includes the content of individuals’ non-public communications)?**  
  
Yes  
  
**Does the dataset contain data that, if viewed directly, might be offensive, insulting, threatening, or might otherwise cause anxiety?**  
  
No  
  
**Does the dataset not relate to people (e.g., animals, cell lines, environment)?**  
  
DIRECT RELATION TO PEOPLE  
  
**Does the dataset identify any subpopulations (e.g., by age, gender, etc.)?**  
  
Age and gender are available and hence any information may be stratified according to these variables  
  
**Is it possible to identify individuals (i.e., one or more natural persons), either directly or indirectly (i.e., in combination with other data) from the dataset?**  
  
Patient IDs are pseudonymized in all datasets. It is potentially possible to identify individuals indirectly in combination with other data.  
  
**Does the dataset contain data that might be considered sensitive in any way (e.g., data that reveals racial or ethnic origins, sexual orientations, religious beliefs, political opinions or union memberships, or locations; financial or health data; biometric or genetic data; forms of government identification, such as social security numbers; criminal history)?**  
  
No  
  
**Any other comments?**  
  
 <i> not answered </i>  

# Collection Process
  
**How was the data associated with each instance acquired?**  
  
 <i> not answered </i>  
  
**What mechanisms or procedures were used to collect the data (e.g., hardware apparatus or sensor, manual human curation, software program, software API)?**  
  
 <i> not answered </i>  
  
**If the dataset is a sample from a larger set, what was the sampling strategy (e.g., deterministic, probabilistic with specific sampling probabilities)?**  
  
 <i> not answered </i>  
  
**Who was involved in the data collection process (e.g., students, crowdworkers, contractors) and how were they compensated (e.g., salaried, immaterial through prizes / authorship / etc) and how much (e.g., according to competitive scales mandated by [insert body or institution])?**  
  
 <i> not answered </i>  
  
**Over what timeframe was the data collected?**  
  
 <i> not answered </i>  
  
**Were any ethical review processes conducted (e.g., by an institutional review board)?**  
  
 <i> not answered </i>  
  
**Does the dataset not relate to people (e.g., animals, cell lines, environment)?**  
  
 <i> not answered </i>  
  
**Did you collect the data from the individuals in question directly, or obtain it via third parties or other sources (e.g., websites)?**  
  
 <i> not answered </i>  
  
**Were the individuals in question notified about the data collection?**  
  
 <i> not answered </i>  
  
**Did the individuals in question consent to the collection and use of their data?**  
  
 <i> not answered </i>  
  
**If consent was obtained, were the consenting individuals provided with a mechanism to revoke their consent in the future or for certain uses?**  
  
 <i> not answered </i>  
  
**Has an analysis of the potential impact of the dataset and its use on data subjects (e.g., a data protection impact analysis) been conducted?**  
  
 <i> not answered </i>  
  
**Any other comments?**  
  
 <i> not answered </i>  

# Preprocessing, Cleaning, Labling
  
**Was any preprocessing/cleaning/labeling of the data done (e.g., discretization or bucketing, tokenization, part-of-speech tagging, SIFT feature extraction, removal of instances, processing of missing values)?**  
  
 <i> not answered </i>  
  
**Was the “raw” data saved in addition to the preprocessed/cleaned/labeled data (e.g., to support unanticipated future uses)?**  
  
 <i> not answered </i>  
  
**Is the software used to preprocess/clean/label the instances available?**  
  
 <i> not answered </i>  
  
**Any other comments?**  
  
 <i> not answered </i>  

# Uses
  
**Has the dataset been used for any tasks already?**  
  
 <i> not answered </i>  
  
**Is there a repository that links to any or all papers or systems that use the dataset?**  
  
 <i> not answered </i>  
  
**What (other) tasks could the dataset be used for?**  
  
 <i> not answered </i>  
  
**Is there anything about the composition of the dataset or the way it was collected and preprocessed/cleaned/labeled that might impact future uses?**  
  
 <i> not answered </i>  
  
**Are there tasks for which the dataset should not be used?**  
  
 <i> not answered </i>  
  
**Any other comments?**  
  
 <i> not answered </i>  

# Distribution
  
**Will the dataset be distributed to third parties outside of the entity (e.g., company, institution, organization) on behalf of which the dataset was created**  
  
 <i> not answered </i>  
  
**How will the dataset be distributed (e.g., tarball on website, API, GitHub)?**  
  
 <i> not answered </i>  
  
**When will the dataset be distributed?**  
  
 <i> not answered </i>  
  
**Will the dataset be distributed under a copyright or other intellectual property (IP) license, and/or under applicable terms of use (ToU)?**  
  
 <i> not answered </i>  
  
**Have any third-parties imposed IP-based or other restrictions on the data associated with the instances?**  
  
 <i> not answered </i>  
  
**Do any export controls or other regulatory restrictions apply to the dataset or to individual instances?**  
  
 <i> not answered </i>  
  
**Any other comments?**  
  
 <i> not answered </i>  

# Maintenance
  
**Who is supporting/hosting/maintaining the dataset?**  
  
 <i> not answered </i>  
  
**How can the owner/curator/manager of the dataset be contacted (e.g., email address)?**  
  
 <i> not answered </i>  
  
**Is there an erratum?**  
  
 <i> not answered </i>  
  
**Will the dataset be updated (e.g., to correct labeling errors, add new instances, delete instances)?**  
  
 <i> not answered </i>  
  
**If the dataset relates to people, are there applicable limits on the retention of the data associated with the instances (e.g., were individuals in question told that their data would be retained for a fixed period of time and then deleted)?**  
  
 <i> not answered </i>  
  
**Will older versions of the dataset continue to be supported/hosted/maintained?**  
  
 <i> not answered </i>  
  
**If others want to extend/augment/build on/contribute to the dataset, is there a mechanism for them to do so?**  
  
 <i> not answered </i>  
  
**Any other comments?**  
  
 <i> not answered </i>  
