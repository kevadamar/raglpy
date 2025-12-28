# RAGL

Sebuah experiment pembelajaran untuk kumpulan percobaan RAG (Retrieval-Augmented Generation).

## Overview

This repository contains experimental implementations of RAG systems for learning and research purposes. The experiments explore various techniques for document chunking, embedding generation, vector storage, and LLM-based question answering.

## Tech Stack

- **LangChain** - Framework for LLM applications
- **FAISS** - Vector similarity search
- **Sentence Transformers** - Text embeddings (all-MiniLM-L6-v2)
- **Google Generative AI** - Gemini 2.5 Flash for answer generation
- **Transformers** - Hugging Face transformers library

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

See [learn-1.ipynb](learn-1.ipynb) for a complete example demonstrating:
- Loading and chunking documents
- Generating embeddings with Sentence Transformers
- Building a FAISS vector index
- Retrieving relevant chunks based on queries
- Generating answers using Google Gemini

## License

MIT
