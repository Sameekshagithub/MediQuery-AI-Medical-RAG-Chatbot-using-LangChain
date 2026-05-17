#🏥 MediQuery-AI-Medical-RAG-Chatbot-using-LangChain 

An intelligent **Medical AI Assistant** built using **Retrieval-Augmented Generation (RAG)**, **LangChain**, **Groq LLM**, **FAISS Vector Database**, and **Streamlit**.

This chatbot answers medical questions from uploaded medical PDFs such as:

* prescriptions
* medical reports
* healthcare guides
* treatment manuals
* research papers

The chatbot retrieves relevant information from uploaded documents and generates grounded responses using Large Language Models (LLMs).

---

# 🚀 Features

✅ Upload Multiple Medical PDFs
✅ Retrieval-Augmented Generation (RAG)
✅ Conversational AI Chatbot
✅ Groq Llama3 Integration
✅ FAISS Vector Database
✅ Semantic Search
✅ Chat History
✅ Source Citation
✅ Conversational Memory
✅ Streamlit UI
✅ Medical Safety Disclaimer
✅ Modular Project Structure
✅ Production-Style Architecture

---

# 🧠 What is RAG?

RAG (Retrieval-Augmented Generation) is an AI architecture that:

1. Retrieves relevant information from documents
2. Sends retrieved context to the LLM
3. Generates grounded answers

Instead of answering from general knowledge, the chatbot answers directly from uploaded medical documents.

---

# 📌 Why RAG for Healthcare?

Healthcare applications require:

* factual accuracy
* reduced hallucination
* grounded responses
* document-based answers

RAG improves reliability by using trusted medical documents as context.

---

# 🏗️ Project Architecture

```text
User Question
      ↓
Embedding Generation
      ↓
Vector Similarity Search (FAISS)
      ↓
Top Relevant Chunks Retrieved
      ↓
LLM (Groq Llama3)
      ↓
Final Grounded Answer
```

---

# 📂 Project Structure

```text
medical-rag-chatbot/
│
├── app.py
├── requirements.txt
├── .env
├── README.md
│
├── data/
├── vectorstore/
├── chat_history/
│
├── src/
│   ├── loader.py
│   ├── splitter.py
│   ├── embeddings.py
│   ├── vectordb.py
│   ├── rag_chain.py
│   ├── memory.py
│   ├── prompts.py
│   ├── utils.py
│   └── database.py
│
├── assets/
│   └── styles.css
│
└── notebooks/
    └── experimentation.ipynb
```

---

# ⚙️ Technologies Used

| Technology            | Purpose               |
| --------------------- | --------------------- |
| Python                | Backend               |
| Streamlit             | Frontend UI           |
| LangChain             | RAG Framework         |
| Groq                  | LLM Inference         |
| FAISS                 | Vector Database       |
| HuggingFace           | Embeddings            |
| Sentence Transformers | Semantic Embeddings   |
| PyPDF                 | PDF Parsing           |
| dotenv                | Environment Variables |

---

# 📦 Installation

## 1️⃣ Clone Repository

```bash
git clone <your-github-repo-url>
cd medical-rag-chatbot
```

---

## 2️⃣ Create Virtual Environment

### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

### Mac/Linux

```bash
python3 -m venv venv
source venv/bin/activate
```

---

# 📥 Install Dependencies

```bash
pip install -r requirements.txt
```

---

# 🔑 Setup Groq API Key

Get free API key from:

