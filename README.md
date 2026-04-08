# 🚀 Advanced RAG Systems (Self, Corrective, Hybrid & Adaptive RAG)

This repository contains implementations and experiments with multiple Retrieval-Augmented Generation (RAG) architectures, including Self-RAG, Corrective RAG, Hybrid RAG, and a custom-designed Adaptive Hybrid RAG system.

The goal of this project is to explore how different retrieval strategies and LLM-based reasoning pipelines improve response accuracy, robustness, and factual reliability.

---

## 📌 Implemented Architectures

### 1. Self-RAG
- LLM-driven retrieval decision making
- Iterative refinement of answers
- Self-checking and reasoning-based retrieval

---

### 2. Corrective RAG (CRAG)
- Evaluates retrieved documents for relevance
- Triggers fallback or correction when retrieval is weak
- Improves robustness in noisy retrieval environments

---

### 3. Hybrid RAG
- Combines Dense Retrieval (FAISS) + Sparse Retrieval (BM25)
- Balances semantic understanding with keyword matching
- Improves recall and retrieval coverage

---

### 4. Adaptive Hybrid RAG (Custom System)
- Dynamically decides retrieval strategy based on query type
- Integrates:
  - Hybrid retrieval (Dense + Sparse)
  - Reranking of retrieved documents
  - Self-evaluation of context relevance
  - Iterative correction loop if answer quality is low
- Designed to improve reliability and reduce hallucinations

---

## 🧠 Key Features

- Modular RAG pipeline design
- Hybrid retrieval system (FAISS + BM25)
- LLM-based evaluation and reasoning
- Self-corrective generation loop
- Notebook-based experiments for easy reproducibility
- Custom adaptive retrieval strategy

---

## 🏗️ System Architecture Overview
User Query
↓
Retrieval Decision Layer
↓
Hybrid Retrieval (Dense + Sparse)
↓
Reranking (Relevance scoring)
↓
Context Construction
↓
LLM Generation
↓
Answer Evaluation (Self-check)
↓
Final Response OR Retry Loop


---

## ⚙️ Tech Stack

- Python 🐍
- LangChain / LangGraph
- FAISS (Dense Vector Search)
- BM25 (Sparse Keyword Search)
- OpenRouter / LLM APIs
- Jina Embeddings
- Jupyter Notebooks

---

## 📂 Repository Structure


self_rag.ipynb
corrective_rag.ipynb
hybrid_rag.ipynb
adaptive_hybrid_rag.ipynb
requirements.txt
.env.example
README.md


---

## 🔐 Environment Variables

Create a `.env` file:


OPENAI_API_KEY=your_key_here
JINA_API_KEY=your_key_here
OPENROUTER_API_KEY=your_key_here


---

## 🚀 Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/your-username/advanced-rag-systems.git
cd advanced-rag-systems
2. Create virtual environment
python -m venv venv
source venv/bin/activate   # Mac/Linux
venv\Scripts\activate      # Windows
3. Install dependencies
pip install -r requirements.txt
4. Run notebooks
```
Open Jupyter and explore:

jupyter notebook
📊 Motivation

Traditional RAG systems often fail due to:

Poor retrieval quality
Lack of reasoning over retrieved context
Hallucinations from LLMs
No feedback loop

This project explores multiple architectures to solve these problems by combining retrieval, reranking, and self-evaluation.

🔮 Future Improvements
Cross-encoder reranking integration
Multi-hop reasoning support
Memory-augmented RAG
Evaluation using RAGAS / DeepEval
Deployment as API service
👨‍💻 Author

Ahmad Ali Javed

Exploring advanced LLM systems, RAG pipelines, and AI agent architectures.
