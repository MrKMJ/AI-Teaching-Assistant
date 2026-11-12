# AI Teaching Assistant

A real-time, accessibility-first AI teaching assistant built in 3 days for lablab.ai's **"Fall in Love with DeepSeek"** hackathon.

Students chat with an assistant powered by **DeepSeek V3** that answers questions in short, precise, curriculum-friendly language, with separate conversation threads per topic.

## Features

- **Real-time chat** over WebSockets (Flask-SocketIO)
- **Threaded conversation memory**: each thread keeps its own history, and threads can be deleted
- **DeepSeek V3** via the AIML API (OpenAI-compatible client), with tuned temperature / top-p
- **Accessibility-first UI**: screen-reader support, voice assistance and an adaptive interface
- React + TypeScript frontend built with Vite and Radix UI components

## Tech stack

| Layer | Technology |
|-------|------------|
| LLM | DeepSeek V3 (`deepseek/deepseek-chat`) via AIML API |
| Backend | Python, Flask, Flask-SocketIO, OpenAI SDK, LangChain |
| Frontend | React, TypeScript, Vite, Radix UI |
| Deployment | Vercel (frontend) |

## Project structure

```
AI-Teaching-Assistants-for-Schools-main/
├── backend/
│   ├── ai_assistant.py   # Assistant class: LLM client + per-thread memory
│   ├── app-server.py     # Flask-SocketIO server (message / delete_thread events)
│   ├── app-client.py     # CLI test client
│   └── requirements.txt
└── frontend/             # React + TypeScript (Vite) chat UI
```

## Run locally

```bash
# Backend
cd AI-Teaching-Assistants-for-Schools-main/AI-Teaching-Assistants-for-Schools-main/backend
pip install -r requirements.txt
echo "API_KEY=your_aimlapi_key" > .env
python app-server.py

# Frontend (new terminal)
cd ../frontend
npm install
npm run dev
```

## Team

Built by **Khawaja Moinuddin Jamal** with Hafiz Hassan Mustafa and Ahmed Ouda.

---

## Hire me to build this for you

Want an LLM assistant like this trained on your own course material or documents? I build these through Fiverr.

- [Custom RAG AI chatbot trained on your documents](https://www.fiverr.com/moinjamal/develop-custom-ai-chatbots-and-automate-your-business-tasks)
- [Fine-tune an LLM or train a custom ML model on your data](https://www.fiverr.com/moinjamal/fine-tune-an-llm-and-train-custom-machine-learning-models-on-your-data)

[![Hire me on Fiverr](https://img.shields.io/badge/Hire_me_on-Fiverr-1DBF73?style=for-the-badge&logo=fiverr&logoColor=white)](https://www.fiverr.com/moinjamal)
