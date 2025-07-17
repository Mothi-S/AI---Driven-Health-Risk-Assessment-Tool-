# 🧠 AI-Driven Health Risk Assessment Tool

An intelligent, conversational AI system designed to assist users in understanding health conditions, symptoms, and medical terminology using state-of-the-art natural language processing techniques. Built on the **LLaMA 2** language model, enhanced with **Retrieval-Augmented Generation (RAG)** and **FAISS**, the chatbot delivers accurate, relevant, and real-time medical insights in a user-friendly interface.

---

## 🚀 Project Objective

To create an accessible AI-powered medical assistant that:
- Answers health-related queries with contextual accuracy
- Helps users understand medical terms, symptoms, and conditions
- Promotes general health awareness and education

> ⚠️ **Disclaimer**: This tool is intended for **educational and informational purposes only**. It is **not** a substitute for professional medical advice, diagnosis, or treatment.

---

## 🧰 Technologies Used

- **[LLaMA 2](https://ai.meta.com/llama/)** – Foundation language model
- **[FAISS](https://github.com/facebookresearch/faiss)** – Efficient similarity search and clustering of dense vectors
- **RAG (Retrieval-Augmented Generation)** – Combines language modeling with vector search
- **Chainlit** – Fast and interactive frontend for LLM-based apps
- **Python** – Core language for backend and logic
- **LangChain** – For chaining LLM and search logic (if used)
- **Hugging Face Transformers** – For managing LLaMA 2 model (if used)

---

## 📁 Project Structure

AI-HealthChatbot/
├── app.py               # Main Chainlit application file
├── ingest.py            # Script to ingest and embed medical documents
├── model.py             # Handles LLaMA 2 integration and RAG logic
├── data/                # Folder containing raw medical documents (PDFs, text, etc.)
│   └── *.pdf, *.txt     # Example: Medical articles, symptom guides
├── faiss_index/         # Serialized FAISS index files (generated after ingest)
├── utils/               # Utility functions (embedding helpers, preprocessing, etc.)
│   └── helpers.py
├── requirements.txt     # Python dependencies
├── .env                 # Environment variables (API keys, configs)
├── .gitignore           # Files/folders ignored by Git
└── README.md            # Project documentation (this file)


---

## 🧠 Key Components

### 1. **Document Ingestion**
- Parses medical literature (PDF, TXT)
- Converts documents into embeddings using pre-trained models
- Stores vectorized data in a FAISS index

### 2. **Semantic Search**
- FAISS retrieves top-k relevant chunks based on user query
- Ensures that the chatbot has context-rich, relevant data

### 3. **Conversational Agent**
- LLaMA 2 generates natural, informative responses
- RAG approach helps the model ground its answers in retrieved knowledge

### 4. **User Interface**
- Chainlit provides a clean, responsive, and conversational UI
- Users can input queries and get real-time medical information

## 📸 Screenshots

### 🔹 Chainlit Web App

![Chainlit UI Screenshot](chainlit_ui.PNG)

---

## 🛠️ How to Run Locally

1. **Clone the Repository**
```bash
git clone https://github.com/yourusername/AI-HealthChatbot.git
cd AI-HealthChatbot

2. **Ingest Medical Documents**
python ingest.py

3. **Run the Chatbot**
chainlit run app.py
