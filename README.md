# Qualitative Codes Ontology (QualiCO)
This describes the ontology I developed for qualitative coding schemas. This ontology describes qualitative coding schemas. It can be implemented easily. I kept the representation simple in an table, but might provide a version in RDF in the future. This is still work in progress, I also do some user testing on it. But if you encounter issues or have remarks I am happy to hear from you. Also if you want to implement it into your research data repository, I am happy to hear from you.

There are two publications on this research out: 
* Julian Hocker, Taryn Bipat, Mark Zachry, and David W. McDonald. 2020. Sharing your coding schemas: Developing a Platform to fit within the Qualitative Research Workflow. In Proceedings of the 16th International Symposium on Open Collaboration (OpenSym 2020). Association for Computing Machinery, New York, NY, USA, Article 2, 1–10. DOI:https://doi.org/10.1145/3412569.3412574
*  Hocker, J., Schindler, C. and Rittberger, M. (2020), "Participatory design for ontologies: a case study of an open science ontology for qualitative coding schemas", Aslib Journal of Information Management, Vol. 72 No. 4, pp. 671-685. https://doi.org/10.1108/AJIM-11-2019-0320 
* Julian Hocker, Taryn Bipat, David W. McDonald et al. Evaluating QualiCO: An Ontology to Facilitate Qualitative Methods Sharing to Support Open Science, 20 January 2021, PREPRINT (Version 1) available at Research Square [https://doi.org/10.21203/rs.3.rs-148261/v1]
  
I used to following standards to comply with other work in the field:
* Bibliographic information: [BiBo](https://github.com/structureddynamics/Bibliographic-Ontology-BIBO) and [Dublin Core](http://dublincore.org/)
* research data description: [DDI](https://ddialliance.org/) and the [metadata schema by Verbund FDB](https://www.forschungsdaten-bildung.de/files/fdbinfo_8_Metadatenset_v1.0.pdf) (German association for research data in education)

## Structure
The ontology consists of several entities: the metadata for the codes, the metadata for the coding frames and also metadata to describe the research data that was analyzed, the publications that were created as well as the projects in which the coding frames were developed. It became evident that it is not enough to describe only the coding schemas, but there is other information needed as well. The following graphic shows the structure of the ontology:

![Structure of the ontology](https://github.com/julianhocker/Quali-Codes-Ontology/blob/master/stucture.jpg "Structure of the ontology")

## Coding Schema
These metadata describe the coding schema. It also gives further information how it was developed and how the coding was done. There is also the possibility to share your project data or your coding schema as REFI-QDA Project or REFI-QDA Codebook file.

|Name   |Description   |  Mapping to metadata standard   |type of field  |justification/background| required|
|---|---|---|---|---|---|
|Title | Title fo the coding schema | dc:title | text | | yes
|Author   |Person, who created the coding schema   |dc:creator   |text   |   |yes
|ID | Identifier for the coding schema, preferably a DOI | dc:id | any kind of id | | yes
|Method |Which method you used to create the codes, e.g. Grounded Theory with Strauss/Glaser or Strauss/Corbyn. |   |text/dropdown   |   |yes
|Method comment |specify further how you used the method. Also describe how strictly you used these methods|dc:description | text |qualitative methods are quite diverse and people use them quite openly|no
|Research area   |Where do you see this research?   |   |text   |   |yes
|Theoretical background   |Which theories did you use, e.g. from psychology, sociology and which codes did you derive from these? |   |text  |   |yes
|Research questions   |What were the research questions you wanted to answer? |   |text   |   |yes
|Process of creation|Describe how you created the codes. Did you code alone or with a team? How did you create the codes? How and which codes did you change in the process and why? | | text | | yes
|Coding cycles | Describe how you coded, based on Saldana (2015, coding manual for qualitative researchers,  p 68) | | text/dropdown | | no
|Description of coding cycles |How did you code? Describe the process how you coded the data. | |text | not everyone is familiar with Saldana, so people can give more information about the coding cycles here. Also describe how you did dimensionalization if you used Grounded Theory | yes
|Inter-coder reliability|How high was the inter-coder-reliability? How did you measure it| | text | |no
|Software|Which software was used, or did you code on paper?| |text | | yes
|Date|When did you create the codes (start and end date)  |dc:date   |date   |   |yes
|Coding schema as QDA-XML   |Possibility to upload complete coding frame via [REFI-QDA Codebook](https://www.qdasoftware.org/products-codebook-exchange/) or other way to exchange all codes  |   |File   |   | yes
|Project as XML Project exchange file   |Possibility to upload complete coding frame via [REFI-QDA Project ](https://www.qdasoftware.org/products-project-exchange/)   |   |File   |   |no
|Visualizations | Possibiilty to upload visualizations, e.g. maps if you used Situation analysis| |file |Visualizations are important ways to get an overview on the codes and can help others understand your codes | no
|Keywords|Keywords for the research|for German: Thesaurus Bildungsforschung; dc:subject | text | |yes
|Language | Language in which the coding schema was created | dc:language | text| |yes
|Format | Format of the coding schema |dc:format| text, should be "qdpx"| | no
|Type | Type of the data, if your format is qdpx, choose "dataset" | dc:type | text| | yes
|Rights | statement of copyright for the coding schema (defined by research data center) | dc:rights| text| | no
|Publisher | Name of the repository where coding schema is published | dc:publisher | text | | no

I did not include dc:source, dc:relation, dc:coverage in this. There is no general comment in this class, so I put the dc:description to the method comment, which I think is the most important information

## Codes
This describes the codes itself. I used as a basis the book 'The coding manual for qualitative researchers' by Saldana and the book 'qualitative content analysis in practice' by Schreier. THe goal here is to define a standard how codes should be described.

|Name   |Description   |Link to standard vocabulary   |type of field   |   | Required
|---|---|---|---|---|---|
|Name   |Name of the code   |   |text   |   |yes
|Including criterion   |What needs to be in the text to use this code   |   |text   |Saldana (2015)|no
|Excluding criterion   |When not to use it |   |text   |   |no
|Anchor example   |Example when code is used |   |text   |   |yes
|Counter example   |Example when not to use this code |   |text   |   |no
|Provenence|Where does code come from? | |text/dropdown (inductive, deductive, in-vivo, socially constructed)| | yes
|Count|How often code was used in reserach project | | number| |no
|Number of connections to other codes | to how many other codes is the code connected in your coding schema in Grounded Theory? | | number ||no

## Study
In interviews I got the feedback that it is important to get information about the overall study, in which the coding schema was created, like was this part of a larger study or just a small project. First, this was named project and then renamed to study because [DDI](https://ddialliance.org) as well as research data centers like [Forschungsdatenzentum Bildung](https://www.fdz-bildung.de/) focus on studies rather than projects.

|Name   |Description   |Link to standard vocabulary   | type of field   |Justification/background|Required|
|---|---|---|---|---|---|
|Name   |Name of the study   |dc:title   |text   |   | yes
|Persons   |People who are involved in the project   |dc:contributor   |text|People mentioned that it makes sense to see who was involved to get a glimpse of how the ideas were |no
|contact person   |People who can be contacted if there are questions   |dc:creator   |text   |People mentioned in design phase II that it makes sense to have a person that they can contact and this is more important than the head of the project, which might be not involved that much  |yes
|Institutions | Institutions who did the study |dc:contributor | text | |yes
|Date   |When was the project active?   |dc:date  |text field/time span|important to see when the study was done |yes
|Description   |Description of the study, contains research method and implication; research questions and goals; also theoretical background and if there were primary or secondary data |dc:description   |text   |  |yes
|Link   |Link to webpage of the project where users can get more information |dc:identifier   |URL|It was mentioned that people want to get in contact and find out more about the study, therefore the link to the study |yes  
|Kind of study   |internal project/dissertation/third-party-funded |   |text/dropdown   |  | yes
|Comment to kind of study | possibility to give further information | text | | yes
|sub-studies | link to sub-studies that were part of this study | | link| Participants expressed need to link studies if they were part of larger studies|no
|Keyword   |Keyword from a controlled vocabulary |dc:subject   |text   |  |yes

## Publications
These metadata help to identify the publication in which the coding schema was used. In my prototype I do not want to implement a complete literature management, only basic information, so people can find the publication. If you implement this ontology within a literature information system, you already have this information

|Name   |Description   |Link to standard vocabulary   |type of field   |Justification/background|Required|
|---|---|---|---|---|---|
|Title   |Title of the publication   |dc:title     |text   |standards for literature description|yes
|Autor   |Name of the author   |dc:creator    |text   |standards for literature description|yes
|Date   |When was it published?   |dc:date   |date   |standards for literature description|yes
|DOI   |Unique identifier for document, preferable DOI or other like URN   |dc:identifier   |DOI   |standards for literature description|yes
|Keyword   |Keyword that describes the publication   |dc:subject  |Controlled vocabulary   |   |yes
|Abstract   |Abstract of the publication   |dc:description  |Text   |Mentioned in interviews, people thought it makes sense, so they do not have to click on DOI to see abstract|yes
|Bibliographic string|Information about publication that you can copy to cite it (only needed if no Unique identifier is provided)| |Text|mentioned in interviews, makes literature easier to find when there is no DOI|yes

## Research data
Codes are often developed based on data, also data is sometimes created with certain questions in mind. I put them apart because there is also the possibility to use codes on several datasets and to reuse data. In an optimal world, this research data would just be in your research data archive and therefore people can just with one click get the data as well as the codes ;)

|Name   |Description   |Link to standard vocabulary   |type of field   |Justification/background|Required|
|---|---|---|---|---|---|
|DOI   |The unique identifier of the data|dc:identifier   |DOI   |   |yes
|Creation of data| How data was created, e.g. interview, observation|DDI:ModeOfCollection|text/dropdown| |yes
|Creation of data/comment | specify how you did your interviews | |text | | no 
|Time of creation |Specifies when research data was created | dc:date | start date; end date | | yes
|sampling|How did you select your test persons; what were the criteria? was sampling representative? | |text  | |yes
|unit of analysis | describe demographic of participants and other information like status or job | | text||no
|Instrument for creation|What you used to create the data, e.g. interview guidelines| |file | | yes
|Research discipline|What is the background of the discipline you created the data?| |text | | no
|Keyword   |Keyword from a controlled vocabulary |dc:subject   |text   | |yes
|Postscripts | Postscripts are all kind of notes you took, after interviews or observations | | text/possibility to upload files |provide additional information to the research data| no
|Language | Language in which the research data was created | cd:language | text| |yes
|Format | Format of the research data |dc:format| text| | no
|Type | Type of the data, if your format is qdpx, choose "dataset" | dc:type | text| | yes
|Rights | statement of copyright for the research data (defined by research data center) | dc:rights| text| | no
|Publisher | Name of the repository where data is published | dc:publishder | text | | no
