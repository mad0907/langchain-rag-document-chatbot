## 📘 LangChain RAG – Procurement Assistant

This project demonstrates how to build a RAG (Retrieval Augmented Generation) based AI assistant using LangChain + Gemini + FAISS.

The AI reads a document (Procurement Process) and answers questions only from that document, just like an open-book exam AI.

🧠 What This Project Does

Loads a Word / PDF document

Splits it into small chunks

Converts text into embeddings (numbers)

Stores them in a vector database (FAISS)

Retrieves relevant chunks when a question is asked

Uses Gemini LLM to generate the final answer

📂 Folder Structure (Example)
project/
│
├── ProcurementProcess.docx
├── rag.ipynb
└── README.md

⚙️ Installation – Required Libraries

Run this in Google Colab or terminal before starting:

!pip3 install -qU \
python-dotenv \
langchain \
langchain-core \
langchain-community \
langchain-google-genai \
google-generativeai \
faiss-cpu \
python-docx \
docx2txt \
pypdf \
pandas \
sentence-transformers

📦 Libraries Used
Library	Purpose
langchain	Core framework for RAG pipeline
langchain-community	Vector stores, loaders
langchain-google-genai	Gemini LLM integration
faiss-cpu	Vector database for similarity search
docx2txt	Reading Word documents
pypdf	Reading PDFs
sentence-transformers	Embeddings generation
pandas	Data handling
python-dotenv	Environment variables

## 🔑 API Key Setup (Google Colab)

Open Secrets Panel (🔑 icon in left sidebar)

Add key:

Name: APIKEY

Value: Your Gemini API Key

Use in code:

from google.colab import userdata
api_key = userdata.get('APIKEY')

Otherwise if using Notebook, Get Api key from .env file

## ▶️ How It Works – Flow

Load Document – Reads Word/PDF file

Split Text – Breaks into small chunks

Embeddings – Converts text into vectors

FAISS Store – Saves vectors for fast search

Retriever – Finds relevant chunks

LLM (Gemini) – Generates human-like answer

Prompt – Controls AI behavior

Chain – Connects everything together

## 💬 Example Question
Who can initiate procurement request?


## AI will search only inside the procurement document and return a contextual answer.

🧩 Concept in One Line

RAG = Search First → Answer Later

## 🚀 Use Cases

Document Q&A

HR policy bots

Legal assistants

Customer support knowledge base

Enterprise internal search

## 🛡️ Notes

Do NOT hardcode API keys in notebook.

Use Secrets or .env files.

Keep document size moderate for faster embedding.
