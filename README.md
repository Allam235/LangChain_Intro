# Synthetic Patient Data Retrival

## 📁 Project Branches

This repository contains different versions of the project tailored for specific use cases. Switch branches depending on what you want to run:

* **`main`**: A RAG Retrival Pipeline using a StreamLit app to query info using a MySQL Database of Patient Data as context
* **`notebook-intro`**: A Basic RAG Retrival Pipeline to learn LangChain - Learned from https://www.youtube.com/watch?v=o126p1QN_RI



### Basic RAG Retrieval Pipeline
Introduction to RAG using LangChain

- Document Loader
    - Loads PDFs and other modals into Langchain Documents
- Chunking
    - Recursive Text Chunking by chunk size, and overlap some amount of text between chunks
- Embedding Manager
    - Uses SentanceTransformer with a HuggingFace model to generate embeddings
- VectorStore
    - Creates a Chroma DB Vector Store Collection
    - Adds the metadata stored in the chunked documents, and the embeddings
- Rag Retrieval
    - Embeds Query as a vector, runs cosine similarity, and returns the top_k chunks from Chroma DB
        - Minimum cosine similarity