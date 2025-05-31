# 📄 Document Intelligence Platform – Ergosphere Internship Assignment

This is a full-stack Document Intelligence Platform that enables users to upload documents and ask questions about their contents using a Retrieval Augmented Generation (RAG) pipeline.


## 📦 Tech Stack

- **Backend**: Django REST Framework
- **Database**: MySQL for metadata, ChromaDB for vector storage
- **Frontend**: Next.js (React) + Tailwind CSS
- **AI Integration**: LM Studio / OpenAI API (for RAG)
- **File Storage**: Local

---

## ⚙️ Setup Instructions

### 🧠 LM Studio Setup (recommended)
1. Download LM Studio: https://lmstudio.ai/
2. Load a LLaMA or Mistral model (e.g., `mistral-7b-instruct-v0.2.Q4_K_M.gguf`)
3. Enable the OpenAI-compatible API in LM Studio settings
4. Update your RAG code to query `http://localhost:1234/v1/chat/completions`

---

### 🔧 Backend

```bash
# Backend Setup
cd backend
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt

# MySQL Setup
# Create a database `rag_db` and configure settings.py accordingly

python manage.py makemigrations
python manage.py migrate
python manage.py runserver
