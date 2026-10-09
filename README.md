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

## Setup & Running
1. Clone the repository and install dependencies:
   ```bash
   pip install -r requirements.txt
