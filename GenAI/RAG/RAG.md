# What is RAG?

### Defination : 

    RAG is an Advance AI technique is AI technique thst combines Retrieval system With a generative Large language Model to produce more accurate and contextually relevant answers.


# Retrievel-Augmented Generation

## Retrieval:
The system searches a knowledge-base or database (like documents, PDFs, or websites ,vector database(qudrent ,FAISS , Pinecone)) to find relevant information about the user’s query.

## Augmentation:(user query + Retrieval Data) 
The word “augmentation” simply means enhancement or addition.

Adding external information (retrieved from a knowledge source) to the language model’s internal knowledge before generating the answer.

The retrived information is then added to the user original prompt.

## Generation:(Generat answer usign Rag augmentation)
The LLM model like(GPT,claude) then reads those retrived documents and use them to craft a final answer --in human -like-language and natural


### Exmple: 

    🧱 RAG Architecture (Conceptually)
    User Query
    ↓
    Retriever → searches in → Knowledge Base (vector database like FAISS, Pinecone, etc.)
    ↓
    Top Relevant Documents
    ↓
    Generator (e.g., GPT model)
    ↓
    Final Answer (with context from retrieved docs)

### Structure : [Data Source] --> LLM(System prompt) --> Chat

use Business data from the db and convert into TEXT and set with llm system prompt and then user chat with llm for get information about our own business data,live data , old data etc

EX: User upload business seels pdf file in system then after stord data in DB(ex : postgres etc..) and when user ask any time for get information about the owne business when llm use this perticuler user business data and give all answer the qestion with user friendly

But here is one problem for limitation token size(llm token windows size)  below solution available 

# RAG Small Pipline Exmple with manage Token limitation with chunks

path : ![Alt text](.Langchain\img\RAG_small_pipline.png)
 
This pipline Help to understand HOW RAG techniques is work

# Magic Code 🧠

Here above available define RAG structur and RAG small pipline

    Structur : [Data source] --> [LLM generate] --> chat

    What exactly do here between Data source and LLM response

Here available a Image

```bash
title : RAG How to hendle base DATA
path : GenAI-> img->02_image number 🧠  
```
## Understand this Image 🧠:
- *1. Indexing/ ingestion*
    - when upload and give user owne base Knowledge when conver into chunk range(100,200,500) according model capacity(Token Windows) in vector databse

    - ingestion process run only one time when user gives any kind of data , no required to process every time with user data becuse they alredy stord in vector DB

    - User data first convert into text like pdf ->text ,image->OCR, CSV -> text.

- *2. retrival(RAG)* 
    - get user query convert into vector and match(search) vecto in vector db (user vector == db vector) then db send response while DB response and User query send to LLM model this LLM model create human like answer using Base knowledge.

    user query ->convert into vector -> serch same vector in vector DB -> DB send response -> send to llm query and DB response -> LLM Create Human like response -> send all answer to User. 

**NOTE : [SOTA]: State of the art (clude soneate,GPT,gemini ,lama)**



