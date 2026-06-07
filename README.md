# ScientificDatasets
This repo is used to share the datasets' csv files associated with our Research paper "Towards Fully Automated Trend Prediction from Scientific Literature"." The datasets are "Wireless Networks and Mobile Computing" and "Software Engineering".


## Trend Prdiction Datasets

Two datasets are constructed following the same data collection and preprocessing strategy, differing only in the domain-specific keywords used for retrieval. The first dataset targets the "Wireless Networks and Mobile Computing (WNMC)" domain and serves as the primary dataset to evaluate the proposed trend prediction framework. The second dataset focuses on "Software Engineering (SE)" and is used for cross-domain validation to assess the framework's generalization ability. 

Each dataset is constructed using a keyword-driven retrieval strategy, where representative keywords are defined for each domain to capture both foundational topics and emerging research directions. This ensures broad and balanced coverage of the targeted fields. Data collection is performed using the OpenAlex API.

To ensure data quality and consistency, filtering and normalization steps are applied. Only open-access journal articles and conference papers with both titles and abstracts are retained, and keyword relevance is enforced through matching in the title or abstract. Duplicate records are removed using DOI filtering, and publication dates and venue names are standardized. The final datasets include key metadata such as DOI, title, abstract, authors, venue, and publication date to support subsequent analysis.


### "Wireless Networks and Mobile Computing" (main dataset): 
136,047 papers collected from 2010 to 2025 using 11 domain-specific keywords present in either the title or the abstract (wireless networks, WiFi, 5G, ad hoc networks, mobile computing, ubiquitous computing, edge computing, Internet of Things, smart devices, sensor networks).
    
### Software Engineering (validation dataset):
449,931 papers collected from 2010 to 2025 using 11 software engineering-related keywords present in the title or abstract (software engineering, software development, software design, software architecture, software testing, software maintenance, software verification, software validation, agile software development, DevOps, and software refactoring).
