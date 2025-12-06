# 🎬 Movie Question Answering System (RAG + LLM)

An intelligent system that answers natural-language questions about **10,000 IMDB movies** using **Retrieval-Augmented Generation (RAG)** and **LLM-based code generation**.

The system supports two query types:
- **Semantic queries** → answered using embeddings + FAISS + Qwen LLM  
- **Factual queries** → answered via pandas code generation + safe execution

---

## 🚀 Features

### 🔍 Semantic Movie Search (RAG)
- Embeddings from **sentence-transformers/all-MiniLM-L6-v2**
- FAISS vector index (9999 movie embeddings)
- Qwen2.5-7B LLM for contextual answers  
- Source movie list returned for transparency

### 📊 Factual Question Answering
- Qwen2.5-Coder-7B generates pandas code
- Custom **safe execution sandbox**  
- Blocks unsafe operations (`open`, `os`, `eval`, etc.)
- Auto-formats numeric results into natural language

### 🤖 Smart Query Classification
Automatically identifies:
- **semantic** → themes, recommendations, descriptions  
- **factual** → ratings, counts, averages, max/min  

### 📘 Unified Interface
Ask any question using:
```python
answer_question("Your question here")

## 🛠️ Tech Stack

| Component          | Technology                         |
| ------------------ | ---------------------------------- |
| Embeddings         | sentence-transformers              |
| Vector Index       | FAISS                              |
| LLM (Semantic)     | Qwen2.5-7B-Instruct                |
| LLM (Factual Code) | Qwen2.5-Coder-7B                   |
| Frameworks         | HuggingFace Transformers, PyTorch  |
| Data               | IMDB Top 10K Movies CSV            |
| Environment        | Google Colab Pro (GPU recommended) |

