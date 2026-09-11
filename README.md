<h1 align="center">🚀 AI-Powered Multi-Channel Content Distribution Engine</h1>

<p align="center">
  <strong>An advanced, zero-touch workflow built on n8n that automates content aggregation, AI-driven summarization, and cross-platform publishing.</strong>
</p>

---

## 📌 Project Overview
Managing content across multiple platforms requires significant manual effort. This project solves that bottleneck by establishing an autonomous pipeline. Triggered by a simple Google Sheet update, the engine processes raw data, leverages **Google Gemini AI** for intelligent formatting and summarization, and dynamically distributes multimedia content across professional and social channels.

## 🏗️ System Architecture & Workflow Flow

![Workflow Architecture](https://drive.google.com/uc?export=view&id=1YWyrJG5YwZ87ivZWvSMycbTtqKV_yDtF)

The n8n visual canvas above demonstrates the complex routing and automation logic:
* **The Trigger:** The workflow initiates automatically via a **Google Sheets Trigger** upon new data entry.
* **Data Transformation:** Custom **JavaScript Nodes** and **HTTP Requests** parse, clean, and route the incoming data payloads.
* **The AI Brain:** Integrated **Google Gemini Chat Models** process the text, executing tasks like `summarize article` and generating platform-specific copy via Basic LLM Chains.
* **Multi-Branch Distribution:**
  * **LinkedIn:** Auto-creates professional posts.
  * **Telegram:** Dispatches text, photos, and video messages to designated channels/bots.
  * **Discord:** Pushes formatted messages to server webhooks.
  * **Gmail:** Sends internal notifications and structured email summaries.

## 🛠️ Tech Stack & Integrations
* **Workflow Orchestration:** n8n (Self-hosted via Docker)
* **AI & LLM:** Google Gemini API
* **Data Processing:** Node.js (Custom JavaScript blocks), REST APIs
* **Database/Input:** Google Sheets API
* **Publishing Endpoints:** LinkedIn API, Telegram Bot API, Discord Webhooks, Gmail SMTP

## ⚡ Key Features
* **100% Autonomous:** Eliminates manual cross-posting efforts completely.
* **Format Agnostic:** Capable of handling and distributing Text, Photos, and Videos conditionally.
* **Smart Content Scaling:** Uses AI to adapt a single piece of content into multiple formats suited for different platforms.
* **Fault Tolerant:** Built with robust branching to ensure one failed API call doesn't stop the entire distribution pipeline.

## 🚀 How to Run Locally
1. Clone this repository.
2. Spin up the n8n environment using Docker and expose it via Ngrok for webhook support.
3. Import the `workflow.json` file into your n8n instance.
4. Configure your credentials for Google, Gemini, LinkedIn, Telegram, and Discord within the n8n UI.
5. Activate the workflow!

---
<p align="center"><i>Engineered for maximum reach with minimum effort.</i></p>
