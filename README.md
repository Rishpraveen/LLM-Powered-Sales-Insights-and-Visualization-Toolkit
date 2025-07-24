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

