



# Motivation
  
**For what purpose was the dataset created?**  
  
The present dataset was created for machine learning in order to improve the prediction of bloodstream infections. The dataset combines clinical blood parameters, age, sex as well as previous admissions to blood culturing results (negative and positive) and resistance profile of the infecting pathogen over a period of more than 10 years.   
  
**Who created the dataset (e.g., which team, research group) and on behalf of which entity (e.g., company, institution, organization)?**  
  
Dept. of Clinical Microbiology, Rigshospitalet created the dataset In collaboration with dept. of clinical Biochemistry,  Rigshospitalet   
  
**Who funded the creation of the dataset?**  
  
 <i> not answered </i>  
  
**Any other comments?**  
  
Name of person answering questions: 
Karen Leth Nielsen Karen.leth.nielsen.01@regionh.dk
Frederik Boëtius Hertz Frederik.boetius.hertz@regionh.dk
Karen Leth Nielsen Karen.Leth.Nielsen.01@regionh.dk   

# Composition
  
**What do the instances that comprise the dataset represent (e.g., samples, images, people)?**  
  
The whole dataset represents the event or lack thereof of a step leading to activation of the immune response. D1: Peptides measured in a stability assay, investigating whether a there is a complex formed with the MHC molecule and how stable that complex is. Two columns: one with peptide (9 amino acids), one with measurement. ELISA measurement. The MS dataset represents peptide ligands investigated to be binding to MHC. D2: Each instance is a peptide found to be bound to MHC. Peptides vary in length. Only positive (binding) instances are present. Peptides with modifications (e.g. + OX(M14)) can be disregarded.  
  
**How many instances are there in total?**  
  
D1: 4919 (each instance represents a unique peptide:MHC) D2: 2827 (each instance represents a unique peptide:MHC)  
  
**Does the dataset contain all possible instances or is it a sample (not necessarily random) of instances from a larger set?**  
  
The datasets represent a small sample from the whole peptide space. If peptides are tested randomly only around 1% of the measured peptides binds to MHC. The provided datasets are thus enriched and allow building a model that can contain features describing the studied problem.  
  
**What data does each instance consist of?**  
  
Each data instance is a measurement of stability of a unique peptide:MHC complex, in case of the Stability dataset. For the MS datasets each instance is representing whether the peptide was/was not present in the eluted ligands.  
  
**Is there a label, target, or outcome (e.g., mortality) associated with each instance?**  
  
Yes, each peptide sequence is associated with an outcome. D1: normalized stability, measured with ELISA. Normalisation (% stability) is per batch, to a reference peptide (100%). D2: detection of the peptide via Mass Spec (binding/non-binding) binary value.  
  
**Is any information missing from individual instances?**  
  
No  
  
**Are relationships between individual instances made explicit (e.g., familial links, or samples derived from the same patient or same exposure)?**  
  
No  
  
**Are there recommended data splits (e.g., training, development/validation, testing)?**  
  
For iterative models it is common to use 5-fold cross validation. Sometimes nested, such that there is also one rotating bin left for early stopping.  
  
**Are there any errors, sources of noise, or redundancies in the dataset?**  
  
Yes. There are several duplicates in D1. Some of which are the control measurements, those can be disregarded when using the data. The control peptides are longer than 9 residues. D1 is known to have less noise than D2.  
  
**Is the dataset self-contained, or does it link to or otherwise rely on external resources (e.g., websites, public databases, other datasets and/or private silos)?**  
  
It is self-contained. Validation data (known immunogenic peptides) can be found at IEDB (www.iedb.org). One-hot encoding can be done without external data, but it is also possible to use evolutionary information (BLOSUM) or other distance matrix to encode each of the amino acids.  
  
**Does the dataset contain data that might be considered confidential (e.g., data that is protected by legal privilege or by doctor-patient confidentiality, data that includes the content of individuals’ non-public communications)?**  
  
Yes, D1 is confidential, unpublished and with commercial interest. Anyone needs to sign an NDA.  
  
**Does the dataset contain data that, if viewed directly, might be offensive, insulting, threatening, or might otherwise cause anxiety?**  
  
The data is related to a mouse genotype (allele). When expanding this type of models it is important to consider that genotypes are covered in an unbiased manner (some alleles are more prevalent in some ethnicities).  
  
**Does the dataset not relate to people (e.g., animals, cell lines, environment)?**  
  
Yes, it does not relate to people. The dataset relates to mice.  
  
**Does the dataset identify any subpopulations (e.g., by age, gender, etc.)?**  
  
 <i> not answered </i>  
  
**Is it possible to identify individuals (i.e., one or more natural persons), either directly or indirectly (i.e., in combination with other data) from the dataset?**  
  
 <i> not answered </i>  
  
**Does the dataset contain data that might be considered sensitive in any way (e.g., data that reveals racial or ethnic origins, sexual orientations, religious beliefs, political opinions or union memberships, or locations; financial or health data; biometric or genetic data; forms of government identification, such as social security numbers; criminal history)?**  
  
 <i> not answered </i>  
  
