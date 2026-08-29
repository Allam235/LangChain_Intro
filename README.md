# LangChain_Intro
Introduction to RAG using LangChain

### Basic RAG Retrieval Pipeline

Use manager classes to streamline process

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