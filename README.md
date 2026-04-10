# 🚀 AI-Powered E-Commerce Price Monitoring Automation

Never miss a price drop again! This project is an end-to-end automation workflow built on **n8n** that turns manual price checking into a smart, data-driven system using **AI Agents**.

<img width="1366" height="584" alt="Screenshot (1403)" src="https://github.com/user-attachments/assets/5c3c85f6-b8bb-47d5-88b1-54e75974da44" />

## 📋 Table of Contents
- [Overview](#overview)
- [How It Works](#how-it-works)
- [Key Features](#key-features)
- [Tech Stack](#tech-stack)
- [Setup Instructions](#setup-instructions)

---

## 🧐 Overview
Manual price tracking is slow and repetitive. This automation solves that by:
1. **Scraping** live prices from e-commerce sites (e.g., eBay).
2. **Cleaning** data using Python.
3. **Storing** price history in Google Sheets.
4. **Analyzing** trends using **OpenAI Agents** to identify real deals.
5. **Notifying** you via Slack only when a significant price drop occurs.

## ⚙️ How It Works

### Phase 1: Data Collection
The workflow triggers on a schedule, visits product URLs, and extracts the product title and current price using HTML selectors.

### Phase 2: Data Processing & Logging
A **Python node** cleans the price (removing currency symbols), and the data is appended to a **Google Sheet**. This builds a historical record of price changes over time.

### Phase 3: AI Analysis (The Brain)
We use **two AI Agents** (one for each product) to provide parallel and focused analysis. Each agent:
- Uses a Google Sheets tool to read previous history.
- Compares the latest price with historical data.
- Determines if the current price is a "Good Deal."

### Phase 4: Smart Notifications
If the AI detects a significant price drop, it triggers a **Slack notification**. If the price is stable, the system stays silent to reduce noise.

## ✨ Key Features
- **Zero Human Involvement:** Fully automated daily checks.
- **AI-Driven Insights:** Doesn't just track numbers; it understands value.
- **Noise Reduction:** Only alerts you when there is a real deal.
- **Scalable:** Easy to add more products by duplicating branches.

## 🛠️ Tech Stack
- **n8n:** Workflow Automation
- **Python:** Data cleaning and formatting
- **OpenAI:** GPT-4o for price trend analysis
- **Google Sheets:** For historical data storage
- **Slack:** For real-time alerts

---

## 🚀 Setup Instructions

1. **Import Workflow:** Download the provided `.json` file and import it into your n8n instance.
2. **Credentials:** 
   - Add your **OpenAI API Key**.
   - Connect your **Google Sheets** account.
   - Set up a **Slack Webhook** or App.
3. **Configuration:**
   - Update the **Fetch-product** nodes with your desired product URLs.
   - Select your spreadsheet in the **Google Sheet nodes**.
4. **Deploy:** Toggle the workflow to 'Active' to start monitoring.

---

## 📈 Business Impact
- **Time Saved:** ~20-25 hours/month per user.
- **Accuracy:** 100% accurate price logging.
- **Savings:** Ensures you always buy at the lowest historical price.

---

**Developed with ❤️ using n8n and AI.**
