# Autism Specialist Chatbot

## Overview
This project implements an **Autism Specialist Chatbot** that can answer questions about autism, retrieve patient data, and provide guidance using a PDF-based medical knowledge base. The chatbot is built using **Python, LangGraph, Gradio, FAISS vector stores, and Groq LLM**, providing interactive and intelligent responses with memory of recent conversations.

## Features
- **Patient Data Retrieval**: Search patients by ID or name from a CSV database (1000+ patient records).  
- **Medical Knowledge Access**: Retrieve relevant autism knowledge from a PDF document using vector search.  
- **LLM-Powered Responses**: Generates concise, context-aware responses using **Groq LLM** with integrated tools.  
- **Conversation Memory**: Remembers last 5 interactions to provide continuity in dialogue.  
- **Interactive Gradio UI**: Chat interface with example queries, memory summary, and ability to clear conversation history.  
- **State-Based Flow**: Uses **LangGraph** to manage conversational states like greetings, patient-related queries, and general autism questions.  


## Usage
1. Clone the repository:
```
git clone <your_repo_url>
cd <repo_name>
```
2. Install dependencies:
```
pip install -r requirements.txt
```
3. Set your **GROQ_API_KEY** in `.env`:
```
GROQ_API_KEY=<your_api_key>
```
4. Run the chatbot:
```
python run_chatbot.py
```
5. Open the Gradio UI in your browser (default: `http://127.0.0.1:7860`) and interact with the chatbot.  
6. Optional: Run internal tests:
```
python -c "from autism_chatbot import run_tests; run_tests()"
```

## Technologies Used
- **Python 3.10+**  
- **Gradio** – Interactive web UI for chatbot  
- **LangGraph** – State-based conversation management  
- **Groq LLM (ChatGroq)** – Generates AI responses  
- **FAISS + HuggingFace Embeddings** – Vector database for patient CSV and PDF knowledge  
- **Pandas** – CSV data management  
- **PyPDFLoader** – Load and split PDF content for vector storage  
- **dotenv** – Environment variable management  

## Example Queries
- "Hi there"  
- "Can I get patient with ID 45?"  
- "What are autism symptoms?"  
- "Tell me about patient John"  
- "What treatments are recommended for her?"  
- "Show patients with ADHD"  

## License
MIT License
