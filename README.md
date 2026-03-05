<div align="center">

# 🧠 ChunkWise AI

### Intelligent Document Q&A Powered by Semantic Search

[![Python](https://img.shields.io/badge/Python-3.8%2B-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![LangChain](https://img.shields.io/badge/LangChain-0.0.284-green)](https://www.langchain.com/)
[![Streamlit](https://img.shields.io/badge/Streamlit-1.22-FF4B4B?logo=streamlit&logoColor=white)](https://streamlit.io/)
[![OpenAI](https://img.shields.io/badge/OpenAI-0.28-412991?logo=openai&logoColor=white)](https://openai.com/)
[![FAISS](https://img.shields.io/badge/FAISS-1.7.4-blue)](https://github.com/facebookresearch/faiss)

> **Stop copy-pasting articles into ChatGPT.** ChunkWise AI reads, understands, and answers questions from your own documents — fast, precise, and cost-effective.

![ChunkWise AI Banner](https://github.com/user-attachments/assets/10a950dc-690c-4fb4-98cf-8138c458488e)

</div>

---


## 💡 About

ChunkWise AI is an intelligent chatbot system that transforms large documents into searchable, semantically meaningful chunks using **LangChain**, **FAISS**, and **OpenAI**. It retrieves only the most relevant information, delivering fast and precise answers with minimal token usage.

**The problem it solves:**
- ❌ Manual copy-paste of long articles is painful and tedious
- ❌ Most models choke beyond ~3,000 words
- ❌ You often need just the right chunk, not the entire article

**The solution:**
- ✅ Automatically ingest documents and web articles
- ✅ Semantically split, embed, and index content
- ✅ Retrieve only what matters and generate focused answers

---

## ⚙️ How It Works

```
📄 Load Documents
      ↓
✂️  Chunk & Split (RecursiveCharacterTextSplitter)
      ↓
🔢 Embed (OpenAI Embeddings → Vectors)
      ↓
💾 Store in Vector DB (FAISS Index)
      ↓
🔍 Retrieve relevant chunks (Semantic Search)
      ↓
🤖 Generate answer (OpenAI LLM)
      ↓
💬 Display in Streamlit UI
```

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| 🔗 **URL Ingestion** | Load articles by pasting URLs directly into the sidebar |
| ✂️ **Smart Chunking** | Recursive splitting preserves context across paragraphs, sentences, and words |
| 🔢 **Semantic Embeddings** | Converts text into vector representations that capture meaning |
| ⚡ **FAISS Indexing** | Lightning-fast similarity search over your document vectors |
| 💬 **Q&A with Sources** | Ask questions and get answers with source attribution |
| 💾 **Persistent Index** | FAISS index is saved locally for reuse across sessions |

---

## 🛠️ Tech Stack

| Component | Technology |
|-----------|------------|
| **Framework** | [LangChain](https://www.langchain.com/) |
| **LLM** | [OpenAI GPT](https://openai.com/) |
| **Vector Store** | [FAISS](https://github.com/facebookresearch/faiss) |
| **Frontend** | [Streamlit](https://streamlit.io/) |
| **Embeddings** | OpenAI Embeddings |
| **Document Loader** | LangChain UnstructuredURLLoader |

---

## 🚀 Getting Started

### Prerequisites

- Python 3.8+
- An [OpenAI API key](https://platform.openai.com/account/api-keys)

### Installation

**1. Clone the repository**

```bash
git clone https://github.com/Poorna-Chandra-D/ChunkWise_AI.git
cd ChunkWise_AI
```

**2. Install dependencies**

```bash
pip install -r requirements.txt
```

**3. Configure your API key**

Create a `.env` file in the project root:

```env
OPENAI_API_KEY=your_api_key_here
```

---

## 📖 Usage

**Start the application:**

```bash
streamlit run main.py
```

**Then follow these steps:**

1. 🌐 **Enter URLs** — Paste up to 3 article URLs in the sidebar
2. ▶️ **Process** — Click **"Process URLs"** to load, split, embed, and index the content
3. ❓ **Ask Questions** — Type your question in the main area and get contextual answers with sources

---

## 📁 Project Structure

```
ChunkWise_AI/
├── main.py                         # Streamlit application entry point
├── requirements.txt                # Python dependencies
├── .env                            # OpenAI API key (create this yourself)
├── faiss_store_openai.pkl          # FAISS index (generated at runtime by main.py)
├── text_loaders_splitters.ipynb    # Notebook exploring text loading & splitting
├── llm_about.txt                   # LLM reference notes
├── player.csv                      # Sample data file
└── README.md                       # You are here!
```

---

## 🔬 Architecture Deep Dive

### 1. Document Loading & Chunking

Documents are loaded via `UnstructuredURLLoader` and split using `RecursiveCharacterTextSplitter`, which intelligently breaks text by:

**Paragraphs → Sentences → Words → Characters**

This keeps each chunk within token limits while preserving context.

![Chunking Pipeline](https://github.com/user-attachments/assets/dc1d29e8-775b-4f0d-b093-50b849c61871)

### 2. Embeddings & Vector Storage

Text chunks are transformed into numerical vectors using **OpenAI Embeddings**. These vectors capture semantic meaning — so *"iPhone review"* and *"Apple product feedback"* end up close together in vector space.

Vectors are indexed using **FAISS** for instant similarity search.

![Embeddings & FAISS](https://github.com/user-attachments/assets/0e0d8210-9579-4e71-bea3-1aacc383d3d0)

### 3. Retrieval-Augmented Generation (RAG)

When you ask a question:
1. Your query is converted into a vector
2. FAISS finds the most semantically similar chunks
3. Only those chunks are sent to the LLM
4. The LLM generates a focused, cost-efficient answer

![Full Pipeline](https://github.com/user-attachments/assets/d0fad1c1-d578-4155-8586-12e8f5bb65d3)

---

## 📸 Screenshots

<div align="center">

| Architecture Overview | Chatbot Pipeline |
|:---:|:---:|
| ![Architecture](https://github.com/user-attachments/assets/7b6a347b-5a36-464d-94e0-6153e75e7e91) | ![Pipeline](https://github.com/user-attachments/assets/c19e25a0-dd9c-4c59-93ae-95477bc6da1c) |

</div>
---
<div align="center">

**Built with ❤️ by [Poorna Chandra D](https://github.com/Poorna-Chandra-D)**

⭐ Star this repo if you find it useful!

</div>

