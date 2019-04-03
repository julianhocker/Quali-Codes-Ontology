# Quali Codes Ontology
This describes the ontology I developed for qualitative coding frames. This ontology describes qualitative coding frames. It can be implemented easily. I kept the representation simple in an table, but might provide a version in RDF in the future. This is still work in progress, I also do some user testing on it. But if you encounter issues or have remarks I am happy to hear from you. Also if you want to implement it into your research data repository, I am happy to hear from you

## Structure
The ontology consists of several entities: the metadata for the codes, the metadata for the coding frames and also metadata to describe the research data that was analyzed, the publications that were created as well as the projects in which the coding frames were developed

## Coding frames
|Name   |Description   |   |   |   |
|---|---|---|---|---|
|   |   |   |   |   |
|   |   |   |   |   |
|   |   |   |   |   |

## Codes

## Projects

## Publications
These metadata help to identify the publication. In my prototype I do not want to implement a complete literature management, only basic information, so people can find the publication.

|Name   |Description   |Link to standard vocabulary   |   |   |
|---|---|---|---|---|
|Name   |Name of the publication   |dc:title   |   |   |
|Autor   |Name of the author   |dc:creator   |   |   |
|Date   |When was it published?   |dc:date   |   |   |
|DOI   |Unique identifier for document, preferable DOI   |dc:identifier   |   |   |

## Research data
Codes are often developed based on data, also data is sometimes created with certain questions in mind. I put them apart because there is also the possibility to use codes on several datasets and to reuse data

|Name   |Description   |Link to standard vocabulary   |   |   |
|---|---|---|---|---|
|DOI   |The unique identifier of the data|   |   |   |
|Creation of data| How data was created, e.g. interview, observation|DDI:ModeOfCollection
|sampling|How did you select your test persons| |  | ||
|Sampling size|How many interviews/observation did you do?
|Instrument for creation|What people used to create the data, e.g. interview guidelines
|Project|In what project was the data created?   |   |   |   |
|Example data|Possibility to upload e.g. one interview that you are allowed to publish|   |   |   |
|Research discipline|What is the background of the discipline you created the data?
|Further description|Field to add further information
