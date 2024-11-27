---
aliases:
  - "Types of RAG: An Overview (article)"
up:
  - [[AI-articles]]
---
up:  [[AI-articles]]
URL: https://blog.jayanthk.in/types-of-rag-an-overview-0e2b3ed71b82
# Types of RAG: An Overview
Jayanth Krishnaprakash  Jan 20, 2024

Retrieval Augmented Generation is the hottest technique in the current world of AI to prevent Large Language Models from hallucination and enable them to generate accurate responses. Talking about the various types of RAG approaches, it can be broadly classified into three categories: Naive RAG, Advanced RAG and Modular RAG. In this article, we’ll look at these three types and the shortcomings of one approach which led to the other.

## Naive RAG
This paradigm of RAG is the earliest adopted methodology. This technique came into the limelight after the realization of the fact that LLMs can’t keep up with realtime data and can’t answer queries related to topics which weren’t a part of the model’s training data. For example, if you ask ChatGPT 3.5 about the 2023 ICC Cricket World Cup, it cannot answer because the model’s cutoff knowledge was before this event happened and hence it cannot answer queries related to that.

The Naive RAG technique follows a process that includes indexing, retrieving, augmenting and generation of response. Let’s look at each of the steps one by one in detail.

![[1_xboctXHU2A49SiJqjjKxkg.webp]]
Naive RAG

### Indexing

Indexing is the data preparation step where the data on which retrieval is performed is extracted and cleaned from data sources like files, URLs etc. and converted to plain text. This plain text is commonly a string of multiple thousands of characters. For instance, say you want to perform question answering from your university textbook with help of LLMs. The entire book cannot be fed to the LLM since it might exceed the context window of the LLM. Hence, we break the entire content into smaller and manageable pieces called chunks, and this process is called chunking. These chunks are then transformed into high-dimensional vectors with help of embedding models. At the end of this step, we have a list of chunk-vector pairs of the data source.

### Retrieval

This is a crucial step in the process where once the user query is received, the same embedding model used to create vectors of the data sources is used to encode the query into a vector. This vector is used to perform similarity search over the pool of vector embeddings of the data sources and find out the most similar chunks. The similarity search methods that are mostly employed are cosine similarity, dot product, euclidean distance etc. The retrieved chunks are used in the generation step to get response.

### Generation

The retrieved chunks along with the user query and instructions are coalesced into a single prompt, which is then fed to the LLM for generating response. Due to the addition of extra information to the prompt, the LLM has sufficient data to generate relevant response. It can be restricted to provide response adhering only to the retrieved chunks. Feeding the chat history of the interactive conversation between the LLM and the user also improves the quality of responses.

### Shortcomings of Naive RAG

Naive RAG approach has a lot of shortcomings when it comes to reducing hallucinations. This approach suffers from low precision when relevant chunks are not retrieved properly. The presence of outdated data in the corpus leads to inaccurate chunk retrieval. The response generated may not be grounded on the additional context provided. The sequencing of chunks does matter. The order in which the chunks are arranged should be according to the relevance to the query. There’s also a risk of constraining the response and it just containing the retrieved information

## Advanced RAG

The Advanced RAG approach was developed to overcome the shortcomings of Naive RAG. In addition to the steps involved in Naive RAG, a bunch of techniques are implemented to improve the quality of responses, which includes Pre-retrieval and Post-retrieval processes.

![[1_Bw_Mz4oqzddpXjcE2zPEww.webp]]
Advanced RAG

### Pre-Retrieval Processes

The goal of this process is to improve the quality of content being indexed. The standard of text from data sources is enhanced by removing irrelevant information, removing ambiguity and inaccuracies, maintaining context, updating outdated documents etc. Adding suitable metadata to each chunk significantly improves the quality of retrieved documents. There might be scenarios where the user query may not be the best prompt to feed to the LLM. So, query rewriting techniques are implemented where we rewrite the query based on the LLM’s characteristics to improve the quality of generation.

### Post-Retrieval Processes

After the high-quality chunks are retrieved, the way in which these are merged with the user query to form the prompt influences the quality of generation. Simply appending chunks to the user query may exceed the context window limit, introduce noise and degrade the response quality. So, additional techniques like re-ranking, prompt compression are implemented to overcome these challenges.

Reranking technique is implemented to reorder the sequence of retrieved chunks based on the contextual similarity between the chunk and the user query rather than just comparing the vector similarity. Prompt compression technique is used to reduce noise in the retrieved documents. This includes compressing irrelevant information, highlighting important passages, reducing context length etc.

## Modular RAG

The Modular RAG approach differs from the traditional Naive RAG by introducing enhanced functionalities. ==It integrates a search module for similarity retrieval and adopts a fine-tuning approach in the retriever.== This structure, increasingly common in the RAG domain, provides greater adaptability through restructured modules and iterative methodologies. It allows for either a serialized pipeline or end-to-end training, addressing specific challenges more effectively. The connection between the paradigms — Naive RAG, Advanced RAG, and Modular RAG — demonstrates a relationship of inheritance and developmental progression. Some techniques include Hybrid Search, Recursive Retrieval and Querying, Step-back approach, Sub-queries, Hypothetical Document Embeddings.

### Hybrid Search

Hybrid Search optimizes RAG performance by integrating various search techniques, including keyword-based, semantic, and vector searches. This approach leverages each method’s strengths to ensure consistent retrieval of relevant and context-rich information, enhancing the overall efficacy of the RAG pipeline.

### Recursive Retrieval and Query Engine

Recursive Retrieval involves acquiring smaller chunks initially to capture key semantic meanings, providing larger chunks with more contextual information to the LLM later. This two-step retrieval method strikes a balance between efficiency and delivering contextually rich responses.

### StepBack approach

The StepBack-prompt approach encourages the LLM to reason around broader concepts and principles, leading to improved performance in challenging, inference-based tasks. This retrieval-enhancing step is applied both in generating responses to backward prompts and in the final question-answering process.

### Sub-Queries

Depending on the scenario, various query strategies like tree queries, vector queries, or simple sequential querying of chunks can be employed as sub-queries in Modular RAG.

### Hypothetical Document Embeddings
Hyde operates on the belief that generated answers might be closer in the embedding space than a direct query. Using the LLM, Hyde creates a hypothetical document in response to a query and uses its resulting embedding to retrieve real documents similar to the hypothetical one. While effective, it may have limitations when the language model is unfamiliar with the subject matter, potentially leading to errors.

## Conclusion
This article explains the various RAG approaches in detail, along with the shortcomings and improvements of each. In the upcoming blogs, we’ll look at the technical implementation of some RAG techniques.