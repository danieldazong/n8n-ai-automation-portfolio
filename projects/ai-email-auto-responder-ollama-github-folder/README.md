# AI Email Auto-Responder (Ollama)

## Overview

This n8n workflow checks unread emails on a recurring schedule, uses a local Ollama LLM to classify each email, filters spam, drafts a professional reply, and prepares the response for human review.

## Business Problem

Teams often lose time manually checking inboxes, identifying message priority, filtering spam, and writing repetitive replies. This slows down customer communication and increases the chance of missed or inconsistent responses.

## Solution

This workflow uses n8n and Ollama to create an AI-assisted email response system. It reads unread emails through IMAP, classifies the message category, filters spam, generates a helpful reply, and formats the draft for review before sending.

## Tools Used

- Filter Logic
- HTTP Request
- IMAP Email
- Llama 3
- Ollama
- Set Node / Data Mapping
- n8n
- n8n Schedule Trigger

## Tags

AI, Ollama, Email, Automation

## Workflow Steps

1. **Check Every 5 Minutes**
2. **Get Unread Emails (IMAP)**
3. **1. Classify Email (Ollama)**
4. **Filter Spam**
5. **2. Draft Reply (Ollama)**
6. **Prepare Draft for Review**

## Key Features

- Scheduled inbox checking every 5 minutes
- Reads unread emails through IMAP
- Uses Ollama locally for email classification
- Classifies emails into categories such as urgent, question, feedback, spam, or other
- Filters spam before drafting a reply
- Drafts professional email replies with AI
- Prepares structured output for human review
- Keeps AI processing local through Ollama

## Business Value

- Reduces manual inbox review time
- Helps teams respond faster to common emails
- Improves consistency in email communication
- Adds an AI review layer without automatically sending messages
- Can be adapted for customer support, internal operations, sales inquiries, and service businesses

## Security Notes

This public portfolio version removes or replaces credentials and sensitive values.

Do not upload:

- Real IMAP credentials
- Email passwords
- OAuth tokens
- Customer emails
- Private inbox data
- Production webhook URLs
- Real message content

## Required Setup

Before using this workflow in your own n8n instance, configure:

```text
OLLAMA_BASE_URL=http://localhost:11434
OLLAMA_MODEL=llama3:8b
IMAP_CREDENTIALS=your n8n IMAP credential
```

You also need Ollama running locally with the selected model installed.

## Screenshots

Add screenshots inside the `screenshots/` folder.

Recommended screenshots:

- Full n8n workflow canvas
- Schedule Trigger node
- IMAP unread email node
- Ollama classification HTTP request
- Spam filter logic
- Ollama draft reply node
- Prepared review output
- Successful execution result

## Demo

Add your Loom, YouTube, or portfolio video link here.

## Portfolio Positioning

This project demonstrates AI workflow automation, local LLM integration, email operations, conditional logic, and human-in-the-loop automation design.
