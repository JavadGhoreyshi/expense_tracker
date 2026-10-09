# AI-Powered Telegram Expense Tracker

An automated personal finance bot for Telegram that extracts transaction intents using Google Gemini and logs categorized expenses into Google Sheets in real time.

## Features
- **Natural Language Parsing:** Uses Gemini to identify transaction actions (add, edit, delete, list) and extract dates, items, and prices from free-form text.
- **Google Sheets Integration:** Automatically syncs expense logs and updates summary budgets.
- **Currency Conversion:** Fetches live market exchange rates for dual Toman/USD logging with fallback caching.
- **Fuzzy Item Matching:** Identifies items for edits or deletions even with typos.

## Tech Stack
- Python 3.10+
- `python-telegram-bot`
- `google-genai` (Gemini API)
- `gspread` (Google Sheets API)
- `requests`

## Prerequisites
- Python 3.10 or higher
- A Telegram account (to create a bot via [@BotFather](https://t.me/BotFather))
- A Google Cloud project with Google Sheets API enabled (Service Account credentials)
- A Google Gemini API key

## Getting Started

### 1. Clone Repository
```bash
git clone https://github.com/JavadGhoreyshi/expense_tracker.git
cd expense_tracker
