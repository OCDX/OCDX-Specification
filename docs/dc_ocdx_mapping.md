**AGENT**

| **Related DC Term** | **OCDF Term** | **Definitions: What does a term mean, and what is it supposed to do? Example** | **Required?** | **Repeatable?** | **Data format** | **Example** |
| --- | --- | --- | --- | --- | --- | --- |
| Agent | Agent | Header | Yes | Yes |   |   |
| Agent | agentName | Transcribe from source | Yes | Yes |   | Leskovec, Jure |
|   | agentRole | Should indicate the agent's role in collecting and/or preparing dataset. Some possible categories could be: grant funder, corporate sponsor, primary investigator, general contributor. **Grant funder** : should refer to an entity that provided funds for research that resulted in the dataset's creation); **Corporate sponsor** : should refer to a for profit entity that provided funds for research that resulted in the dataset's creation; **Primary investigator** should refer to the individual or individuals who initiated and are responsible for the **Primary researcher:** research that resulted in the creation of a dataset); **General contributor:** can refer to an individual associated with a research project but not listed as a Primary Investigator | No | Yes |   | Primary researcher |
| Agent | agentAffiliation | Base on agent's mode of describing its affiliation and function. Possible sources of information: about pages, form of URL (.gov, .edu, .com etc.). Private individual (individual should be the person  primarily responsible for the creation of a dataset. This does NOT mean that a single subject was the focus of the project, just that a single individual was responsible for overseeing the dataset's creation and preparation); **Private corporation** (A private for profit entity that collects data for the creation of datasets. This could include YouTube, Facebook, Twitter); **NGO** (A private for not for profit entity that collects data for the creation of datasets. This could include Pew or  Universities ); **Government agency** (Government should refer to federal, state, county or municipal endeavor to collect and prepare data for a dataset); **Educational institution** (Agent being  associated dataset  is affiliated with a College or university). | No | Yes |   | Educational institution |
|   | contactEmail |   | No | Yes | Copy and paste from source in order it appears. First mode of contact listed is the preferred mode of contact. | SNAP Dataset Mailing List |
|   | contactPhone |   | No | Yes | Copy from source in order it appears. First mode of contact listed is the preferred mode of contact. |   |



**DESCRIPTION OF DATASET**

