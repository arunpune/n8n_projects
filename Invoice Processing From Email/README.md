# 📧 AI-Powered Invoice Processing from Email (n8n)

An intelligent automation workflow built using n8n that extracts invoice details directly from emails and logs them into Google Sheets using AI.

---

## 📌 Overview

This project automates invoice tracking by connecting Gmail, AI (Google Gemini), and Google Sheets.

Whenever a new email arrives, the system:
- Reads the email content  
- Uses AI to extract invoice details  
- Stores the structured data into a spreadsheet  

No manual data entry. No copy-pasting. Just clean, automated logging.

---

## 🏗️ Workflow Architecture

### 🔹 Main Components

- **Gmail Trigger**  
  Listens for incoming emails  

- **AI Processing (Google Gemini)**  
  Extracts:
  - Invoice ID  
  - Invoice Amount  

- **Google Sheets Node**  
  Appends extracted data into a spreadsheet  

---

## 🔄 Workflow Flow
``` mermaid 
flowchart TD
    A[📩 Gmail Trigger] --> B[📄 Extract Email Snippet]
    B --> C[🧠 Google Gemini AI Model]

    C --> D[🔍 Extract Invoice ID]
    C --> E[💰 Extract Price]

    D --> F[📦 Format JSON Output]
    E --> F

    F --> G[📊 Google Sheets]
    G --> H[✅ Append Invoice Data]

    subgraph Input
        A
        B
    end

    subgraph AI Processing
        C
        D
        E
        F
    end

    subgraph Output
        G
        H
    end
```

---
## 🔄 Workflow Visual


<p align="center">
  <img src="https://github.com/user-attachments/assets/aa5dee40-d02a-4d53-9062-04db4bfec372" alt="Workflow Diagram" width="800"/>
</p>

---
## 🧠 How It Works

### 1. Email Detection (Gmail)
- The workflow triggers automatically when a new email is received  
- It captures the email snippet (content preview)

---

### 2. AI Extraction
The AI model processes the email and extracts:

- Invoice ID  
- Price (numeric value)

It returns structured JSON like:
```json
{
  "invoice_id": "INV12345",
  "price": 4999
}
```
---
## 🛠️ Tech Stack

- **n8n** – Workflow automation  
- **Gmail API** – Email trigger  
- **Google Gemini (PaLM API)** – AI-based data extraction  
- **Google Sheets API** – Data storage  
- **OAuth2 Authentication**

---

## 🔐 Required Credentials

To run this workflow, configure the following in n8n:

- Gmail OAuth2 credentials  
- Google Gemini (PaLM API) API key  
- Google Sheets OAuth2 credentials  

---

## ✅ Features

- Automatic email monitoring  
- AI-based invoice data extraction  
- Structured JSON output parsing  
- Real-time Google Sheets updates  
- No manual data entry required  
- Lightweight and scalable workflow  
- Works with unstructured email content  

---

## 🎯 Use Cases

- Automated invoice tracking system  
- Expense and billing management  
- Email-to-database automation  
- AI-powered document data extraction  
- Portfolio project for automation + AI  
