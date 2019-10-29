# Qualitative Codes Ontology
This describes the ontology I developed for qualitative coding frames. This ontology describes qualitative coding frames. It can be implemented easily. I kept the representation simple in an table, but might provide a version in RDF in the future. This is still work in progress, I also do some user testing on it. But if you encounter issues or have remarks I am happy to hear from you. Also if you want to implement it into your research data repository, I am happy to hear from you.

This is a beta-version of the complete ontology, I am doing some user testing until the beginning of 2020, but I am also happy to hear your opinion. Just open an issue ;)

## Relations
![Relations between codes](https://github.com/julianhocker/Quali-Codes-Ontology/blob/master/relations.png "Relations between codes")

## Structure
The ontology consists of several entities: the metadata for the codes, the metadata for the coding frames and also metadata to describe the research data that was analyzed, the publications that were created as well as the projects in which the coding frames were developed

## Coding frames

|Name   |Description   |  Link to standard vocabulary   |type of field  |   |
|---|---|---|---|---|
|Author   |Person, who created the code   |   |text   |   |
|Method |Which method you used to create the codes, e.g. Grounded Theory with Strauss/Glaser or Strauss/Corbyn|   |text/dropdown   |   |
|Discipline   |What is the background of the researcher   |   |text   |   |
|Theoretical background   |Which theories did you use, e.g. from psychology, sociology |   |text  |   |
|Date|When did you create the codes  |dc:date   |date   |   |
|Research questions   |What were the research questions you wanted to answer? |   |text   |   |
|Software|Which software was used, or did you code on paper?| |text
|Project   |Link to project in which the coding frame was created   |   |URL   |   |
|Data   |Link to data on which the coding frame was developed |   |URL   |   |
|Publication   |Link to publication |   |URL   |   |
|Coding frame as QDA-XML   |Possibility to upload complete coding frame via [REFI-QDA Codebook](https://www.qdasoftware.org/products-codebook-exchange/)   |   |File   |   |
|Coding frame as XML Project exchange file   |Possibility to upload complete coding frame via [REFI-QDA Project ](https://www.qdasoftware.org/products-project-exchange/)   |   |File   |   |
|Description of coding |How did you code? According to Saldana (2015, p 68)| |text/dropdown
|Description of dimensionalization| How did you do axial coding if you used Grounded Theory?| | text
|Maps | Possibiilty to upload maps if you used Situation analysis| |file
|Further description | Add further description | |text

## Codes
This describes the codes itself. I used as a basis the book 'The coding manual for qualitative researchers' by Saldana (see page xx) and the book 'qualitative content analysis in practice' by Schreier.

|Name   |Description   |Link to standard vocabulary   |type of field   |   |
|---|---|---|---|---|
|Name   |Name of the code   |   |text   |   |
|Including criterion   |What needs to be in the text to use this code   |   |text   |   |
|Excluding criterion   |When not to use it |   |text   |   |
|Anchor example   |Example when code is used |   |text   |   |
|Counter example   |Example when not to use this code |   |text   |   |
|Connection between codes   |How does this code relate to another code?  |Could use connections provided by SKOS, not decided yet   |link/SKOS  |   |
|Provenence|Where does code come from (e.g. other study or in-vivo)| |text

## Study
In interviews I got the feedback that it is important, how the coding frames were created. Therefore I added the possibility to add information about the project.

|Name   |Description   |Link to standard vocabulary   | type of field   | |
|---|---|---|---|---|
|Name   |Name of the study   |   |text   |   
|Persons   |People who are involved in the project   |   |text   | 
|contact person   |People who can be contacted if there are questions   |   |text   |   
|Date   |When was the project active?   |  |text field/time span   |   
|Description   |Description of the study, contains research method and implication; research questions and goals; also theoretical background and if there were primary or secondary data |   |text   |  
|Link   |Link to webpage of the project where users can get more information |   |URL   |  
|Research area   |In which area of research was it conducted? |   |text   |  
|Kind of study   |internal project/dissertation/third-party-funded |   |text   |  
|Keyword   |Keyword from a controlled vocabulary |   |text   |  

## Publications
These metadata help to identify the publication. In my prototype I do not want to implement a complete literature management, only basic information, so people can find the publication.

|Name   |Description   |Link to standard vocabulary   |type of field   |   |
|---|---|---|---|---|
|Name   |Name of the publication   |dc:title     |text   |
|Autor   |Name of the author   |dc:creator    |text   |
|Date   |When was it published?   |dc:date   |date   |
|DOI   |Unique identifier for document, preferable DOI or other like URN   |dc:identifier   |DOI   |   |
|Keyword   |Keyword that describes the publication   |  |Controlled vocabulary   |   |
|Abstract   |Abstract of the publication   |   |Text   |   |
|Bibliographic string|Information about publication that you can copy to cite it (only needed if no Unique identifier is provided)| |Text||

## Research data
Codes are often developed based on data, also data is sometimes created with certain questions in mind. I put them apart because there is also the possibility to use codes on several datasets and to reuse data. In an optimal world, this research data would just be in your research data archive and therefore people can just with one click get the data as well as the codes ;)

|Name   |Description   |Link to standard vocabulary   |type of field   |   |
|---|---|---|---|---|
|DOI   |The unique identifier of the data|   |DOI   |   |
|Creation of data| How data was created, e.g. interview, observation|DDI:ModeOfCollection|text
|sampling|How did you select your test persons; what were the criteria? was sampling representative? demographic background of participants, how many people were involved?| |text  | ||
|Instrument for creation|What you used to create the data, e.g. interview guidelines| |file
|Research discipline|What is the background of the discipline you created the data?| |text
|Research question|What research questions lead the creation of the data| |text
|Keyword   |Keyword from a controlled vocabulary |   |text   | 
