# 🧠 HelpMateAI: Retrieval-Augmented Search System for Insurance Documents

[![LangChain](https://img.shields.io/badge/Built%20With-LangChain-blue)](https://www.langchain.com/)
[![LLM-Ollama](https://img.shields.io/badge/LLM-Ollama%203.2-yellow)](https://ollama.com/)
[![Embeddings](https://img.shields.io/badge/Embeddings-MiniLM--L6--v2-green)](https://huggingface.co/sentence-transformers/all-MiniLM-L6-v2)
[![Vector DB](https://img.shields.io/badge/Vector%20DB-ChromaDB-purple)](https://www.trychroma.com/)
[![License](https://img.shields.io/github/license/HelloShibani/HelpMate_AI)](https://github.com/HelloShibani/HelpMate_AI/blob/main/LICENSE)



HelpMateAI is a modular Retrieval-Augmented Generation (RAG) system designed to navigate complex insurance documents using semantic search and generative answering. Built using LangChain, HuggingFace Transformers, Ollama 3.2, and ChromaDB, it efficiently extracts and surfaces relevant information from lengthy, structured PDF documents like insurance policies.

---

## 🔍 Problem Statement

Insurance policies are often long, dense, and difficult to interpret. This project addresses:

- ❓ Difficulty locating specific clauses or definitions
- ⏱️ Time-consuming manual search
- 🧾 Need for human-readable, context-aware summaries

HelpMateAI provides a lightweight, extensible framework to improve document comprehension and accelerate decision-making.

---

## 🚀 Features

- 📄 **PDF Processing**: Parses text and tables using `pdfplumber`
- 🧠 **Semantic Embeddings**: Leverages `all-MiniLM-L6-v2` from HuggingFace for robust semantic representation
- 🔎 **Vector Search**: ChromaDB for persistent, fast, chunk-level retrieval
- 🔁 **Re-ranking (Optional)**: Cross-encoder for refining semantic hits
- ✍️ **LLM Response Generation**: Uses Ollama 3.2 via LangChain for contextual answers
- 🧩 **Metadata Handling**: Captures page numbers and source chunks for better traceability
- ⚡ **Caching Layer**: Avoids redundant retrievals for recurring queries

---

## 📦 Technology Stack

| Component        | Usage                                      |
|------------------|---------------------------------------------|
| `Python`         | Core scripting and orchestration            |
| `pdfplumber`     | PDF parsing (text and tables)               |
| `HuggingFace`    | Embedding model (`all-MiniLM-L6-v2`)        |
| `ChromaDB`       | Vector store for semantic search            |
| `LangChain`      | Tool orchestration + Ollama integration     |
| `Ollama 3.2`     | Lightweight LLM for question answering      |
| `pandas`         | Data handling and JSON/DF preprocessing     |

---

## 🧱 System Architecture

```text
┌────────────┐     ┌────────────┐     ┌──────────────┐     ┌──────────────┐
│ PDF Parser │ →→ │ Embeddings │ →→ │ Vector Search │ →→ │ LLM Response │
└────────────┘     └────────────┘     └──────────────┘     └──────────────┘
     ↑                    ↓                 ↑                       ↓
 Metadata           ChromaDB Store      Reranker (opt.)       Final Answer
```

---

## 🧪 Quickstart

```bash
# 1. Install dependencies
pip install -r requirements.txt

# 2. Run the notebook
jupyter notebook notebooks/HelpMate_AI_Ollama.ipynb
```

---

## 📚 Project Report

A detailed technical report is available in the `reports/` folder:  
📄 [📥 Download Project Report HELPMATE_AI.pdf](https://raw.githubusercontent.com/HelloShibani/HelpMate_AI/main/Reports/Project%20Report%20HELPMATE_AI.pdf)

---

## 🔄 Future Roadmap

Planned extensions to improve usability, transparency, and scale:

- [ ] Streamlit/Gradio UI for non-technical users
- [ ] Hybrid RAG with rule-based fallback and citations
- [ ] In-app table visualizer and clause tracking
- [ ] Multi-document summarization & comparison

---

## 🗺️ Roadmap & Open Issues

This system is evolving toward a more robust, fallback-aware document QA pipeline.

Current areas of focus:

- [ ] **Add Fallback Logic for Missing Vector Embeddings** ([#1](https://github.com/HelloShibani/HelpMate_AI/issues/1))  
- [ ] **Score and Rank Answers by Retrieval Confidence** ([#2](https://github.com/HelloShibani/HelpMate_AI/issues/2))  
- [ ] **Chunking Strategy Evaluation Notebook** ([#3](https://github.com/HelloShibani/HelpMate_AI/issues/3))  
- [ ] **.env Template for Local Config** ([#4](https://github.com/HelloShibani/HelpMate_AI/issues/4))  
- [ ] **Architecture Diagram for System Flow** ([#5](https://github.com/HelloShibani/HelpMate_AI/issues/5))

Check out all [📌 Open Issues](https://github.com/HelloShibani/HelpMate_AI/issues)  
or open a new one to explore edge cases, extensions, or improvements.

---

## 👥 Authors

- **Shibani Roychoudhury**  
  _Data Science Professional | Applied NLP | Explainable AI_  
  [LinkedIn](https://www.linkedin.com/in/shibani-roychoudhury/) | [GitHub](https://github.com/Helloshibani)

- **Himanshu Agrawal**  
  _AI Practitioner | Software Engineer at Mediaocean_  
  [LinkedIn](https://www.linkedin.com/in/himanshuagrawal18/)

- **Adarsh S A**  
  _Analytics Professional at ANZ | Data & Decision Systems_  
  [LinkedIn](https://www.linkedin.com/in/adarsh-sa/)


**Shibani Roychoudhury**  
_Data Science Professional | Applied NLP | Explainable AI_  
📫 [LinkedIn](https://www.linkedin.com/in/shibani-roychoudhury/)  
🌐 [GitHub](https://github.com/Helloshibani)

---

## 📜 License

This project is licensed under the [MIT License](LICENSE).