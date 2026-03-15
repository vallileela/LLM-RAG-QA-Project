# LLM-RAG-QA-Project

# 📄 Document Question Answering System using RAG

This project is a **Retrieval-Augmented Generation (RAG) based Question Answering system** built using **Streamlit, FAISS, Sentence Transformers, and LLaMA**.

Users can upload a **PDF document** and ask questions, and the system will generate answers based only on the content of the uploaded document.

The system retrieves relevant information from the document and uses a **Large Language Model (LLM)** to generate accurate responses.

---

# 🚀 Features

- Upload and process **PDF documents**
- Automatic **text extraction**
- Intelligent **text chunking**
- **Vector database creation using FAISS**
- **Semantic search** using embeddings
- **LLM-based answer generation**
- **Answer quality evaluation using similarity score**
- Interactive **Streamlit user interface**
- Loading indicator while generating answers

---

# 🧠 Project Architecture

The system follows a **Retrieval-Augmented Generation (RAG) pipeline**:
PDF Upload
│
▼
Text Extraction (PyMuPDF)
│
▼
Text Chunking
│
▼
Embedding Generation
(Sentence Transformers)
│
▼
Vector Database (FAISS)
│
▼
User Question
│
▼
Semantic Retrieval
│
▼
Context + Question
│
▼
LLM (LLaMA)
│
▼
Generated Answer
│
▼
Evaluation Metric
(Question → Answer Similarity)

---

# 🛠 Technologies Used

- **Python**
- **Streamlit** – Web interface
- **FAISS** – Vector database for similarity search
- **Sentence Transformers** – Text embeddings
- **LLaMA (via CTransformers)** – Language model
- **LangChain Text Splitters** – Document chunking
- **PyMuPDF (fitz)** – PDF text extraction
- **NumPy** – Numerical operations

---

# 📂 Project Structure
project-folder
│
├── models/
│ └── llama-2-7b-chat.ggmlv3.q4_K_M.bin
│
├── QA_chatbot.py
│
├── requirements.txt
│
└── README.md

📦 Required Libraries
Example requirements.txt
streamlit
pymupdf
faiss-cpu
numpy
sentence-transformers
langchain-text-splitters
ctransformers

🤖 Model Setup

Download a GGUF or GGML LLaMA model and place it inside the models folder.

Example:

models/
llama-2-7b-chat.ggmlv3.q4_K_M.bin

Update the model path in the code if required.

🧪 Evaluation Metric

The system evaluates the generated answer using semantic similarity.

Question → Answer Similarity

It calculates cosine similarity between question embedding and generated answer embedding.

Higher score indicates the answer is more relevant to the question.

📷 Application Workflow

Upload a PDF document

Text is extracted from the document

Text is divided into smaller chunks

Embeddings are generated

FAISS vector database is created

User asks a question

Relevant document chunks are retrieved

LLM generates an answer

Similarity score evaluates answer quality

💡 Example Use Cases

Medical document question answering

Research paper Q&A

Company policy document search

Legal document assistance

Knowledge base chatbot

📈 Future Improvements

Multiple document support

Chat history

Improved RAG evaluation metrics

Larger LLM models

Document highlighting

Cloud deployment
