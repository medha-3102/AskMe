# AskMe – RAG-based Document Query Engine

AskMe is a query engine built using Retrieval-Augmented Generation (RAG) that allows users to upload PDF documents and ask questions based on their content. The system retrieves relevant context and generates accurate, context-aware responses.

## Features
- Upload PDF documents  
- Semantic search using embeddings  
- Question answering based on document content  
- Context-aware responses  
- Fast retrieval using vector database  
- Sentence-level similarity filtering  

## How It Works (RAG Pipeline)

1. Document Upload – Upload PDF files  
2. Text Extraction – Extract text using PyPDF  
3. Chunking – Split text into smaller chunks  
4. Embeddings – Convert chunks into vectors using Sentence Transformers  
5. Storage – Store embeddings in ChromaDB  
6. Query Processing  
   - Convert query into embedding  
   - Retrieve relevant chunks  
   - Perform sentence-level similarity  
7. Response Generation – Return answer from retrieved context  

## Tech Stack

- Python  
- Sentence-Transformers  
- Hugging Face Transformers  
- ChromaDB  
- PyPDF  
- NumPy  
- Google Colab  

## Installation

pip install sentence-transformers chromadb pypdf transformers accelerate

## Usage

### Upload PDF
```python
from google.colab import files
uploaded = files.upload()
