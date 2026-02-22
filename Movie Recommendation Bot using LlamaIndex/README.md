# Movie Recommendation Bot using LlamaIndex

This project implements a movie recommendation chatbot using LlamaIndex and Hugging Face models.  
The system indexes movie data from a CSV file, converts it into vector embeddings, and allows users to query the dataset using natural language.

The bot recommends movies based on genre and rating, demonstrating how LlamaIndex can power intelligent retrieval-based AI applications.

---

## Project Overview

AI agents are becoming increasingly important in building modern AI systems.  
This project showcases how LlamaIndex can be used to:

- Index structured data (CSV dataset)
- Convert text into vector embeddings
- Enable natural language querying
- Generate context-aware responses using an LLM

The system works as follows:

1. The user enters a query such as "Show me some action movies".
2. The system searches through indexed movie data.
3. Relevant movies are retrieved based on semantic similarity.
4. The language model generates formatted recommendations.
5. The user receives a clean, readable list of movies.

---

## Features

- Natural language movie search
- Vector-based semantic retrieval
- Hugging Face embedding model
- Lightweight LLM for response generation
- CSV-based dataset ingestion
- Interactive command-line chatbot
- Optimized model loading using 4-bit quantization

---

## Tech Stack

- Python 3.10+
- LlamaIndex
- Hugging Face Transformers
- PyTorch
- Sentence Transformers
- TinyLlama Chat Model
- Pandas

---

## Dataset

This project uses a CSV file containing:

Movie ID

Title

Genre

Rating

# Model Configuration
Embedding Model

sentence-transformers/all-MiniLM-L6-v2

Converts movie descriptions into vector embeddings for semantic search.

Language Model

TinyLlama/TinyLlama-1.1B-Chat-v1.0

Generates formatted responses based on retrieved documents.

Loaded in 4-bit mode for memory efficiency.

# How It Works
1. Load Dataset

Reads CSV file into a Pandas DataFrame.

2. Create Document Objects

Each movie row is converted into a LlamaIndex Document with metadata.

3. Build Vector Index

A VectorStoreIndex is created from the documents to enable fast similarity search.

4. Query Engine

The query engine retrieves relevant movie entries based on user input.

5. Response Formatting

The raw model response is cleaned and formatted into a structured recommendation list.

# Running the Application

Run the script:

python movie_bot.py

Use Cases of LlamaIndex

Recommendation Systems

Document Search Engines

Enterprise Knowledge Retrieval

Chatbots and Virtual Assistants

Sentiment Analysis

Multilingual Information Retrieval

# Advantages

Handles structured and semi-structured data

Supports large datasets

Modular indexing system

Easy integration with Hugging Face models

Memory-efficient model loading

# Future Improvements

Add rating-based ranking logic

Support multi-genre filtering

Add web UI using Streamlit

Deploy using FastAPI

Replace CSV with database backend

Add user personalization history
You will see:

Welcome to MovieRecBot!
How can I assist you in finding your next movie to watch?

Enter a genre such as:

Action

Type:

exit

to end the session.

Example Output
MovieRecs Assistant:
- The Dark Knight
- Mad Max: Fury Road
- Gladiator
