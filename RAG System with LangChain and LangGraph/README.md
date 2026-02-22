# Retrieval-Augmented Generation (RAG) System using LangChain & LangGraph

This project implements a Retrieval-Augmented Generation (RAG) system that enhances large language model responses by grounding them in external documents.  

Instead of relying solely on a pre-trained model’s internal knowledge, the system retrieves relevant document chunks using vector similarity search and injects them into the model prompt to generate accurate, context-aware answers.

The workflow is orchestrated using LangGraph, enabling a modular and maintainable AI pipeline.

---

## Overview

Traditional LLMs can hallucinate or provide outdated information.  
This system improves reliability by:

1. Loading external documents.
2. Splitting them into smaller chunks.
3. Converting chunks into vector embeddings.
4. Performing semantic similarity search.
5. Injecting retrieved context into the LLM prompt.
6. Generating grounded answers.

The result is a domain-adaptable, context-aware question answering system.

---

## Architecture

The system consists of the following stages:

- Document Loading (LangChain)
- Text Chunking
- Embedding Generation
- Vector Storage
- Semantic Retrieval
- Answer Generation
- Workflow Orchestration (LangGraph)


# Workflow sequence:
User Question
↓
Classify
↓
Retrieve Relevant Chunks
↓
Generate Answer using Context
↓
Refine Output
↓
Final Response


LangGraph manages state transitions between these stages.

---

## Tech Stack

- Python 3.10+
- LangChain
- LangGraph
- OpenAI Embeddings
- GPT-4.1 (or compatible model)
- NetworkX
- Matplotlib

---

## How It Works
1. Document Loading

Documents are read from a JSON file and converted into LangChain Document objects.

2. Text Splitting

Large documents are split into overlapping chunks to preserve contextual continuity.

3. Embeddings

Each chunk is converted into a vector representation using OpenAI embeddings.

4. Vector Store

Vectors are stored in an in-memory vector database for similarity search.

5. Retrieval

When a user asks a question, the system retrieves the top-k most relevant document chunks.

6. Generation

The retrieved context is injected into a structured prompt and sent to the LLM to generate a grounded response.

7. Workflow Orchestration

LangGraph defines and executes the retrieval-generation pipeline as a stateful graph.

# Advantages

Grounded Responses – Reduces hallucination by using real documents.

Domain Adaptability – Easily switch knowledge bases for different domains.

Efficient Context Usage – Only relevant chunks are passed to the model.

Modular Workflow – LangGraph allows easy extension of pipeline stages.

Maintainable Architecture – Clear separation between retrieval and generation logic.

# Example Use Cases

Domain-specific chatbots

Research assistants

Internal company knowledge systems

Legal or healthcare document QA

Financial document analysis

# Future Improvements

Persistent vector database (e.g., Chroma, FAISS)

Web interface using FastAPI or Streamlit

Hybrid search (keyword + semantic)

Multi-document ingestion (PDFs, web scraping)

Evaluation metrics for answer accuracy
