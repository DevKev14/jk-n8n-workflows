# n8n Automation Portfolio
 
Hi, I'm **John Kevin Morera**, an IT Support Engineer transitioning into workflow automation and AI solutions. This repository showcases my n8n projects, where I combine my troubleshooting, systems administration, and process optimization experience to build practical automation workflows.
 
## Projects
 
| Project | Description | Tech Stack |
|----------|-------------|------------|
| **Knowledge Base & RAG AI Agent** | Automatically ingests documents from Google Drive into a vector database, enabling an AI-powered chat agent to answer questions using retrieved knowledge. | n8n, Google Drive, OpenAI, Pinecone |
| **Real Estate Lead Triage - Gmail to Slack** | Monitors Gmail for incoming real estate inquiries, classifies and qualifies leads using AI, filters out spam and irrelevant messages, and sends qualified leads directly to Slack. | n8n, Gmail, OpenAI GPT-4o-mini, Slack |
 
---
 
# Featured Project: Knowledge Base & RAG AI Agent
 
An automated Retrieval-Augmented Generation (RAG) system that keeps a knowledge base continuously updated and accessible through an AI chat interface.
 
### Key Features
 
#### 📥 Automated Document Ingestion
- Detects new or updated files in Google Drive.
- Downloads and processes documents automatically.
- Generates embeddings using OpenAI.
- Stores vectorized data in Pinecone for semantic search.
 
#### 🤖 AI-Powered Chat Agent
- Searches the Pinecone vector database for relevant information.
- Retrieves context from indexed documentation.
- Generates accurate responses grounded in the knowledge base.
- Demonstrated using **iOS 18 documentation** as the source material.
 
### Workflow Overview
 
1. Google Drive detects a new or modified file.
2. n8n downloads and processes the document.
3. OpenAI generates embeddings.
4. Pinecone stores vector data.
5. The AI Agent retrieves relevant context.
6. Users receive context-aware answers through chat.
 
### Screenshot
 
![Knowledge Base & RAG AI Agent](https://github.com/user-attachments/assets/5e681617-eb1c-4116-9975-228849d09e6c)
 
---
 
# Featured Project: Real Estate Lead Triage - Gmail to Slack
 
An AI-powered workflow that automatically evaluates incoming real estate inquiries and routes qualified leads directly to the sales team.
 
### Key Features
 
#### 📧 Email Monitoring
- n8n continuously monitors a Gmail inbox for new messages.
 
#### 🧠 AI Lead Classification
- GPT-4o-mini analyzes incoming emails.
- Determines if a message is a legitimate real estate lead.
 
#### ✅ Lead Qualification
The workflow extracts and evaluates:
- Budget range
- Buying timeline
- Property preferences
- Viewing requests
- Contact details
 
#### 🚫 Lead Filtering
- Filters spam and irrelevant messages.
- Removes casual inquiries that do not meet lead criteria.
 
#### 🔔 Slack Notifications
- Sends qualified leads to Slack in real time.
- Provides sales teams with actionable lead information for faster follow-up.
 
### Workflow Overview
 
1. Gmail receives a new email.
2. n8n retrieves the message.
3. AI Agent classifies the inquiry.
4. Structured output evaluates qualification criteria.
5. Spam and low-quality leads are filtered out.
6. Qualified leads are posted to Slack automatically.
 
---
 
## Skills Demonstrated
 
- Workflow Automation
- AI Agent Development
- Retrieval-Augmented Generation (RAG)
- Vector Databases
- Prompt Engineering
- Email Automation
- Lead Qualification Systems
- API Integrations
- Process Optimization
- No-Code / Low-Code Solutions
 
## Tools & Technologies
 
- **n8n**
- **OpenAI**
- **Pinecone**
- **Google Drive API**
- **Gmail API**
- **Slack API**
- **AI Agents**
- **Vector Search**
- **Automation Workflows**
 
---
 
## About Me
 
I'm an IT Support Engineer with experience in troubleshooting, systems administration, and end-user support. I'm currently expanding into workflow automation and AI-powered solutions
