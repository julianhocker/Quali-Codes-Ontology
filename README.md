# Qualitative Codes Ontology (QualiCO)
This describes the ontology I developed for qualitative coding schemas. This ontology describes qualitative coding schemas. It can be implemented easily. I kept the representation simple in an table, but might provide a version in RDF in the future. This is still work in progress, I also do some user testing on it. But if you encounter issues or have remarks I am happy to hear from you. Also if you want to implement it into your research data repository, I am happy to hear from you.

There are two publications on this research out: 
* Julian Hocker, Taryn Bipat, Mark Zachry, and David W. McDonald. 2020. Sharing your coding schemas: Developing a Platform to fit within the Qualitative Research Workflow. In Proceedings of the 16th International Symposium on Open Collaboration (OpenSym 2020). Association for Computing Machinery, New York, NY, USA, Article 2, 1–10. DOI:https://doi.org/10.1145/3412569.3412574
*  Hocker, J., Schindler, C. and Rittberger, M. (2020), "Participatory design for ontologies: a case study of an open science ontology for qualitative coding schemas", Aslib Journal of Information Management, Vol. 72 No. 4, pp. 671-685. https://doi.org/10.1108/AJIM-11-2019-0320 
  
I used to following standards to comply with other work in the field:
* Bibliographic information: [BiBo](https://github.com/structureddynamics/Bibliographic-Ontology-BIBO)
* research data description: [DDI](https://ddialliance.org/) and the [metadata schema by Verbund FDB](https://www.forschungsdaten-bildung.de/files/fdbinfo_8_Metadatenset_v1.0.pdf) (German association for research data in education)


## Relations
![Relations between codes](https://github.com/julianhocker/Quali-Codes-Ontology/blob/master/relations.png "Relations between codes")

## Structure
The ontology consists of several entities: the metadata for the codes, the metadata for the coding frames and also metadata to describe the research data that was analyzed, the publications that were created as well as the projects in which the coding frames were developed

## Coding Schema

|Name   |Description   |  Link to standard vocabulary   |type of field  |justification/background| required|
|---|---|---|---|---|---|
|Author   |Person, who created the code   |   |text   |   |yes
|Method |Which method you used to create the codes, e.g. Grounded Theory with Strauss/Glaser or Strauss/Corbyn. |   |text/dropdown   |   |yes
|Method comment |specify further how you used the method. Also describe how strictly you used these methods| | text |qualitative methods are quite diverse and people use them quite openly|no
|Research area   |Where do you see this research?   |   |text   |   |yes
|Theoretical background   |Which theories did you use, e.g. from psychology, sociology and which codes did you derive from these? |   |text  |   |yes
|Research questions   |What were the research questions you wanted to answer? |   |text   |   |yes
|Process of creation|Describe how you created the codes. Did you code alone or with a team? How did you create the codes? How and which codes did you change in the process and why? | text | | yes
|Coding cycles | Describe how you coded, based on Saldana (2015, coding manual for qualitative researchers,  p 68) | | text/dropdown | | no
|Description of coding cycles |How did you code? Describe the process how you coded the data. | |text | not everyone is familiar with Saldana, so people can give more information about the coding cycles here. Also describe how you did dimensionalization if you used Grounded Theory | yes
|Inter-coder reliability|How high was the inter-coder-reliability? How did you measure it| | text | |no
|Software|Which software was used, or did you code on paper?| |text | | yes
|Date|When did you create the codes (start and end date)  |dc:date   |date   |   |yes
|Coding schema as QDA-XML   |Possibility to upload complete coding frame via [REFI-QDA Codebook](https://www.qdasoftware.org/products-codebook-exchange/) or other way to exchange all codes  |   |File   |   | yes
|Project as XML Project exchange file   |Possibility to upload complete coding frame via [REFI-QDA Project ](https://www.qdasoftware.org/products-project-exchange/)   |   |File   |   |no
|Visualizations | Possibiilty to upload visualizations, e.g. maps if you used Situation analysis| |file |Visualizations are important ways to get an overview on the codes and can help others understand your codes | no
|Keywords|Keywords for the research|for German: Thesaurus Bildungsforschung | text | |yes

## Codes
This describes the codes itself. I used as a basis the book 'The coding manual for qualitative researchers' by Saldana (see page xx) and the book 'qualitative content analysis in practice' by Schreier.

|Name   |Description   |Link to standard vocabulary   |type of field   |   | Required
|---|---|---|---|---|---|
|Name   |Name of the code   |   |text   |   |yes
|Including criterion   |What needs to be in the text to use this code   |   |text   |Saldana (2015)|no
|Excluding criterion   |When not to use it |   |text   |   |no
|Anchor example   |Example when code is used |   |text   |   |yes
|Counter example   |Example when not to use this code |   |text   |   |no
|Provenence|Where does code come from? | |text/dropdown (inductive, deductive, in-vivo, socially constructed)| | yes
|Count|How often code was used in reserach project | | number
|Number of connections to other codes | to how many other codes is the code connected in your coding schema in Grounded Theory? | | number |no
## Study
In interviews I got the feedback that it is important, how the coding frames were created. Therefore I added the possibility to add information about the project. First, this was named project and then renamed to study because [DDI](https://ddialliance.org) as well as research data centers like [Forschungsdatenzentum Bildung](https://www.fdz-bildung.de/) focus on studies rather than projects.

|Name   |Description   |Link to standard vocabulary   | type of field   |Justification/background|
|---|---|---|---|---|
|Name   |Name of the study   |   |text   |   
|Persons   |People who are involved in the project   |   |text|People mentioned that it makes sense to see who was involved to get a glimpse of how the ideas were 
|contact person   |People who can be contacted if there are questions   |   |text   |People mentioned in design phase II that it makes sense to have a person that they can contact and this is more important than the head of the project, which might be not involved that much  
|Institutions | Institutions who did the study | | text | 
|Date   |When was the project active?   |  |text field/time span|important to see when the study was done 
|Description   |Description of the study, contains research method and implication; research questions and goals; also theoretical background and if there were primary or secondary data |   |text   |  
|Link   |Link to webpage of the project where users can get more information |   |URL|It was mentioned that people want to get in contact and find out more about the study, therefore the link to the study   
|Kind of study   |internal project/dissertation/third-party-funded |   |text/dropdown   |  
|Comment to kind of study | possibility to give further information | text |
|sub-studies | link to sub-studies that were part of this study | | link| Participants expressed need to link studies if they were part of larger studies
|Keyword   |Keyword from a controlled vocabulary |   |text   |  

## Publications
These metadata help to identify the publication. In my prototype I do not want to implement a complete literature management, only basic information, so people can find the publication.

|Name   |Description   |Link to standard vocabulary   |type of field   |Justification/background|
|---|---|---|---|---|
|Title   |Title of the publication   |dc:title     |text   |standards for literature description|
|Autor   |Name of the author   |dc:creator    |text   |standards for literature description|
|Date   |When was it published?   |dc:date   |date   |standards for literature description|
|DOI   |Unique identifier for document, preferable DOI or other like URN   |dc:identifier   |DOI   |standards for literature description|
|Keyword   |Keyword that describes the publication   |  |Controlled vocabulary   |   |
|Abstract   |Abstract of the publication   |   |Text   |Mentioned in interviews, people thought it makes sense, so they do not have to click on DOI to see abstract|
|Bibliographic string|Information about publication that you can copy to cite it (only needed if no Unique identifier is provided)| |Text|mentioned in interviews, makes literature easier to find when there is no DOI|

## Research data
Codes are often developed based on data, also data is sometimes created with certain questions in mind. I put them apart because there is also the possibility to use codes on several datasets and to reuse data. In an optimal world, this research data would just be in your research data archive and therefore people can just with one click get the data as well as the codes ;)

|Name   |Description   |Link to standard vocabulary   |type of field   |Justification/background|
|---|---|---|---|---|
|DOI   |The unique identifier of the data|   |DOI   |   |
|Creation of data| How data was created, e.g. interview, observation|DDI:ModeOfCollection|text/dropdown
|Creation of data/comment | specify how you did your interviews | 
|sampling|How did you select your test persons; what were the criteria? was sampling representative? | |text  | |
|unit of analysis | describe demographic of participants and other information like status or job | | text|
|Instrument for creation|What you used to create the data, e.g. interview guidelines| |file
|Research discipline|What is the background of the discipline you created the data?| |text
|Keyword   |Keyword from a controlled vocabulary |   |text   | 
|Postscripts | Postscripts are all kind of notes you took, after interviews or observations | | text/possibility to upload files |provide additional information to the research data
