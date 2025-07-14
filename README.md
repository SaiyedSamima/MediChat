# MediChat
AI Doctor Chatbot <!-- MediChat -->
A Retrieval‑Augmented‑Generation (RAG)–based web application that delivers accurate, context‑aware medical answers in natural language.
It combines a curated 637‑page medical textbook, vector search in Pinecone, and OpenAI’s GPT model behind a clean ChatGPT‑style interface.

| Feature                                  | Why it matters                                                                       |
| ---------------------------------------- | ------------------------------------------------------------------------------------ |
| **Reliable medical knowledge base**      | Answers are grounded in peer‑reviewed text (no hallucinations from the open web).    |
| **Retrieval‑Augmented Generation (RAG)** | Fetches the most relevant passages, then synthesises a concise response.             |
| **Semantic search with embeddings**      | Understands meaning, not just keywords, boosting answer accuracy.                    |
| **Chat‑style UI (Flask)**                | Familiar, mobile‑friendly interface that feels like talking to a doctor’s assistant. |
| **Scalable micro‑service design**        | Swap models, add data sources, or deploy to cloud servers with minimal code change.  |


1.Embedding Service – Converts user query and textbook chunks into high‑dimensional vectors.

2.Pinecone – Stores vectors and returns the top‑k semantically similar chunks.

3.Gemini – Generates the final answer, citing the retrieved chunks.

4.Flask – Orchestrates traffic and serves the chat interface.


| Layer             | Tool / Library                               |
| ----------------- | -------------------------------------------- |
| Language Model    | **OpenAI GPT‑4o** (API)                      |
| RAG Orchestration | **LangChain**                                |
| Embeddings        | **SentenceTransformer** (`all‑MiniLM‑L6‑v2`) |
| Vector Storage    | **Pinecone** (cosine similarity)             |
| Backend           | **Python 3.10**, **Flask**                   |
| Front‑end         | Vanilla JS + Bootstrap                       |
| Dev & Ops         | Docker, dotenv, GitHub Actions               |



🔮 Future Work
Voice input/output via WebRTC

Multilingual support (Hindi, Spanish, etc.)

Live updates from CDC / WHO APIs

HIPAA‑compliant user profile integration

🤝 Contributing
Fork the repo & create a feature branch

Follow Black + isort formatting (pre‑commit run -a)

Open a PR with a clear description; one of the maintainers will review.

🛡️ License
This project is licensed under the MIT License.
See LICENSE for details.

🙏 Acknowledgements
OpenAI for LLM APIs

Pinecone for generous academic tier

Hugging Face community for open‑source transformer models