[Groq Console](https://console.groq.com?utm_source=chatgpt.com)

Create `.env`

```env
GROQ_API_KEY=your_api_key_here
```

---

# ▶️ Run Application

```bash
streamlit run app.py
```

---

# 🧪 Sample Medical Questions

* What medications are prescribed?
* Summarize the patient report
* What are the treatment recommendations?
* What diagnosis is mentioned?
* Explain the lab results
* What symptoms are described?
* What precautions are suggested?

---

# 🧠 RAG Pipeline Workflow

## Step 1: PDF Upload

Users upload medical PDFs through Streamlit.

---

## Step 2: Document Loading

PDFs are loaded using:

```python
PyPDFLoader
```

---

## Step 3: Text Chunking

Large documents are split into smaller chunks using:

```python
RecursiveCharacterTextSplitter
```

Why chunking?

* improves retrieval
* reduces token usage
* improves semantic search

---

## Step 4: Embedding Generation

Each chunk is converted into vector embeddings using:

```python
sentence-transformers/all-MiniLM-L6-v2
```

---

## Step 5: Vector Storage

Embeddings are stored in:

```python
FAISS
```

FAISS performs fast similarity search.

---

## Step 6: Retrieval

When user asks question:

* query embedding generated
* top-k relevant chunks retrieved

---

## Step 7: LLM Generation

Retrieved context passed to:

* Llama3
* Mixtral
* Groq models

LLM generates grounded answer.

---

# 💬 Conversational Memory

The chatbot remembers previous conversation using:

```python
ConversationBufferMemory
```

This enables:

* contextual follow-up questions
* conversational continuity
* chat history tracking

---

# 🛡️ Medical Safety Layer

⚠️ Disclaimer:
This chatbot is not a licensed medical professional.

The chatbot:

* avoids hallucination
* avoids unsafe diagnosis
* refuses emergency instructions
* recommends consulting doctors

---

# 🔍 Semantic Search

Semantic search retrieves information based on meaning instead of keyword matching.

Example:

* “heart pain”
* “chest discomfort”

Both retrieve similar context.

---

# 📊 Vector Database

FAISS stores:

* document chunks
* embeddings
* metadata

Benefits:

* fast retrieval
* scalable search
* efficient similarity matching

---

# 🖥️ Frontend Features

✅ Modern Streamlit UI
✅ Upload PDFs
✅ Chat Interface
✅ Typing Animation
✅ Sidebar Statistics
✅ Source Citations
✅ Dark/Light Theme
✅ Download Chat History
✅ Clear Chat Button

---

# 📚 Source Citations

Each answer includes:

* retrieved chunks
* source references
* page numbers
* similarity context

This improves transparency and trust.

---

# 📁 requirements.txt

```txt
streamlit==1.35.0
langchain==0.1.16
langchain-community==0.0.32
langchain-groq==0.1.4
groq==0.4.2
faiss-cpu==1.8.0
sentence-transformers==2.7.0
python-dotenv==1.0.1
pypdf==4.2.0
tiktoken==0.7.0
```

---

# 🧹 Environment Variables

Create `.env`

```env
GROQ_API_KEY=your_api_key
```

---

# 🚀 Deployment on Streamlit Cloud

## Push to GitHub

```bash
git init
git add .
git commit -m "Medical RAG Chatbot"
git branch -M main
git remote add origin <repo-url>
git push -u origin main
```

---

## Deploy

1. Push code to [GitHub](https://github.com?utm_source=chatgpt.com)
2. Open [Streamlit Cloud](https://streamlit.io/cloud?utm_source=chatgpt.com)
3. Connect GitHub repository
4. Add secrets:

```toml
GROQ_API_KEY="your_key"
```

5. Deploy app

---

# 📈 Future Improvements

* Multi-user authentication
* Voice-enabled chatbot
* OCR support
* Medical image analysis
* Hybrid search
* Pinecone integration
* Chat export PDF
* Multi-language support
* Doctor recommendation system

---

# 🧠 Key Concepts Learned

* Retrieval-Augmented Generation
* Vector Databases
* Semantic Search
* Embeddings
* Conversational AI
* LangChain Pipelines
* Prompt Engineering
* LLM Integration
* Streamlit Deployment

---

# ⚠️ Disclaimer

This project is for educational purposes only.

This chatbot:

* is NOT a medical professional
* should NOT replace doctors
* should NOT be used for emergencies

Always consult qualified healthcare professionals.

---

# 👩‍💻 Author Sameeksha Rai

Built with ❤️ using:

* Python
* LangChain
* Groq
* Streamlit
* FAISS

---