| **Related DC Term** | **OCDF Term** | **Definitions: What does this term mean, and what is it supposed to do?  ** | **Required?** | **Repeatable?** | **Data format** | **Example** |
| --- | --- | --- | --- | --- | --- | --- |
| description | datasetDescription | Header | Yes | No |   |   |
| title | datasetTitle |   | Yes | No | Transcribe from source. If this is not available then create a descriptive title that represents the creator and/or subject of the dataset. This description should include the subject of the research and the dates covered by the dataset. | Amazon product co-purchasing network metadata |
| abstract | datasetAbstract |   | Yes | No | Complete summary of the dataset, which should include dates for creation/capture, institutional affiliation and motivations for data collection. When possible copy from source. | Data was collected by crawling Amazon website and contains product metadata and review information about 548,552 different products (Books, music, CDs, DVDs and VHS). |
| abstract | documentationAnalysis | Is documentation for the mode of data collection and transformation? | Yes | No |   | Yes |
|   | datasetCitation |   | Yes | No |  This will provide a citation format for the dataset NOT publications that used or referenced the dataset. Use APA 6th edition guidelines for citing electronic resources.   | Stanford Network Analysis Project (2006). Amazon product co-purchasing network analysis [Data file]. Retrieved from [https://snap.stanford.edu/data/amazon-meta.html](https://snap.stanford.edu/data/amazon-meta.html) |
| identifier | datasetURL |   | Yes | No | Copy the URL that appears on the page that provides access to the files comprising the dataset | https://snap.stanford.edu/data/amazon-met |
|   |   |   |   |   |   |   |
| accrualMethod | modeOfCollection | How was the data collected? The following sub elements will help identify sources of information that will accurately describe the methods a researcher used to create a dataset | Yes | No |   |   |
| extent | sample | Where was data collected from? Who or what  is the data about? | Yes | No |   | Amazon.com |
|   | temporalStructure | How was the dataset created -- was a site mined over the course of many days, weeks or months? Is the dataset comprised of a continuous process of collection or were data collected at random or predetermined intervals? | Yes | No |   | Continuous |
| date | dateOfCollection\_earliest | List the earliest  date for when data associated with the dataset began.If no dates are available do not include. Take information from dataset descriptions and/or publications referencing the dataset. | Yes | No | Use ISO date entry standard: yyyy-mm-dd. | 2006-06 |
| date | dateOfCollection\_latest | List the latest date for when data associated with the dataset began.If no dates are available do not include. Take information from dataset descriptions and/or publications referencing the dataset. | Yes | No | Use ISO date entry standard: yyyy-mm-dd. | 2006-08 |
|   |   |   |   |   |   |   |
| mediaTypeOrExtent | filesAndFormats | Take this information from documentation about the dataset. This set of elements should help describe how a researcher produced their dataset. | Yes | Yes |   |   |
| mediaType | fileFormats | File formats researchers will download  in order to access datasets. Make selection based on information in file directory whenever possible. | Yes | Yes | If multiple files are available separate list using semicolons Use standard abbreviations (jpg, tiff, zip, gif) enter size and then type.   Capitalize file size, use standard notation for file size (MB etc.).   | txt.gz; 201 MB |
| mediaType | fileContents | After downloading and opening files, what will a person be looking at? Text, integers, photos, maps, visualizations of networks etc.? | Yes | Yes |   | Text |
| bibliographicCitation | publicationCitation | Has the dataset been used in a scholarly publication(s)? | No | Yes |APA 6th edition format
   | Leskovec, J., Adamic, L. & Adamic, B. (2007). The dynamics of viral marketing. _ACM Transactions on the Web 1_(1). DOI http://www.cs.cmu.edu/~jure/pubs/viral-tweb.pdf |
| extent | privacyEthics | These elements will help describe how a researcher collected data and what steps they took to protect and preserve participant's rights and privacy. | Yes | No |   |   |
| accessRights | specialRisks | Is this data prone to any special risks about which researchers should be aware | Yes | Yes |   | No |
| subject | PII | Are there any personally identifiable information included in the dataset a research would need to take special precautions with? | Yes | Yes |   | No |
| modified | anonymizedData | Has anything been excluded, removed or altered in the dataset in order to protect the identities, integrity and rights of participants?: If no, this must be stated:  names anonymized; images excluded; date of birth; date of death; social security (or other identifying numbers); race and ethnicity categories; health and wellness data; religious affiliations; location or GPS coordinates; other (with a text box to specify); Other (please describe) | Yes | Yes |   | IDTitleGroupSalesrank SimilarCategoriesReviews |
| subject | participantInfo | Were specific fields mined? Should be a yes/no question, and if yes then select checkboxes: participant data included in the dataset: names; images; date of birth; date of death; social security (or other identifying numbers); race and ethnicity categories; health and wellness data; religious affiliations; location or GPS coordinates; other (please specify) | Yes | Yes |   | Product IdASINTitle (product name)Group (product category)SalerankSimilar (products)CategoriesReviews |
| accessRights | oversight | What types of institutional oversight applied to data collection and/or analysis:  IRB (Institutional Review Board); REBs (Research Ethics Boards); RECs (Research Ethics Committees); Not required | Yes | Yes |   | IRB |
| accessRights | informedConsent | Was informed consent obtained? Or were participants notified of their inclusion in the dataset? | Yes | No |   | No |
|   |   |   |   |   |   |   |
| accessRights | accessAndUse\_dataset |   |   |   |   |   |
| accessRights | accessPermissions | Are there any notices or statements that limit how a dataset can be re-used?  Are there any steps a researcher should take to gain access to the information contained in the data set? Are there any types of projects or institutions that will not be permitted to use the dataset? | Yes | No |   | No |
| acrualPolicy | reuseGuidelines | Are there any steps a researcher should take when they are re-using this dataset in order to ensure the continued protection of subject's included in the original study? When possible copy statements directly from dataset or data repository. | Yes | No |   | No |


**DESCRIPTION OF DATA SOURCE**

| **Related DC Term** | **OCDF Term** | **Definitions: What does this term mean, and what is it supposed to do?** | **Required?** | **Repeatable?** | **Data format** | **Example** |
| --- | --- | --- | --- | --- | --- | --- |
| mediator | datasetSource |   | Yes | No |   |   |
| title | repositoryName | Write out the full name of the source and if there is an acronym put it in brackets | Yes | No |   | Stanford Network Analysis [SNAP] |
| type | repositoryType | Private individual (individual should be the person  primarily responsible for the creation of a dataset. This does NOT mean that a single subject was the focus of the project, just that a single individual was responsible for overseeing the dataset's creation and preparation), **Government agency** (Government should refer to federal, state, county or municipal endeavor to collect and prepare data for a dataset), **NGO** (A private for not for profit entity that collects data for the creation of datasets. This could include Pew or  Universities ), **Private corporation** (A private for profit entity that collects data for the creation of datasets. This could include YouTube, Facebook, Twitter) **Educational institution** (Agent being  associated dataset is affiliated with a College or university). Whenever possible base decision on information contained in the dataset or posted on the data repository site. | Yes | Yes |   | Educational Institution |
| identifier | repositoryURL |   | Yes | No | Copy and paste URL for homepage of repository | [https://snap.stanford.edu/index.html](https://snap.stanford.edu/index.html) |
| references | availableDatasets |   | No | Yes |   |   |
| accessRights | termsOfUse | Are there any notices or statements that limit access and use of datasets stored in the repository or host site? | Yes | No |   | No |
| accessRights | institutionalRequirement | Were there any legal or institutional guidelines about how to collect, manage and preserve data? When possible copy statements directly from dataset or data repository. | Yes | No |   | No |
| bibliographicCitation | repositoryCitation | This will provide a citation format for the dataset repository or publisher. This should, as a minimum, include: Repository, publisher host (etc.) name, URL for navigating to the site and the date that the site was last updated and.or copyrighted.  Derived from APA 6th edition guidelines for citing electronic resources. | Yes | No |   | SNAP. [https://snap.stanford.edu/index.html](https://snap.stanford.edu/index.html)  |

**METADATA CREATION (COURSES)**

| **Related DC Term** | **OCDF Term** | **Definitions: What does this term mean, and what is it supposed to do?** | **Required?** | **Repeatable?** | **Data format** | **Example** |
| --- | --- | --- | --- | --- | --- | --- |
| title | courseTitle | Supply the Course title and if possible number | No | No |   | ISLT 9000 Data Science |
| educationalLevel | courseLevel | Identify if the course is undergraduate or graduate level. If the course is blended, students should base their selection on the level they registered for | No | No |   | Graduate |
| contributor | courseInstructor | Provide the name of the instructor responsible for the course | No | No |   | Dr. Sean P. Goggins |
| contributor | courseInstitution | Provide the name of the University and department the course was offered through | No | No |   | University of Missouri, School of Information Science & Learning Technologies |
| date | courseDates | Identify the semester (or quarter) and year for the course. | No | No |   | Spring 2015 |
|   | courseSyllabus | Is the course syllabus archived in OCDF? | No | No |   | No |