# n8n Automation Portfolio

Hi, I'm **John Kevin Morera**, an IT support engineer moving into workflow and AI automation. This repository collects the n8n projects I've built while putting my troubleshooting and systems background to work on automation.

## Projects

| Project | What it does | Tools |
|---|---|---|
| [Knowledge Base & RAG AI Agent](./knowledge-base-rag-agent) | Automatically ingests documents from Google Drive into a vector database, then answers questions about them through an AI chat agent. | n8n, Google Drive, OpenAI, Pinecone |
| [Real Estate Lead Triage — Gmail to Slack](https://github.com/DevKev14/jk-n8n-workflows/blob/main/real-estate-lead-triage) | Monitors a Gmail inbox, uses an AI Agent with structured output to classify and qualify real estate leads, then sends qualified leads to Slack while filtering out spam and casual inquiries. | n8n, Gmail, OpenAI GPT-4o-mini, Slack |

## Featured: Knowledge Base & RAG AI Agent

- **Ingestion:** Google Drive triggers fire when a file is created or updated, the file is downloaded, converted to embeddings, and stored in Pinecone.
- **Chat agent:** An AI agent searches the Pinecone knowledge base (iOS 18 documentation) and answers questions using retrieved context.
<img width="1496" height="468" alt="Image" src="https://github.com/user-attachments/assets/5e681617-eb1c-4116-9975-228849d09e6c" />
## Featured: Real Estate Lead Triage — Gmail to Slack

Email monitoring: n8n polls a Gmail inbox for new incoming emails.
AI classification: An AI Agent powered by GPT-4o-mini analyzes each email and determines whether it is a real estate lead.
Lead qualification: Structured output evaluates factors such as budget, buying timeline, property interest, and viewing requests.
Lead filtering: Spam, irrelevant messages, and casual inquiries are filtered out before reaching the sales team.
Slack notification: Qualified leads are automatically posted to Slack in real time, giving the sales team the information needed for follow-up.


