# 🤖 n8n Smart Personal Agent Workflow

<img width="1701" height="715" alt="image" src="https://github.com/user-attachments/assets/1795bb02-0333-47cc-82c0-2441bc0a4f48" />


This project is an advanced **multi-agent automation workflow** built using [n8n](https://n8n.io). It includes intelligent agents that interact with:
- **Gmail** (email automation)
- **Google Calendar** (event handling)
- **Airtable** (contact management)
- **YouTube + Google Sheets** (content research & planning)
- **LLMs via OpenRouter** (GPT-4.1-mini)
- **Telegram (chat interface)**

## 📌 Features

### 🔹 Master Agent
Acts as the main orchestrator. It:
- Receives user input from a chat trigger
- Delegates tasks to the appropriate sub-agents (email, calendar, contacts, content)
- Uses `Think` agent to reflect and validate each task

### 🔹 Email Agent
Manages all Gmail-related tasks:
- Send Emails
- Create Drafts
- Reply to Emails
- Get Emails / Labels
- Mark as Unread / Apply Labels

### 🔹 Calendar Agent
Handles event scheduling with Google Calendar:
- Create solo or attendee events
- Get, update, and delete events

### 🔹 Contact Agent
Interfaces with Airtable to:
- Get contact details
- Add or update contact records

### 🔹 YouTube Agent
Supports content creation:
- Scrape high-performing YouTube videos using Apify
- Suggest new ideas
- Append them to Google Sheets

### 🔹 Think Agent
LLM-powered reasoning step that validates choices made by the system for reliability.

### 🔹 GPT 4.1-mini
Used across agents via OpenRouter for intelligent prompt handling.

### 🔹 Telegram Integration
Includes a `chatTrigger` node to allow real-time conversations with the AI agent.

---

## 🧠 How It Works

1. **User Message** ➝ Telegram → Master Agent
2. **Master Agent** determines the task (email, calendar, etc.)
3. **Sub-Agent** (like Email Agent) processes the request
4. **LLM (GPT 4.1-mini)** used for reasoning and formatting
5. **Think Agent** validates the action
6. **Simple Memory** stores short session context

---

## ⚙️ Requirements

- n8n instance (Cloud or Self-hosted)
- Gmail OAuth2 credentials
- Google Calendar OAuth2
- Airtable API Token
- OpenRouter API key
- Telegram Bot Token
- Apify API Key (for YouTube scraping)
- Google Sheets access for storing ideas

---

## 🏁 Setup

1. Import the `My workflow.json` into your n8n instance.
2. Set up credentials for:
   - Gmail
   - Google Calendar
   - Airtable
   - OpenRouter
   - Apify
   - Telegram
3. Connect your Google Sheet for YouTube ideas.
4. Start the workflow and send messages via Telegram to begin interacting.

---

## 📒 Example Prompts

- "Send a follow-up email to John Doe about the meeting"
- "Create a calendar event tomorrow at 3 PM with Sarah"
- "Add Sam Lee to my contacts with email sam@example.com"
- "Get 3 high-performing videos on AI tools this month"

---

## 🧩 Credits

Built with:
- [n8n](https://n8n.io)
- [OpenRouter](https://openrouter.ai)
- [Google APIs](https://developers.google.com/)
- [Airtable](https://airtable.com)
- [Apify YouTube Scraper](https://apify.com/streamers/youtube-scraper)

---

## 🛡️ License

MIT License. Use at your own risk. Ensure data privacy and API usage compliance.

