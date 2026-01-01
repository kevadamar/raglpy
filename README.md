# RAGL

Sebuah experiment pembelajaran untuk kumpulan percobaan RAG (Retrieval-Augmented Generation).

## Overview

This repository contains experimental implementations of RAG systems for learning and research purposes. The experiments explore various techniques for document chunking, embedding generation, vector storage, and LLM-based question answering.

## Tech Stack

- **LangChain** - Framework for LLM applications
- **FAISS** - Vector similarity search (learn-1.ipynb)
- **ChromaDB** - Persistent vector database (learn-2.ipynb)
- **Sentence Transformers** - Text embeddings (all-MiniLM-L6-v2)
- **NLTK** - Text splitting for document chunking
- **Google Generative AI** - Gemini 2.5 Flash for answer generation and embeddings (gemini-embedding-001)
- **PyPDF** - PDF document loading
- **LangChain Community** - Document loaders and utilities

## Setup

1. Create a virtual environment:
```bash
python -m venv .venv
source .venv/bin/activate  # Linux/Mac
# or
.venv\Scripts\activate  # Windows
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Configure environment variables:
```bash
cp .env.example .env
# Edit .env and add your GEMINI_API_KEY
```

## Usage

This repository contains multiple notebooks demonstrating different RAG implementations:

### [learn-1.ipynb](learn-1.ipynb) - Basic RAG with FAISS
A simple RAG implementation demonstrating:
- Loading and chunking documents with RecursiveCharacterTextSplitter
- Generating embeddings with Sentence Transformers (all-MiniLM-L6-v2)
- Building a FAISS vector index for similarity search
- Retrieving relevant chunks based on queries
- Generating answers using Google Gemini

### [learn-2.ipynb](learn-2.ipynb) - RAG with ChromaDB
A more advanced RAG implementation featuring:
- Loading PDF documents with PyPDFLoader
- Text chunking with NLTKTextSplitter
- Using Google Generative AI embeddings (gemini-embedding-001)
- Persistent vector storage with ChromaDB
- LangChain RAG chain with RunnablePassthrough
- Multi-language support (Indonesian queries)

## License

MIT
