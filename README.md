# n8n Automation Portfolio

Hi, I'm **John Kevin Morera**, an IT support engineer moving into workflow and AI automation. This repository collects the n8n projects I've built while putting my troubleshooting and systems background to work on automation.

## Projects

| Project | What it does | Tools |
|---|---|---|
| [Knowledge Base & RAG AI Agent](./knowledge-base-rag-agent) | Automatically ingests documents from Google Drive into a vector database, then answers questions about them through an AI chat agent. | n8n, Google Drive, OpenAI, Pinecone |

## Featured: Knowledge Base & RAG AI Agent

- **Ingestion:** Google Drive triggers fire when a file is created or updated, the file is downloaded, converted to embeddings, and stored in Pinecone.
- **Chat agent:** An AI agent searches the Pinecone knowledge base (iOS 18 documentation) and answers questions using retrieved context.

## How to use a workflow

1. Open the project folder and copy the contents of `workflow.json`.
2. In n8n, paste it onto the canvas with `Ctrl+V` (or use **Import from File**).
3. Connect your own credentials: Google Drive, Pinecone, and OpenAI.

> No API keys or secrets are stored in this repository. Credentials must be added in your own n8n instance.


<img width="1496" height="468" alt="Image" src="https://github.com/user-attachments/assets/5e681617-eb1c-4116-9975-228849d09e6c" />
