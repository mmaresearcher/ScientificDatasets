# ScientificDatasets
This repo is used to share the datasets' csv files associated with our Research paper "Towards Fully Automated Trend Prediction from Scientific Literature"." 

## Topic Labeling Datasets
The performance of supervised topic labeling relies heavily on the availability of reliable keyword–label pairs. To ensure both semantic quality and broad domain coverage, two complementary datasets were developed.

### 1) Verified Dataset
The Verified Dataset comprises expert-validated topic keyword–label pairs designed to ensure semantic accuracy and relevance. To construct this dataset, a structured validation study was conducted involving 35 PhD holders from The German University in Cairo across eight academic disciplines, including Media Engineering and Technology, Information Engineering and Technology, Engineering and Materials Science, Pharmacy and Biotechnology, Management Technology, Applied Sciences and Arts, Mathematics, and Physics. For each participant, between three and six research specializations were identified using publicly available academic profiles.

For every research field, Gemini was used to generate seven topic keyword–label pairs through a controlled prompting strategy. Experts were then asked to evaluate pairs within their areas of expertise and determine whether the assigned label accurately represented the semantic meaning of the corresponding keywords by selecting either Agree or Disagree. To enhance evaluation reliability, the survey included a small number of intentionally incorrect keyword–label pairs containing obvious semantic mismatches. These control questions served as attention checks, and participants who consistently approved such incorrect pairs were excluded from the analysis. Overall, 931 topic keyword–label pairs were evaluated, of which 812 received Agree judgments, resulting in an agreement rate of 87.22%. The validated pairs retained after this process constitute the Verified Dataset used in this study.

### 2) Taxonomy Dataset
To ensure extensive coverage across a wide range of scientific domains, a second dataset was developed based on Elsevier’s Digital Commons Three-Tiered Taxonomy of Academic Disciplines. This taxonomy provides a hierarchical classification of academic knowledge, spanning broad disciplines, intermediate subdisciplines, and specialized research fields.

The present study utilizes the third level of the taxonomy, which contains 913 fine-grained research fields (e.g., Physical Sciences and Mathematics → Computer Sciences → Software Engineering). For each field, topic keyword–label pairs were generated using Gemini, employing the same controlled prompting framework adopted in the expert validation experiment. This approach ensures consistency in structure, semantic specificity, and correspondence with realistic topic modeling outputs.

During dataset creation, two research fields, including Holocaust and Genocide Studies, were omitted because the model declined to produce outputs due to built-in ethical constraints. Consequently, the final dataset encompasses 911 research fields. Seven topic keyword–label pairs were generated for each field, resulting in a total of 6,377 pairs.


## Trend Prediction Datasets
Two datasets are constructed following the same data collection and preprocessing strategy, differing only in the domain-specific keywords used for retrieval. The first dataset targets the "Wireless Networks and Mobile Computing (WNMC)" domain and serves as the primary dataset to evaluate the proposed trend prediction framework. The second dataset focuses on "Software Engineering (SE)" and is used for cross-domain validation to assess the framework's generalization ability. 

Each dataset is constructed using a keyword-driven retrieval strategy, where representative keywords are defined for each domain to capture both foundational topics and emerging research directions. This ensures broad and balanced coverage of the targeted fields. Data collection is performed using the OpenAlex API.

To ensure data quality and consistency, filtering and normalization steps are applied. Only open-access journal articles and conference papers with both titles and abstracts are retained, and keyword relevance is enforced through matching in the title or abstract. Duplicate records are removed using DOI filtering, and publication dates and venue names are standardized. The final datasets include key metadata such as DOI, title, abstract, authors, venue, and publication date to support subsequent analysis.

### 1) "Wireless Networks and Mobile Computing": 
268,095 papers were collected from 2010 to 2025 using 10 domain-specific keywords present in either the title or the abstract (“mobile computing”, “WiFi”, “5G”, “6G”, “Internet of Things”, “Edge Computing”, “Wireless Sensor Networks”, “Vehicular Networks”, “Software Defined Networking”, and “Network Function Virtualization”). 
Link to download this large Dataset: [Wireless Networks and Mobile Computing Dataset](https://drive.google.com/file/d/1apZ4PrpYcyUvmTfWTpP4G5D6YWxff9eo/view?usp=sharing) 
    
### 2) Software Engineering:
24,863 papers were collected from 2010 to 2025 using software engineering-related keywords present in the title or abstract (including:  “software engineering", “software development", “software design", “software architecture", “software testing", “requirements engineering", “code review", “automated program repair", “mining software repositories", “DevOps", “microservices", “technical
debt’, “static analysis", and related topics).
Link to download this large Dataset: [Software Engineering Dataset](https://drive.google.com/file/d/1mkJL3Je85xeGCD4mgUnaNhQWgQq1UOhP/view?usp=sharing) 
