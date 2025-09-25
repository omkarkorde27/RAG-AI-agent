RAG AI Agent
A Retrieval-Augmented Generation (RAG) AI agent built with Python that processes PDF documents, creates embeddings, stores them in a vector database, and provides intelligent question-answering capabilities using Large Language Models.
Features

Document Processing: Load and process PDF documents with automatic text chunking
Vector Embeddings: Generate high-quality embeddings using SentenceTransformers
Vector Storage: Persistent storage with ChromaDB for efficient similarity search
Intelligent Retrieval: Query-based document retrieval with similarity scoring
LLM Integration: Answer generation using Groq's LLama models
Advanced RAG Pipeline: Enhanced retrieval with confidence scoring and source attribution

Architecture
PDF Documents → Text Chunking → Embeddings → ChromaDB → RAG Retrieval → LLM Response
Installation

Clone the repository:

bashgit clone <repository-url>
cd RAG-AI-agent

Create a virtual environment:

bashpython -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate

Install dependencies:

bashpip install -r requirements.txt

Set up environment variables:

bash# Create a .env file in the root directory
echo "GROQ_API_KEY=your_groq_api_key_here" > .env
Project Structure
RAG-AI-agent/
├── main.py                    # Entry point
├── notebook/
│   └── document.ipynb         # Main RAG implementation notebook
├── data/
│   ├── pdf/                   # PDF documents storage
│   ├── text_files/            # Text documents storage
│   └── vector_store/          # ChromaDB persistence
├── requirements.txt           # Python dependencies
├── .env                       # Environment variables (create this)
└── README.md                  # This file
Usage
Quick Start

Place your PDF documents in the data/pdf/ directory
Run the Jupyter notebook:

bashjupyter notebook notebook/document.ipynb

Follow the notebook sections:

Document loading and chunking
Embedding generation
Vector store creation
RAG retrieval setup
Query processing