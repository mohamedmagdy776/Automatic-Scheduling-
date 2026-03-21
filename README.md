# 📅 Automatic Scheduling Agent (n8n + AI)

An intelligent automation system built with **n8n + AI** that allows a business owner to schedule meetings with employees via Telegram — using text messages — with automatic conflict checking, Google Calendar event creation, and email notifications.

---

## 🚀 Overview

This project simulates a smart scheduling assistant that interacts with the business owner through Telegram, collects meeting details, checks for conflicts, and automatically creates calendar events.

---

## 🧠 Workflow Structure

The workflow operates in the following sequence:

### 1. 📩 Telegram Trigger
- Captures incoming text messages from the business owner

### 2. 🤖 AI Agent
- Core intelligence of the system
- Powered by **OpenAI GPT** model
- Uses **Simple Memory** to maintain conversation context per user
- Connected tools:
  - 📊 **Google Sheets** — reads employee database (Name, Role, Phone, Email)
  - 📅 **Google Calendar** — checks conflicts & creates 30-minute events
  - 📧 **Gmail** — sends meeting invitation emails with Meet link
  - 💬 **Telegram** — sends confirmations, conflicts, and updates to the owner
  - 🧠 **OpenAI Chat Model** — interprets intent and manages conversation flow
  - 💾 **Simple Memory** — stores meeting details per user before confirmation

### 3. 📨 Telegram (Send a Text Message)
- Sends the final response back to the business owner

---

## 📋 Agent Rules

- **Always confirm** before scheduling: Date, Start Time, Duration, Employee, Topic, Location/Meet Link
- **Block** any calendar conflicts automatically
- **Schedule only** after explicit owner confirmation
- **Respond in the same language** as the user (Arabic or English)
- **Never switch languages** mid-conversation

---

## 📁 Data Source (Google Sheets)

The agent reads employee data from a connected Google Sheets database containing:

- Employee Name
- Role / Title
- Phone Number
- Email Address

---

## ⚙️ Tech Stack

- **n8n** — Workflow automation platform
- **OpenAI GPT** — AI agent and intent understanding
- **Telegram Bot API** — User interface for the business owner
- **Google Calendar API** — Conflict checking and event creation
- **Google Sheets API** — Employee database
- **Gmail API** — Email notifications

---

## 🌍 Timezone

All scheduling is handled in **Africa/Cairo (GMT+2)** timezone to ensure accurate meeting times for Egypt-based operations.

---

## 👤 Author

**Eng. Mohamed Magdy Mohamed Elghandour**  
AI Automation Engineer
