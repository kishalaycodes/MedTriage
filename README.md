# 🏥 MedTriage – AI Emergency Triage System

MedTriage is an **AI-powered emergency triage system** that analyzes patient symptoms and provides **real-time medical prioritization and response suggestions**.

Built using **LLMs, vector search (FAISS), and semantic embeddings**, this system simulates how emergency departments assess patient severity.

---

## 🚀 Overview

This project combines:

- 🧠 **LLM (Groq - LLaMA 3.1)** for intelligent reasoning  
- 🔍 **FAISS vector database** for fast similarity search  
- 📊 **Sentence Transformers** for semantic understanding  
- ⚡ **Streamlit UI** for real-time interaction  

It processes raw patient input → extracts symptoms → retrieves relevant medical protocols → compresses context → generates emergency triage decisions.

---

## 🧠 How It Works

1. **Input Processing**
   - Removes irrelevant/old medical history  
   - Extracts key symptoms  
   - Filters relevant emergency signals  

2. **Semantic Search**
   - Converts protocols into embeddings  
   - Uses FAISS to retrieve closest matches  

3. **Context Optimization**
   - Combines patient input + retrieved protocols  
   - Compresses context using ScaleDown API  

4. **AI Decision**
   - Sends optimized prompt to LLM (Groq)  
   - Returns emergency triage response  

---

## ✨ Features

- 🧠 Intelligent symptom extraction  
- ⚡ Fast semantic search with FAISS  
- 📊 Context-aware triage recommendations  
- 🌐 Streamlit web interface  
- 🔌 API-based LLM integration (Groq)  
- 🚑 Emergency-level classification (RED / YELLOW)  

---

## 🛠️ Tech Stack

- **Python**
- **Streamlit**
- **FAISS (Vector DB)**
- **Sentence Transformers**
- **Groq API (LLaMA 3.1)**
- **ScaleDown API (context compression)**
- **Ngrok / Cloudflare Tunnel (deployment)**

---

## 📂 Project Structure

MedTriage/
│── triage_backend.py # Core AI + logic pipeline
│── app.py # Streamlit frontend
│── MedTriage.ipynb # Colab experimentation notebook
│── README.md # Documentation


---

## ⚙️ Installation & Setup

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/kishalaycodes/MedTriage.git
cd MedTriage

### 2️⃣ Install Dependencies

pip install groq faiss-cpu sentence-transformers streamlit pyngrok nest_asyncio

### 3️⃣ Set API Keys

Update in triage_backend.py:

client = Groq(api_key="YOUR_GROQ_API_KEY")

headers = {
    "x-api-key": "YOUR_SCALEDOWN_API_KEY"
}

### 4️⃣ Run the Application

streamlit run app.py

### 5️⃣ Access in Browser

http://localhost:8501

## ▶️ Usage

1. Enter patient symptoms (e.g., chest pain, dizziness)  
2. Click **"Run Triage Analysis"**  
3. Get AI-generated emergency decision  

---

## 🧠 Use Cases

- Emergency triage simulation  
- Health-tech AI prototypes  
- Medical decision-support systems  
- AI + NLP learning projects  

---

## 📜 License

This project is licensed under the **MIT License**.

---

## 👨‍💻 Author

Developed by contributors of MedTriage  

---

## 🌟 Future Improvements

- 🔐 Authentication system  
- ☁️ Cloud deployment (AWS / Vercel)  
- 📊 Advanced analytics dashboard  
- 🧠 Fine-tuned medical AI models  
- 🏥 Integration with real hospital APIs  

---

## 💡 Inspiration

MedTriage aims to provide a **smart, scalable, and AI-driven solution** to assist in emergency healthcare triage and decision-making.
