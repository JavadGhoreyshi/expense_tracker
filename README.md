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
```

### 2. Create & Activate Virtual Environment
```bash
# Windows
python -m venv venv
venv\Scripts\activate

# Linux / macOS
python3 -m venv venv
source venv/bin/activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Configuration
1. Create a `.env` file in the root directory:
   ```env
   TELEGRAM_BOT_TOKEN="your_telegram_bot_token"
   GEMINI_API_KEY="your_gemini_api_key"
   ```
2. Download your Google Service Account key from Google Cloud Console and save it as `credentials.json` in the project root.
3. Share your Google Sheet (named `Expense_Tracker`) with the client email found inside `credentials.json` (grant Editor access).

### 5. Run the Bot
```bash
python bot.py
```