**Any other comments?**  
  
No  

# Collection Process
  
**How was the data associated with each instance acquired?**  
  
Data was directly observed using an instrument. In the case of stability measurements the data is expressed as a binding percentage to a known stable binder.  
  
**What mechanisms or procedures were used to collect the data (e.g., hardware apparatus or sensor, manual human curation, software program, software API)?**  
  
D1: ELISA; D2: Mass Spectroscopy  
  
**If the dataset is a sample from a larger set, what was the sampling strategy (e.g., deterministic, probabilistic with specific sampling probabilities)?**  
  
Sampling strategies include selection with MS and known T cell epitopes from databases.  
  
**Who was involved in the data collection process (e.g., students, crowdworkers, contractors) and how were they compensated (e.g., salaried, immaterial through prizes / authorship / etc) and how much (e.g., according to competitive scales mandated by [insert body or institution])?**  
  
D1: Employees at Immunitrack payed by Immunitrack ApS and Innovation Foundation. D2: Sofron et al. 2016 (doi: 10.1002/eji.201545930)  
  
**Over what timeframe was the data collected?**  
  
Not relevant.  
  
**Were any ethical review processes conducted (e.g., by an institutional review board)?**  
  
No, not necessary.  
  
**Does the dataset not relate to people (e.g., animals, cell lines, environment)?**  
  
Yes, it relates to mice.  
  
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
  
No  

# Preprocessing, Cleaning, Labling
  
**Was any preprocessing/cleaning/labeling of the data done (e.g., discretization or bucketing, tokenization, part-of-speech tagging, SIFT feature extraction, removal of instances, processing of missing values)?**  
  
Yes, the stability data is normalized as a percentage in relation to a known stable binder (control).  
  
**Was the “raw” data saved in addition to the preprocessed/cleaned/labeled data (e.g., to support unanticipated future uses)?**  
  
Yes  
  
**Is the software used to preprocess/clean/label the instances available?**  
  
Processing of the stability data was done using Microsoft Excel.  
  
**Any other comments?**  
  
No  

# Uses
  
**Has the dataset been used for any tasks already?**  
  
D1: data is novel. D2: Sofron et al. 2016 (doi: 10.1002/eji.201545930)  
  
**Is there a repository that links to any or all papers or systems that use the dataset?**  
  
No  
  
**What (other) tasks could the dataset be used for?**  
  
Vaccine design for mice. Understanding the biology and binding preference of IAB.  
  
**Is there anything about the composition of the dataset or the way it was collected and preprocessed/cleaned/labeled that might impact future uses?**  
  
Data has commercial interest, is confidential and is under NDA. Findings can be published in agreement with Immunitrack ApS. The raw data can also be published with the paper, if needed, and in agreement with Immunitrack ApS (Who are eager to publish a nice paper on this).  
  
**Are there tasks for which the dataset should not be used?**  
  
Data and any use and application is confidential, and should be discussed with Immunitrack ApS.  
  
**Any other comments?**  
  
No  

# Distribution
  
**Will the dataset be distributed to third parties outside of the entity (e.g., company, institution, organization) on behalf of which the dataset was created**  
  
No, not allowed.  
  
**How will the dataset be distributed (e.g., tarball on website, API, GitHub)?**  
  
Should stay on server.  
  
**When will the dataset be distributed?**  
  
For developers under NDA: When needed. For public: At time of publication.  
  
**Will the dataset be distributed under a copyright or other intellectual property (IP) license, and/or under applicable terms of use (ToU)?**  
  
Yes. Attached NDA.  
  
**Have any third-parties imposed IP-based or other restrictions on the data associated with the instances?**  
  
Yes. Patent pending.  
  
**Do any export controls or other regulatory restrictions apply to the dataset or to individual instances?**  
  
No  
  
**Any other comments?**  
  
No  

# Maintenance
  
**Who is supporting/hosting/maintaining the dataset?**  
  
Immunitrack ApS.  
  
**How can the owner/curator/manager of the dataset be contacted (e.g., email address)?**  
  
By email, at: mprachar @immunitrack.com.  
  
**Is there an erratum?**  
  
No  
  
**Will the dataset be updated (e.g., to correct labeling errors, add new instances, delete instances)?**  
  
There is a possibility that more instances will be added from the public sources (MS data).  
  
**If the dataset relates to people, are there applicable limits on the retention of the data associated with the instances (e.g., were individuals in question told that their data would be retained for a fixed period of time and then deleted)?**  
  
The dataset does not relate to people.  
  
**Will older versions of the dataset continue to be supported/hosted/maintained?**  
  
No. Not expected to be a problem.  
  
**If others want to extend/augment/build on/contribute to the dataset, is there a mechanism for them to do so?**  
  
It is possible to extend the MS data, IEDB is a great source (www.iedb.org).  
  
**Any other comments?**  
  
No  
