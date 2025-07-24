# 🧠 Conversational AI for E-Commerce Insights

This project is an **LLM-powered business intelligence assistant** that enables users to analyze e-commerce performance metrics through natural language queries. It connects tabular CSV data to an in-memory SQL engine and uses Google's Gemini models to convert user prompts into insightful visualizations and analytical responses.

---

## 🚀 Features

- 🔎 **Natural language to SQL** translation using Gemini LLM
- 📊 E-Commerce metrics supported:
  - Total sales
  - Ad spend and RoAS (Return on Ad Spend)
  - CPC (Cost per Click)
  - Promo eligibility
- 🧠 **Auto-formatted responses** with fallback for common queries
- 🎨 **Interactive visualizations** with:
  - Top CPC and RoAS bar charts
  - Ad Spend vs Sales scatter
  - Promotional eligibility pie chart
- 💬 **Enhanced streaming output** with interrupt support and event tracking

---

## 🖥️ Environment Setup (Google Colab Recommended)

1. Upload the following datasets:
   - `Product-Level Ad Sales and Metrics (mapped).csv`
   - `Product-Level Total Sales and Metrics (mapped).csv`
   - `Product-Level Eligibility Table (mapped).csv`

2. Install dependencies:
   !pip install pandas matplotlib sqlalchemy google-generativeai


3. Add your API key:
   - In Colab, use the sidebar > **🔑 Secrets** > Add key as `GEMINI_API_KEY`

---

## 📦 Modules Overview

| Component                     | Role                                              |
|------------------------------|---------------------------------------------------|
| `SQLite`:                    | Stores tabular data in memory                     |
| `Gemini LLM`:                | Converts prompt → SQL                             |
| `Formatter/Formatter+`:      | Converts query result → human-readable summary    |
| `Manual SQL fallback`:       | Handles FAQ-style queries without LLM support     |
| `Matplotlib Visuals`:        | Generates CPC/RoAS/Promo visualizations           |
| `Event stream engine`:       | Streams responses, logs actions, supports overrides |

---

## 💡 Example Queries

Ask questions like:

- **“What is my total sales?”**
- **“Calculate the RoAS (Return on Ad Spend).”**
- **“Which product had the highest CPC?”**
- **“Show me all products not eligible for promo.”**

---

## 📊 Visualizations Included

| Type                        | Chart Description                           |
|----------------------------|----------------------------------------------|
| CPC                        | Top 10 products (bar chart)                  |
| RoAS                       | Top 10 products (bar chart)                  |
| Ad Spend vs Sales          | Scatter plot for correlation analysis        |
| Promo Eligibility          | Pie chart by eligible/not eligible status    |

---

## 📡 Streaming Support

Includes realistic streaming with:

- ✍️ Typing simulation of responses
- 🎯 Event tracking (`stream_start`, `chunk_received`, `stream_complete`)
- ⛔ Interruptible streaming with `q` + Enter support

---

## 📁 Directory Essentials

Make sure the following files are present and correctly named:

- `*.csv` files (as referenced above)
- Main script (`.py` or notebook with full logic)
- GEMINI API key (loaded via Colab secrets or direct assignment)

---

## 📌 Requirements

- Python 3.8+
- Google Gemini API access
- Compatible with Google Colab notebook or local Python runtime

---

## 📜 License

This is a research and demonstration project. Not intended for production environments. Use at your own discretion.

---


