# 📚 Alice in Wonderland - RAG Application

This project demonstrates a **Retrieval-Augmented Generation (RAG) application**.  
The system ingests *Alice's Adventures in Wonderland* by Lewis Carroll (public domain ebook), processes it into embeddings, stores them in a vector database, and enables **context-aware question answering**.

---

## 🚀 Features

- 📖 Uses **Alice in Wonderland** as the knowledge base  
- 🧩 **Text chunking** for efficient retrieval  
- 🔎 **Vector embeddings** to enable semantic search  
- 📂 **Vector store (FAISS)** for storing and retrieving chunks  
- ❓ Ask natural language questions about the book and get accurate, grounded answers  
- 🔧 Fully customizable — swap datasets, embeddings, or models  

---

## 🛠️ Tech Stack

- **Python 3.10+**  
- **LangChain** – orchestration framework  
- **FAISS** – vector store for retrieval  
- **SentenceTransformers** – embeddings (`all-MiniLM-L6-v2`)  
- **OpenAI API** – for LLM responses  
- **Jupyter Notebook / Streamlit** – interface options  

---

## 📂 Project Structure
alice-rag/  
│── data/  
│   └── alice_in_wonderland.txt   # The ebook (public domain)  
│── notebooks/  
│   └── rag_pipeline.ipynb        # End-to-end RAG pipeline  
│── app.py                        # Optional Streamlit/Gradio interface  
│── requirements.txt              # Python dependencies  
│── README.md                     # Project documentation  

---

## ⚡ How It Works

1. **Load Dataset**  
   Import *Alice in Wonderland* text.  

2. **Preprocess & Chunk**  
   Split the text into manageable chunks (e.g., 500 tokens).  

3. **Generate Embeddings**  
   Use `SentenceTransformers` to embed chunks.  

4. **Store in Vector DB**  
   Save embeddings in **FAISS** for fast similarity search.  

5. **Query**  
   User asks a question → query is embedded → FAISS retrieves relevant passages → OpenAI API generates the final answer.  

6. **Answer Generation**  
   A local LLM (HuggingFace / Ollama) generates an answer grounded in retrieved passages.

---
