# Llama Index RAG ChatBot

A Retrieval-Augmented Generation (RAG) chatbot built with Llama Index for intelligent document analysis and querying. This project demonstrates how to create a powerful Q&A system that extracts specific information from documents using embeddings and vector search.

## Overview

This chatbot is designed to intelligently parse and query legal documents (such as lease agreements) using:
- Llama Index - for document indexing and retrieval
- HuggingFace Embeddings - for semantic understanding
- Vector Search - for finding relevant document chunks
- Custom Prompts - for structured information extraction

## Features

-  **Document Loading**: Load multiple documents from a directory
-  **Semantic Search**: Uses vector embeddings to find relevant content
-  **Structured Extraction**: Extract lease details in JSON format
-  **Custom Prompts**: Define specific queries for targeted information retrieval
-  **Index Persistence**: Save and load indexes for efficient reuse
-  **Source Tracking**: Get references to the original document sections

## Installation

### Prerequisites
- Python 3.8+
- pip

### Setup

1. Install required dependencies:
```bash
pip install --upgrade llama-index langchain sentence-transformers -q
pip install llama-index llama-index-embeddings-huggingface

llama_index_chatbot/
├── llama_index_RAG_ChatBot.ipynb  # Main notebook with all code
├── sample_data/                   # Your documents to index
├── lease_index/                   # Persisted vector store index
└── README.md                      # This file

Configuration
Embedding Model: BAAI/bge-small-en-v1.5 (HuggingFace)
Similarity Top K: Number of relevant chunks to retrieve (adjust as needed)
Storage Directory: lease_index/ for index persistence

Use Cases
Contract Analysis: Extract key terms from legal documents
Document Q&A: Answer questions about document contents
Data Extraction: Automatically extract structured data from unstructured documents
Multi-Document Search: Query across multiple documents simultaneously


Performance Tips
Increase similarity_top_k for more comprehensive but slower results
Use smaller embedding models for faster inference on CPU
Persist indexes to avoid rebuilding on each run
Filter documents before indexing to reduce size

**Requirements**
llama-index
llama-index-embeddings-huggingface
langchain
sentence-transformers
Python 3.8+
