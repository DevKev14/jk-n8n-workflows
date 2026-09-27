# n8n Automation Portfolio

Hi, I'm **John Kevin Morera**, an IT Support Engineer transitioning into workflow automation and AI solutions. This repository showcases practical n8n projects focused on AI, automation, and process optimization.

## Projects

| Project | Description | Tech Stack |
|---|---|---|
| **Knowledge Base & RAG AI Agent** | Ingests Google Drive documents into Pinecone and uses an AI agent to answer questions using retrieved knowledge. | n8n, Google Drive, OpenAI, Pinecone |
| **Real Estate Lead Triage - Gmail to Slack** | Monitors Gmail, uses AI to classify and qualify real estate leads, filters irrelevant emails, and sends qualified leads to Slack. | n8n, Gmail, OpenAI GPT-4o-mini, Slack |
| **AI Customer Support & Booking System (n8n)** | This project has two parts: a knowledge base pipeline that feeds restaurant info into a Supabase vector store, and a conversational AI agent that answers customer questions via RAG, handles bookings end-to-end, and automatically emails both the restaurant and the customer for every reservation — with a human-support escalation path built in. | n8n, OpenAI (chat + embeddings), Supabase (vector store), Gmail API. |
## Featured Projects
### Knowledge Base & RAG AI Agent

- Automatically processes new and updated Google Drive documents.
- Generates OpenAI embeddings and stores them in Pinecone.
- Uses an AI Agent to retrieve relevant information and answer questions.
- Demonstrated using iOS 18 documentation.

**Workflow:** `Google Drive → Document Processing → OpenAI → Pinecone → AI Agent`
![Knowledge Base & RAG AI Agent](https://github.com/user-attachments/assets/5e681617-eb1c-4116-9975-228849d09e6c)
### Real Estate Lead Triage - Gmail to Slack

- Monitors incoming Gmail messages.
- Uses GPT-4o-mini to identify and qualify real estate leads.
- Evaluates budget, timeline, property interest, and viewing requests.
- Filters spam and irrelevant inquiries.
- Sends qualified leads to Slack automatically.

**Workflow:** `Gmail → AI Agent → Lead Qualification → Filtering → Slack`
<img width="1132" height="439" alt="Image" src="https://github.com/user-attachments/assets/dc7620cd-af88-43ed-91fa-3556e30fe860" />

### AI Customer Support & Booking System (n8n)

- Monitors incoming customer chat messages.
- Uses GPT-4o-mini to answer restaurant FAQs via a Supabase-backed knowledge base (RAG).
- Detects booking intent and collects customer name, email, party size, date/time, and special requests.
- Sends a booking notification email to the restaurant automatically.
- Sends a booking confirmation email to the customer automatically.
- Escalates to human support via email when requested or when the AI can't resolve the query.

**Workflow:** `Chat Trigger → AI Agent → Knowledge Base Retrieval / Booking Collection → Gmail (Restaurant + Customer + Human Support)`
<img width="865" height="635" alt="Image" src="https://github.com/user-attachments/assets/400d58ab-058e-4182-803b-2ae246b351fe" />

### KB for Support and Booking Agent
- Ingests restaurant knowledge (menu, hours, policies, FAQs) into a vector store.
- Generates embeddings using OpenAI.
- Stores and indexes the data in Supabase for fast semantic retrieval.
- Powers the AI agent's RAG-based answers, keeping responses accurate and grounded.
- Keeps the knowledge base easily updatable without touching the agent's core logic.
  
Workflow: `Source Documents → Embeddings (OpenAI) → Supabase Vector Store → RAG Retrieval`
<img width="830" height="454" alt="Image" src="https://github.com/user-attachments/assets/c8df334e-62ae-485f-9e79-93ac05912690" />

## Skills & Technologies

- n8n Workflow Automation
- AI Agents & Prompt Engineering
- RAG & Vector Search
- OpenAI
- Supabase
- Gmail Integration
- Conversational Memory
- API Integrations
- Process Automation

## About Me

I'm an IT Support Engineer with experience in troubleshooting, systems administration, and end-user support. I'm currently expanding my skills into AI automation and workflow solutions.
