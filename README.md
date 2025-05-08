

# 🤖 NoteBot – AI-Powered Lecture Companion

Welcome to **NoteBot**, a smart chatbot powered by Retrieval-Augmented Generation (RAG), designed to answer questions based on your PDF lecture notes. This project was developed as part of a machine learning assignment to explore the power of LLMs in educational tools.

---

## 📘 Project Overview

NoteBot transforms static lecture PDFs into an interactive chat experience. It extracts, embeds, stores, and retrieves contextually relevant answers to your questions – all within a lightweight and user-friendly Google Colab environment.

🔍 **Powered by**:  
- 🧠 `google/gemini-2.0-flash` (via Google GenAI API)  
- 📦 Chroma for vector storage  
- 🧰 LangChain for RAG pipeline  
- 📄 PyPDFLoader for PDF parsing

---

## 🛠️ Features

✅ PDF-to-Chat: Ask questions directly from your lecture PDFs  
📚 Contextual Responses: Powered by semantic retrieval and generation  
🧠 Fast Inference: Uses Gemini Flash for low-latency response times  
🔁 Persistent Vector Store: Save knowledge across sessions via Google Drive  
🧪 Debug Mode: View retrieved chunks with `--verbose` for transparency  
📐 Modular Architecture: Easy to modify, extend, and scale

---

## 🔧 Tech Stack

| Component              | Tool/Library                   |
|------------------------|--------------------------------|
| Language Model         | `google/gemini-2.0-flash`      |
| Vector Store           | `Chroma`                       |
| Embedding Model        | `embedding-001` (Google)       |
| PDF Loader             | `PyPDFLoader` (LangChain)      |
| Text Chunking          | `RecursiveCharacterTextSplitter` |
| Cloud IDE              | Google Colab                   |
| Pipeline Manager       | `LangChain`                    |

---

## 🧱 System Architecture

```

Lecture PDFs ➜ Text Extraction ➜ Chunking ➜ Embedding ➜ Vector DB (Chroma)
⬇                                          ⬇
User Query      ➜ Retriever ➜ LLM (Gemini Flash) ➜ Answer

````

- 📁 PDF handled via `gdown` and `PyPDFLoader`
- 🧩 Chunks: 1000 characters with 200-character overlap
- 🧬 Embeddings stored in Chroma, persisted in Google Drive
- 🎯 Retriever fetches top 5 chunks for each query

---

## 🚀 Getting Started

> 📝 *This setup is designed for Google Colab*

1. **Clone the repo**  
    ```
    git clone https://github.com/your-username/NoteBot.git
    ```

2. **Upload lecture PDF to Google Drive**
   Shareable link or `gdown` ID will be required

3. **Run notebook in Google Colab**
   Open `chatbot-notebook.ipynb` and run all cells step-by-step

4. **Secure your API Key**
   API Key for Google GenAI must be securely entered via `getpass()` in notebook

5. **Ask questions!**
   Use the terminal-style cell to interact with the bot
   Add `--verbose` to see the source documents retrieved

---

## 💬 Example Interaction

```
👩‍🎓 You: What is Docker?
🤖 Bot: Docker is a container engine that packages and runs applications in loosely isolated environments. It provides tooling and a platform to manage the lifecycle of containers, allowing developers to develop, distribute, test, and deploy applications as containers. Docker as a concept can refer to a company, product, platform, CLI tool, or computer program.
.

👩‍🎓 You: What is Kubernetes?
🤖 Bot: Kubernetes (k8s) is an open-source platform for automating deployment,      

```

---

## 🔍 Development Highlights

* ✅ Instruction-tuned prompts ensure factual accuracy
* ⚙️ Modular design simplifies testing and upgrading models or components
* ☁️ Seamless integration with Google Drive for persistent storage
* 🧪 Caching and error handling built-in for smooth UX

---

## 📉 Challenges & Lessons Learned

| Challenge                 | Solution                                          | Lesson Learned                                    |
| ------------------------- | ------------------------------------------------- | ------------------------------------------------- |
| File/Path Errors in Colab | Standardized file handling with `drive.mount()`   | Robust configs prevent cascading issues           |
| API Token Failures        | Used `getpass()` and validity checks              | Secure credential handling is essential           |
| Debugging RAG Pipeline    | Added verbose mode to log intermediate outputs    | Transparency boosts trust and debuggability       |
| Weak Retrieval Matches    | Tuned chunk overlap & considered hybrid retrieval | Good retrieval logic directly impacts LLM quality |

---

## ⚙️ Folder Structure

```
📦 NoteBot/
 ┣ 📄 CTSE_Assignment_02.ipynb
 ┣ 📄 CTSE_ML_Assignment_Report_IT21304088.pdf
 ┣ 📁 CTSE_ML_Assignment_Report_IT21304088.docx
 ┣ 📄 README.md
```

---


## 🧠 Powered By

* 🤖 [Google Gemini](https://cloud.google.com/ai/generative-ai/docs/overview)
* 📦 [Chroma Vector DB](https://www.trychroma.com/)
* 🧰 [LangChain](https://www.langchain.com/)
* 🧪 [Google Colab](https://colab.research.google.com/)

---

## 🧑‍💻 Author

👤 **SHABEER M.S.M**
🎓 Sri Lanka Institute of Information Technology
🔗 IT Number: `IT21304088`

---

## 📽️ Demo

🎥 [Watch Demo Video](#)
📂 [View GitHub Repository](#)

> *“Bringing lecture notes to life — one question at a time!”*

---

## 📃 License

This project is for educational purposes only. All rights reserved © 2025.

