ShopKart AI Customer Support Assistant (RAG)

Overview

ShopKart AI Customer Support Assistant is a Retrieval-Augmented Generation (RAG) application designed to answer customer support queries using company policies as the source of truth.

Instead of relying solely on an LLM's pre-trained knowledge, the system retrieves relevant policy documents from a vector database and generates grounded responses based on retrieved information.

This approach helps reduce hallucinations and ensures responses remain aligned with business policies.

---

Architecture

Customer Query
↓
Embedding Generation (BGE Small)
↓
Semantic Search (ChromaDB)
↓
Relevant Policy Retrieval
↓
Grounded Prompt Construction
↓
Llama 3.3 70B (Groq)
↓
Customer Response

---

Features

- Retrieval-Augmented Generation (RAG)
- Semantic Search using Vector Embeddings
- ChromaDB Vector Database
- BGE Embedding Model
- Groq-hosted Llama 3.3 70B
- Policy-based Customer Support
- Grounded Response Generation
- Reduced Hallucinations
- Persistent Local Vector Storage

---

Technology Stack

AI & LLM

- Llama 3.3 70B Versatile
- Groq API

Embeddings

- BAAI/bge-small-en-v1.5

Vector Database

- ChromaDB

Backend

- Python

Supporting Libraries

- sentence-transformers
- chromadb
- python-dotenv
- groq

---

Knowledge Base

The application currently supports:

- Returns Policy
- Shipping Policy
- Warranty Policy
- Refund Policy

Each policy is embedded and stored inside ChromaDB for semantic retrieval.

---

How It Works

1. Customer submits a query.
2. Query is converted into vector embeddings.
3. ChromaDB performs similarity search.
4. Relevant policy chunks are retrieved.
5. Retrieved context is added to the prompt.
6. Llama 3.3 generates a grounded response.
7. Response is returned to the customer.

---

Example Queries

- How many days do I have to return an item?
- Is express delivery available in my city?
- Is my electronic device covered under warranty?
- When will my refund be processed?

---

Installation

pip install chromadb sentence-transformers groq python-dotenv

Create a ".env" file:

GROQ_API_KEY=your_api_key_here

Run:

python shopkart_rag.py

---

Future Enhancements

- Multi-turn conversation memory
- Order tracking integration
- Product recommendation engine
- Web UI using Streamlit
- Multi-agent customer support workflow
- Real-time policy updates

---

Learning Outcomes

This project demonstrates:

- Retrieval-Augmented Generation (RAG)
- Vector Databases
- Embedding Models
- Semantic Search
- Prompt Engineering
- LLM Integration
- AI-Powered Customer Support Systems

---

Author

Priyang Mishra

Exploring Agentic AI, RAG Systems, Prompt Engineering, and AI Automation.
