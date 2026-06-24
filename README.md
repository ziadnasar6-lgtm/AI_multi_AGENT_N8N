# AI_multi_AGENT_N8N


# 🌐 NexusAgent-n8n: Multi-Agent AI Business Assistant

A powerful, production-ready Multi-Agent Automation System built entirely on **n8n**. Powered by local open-source LLMs via **Ollama**, this system leverages a main Orchestrator AI Agent connected to a network of specialized sub-agents and tools to seamlessly manage emails, corporate Google Sheets, calendars, and live web searches from a single Telegram interface. 🚀

> ### 📝 Repository Description (سطرين للوصف الخارجي)
> A self-hosted multi-agent n8n workflow powered by Ollama that orchestrates specialized sub-agents to handle automated meetings, Google Sheets operations, email communications, and live web exploration via Telegram.

---

## 🌟 Key Features

### 1. 🧠 Central Orchestrator Agent
* **📱 Telegram Interface:** Acts as the primary control bridge handling incoming webhooks and dispatching tasks hands-free.
* **🦙 Local Intelligence:** Backed by an **Ollama Chat Model** and `Simple Memory` node to maintain contextual human-like conversations.

### 2. 🔀 Specialized Sub-Agent Hierarchy
Based on the architecture seen in `2026-06-24 (15).jpg`, the main agent intelligently routes tasks to four specialized sub-agents:

* **📅 Meeting Management Agent (`Handle My meetings`):** 
  * Queries and parses scheduling data directly from Google Sheets rows.
  * Triggers professional Gmail reminders to teams or owners.
  * Automatically provisions structured events in **Google Calendar**.
* **📊 Database & Sheet Agent (`Google sheets Tool`):**
  * Dedicated exclusively to reading, appending, and updating relational records like **Employees** and **Projects** data tables.
* **📧 Dedicated Email Agent (`emails`):**
  * Manages active message retrieval, tracks unseen high-importance mail, and sends immediate status updates.
* **🔍 Web Exploration & Calendar Agent (`Search and calendar`):**
  * Performs live queries via **Google Search** and scrapes application metadata through **Google Play Search**, executing scheduling actions instantly based on extracted text.
 
---

## 🛠️ Prerequisites & Tech Stack

* **🔗 n8n** (Self-hosted or Cloud instance supporting advanced multi-agent structures)
* **🦙 Ollama Instance** (Running multiple model instances or concurrent handling for `Ollama Chat Model`)
* **📊 Google Workspace Account** (With Google Sheets and Google Calendar API scopes authorized)
* **📧 Gmail API Credentials** (OAuth2 access setup)
* **📱 Telegram Bot API Token** (Via `@BotFather`)

---

## 🚀 Setup Instructions

1. **📥 Import the Workflow:**
   * Download the `.json` file of this orchestration workflow.
   * Import it into your n8n workspace panel.

2. **🔑 Configure Specialized Credentials:**
   * Bind your **Telegram Bot Token** to the main entry/exit nodes.
   * Attach authorized **Google OAuth2** credentials to all Google Sheets, Calendars, and Gmail tool nodes.
   * Set up your **Ollama Base URLs** for each sub-agent chat model node to handle parallel model reasoning safely.

3. **⚡ Deploy & Test:**
   * Switch the pipeline to **Active**.
   * Text your bot instructions like: *"Schedule a meeting with the development team tomorrow"* or *"Add a new project row for the AI automation initiative"*, and watch the sub-agents seamlessly split and execute the work!

---

## 📝 License
This project is open-source and available under the MIT License.
