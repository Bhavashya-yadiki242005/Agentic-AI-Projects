# Vector Embedding Memory Chatbot (Python + ChromaDB)

This project implements a simple AI chatbot with long-term memory using **vector embeddings** and a **persistent vector database**.  
The system converts user conversations into embeddings, stores them in ChromaDB, and retrieves relevant past interactions using semantic search to provide context-aware responses.

Unlike traditional chatbots that forget earlier conversations, this assistant can recall previous messages, preferences, and facts even after restarting the application.

---

## Overview

The chatbot works in three main stages:

1. User input is converted into vector embeddings using Sentence Transformers.
2. These embeddings are stored in ChromaDB along with metadata (role, timestamp, conversation ID).
3. When a new query arrives, the system performs semantic similarity search to retrieve relevant memories and injects them into the LLM prompt before generating a response.

This enables:

- Context-aware replies
- Long-term memory
- Semantic (meaning-based) search instead of keyword matching
- Persistent storage across sessions

---

## Features

- Semantic memory using vector embeddings
- Persistent local memory with ChromaDB
- LLM-based response generation
- Automatic memory retrieval for relevant queries
- User and assistant messages stored together
- Interactive command-line chatbot
- Memory inspection and search utilities
- Preference seeding (e.g., language preference)

---

## Tech Stack

- Python 3.10+
- Transformers
- Sentence-Transformers
- ChromaDB
- PyTorch
- Qwen LLM
- HuggingFace Pipeline

---


---

## Installation

# 1. Clone or download the repository

bash
git clone <<YOUR_GITHUB_REPO_LINK>>
cd <<PROJECT_FOLDER>>

# 2. Install dependencies
bash:
pip install chromadb sentence-transformers transformers accelerate einops --upgrade

# Models Used

Chat Model: Qwen/Qwen2.5-0.5B-Instruct

Embedding Model: all-MiniLM-L6-v2

Running the Chatbot

Start the chatbot by running:

python main.py

You will enter an interactive loop:

You: What is vector embedding?
Assistant: ...

To exit:

exit

or

quit

# How Memory Works

Each message is stored as a structured memory item:

Role (user / assistant)

Content

User ID

Conversation ID

Timestamp

Vector embedding

When a new question is asked:

The query is embedded.

ChromaDB finds the most similar past memories.

Retrieved memories are added to the prompt.

The LLM generates a response using both memory and current input.

The new exchange is stored again.

This creates a continuously learning conversation history.

# Example Use Cases

Personal AI assistant with memory

Research assistant

Preference-aware chatbot

Long-term conversational agents

Learning vector databases and RAG concepts

Prototyping memory-enabled AI systems

Memory Search Utility

The project includes a utility to manually search stored memories:

retrieve("your query here")

d previous memories automatically.
