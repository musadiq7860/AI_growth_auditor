AI Growth Audit n8n Workflow
This repository contains the AI Growth Audit n8n workflow, an automated lead generation and consulting tool. It uses AI to analyze a business's core challenges and instantly provide a custom, 3-step growth strategy.

🚀 How It Works
The workflow follows a seamless path from lead capture to strategy delivery:

Lead Capture: A built-in n8n form collects the user's name, business email, website URL, and their biggest growth challenge.

Website Analysis: The workflow uses an HTTP request to scrape data from the provided company website.

AI Strategy Generation: Utilizing a Basic LLM Chain powered by Google Gemini, the system analyzes the business data and the user's specific challenge to generate a professional 3-step strategy.

CRM Update: The lead's information and the generated AI strategy are automatically appended to a Google Sheet ("AI Lead Generation CRM") for tracking.

Automated Response: The custom audit is sent directly to the user via a messaging node (e.g., WhatsApp or Email).

🛠️ Components
Form Trigger: "Get Your Free AI-Powered Growth Audit".

AI Model: Google Gemini (via LangChain integration).

Scraper: HTTP Request node for real-time website data collection.

Storage: Google Sheets for lead management.

📋 Prerequisites
To use this workflow, you will need:

An n8n instance (self-hosted or Cloud).

Google Gemini API credentials.

A Google Sheets document to act as your CRM.

(Optional) Messaging credentials for sending the final report.

⚙️ Installation
Download the AI Growth Audit.json file from this repository.

Open your n8n editor.

Click on the Workflow Menu (top right) and select Import from File.

Select the AI Growth Audit.json file.

Configure your credentials for:

Google Gemini (PaLM) API.

Google Sheets (Map the documentId to your own spreadsheet).

Activate the workflow.

📝 Configuration Note
The LLM is configured with strict formatting rules to ensure a professional output:

Exactly 3 steps.

No markdown symbols like asterisks.

Double line breaks between steps for readability.
