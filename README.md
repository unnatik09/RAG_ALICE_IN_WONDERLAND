# 📚 Alice in Wonderland - RAG Application

This project demonstrates a **Retrieval-Augmented Generation (RAG) application**.  
The system ingests *Alice's Adventures in Wonderland* by Lewis Carroll (public domain ebook), processes it into embeddings, stores them in a **Chroma vector database**, and enables **context-aware question answering** using the OpenAI API.

---

## 🚀 Features

- 📖 Uses **Alice in Wonderland** as the knowledge base  
- 🧩 **Text chunking** for efficient retrieval  
- 🔎 **Vector embeddings** with OpenAI  
- 📂 **Chroma** as the vector store for retrieval  
- ❓ Ask natural language questions about the book and get accurate, grounded answers  
- 🔧 Fully customizable — swap datasets, embeddings, or models  

---

## 🛠️ Tech Stack

- **Python 3.10+**  
- **LangChain** – orchestration framework  
- **Chroma** – vector store for retrieval  
- **OpenAI API** – embeddings + LLM responses  
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
   Use **OpenAIEmbeddings** for chunk embeddings.  

4. **Store in Vector DB**  
   Save embeddings in **Chroma** for fast similarity search.  

5. **Query**  
   User asks a question → query is embedded → Chroma retrieves relevant passages → OpenAI API generates the final answer.  
