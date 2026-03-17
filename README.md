# AI Growth Audit
This repository contains an n8n workflow designed to automate lead generation by providing instant, AI-driven business audits. It captures lead information through a form, scrapes their website, and uses an LLM to generate a customized 3-step growth strategy.
 
## How It Works
The workflow automates the following steps:

 Lead Capture: A public-facing n8n form collects the user's name, business email, website URL, and their primary growth bottleneck.

 Website Scraping: The workflow performs an HTTP request to the provided URL to gather context about the business.

 AI Analysis: A Basic LLM Chain (using Google Gemini) processes the website data and the user's specific challenge.

 Strategy Generation: The AI generates a professional, 3-step actionable growth strategy tailored to the lead's needs.

 CRM Integration: Lead details and the generated strategy are automatically appended to a Google Sheet (acting as a CRM).

 Instant Delivery: The strategy is sent directly to the user (via Messaging/Email nodes).

## Features
 Automated Lead Magnet: Provides immediate value to potential clients.

AI-Powered Insights: Uses Google Gemini for high-quality, contextual advice.

Zero-Manual Entry: Automatically populates your CRM with qualified lead data.

Customizable: Easily swap the LLM or the CRM destination (e.g., Airtable, HubSpot).

## Prerequisites
n8n (Cloud or self-hosted)

Google Gemini API Key (for the AI analysis)

Google Sheets API (for the CRM component)

## Installation
Download the AI Growth Audit.json file.

In your n8n dashboard, create a new workflow.

Click the menu (three dots) and select Import from File.

Select the AI Growth Audit.json file.

Configure the credentials for the following nodes:

Google Gemini (PaLM) API: For the LLM nodes.

Google Sheets: For the "Append row in sheet" node.

Update the Spreadsheet ID in the Google Sheets node to match your own sheet.

Activate the workflow.

## Usage
Once activated, n8n will provide a Form URL. You can share this link directly with leads or embed it on your website. When a user submits the form, the automation triggers instantly.

## Node Structure
Form Trigger: "Get Your Free AI-Powered Growth Audit"

Wait Node: Ensures stability between triggers and requests.

HTTP Request: Scrapes the lead's website content.

Basic LLM Chain: The brain of the operation, using LangChain.

Merge Node: Combines user inputs with AI outputs.

Google Sheets Node: Logs all data for follow-up.
