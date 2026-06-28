# AI Ticket Triage System 🎫

An AI-powered customer support ticket classification and routing system built with n8n, Groq (Llama), Gmail, and Google Sheets.

## 🔧 Tools Used
- **n8n** — Workflow orchestration
- **Groq (Llama)** — AI classification engine
- **Google Sheets** — Audit trail and logging
- **Gmail** — Automated alerts and reminders

## 🔀 How It Works
1. Customer submits a support ticket via form
2. AI Agent classifies it as High, Medium, or Low priority
3. Switch node routes it accordingly:
   - 🔴 **High** → Logged to Sheets → Immediate Gmail alert
   - 🟡 **Medium** → Logged to Sheets → Delayed Gmail reminder
   - 🟢 **Low** → Logged to Sheets only

## 🧠 Key Design Decisions
- Strict one-word output prompt for reliable parsing
- Memory node deliberately removed — stateless classification per ticket
- Sheets as single source of truth before any routing

## 🚧 Future Scope
- Resolution tracking via status column in Sheets
- Second trigger to cancel Medium reminder if ticket resolved
- Slack integration for team notifications

## 📸 Workflow Screenshot
<img width="1453" height="568" alt="image" src="https://github.com/user-attachments/assets/b1db41fc-7da2-4d06-9154-aea52a99a6b0" />


## 🔗 Built As Part Of
GenAI Bootcamp — Career Comeback Hub
