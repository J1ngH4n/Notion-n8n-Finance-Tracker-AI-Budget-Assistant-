# 💰 Notion + n8n Finance Tracker (AI Budget Assistant)

An automated personal finance tracker built with **Notion** and **n8n**, integrating **AI feedback**, **budget analysis**, and **Telegram alerts**.

---

## 🧠 Features

- **Daily Expense Summary** → Sends Telegram reminders based on Notion data.  
- **Weekly Budget Analysis** → Generates AI-powered suggestions using Google Gemini.  
- **Monthly Report** → Summarizes all spending categories and detects overspending.  
- **Fully Automated** → Runs on schedule via n8n triggers.

---

## 🛠️ How It Works

1. **Data in Notion**
   - Expense Record database stores daily transactions.
   - Category & Budget database tracks monthly limits.

2. **n8n Workflow**
   - Fetches data from Notion.
   - Processes it using custom JS/Python.
   - Calls Gemini AI for analysis.
   - Sends formatted reports to Telegram.

---

## 📦 Setup

### 1. Import Workflow
1. Download [`Main Workflow.json`](./n8n-workflow/Main%20Workflow.json)
2. In n8n → “Import Workflow” → choose the file.

### 2. Connect Credentials
- Notion API
- Google Gemini (PaLM API key)
- Telegram Bot token

### 3. Duplicate Notion Template
If you want the same Notion setup:
- [Duplicate Template Link](https://www.notion.so/your-template-link)
- Or import the file in `/notion-template/`

---

## 📸 Demo

| Type | Screenshot |
|------|-------------|
| Daily Summary | *(add screenshot of Telegram daily message)* |
| Weekly Report | *(add AI summary image)* |
| Notion View | *(screenshot of Notion database)* |

---

## ⚙️ Tech Stack
- [n8n](https://n8n.io/)
- [Notion API](https://developers.notion.com/)
- [Google Gemini API](https://ai.google.dev/)
- [Telegram Bot API](https://core.telegram.org/bots/api)

---

## 📜 License
MIT License – Free to use, modify, and share.

---

## 🌟 Author
Developed by **Ng Jing Han** — Finance & Automation Enthusiast.
