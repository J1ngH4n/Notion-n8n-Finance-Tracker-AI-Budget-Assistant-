# 💰 Notion + n8n Finance Tracker (AI Budget Assistant)

An automated finance tracker that connects **Notion**, **n8n**, and **Google Gemini AI** to manage expenses, analyze budgets, and send reports via **Telegram** — all fully automated. All data for this system is securely stored within Notion, a cloud-based note-taking application that has a highly customizable and structured database.

![Workflow Overview](https://github.com/user-attachments/assets/fa95477f-9fc9-4ba8-8838-a64d13052cfd)


---

## 🧠 Features

- 🕗 **Daily Expense Reminder**  
  Retrieves daily expenses from Notion and sends a daily summary to Telegram.

- 📅 **Weekly Spending Review**  
  Calculates weekly totals, highlights overbudget categories, and uses Google Gemini AI to suggest improvements and spending behavior.

- 🗓️ **Monthly Summary**  
  Compiles overall spending by category, compares against budgets, and sends an AI-generated summary.

---

## ⚙️ Workflow Overview

| Component | Description |
|-----------|-------------|
| **Platform** | [n8n](https://n8n.io) |
| **Data Source** | [Notion](https://www.notion.so) |
| **AI Engine** | [Google Gemini API](https://aistudio.google.com/api-keys) |
| **Notifications** | [Telegram Bot](https://core.telegram.org/bots) |
| **Automation File** | `n8n-workflow/Main Workflow.json` |

---

## 🧩 Notion Setup

1. Duplicate this Notion template:  
   👉 [Finance Tracker 2.0 Template](https://forested-macaroon-b41.notion.site/FINANCE-TRACKER-2-0-1-2a1d07d020be815bbe49efcbeace661b?source=copy_link)

2. It includes two databases:
   - `Expense Record` — for daily transactions
   - `Expenses Type & Budget` — for category and budget limits

3. You may change the settings (Budget setting, Expenses Category, Account Details) and try out the feature on your own.

4. After duplication, go to **Settings → My Integrations** in Notion, create a new integration, copy your **secret token**, and share both databases with it (Add Connection → your integration name).

---

## 🔧 How to Import & Connect in n8n

1. Open your n8n instance (local or cloud).
2. Click **Workflows → Import from File → select `n8n-workflow/Main Workflow.json`**.
3. Create the following credentials in n8n:

| Service | Required Fields |
|---------|-----------------|
| **Notion** | Notion Integration Token |
| **Google Gemini** | API Key from Google AI Studio |
| **Telegram** | Token from BotFather |

4. Assign each credential to the correct nodes in the workflow editor.
5. Manually test one workflow to confirm data retrieval and Telegram message delivery.

---

## 📋 Notion Template

This section provides access to the Notion Finance Tracker used in the n8n Finance Tracker.

### Duplicate the Template
[👉 Click here to open and duplicate the Finance Tracker 2.0 Notion Template](https://forested-macaroon-b41.notion.site/FINANCE-TRACKER-2-0-1-2a1d07d020be815bbe49efcbeace661b?source=copy_link)

Once duplicated, make sure to:
1. Share both databases (`Expense Record` and `Expenses Type & Budget`) with your Notion integration.
2. Copy the integration token and use it in n8n's Notion credential.

---

## 🔑 Credentials Setup Guide

To use this workflow, connect these three services in n8n.

### 1️⃣ Notion

**Credential Name:** `Notion account`

#### Steps
1. Go to [Notion My Integrations](https://www.notion.so/my-integrations)
2. Click **New Integration**, copy your secret token.
3. Open your duplicated template:
   - Expense Record
   - Expenses Type & Budget
4. Click **Share → Add connection → your integration**.
5. In n8n:
   - Create a new Notion credential named `Notion account`
   - Paste your secret token.

---

### 2️⃣ Google Gemini

**Credential Name:** `Gemini Finance`

#### Steps
1. Visit [Google AI Studio](https://aistudio.google.com/)
2. Sign in → Create a project → Generate an **API key**
3. In n8n → Paste the API key in the AI agent.
4. Used by the workflow's AI nodes for weekly/monthly reports.

---

### 3️⃣ Telegram Bot

**Credential Name:** `Telegram account`

#### Steps
1. Chat with [@BotFather](https://t.me/BotFather)
2. Run `/newbot` → follow steps → copy token (e.g., `123456:ABC-DEF...`)
3. In n8n:
   - Create credential named `Telegram account`
   - Paste token.
4. Set your **chat ID** in nodes.

---

