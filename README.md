# Creating a searchable database of General Post Office circulars

## Short summary
A question frequently posed to archivists at BT archives is “When did X location receive Y communication technology?” These questions and others like it can be answered by consulting the General Post Office circulars: a set of weekly informational bulletins produced by the Post Office for internal circulation until 1979. The circulars contain a vast amount of information on the historical workings of the Post Office, including: staff appointments, branch openings, mail ship sailings and new technology launches but, to date, no rapidly searchable index to these circulars has existed. Archivists have therefore had to rely on a spreadsheet of references to information in the circulars when seeking to answer questions. 

Our aim was to use digital methods, including generative AI, to create an automatic reference system for circulars dated between 1879 and 1979 that was capable of understanding and responding to queries posed to it in natural language. The task presented a significant challenge as although all of the circulars used by this investigation were typeset and digitised, their use of columnar layouts and tables in various formats, in addition to the poor scan quality of some of the documents, made automated interpretation of the information a challenging task. 

We developed a chatbot application that uses Retrieval Augmented Generation (RAG) to query the circulars in natural language and delivers a natural language response. The chatbot interface acts as the frontend to a vector database datastore, which holds sections of vectorised text from the circulars that are compared for proximity to the vectorised question posed by the user with responses being retrieved dependant on the proximity in vector space of the text sections to the question posed by the user. 


## Research questions

1) Can the circulars be brought together to create a searchable database?
   
2) Can we increase the speed at which an archivist can answer user enquiries about telecommunication installations in their focus area?

3) What accompanying material would a searchable database of communication developments need to ensure it was a) usable and b) useful to researchers?
   
4) Can we query the database to demonstrate how Bradford was speaking to the rest of the world over the 100 years?
   
5) Are there discernible patterns of change over time, and do these correlate to our understanding of social, political, economic, and cultural growth across Britain in the same period?



## People 

- **Natasha Kitcher**: Conceptualization, Data curation, Investigation, Resources, Validation, Writing - original draft, Writing - review & editing 

- **Nayomi Kasthuri Arachchi**: Data curation, Formal analysis, Investigation, Methodology, Software, Validation, Writing - original draft, Writing - review & editing



## Data
- Post Office Circulars 1879 - 1979, courtesy of BT Archives. All digitised and in PDF format.  


## Method


## Tools
- LlamaParse
- Qdrant Cloud vector database
- GPT-3.5 model from OpenAI
- GitHub Codespaces


## Outputs

## Key initial findings


## Challenges




## Licence 
This work is licensed under a [Creative Commons Attribution 4.0 License - CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
