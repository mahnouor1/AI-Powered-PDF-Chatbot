# AI-Powered-PDF-Chatbot
# 🧞‍♂️ Document Genie – AI-Powered PDF Chatbot

Document Genie is an intelligent RAG-based chatbot that lets you **upload PDF files and ask questions** about their content. Whether you're reviewing research papers, contracts, manuals, or reports, Document Genie helps you find answers quickly and accurately — all powered by **Google Gemini's LLM** and vector-based retrieval.

Built as part of an AI hackathon project, this tool demonstrates how retrieval-augmented generation (RAG) can enhance the accuracy and relevance of chatbot responses when dealing with external knowledge (PDF documents in this case).

---

## 🚀 Features

- 📥 **PDF Upload**: Upload multiple PDFs at once.
- 🔍 **Smart Search**: Ask natural language questions about the content.
- 🧠 **LLM + RAG**: Combines Google Gemini (via LangChain) with FAISS vector database for accurate retrieval.
- ⚡ **Fast Responses**: Uses the lightweight `gemini-2.0-flash` model for efficiency.
- 🔐 **Secure API Input**: Google API key input handled securely in the interface.

---

## 💡 How It Works (Behind the Scenes)

1. **PDF Extraction**  
   Your uploaded PDFs are read and the raw text is extracted.

2. **Chunking**  
   The text is split into overlapping chunks to optimize retrieval performance.

3. **Embedding Generation**  
   Each chunk is converted into an embedding using **Google Generative AI Embeddings**.

4. **Vector Storage with FAISS**  
   These embeddings are stored in a **FAISS** vector index, saved locally.

5. **User Question + RAG Pipeline**  
   - Your question is embedded and used to retrieve the most relevant chunks.
   - The retrieved context is passed along with the question to the **Gemini model**.
   - The model generates a detailed, context-aware answer.

---

## 🛠️ Tech Stack

- **Streamlit** – UI framework
- **LangChain** – Orchestration framework for LLM apps
- **Google Generative AI API** – for both embeddings and chat completions (Gemini)
- **FAISS** – Vector database for semantic search
- **PyPDF2** – PDF text extraction
