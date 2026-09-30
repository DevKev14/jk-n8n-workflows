# n8n Automation Portfolio

Hi, I'm **John Kevin Morera**, an IT Support Engineer transitioning into workflow automation and AI solutions. This repository showcases practical n8n projects focused on AI, automation, and process optimization.

## Projects

| Project | Description | Tech Stack |
|---|---|---|
| **Knowledge Base & RAG AI Agent** | Ingests Google Drive documents into Pinecone and uses an AI agent to answer questions using retrieved knowledge. | n8n, Google Drive, OpenAI, Pinecone |
| **Real Estate Lead Triage - Gmail to Slack** | Monitors Gmail, uses AI to classify and qualify real estate leads, filters irrelevant emails, and sends qualified leads to Slack. | n8n, Gmail, OpenAI GPT-4o-mini, Slack |
| **AI Customer Support & Booking System** | This project has two parts: a knowledge base pipeline that feeds restaurant info into a Supabase vector store, and a conversational AI agent that answers customer questions via RAG, handles bookings end-to-end, and automatically emails both the restaurant and the customer for every reservation — with a human-support escalation path built in. | n8n, OpenAI (chat + embeddings), Supabase (vector store), Gmail API. |
| **Email Auto-Sort Agent** | Monitors an inbox, uses AI to classify incoming emails by category/priority, and automatically sorts them into the correct folders or labels — cutting down on manual inbox management. | n8n, Gmail/Outlook, OpenAI |
| **Dead Lead Reactivation Campaign** | An n8n workflow that automatically re-engages inactive sales leads over email and SMS. Every week it pulls dead leads from a Google Sheets CRM, uses AI to segment each lead and write a personalized message, sends it through the right channel, and answers replies on both channels with an AI-driven conversation loop. | n8n, Any Database, Gmail, Twilio, OpenAI |

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

### Email Auto-Sort Agent
- Monitors incoming emails in real time.
- Uses an AI model to classify each email by category, sender intent, or priority.
- Automatically applies labels or moves emails into the appropriate folders.
- Reduces manual inbox triage and keeps important messages easy to find.

Workflow: `Email Trigger → AI Classification → Label/Folder Routing`
<img width="1581" height="597" alt="Image" src="https://github.com/user-attachments/assets/ecb1df54-7597-4c1f-a7cf-1bcf513a5965" />

### Dead Lead Reactivation Campaign
Campaign (outbound)
- Weekly Reactivation Trigger starts the run on a schedule.
- Get Lead Database reads leads from Google Sheets.
- Filter Dead Leads keeps only inactive leads.
- Loop Over Items processes one lead at a time.
- Resolve Channel reads the channel column and decides between email and SMS.
- Segment & Personalize Message is an AI agent (OpenAI gpt-4o-mini) with a structured output parser. It classifies the lead and writes the message.
- Route by Channel sends the lead down the email, SMS, or skipped path.
- Email path: sends the email with Gmail, applies the Business label, and logs the attempt.
- SMS path: sends the text through Twilio and logs the attempt.
- Skipped path: leads that can't be contacted are logged instead of dropped.
  Workflow: `Weekly Schedule Trigger → Lead Database Filter → AI Segmentation & Personalization → Channel Routing (Email / SMS / Skipped)`

Email replies (inbound)
- Gmail Trigger polls for unread emails with the Business label. A Gmail filter applies that label to replies from leads as they arrive.
- Normalize Email Reply extracts the sender, subject, body, and message ID.
- Continue Email Conversation is an AI agent with conversation memory that writes a context-aware response.
- Send Email Reply sends the response from the same Gmail account.
- Mark Email as Handled marks the message as read so it is not processed twice.
  Workflow: `Gmail Trigger → AI Conversation → Send Reply & Mark as Handled`

SMS replies (inbound)
- Twilio Trigger fires when a lead texts back (inbound message received).
- Normalize SMS Reply extracts the sender's number and message text.
- Continue SMS Conversation is an AI agent with its own conversation memory that writes a short, SMS-appropriate reply.
- Send SMS Reply sends the response back through Twilio.
- Write SMS Reply to Outbox records the reply in Google Sheets for tracking.
  Workflow: `Twilio Trigger → AI Conversation → Send SMS Reply & Log`



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
