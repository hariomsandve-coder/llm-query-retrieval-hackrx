<<<<<<< HEAD
# llm-query-retrieval-hackrx
LLM-powered document query system for HackRx 2025
=======

# LLM-Powered Intelligent Query–Retrieval System 🚀

This repository contains the complete implementation of a HackRx 2025 project that uses Large Language Models (LLMs) and semantic search to answer natural language queries from large documents such as insurance policies and contracts.

---

## ✅ Features

- 🔍 Parses PDF/DOCX/email documents from a URL
- 🧠 Embeds and stores document chunks in FAISS vector database
- 💬 Accepts plain English queries (even vague or incomplete)
- 🤖 Uses an LLM (OpenAI GPT/Mistral) to generate a structured, explainable decision
- 🧾 Outputs a JSON with decision, justification, amount, and source clause

---

## 🛠️ Tech Stack

| Component     | Tools Used                  |
|---------------|-----------------------------|
| LLM           | GPT-4o / Mistral (Mocked)   |
| Vector DB     | FAISS                       |
| Embeddings    | SentenceTransformers        |
| Backend       | FastAPI                     |
| Frontend      | (Optional) Streamlit        |

---

## 🚀 Getting Started

### 1. Clone & Install

```bash
git clone https://github.com/your-username/llm-query-system.git
cd llm-query-system
pip install -r requirements.txt
```

### 2. Run Locally

```bash
uvicorn app:app --reload
```

Visit: http://127.0.0.1:8000/docs

---

## 📬 API Endpoint

POST /api/v1/hackrx/run

Sample Request:

```json
{
  "documents": "https://hackrx.blob.core.windows.net/assets/policy.pdf?...",
  "questions": [
    "Will my 1-month policy cover appendix surgery?",
    "What is the waiting period for cataract surgery?"
  ]
}
```

Sample Response:

```json
{
  "decision": "Rejected",
  "justification": "Clause: Surgery is covered only after 90 days waiting period.",
  "amount": "Not Applicable",
  "source": "This policy covers surgeries only after a minimum waiting period..."
}
```

---

## 📦 Deployment Instructions (Render)

1. Push this repo to GitHub
2. Login to https://render.com → New Web Service
3. Runtime: Python 3.10
4. Build Command: `pip install -r requirements.txt`
5. Start Command: `uvicorn app:app --host 0.0.0.0 --port 10000`
6. Copy your Render deployment URL for webhook submission

---

## 📄 License

MIT License
>>>>>>> 26656ca (Initial commit for HackRx project)
