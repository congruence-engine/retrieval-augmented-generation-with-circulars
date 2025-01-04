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
We used a Retrieval Augmented Generation (RAG) strategy to transform the digitised circulars into a searchable database. 

​​The pipeline was constructed sequentially, commencing with the indexing phase followed by the creation of the retrieval mechanism and finally an interface to allow for generation.

In the indexing phase, the files containing the circulars were first parsed from PDF into markdown in sections using a parser developed specifically for PDF files with complex layouts. Conversion from PDF format was required in order to convert the text into a form that could be vectorised further on in the process. Markdown is a useful format to use in RAG applications as it provides the ability to preserve the underlying format of the text and therefore helps to preserve context. 

The markdown outputs were then chunked into smaller sections of text, transformed into vector embeddings and stored in a vector database. The retrieval and generation phases of the pipeline were facilitated through the use of a chat interface built using Chainlit, a Python-based framework for creating and managing chat applications that was implemented using the LangChain framework. Query retrieval and generation was handled using OpenAI’s chat models (GPT-3.5 at the time that the RAG pipeline was assembled). 


## Tools
- LlamaParse
- Qdrant Cloud vector database
- GPT-3.5 model from OpenAI
- GitHub Codespaces


## Outputs
Code and instructions for reassembling the pipeline in an environment of choice:
- rag_llamaparse.ipynb: a Jupyter notebook providing a simple way to get up and running parsing and querying small sections of parsed material from the circulars. Not intended for sections of text greater than c.25 pages. Set up for and tested in a Google Colab environment.
- parse.py: a Python file for parsing the circulars to markdown using LlamaParse, chunking the text, creating vector embeddings and finally storing these embeddings in a vector database
- app.py: a Python file for launching a chat application using Chainlit for querying the database of information extracted from the circulars 
- codespace_instructions.pdf: a primer describing how to configure a GitHub codespace for launching the RAG application  



## Key initial findings


## Challenges




## Licence 
This work is licensed under a [Creative Commons Attribution 4.0 License - CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
