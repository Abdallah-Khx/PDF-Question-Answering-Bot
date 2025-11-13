# Watsonx PDF Question-Answering Bot (RAG Application)

## Overview
This project implements a **Retrieval-Augmented Generation (RAG)** application using IBM Watsonx and LangChain.  
The system allows users to upload a **PDF document** and ask questions about its content.  
The bot responds using information extracted from the uploaded file, providing accurate and context-aware answers.

The application is deployed through a **Gradio web interface**, enabling an interactive and user-friendly experience.

---

## Project Workflow

1. **Upload PDF**  
   The user uploads a PDF document via Gradio.

2. **Document Loading**  
   The PDF is parsed using `PyPDFLoader` to extract its textual contents.

3. **Text Splitting**  
   Text is chunked using `RecursiveCharacterTextSplitter` for optimal embedding and retrieval.

4. **Embedding Generation**  
   Chunks are embedded using IBM’s embedding model:  
   - `ibm/slate-125m-english-rtrvr-v2`

5. **Vector Store Creation (ChromaDB)**  
   Embeddings are stored in a Chroma vector database for fast semantic search.

6. **Retriever Setup**  
   Relevant chunks are selected using similarity-based retrieval.

7. **LLM Response Generation**  
   IBM Watsonx Granite 8B (`ibm/granite-3-2-8b-instruct`) generates the final answer using retrieved context.

8. **Gradio Interface**  
   User interacts with a web UI to upload PDFs and ask questions.

---

## Features

- **RAG-powered QA system** using Watsonx LLM
- **PDF document ingestion**
- **Automatic chunking and embedding**
- **Chroma vector store for semantic retrieval**
- **Context-aware answer generation**
- **Clean Gradio UI for ease of use**
- **Fully modular code (document loading, splitting, embeddings, vector DB, retriever, QA chain)**

---

## Tech Stack

- **Python**
- **LangChain**
- **IBM Watsonx**
  - Granite 8B instruct model
  - Watsonx Embeddings
- **ChromaDB** (vector store)
- **PyPDFLoader**
- **Gradio** (UI)

---

## Author

*Abdallah Khader* <br>
*AI Engineering* <br>
*RAG Application Project 2025* <br>
