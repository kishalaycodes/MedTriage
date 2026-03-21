# 🚑 AI Emergency Response Triage Assistant

## 📌 Overview

The **AI Emergency Response Triage Assistant** is a real-time decision-support system designed to assist medical professionals in emergency situations.

It analyzes **unstructured patient descriptions** (symptoms, history, incident reports) and instantly provides:

- 🩺 Emergency Assessment  
- 🧠 Likely Medical Condition  
- 🚨 Triage Priority  

The system focuses on **speed, relevance, and accuracy** using intelligent data filtering and AI reasoning.

---

## 🎯 Problem Statement

In emergency rooms and disaster scenarios:

- Patient data is **large, noisy, and unstructured**  
- Doctors have **limited time to analyze information**  
- Irrelevant history can delay critical decisions  

👉 This project addresses these challenges by:

- Removing irrelevant context  
- Compressing useful information  
- Generating fast, structured triage decisions  

---

## 🚀 Key Features

- 🧹 **Intelligent Context Pruning**  
  Filters out irrelevant patient history (e.g., outdated records)

- 📉 **Context Compression (ScaleDown API)**  
  Reduces token size for faster processing  

- 🤖 **AI-Powered Triage (Groq LLM)**  
  Uses LLaMA 3.1 for real-time reasoning  

- ⚡ **Low Latency Pipeline**  
  Optimized for near real-time responses  

- 🌐 **Interactive Web UI (Streamlit)**  
  Simple interface for entering patient data and viewing results  

---

## 🏗️ System Architecture

```text
Raw Patient Input
        ↓
Context Pruning
        ↓
FAISS Retrieval (optional)
        ↓
Context Compression (ScaleDown API)
        ↓
LLM Reasoning (Groq - LLaMA 3.1)
        ↓
Structured Triage Output

## 🛠️ Tech Stack

| Category        | Technology                     |
|----------------|-------------------------------|
| Programming    | Python                        |
| LLM            | Groq (LLaMA 3.1)              |
| Embeddings     | Sentence Transformers         |
| Vector Search  | FAISS                         |
| Compression    | ScaleDown API                 |
| Frontend UI    | Streamlit                     |
| Networking     | Cloudflare Tunnel / Ngrok     |
| HTTP Client    | requests                      |
| Environment    | Jupyter Notebook / Colab      |

## 🔑 API Requirements

### 1. Groq API Key
👉 https://console.groq.com/keys  

### 2. ScaleDown API Key
👉 https://scaledown.xyz  

---

## ⚙️ Installation & Setup

### 1. Clone Repository

```bash
git clone https://github.com/kishalaycodes/MedTriage.git
cd MedTriage

### 2. Install Dependencies

pip install groq faiss-cpu sentence-transformers streamlit pyngrok nest_asyncio requests

### 3. Add API Keys

Update your backend file:
GROQ_API_KEY = "your_groq_api_key"
SCALEDOWN_API_KEY = "your_scaledown_api_key"
---

## ▶️ Running the Application

### Run Streamlit App

bash
streamlit run app.py
---

## 🧪 Example Usage

*Input:*

text
Patient is a 58-year-old male with chest pain and shortness of breath.


*Output:*

text
Emergency Assessment: Life-threatening cardiac event  
Likely Condition: Acute Coronary Syndrome  
Triage Priority: Critical  


---

## 🧠 Core Concept: Intelligent Context Pruning

The system removes irrelevant data before AI processing.

### Example:

text
Input:
- Dental history (2010)
- Chest pain (current)

Output:
- Focus only on chest pain


👉 Benefits:

* Faster response
* Reduced token usage
* Higher accuracy

---

## ⚡ Performance Goals

* ⏱️ Response Time: Near real-time
* 📉 Token Reduction: ~30–60%
* 🎯 High relevance triage decisions

---

## 🌐 Web Interface

The system includes a *Streamlit-based UI* where users can:

* Enter patient descriptions
* Run triage analysis
* View structured results instantly

---

## 🔮 Future Enhancements

* 📊 Severity scoring (0–100)
* 🧾 JSON API output for integrations
* 🎙️ Voice input support
* 🌍 Deployment on cloud platforms
* 🏥 Integration with hospital systems

---

## ⚠️ Disclaimer

This project is intended for *educational and research purposes only*.
It is *not a substitute for professional medical judgment*.
Always consult qualified healthcare providers in real-world scenarios.

---

## 👨‍💻 Author

Kishalay Das , Ribhu Basu , Rajnish Pandey

---

## 🤝 Contributions

Contributions are welcome!
Feel free to fork the repository and submit a pull request.

---

## ⭐ Acknowledgements

* Groq (LLM infrastructure)
* ScaleDown (context compression)
* Streamlit (UI framework)

---

## 📄 License

MIT License

## 💡 Inspiration

MedTriage aims to provide a smart, scalable, and AI-driven solution to assist in emergency healthcare triage and decision-making. 
