# 🧠 n8n RAG Workflow Template

This repository contains a pre-configured **n8n JSON workflow template** designed for building and deploying a **Retrieval-Augmented Generation (RAG)** pipeline.

---

## 🔍 What is RAG?

RAG combines traditional retrieval techniques with modern language generation models. Instead of relying solely on a language model's trained knowledge, RAG enables the model to **search external sources** (like documents, databases, or APIs) and use the retrieved information to generate more accurate, relevant, and context-aware responses.

---

## 🧰 Workflow Overview

This n8n template includes a basic RAG setup with the following stages:

1. **Trigger** – Initiates the workflow manually or via Webhook/API.
2. **Document Search** – Queries a vector database or document storage (e.g., Pinecone, Weaviate, Supabase, etc.).
3. **Context Retrieval** – Extracts the top relevant documents or passages.
4. **Prompt Construction** – Assembles a final prompt for the language model (OpenAI, Hugging Face, etc.).
5. **Generation** – Calls the LLM API with the constructed prompt and retrieved context.
6. **Response Handling** – Returns the generated result via email, webhook, or frontend app.
7. **Logging (Optional)** – Logs the interaction for tracking or retraining purposes.

---

## 📂 File Structure


---

## 📥 How to Import

1. Open your n8n instance.
2. Go to **Workflows > Import from File**.
3. Upload the `rag-workflow.json` file.
4. Review the nodes, update credentials (OpenAI API key, DB connection, etc.)
5. Click **Activate** to start using the workflow.

---

## ⚙️ Requirements

- **n8n instance** (cloud or self-hosted)
- **API key for LLM provider** (OpenAI, Cohere, etc.)
- **Vector DB or retrieval source** (Pinecone, Qdrant, Supabase, etc.)
- Optional: Slack Webhook, Notion API, or front-end trigger integration

---

## 🧪 Testing

You can test the workflow manually:
- Trigger the workflow manually
- Input a sample question (e.g. "What are the latest features in GPT-4?")
- Verify the retrieved context and generated answer in the output

---

## 🛠 Customization Tips

- Add **authentication layer** if used in production
- Swap **OpenAI** with **Claude, Gemini, or Mistral** depending on your LLM provider
- Add **error handling nodes** for failed API calls
- Log interactions to **Postgres, Notion, or Airtable** for later analysis

---

## 📄 License

This workflow template is provided for educational and prototyping purposes under the [MIT License](./LICENSE).

---

## 🙋 Need Help?

If you run into issues or want to extend this RAG pipeline further, feel free to open an issue or contact the maintainer.

Happy automating! ⚡
