# RAG AI Agent using n8n, Pinecone & HuggingFace

## 📌 Overview
This project implements a Retrieval-Augmented Generation (RAG) AI Agent using n8n workflows, Pinecone Vector Database, and HuggingFace embeddings.

It allows users to:
- Upload documents
- Convert them into vector embeddings
- Store them in Pinecone
- Query the data using an AI agent powered by Groq (LLaMA 3)

---

## 🧠 Architecture

The system consists of two main workflows:

### 1️⃣ Data Ingestion Pipeline
- Trigger: Manual execution
- Downloads file from Google Drive
- Splits text into chunks
- Converts text into embeddings
- Stores embeddings in Pinecone

### 2️⃣ RAG AI Agent Pipeline
- Trigger: Chat message
- Uses AI Agent with memory
- Retrieves relevant data from Pinecone
- Generates response using Groq LLM

---

## ⚙️ Tech Stack

- n8n – Workflow automation
- Pinecone – Vector database
- HuggingFace – Embeddings (BAAI/bge-small-en)
- Groq – LLM (llama-3.1-8b-instant)
- Google Drive API – File source

---

## 🚀 How to Run

### 1. Setup Requirements
- n8n installed (local/cloud)
- Pinecone account
- HuggingFace API key
- Groq API key
- Google Drive API access

### 2. Import Workflows
- Import both JSON workflow files into n8n
- Configure credentials

### 3. Run Data Pipeline
- Execute Data Loader workflow

### 4. Run AI Agent
- Activate RAG Agent workflow
- Send a chat message

---

## 📊 Features

- Retrieval-Augmented Generation (RAG)
- Vector search using Pinecone
- Context-aware AI responses
- Modular workflows
- Scalable architecture

---

## 👨‍💻 Author

Shravan
