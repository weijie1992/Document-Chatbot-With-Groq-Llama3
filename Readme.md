# 📚 RAG Document Q&A with Groq and Llama 3

A simple Retrieval-Augmented Generation (RAG) app built with **Streamlit**, **Groq's Llama 3 (8b)** model, and **FAISS** vector database.

This app allows you to:

- Upload **PDF research papers**,
- Embed and store them into a local FAISS vector database,
- Ask natural language questions,
- Get precise answers sourced **only** from your PDFs — **no internet search**!

---

## 🚀 Tech Stack

- **[Streamlit](https://streamlit.io/)** — UI framework
- **[Groq API](https://groq.com/)** — Llama 3-8b LLM
- **[FAISS](https://github.com/facebookresearch/faiss)** — Vector database for similarity search
- **[LangChain](https://www.langchain.dev/)** — Chains, retrievers, and embeddings
- **OpenAIEmbeddings** — For embedding text
- **PyPDFLoader** — For loading PDFs
- **Python** 3.9+

---

## 🏗️ Project Structure

```bash
.
├── app.py          # Main Streamlit app
├── research_papers/ # (Your local folder with PDFs)
├── .gitignore      # Ignore research_papers and .env
├── requirements.txt # Python dependencies
├── README.md       # This file
```

---

## ⚙️ Setup Instructions

1. **Clone the repo**

```bash
git clone https://github.com/your-username/rag-document-qa-groq.git
cd rag-document-qa-groq
```

2. **Create a virtual environment**

```bash
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
```

3. **Install dependencies**

```bash
pip install -r requirements.txt
```

4. **Set up environment variables**

Create a `.env` file with the following:

```env
OPENAI_API_KEY=your-openai-api-key
GROQ_API_KEY=your-groq-api-key
```

5. **Prepare your PDFs**

Place your research papers inside the `research_papers/` folder.

6. **Run the app**

```bash
streamlit run app.py
```

---

## ✨ Features

- **Document Embedding**: Click the "Document Embedding" button to create a FAISS vector database from your PDFs.
- **Question Answering**: Type any question related to your uploaded PDFs.
- **Context Display**: See which documents were retrieved using Streamlit expanders.
- **Fast Response**: Powered by Groq's ultra-fast Llama 3 API.

---

## 📋 Sample Usage

1. Upload PDFs to `/research_papers`
2. Launch the app
3. Click "Document Embedding" to build your vector database
4. Enter a question like:
   > "What is task decomposition in multi-agent systems?"
5. See the answer and the supporting documents!

---

## 📦 Requirements

- Python 3.9+
- `streamlit`
- `langchain`
- `langchain-groq`
- `openai`
- `faiss-cpu`
- `python-dotenv`

(Install all via `requirements.txt`)

---
