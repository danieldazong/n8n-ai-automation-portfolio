# Workflow Breakdown

## Trigger

The workflow begins with a schedule trigger that checks for new unread emails every 5 minutes.

## Email Retrieval

The IMAP node retrieves unread emails from the connected inbox.

## Classification

The first Ollama HTTP Request node sends the email content to a local LLM and asks it to classify the email into one category:

- URGENT
- QUESTION
- FEEDBACK
- SPAM
- OTHER

## Spam Filtering

The Filter node checks the classification output and controls whether the workflow should continue.

## Reply Drafting

The second Ollama HTTP Request node generates a professional and concise email reply.

## Review Preparation

The Set node prepares the final structured output with:

- Draft reply
- Original sender
- Reply subject
- Email category

## Workflow Connections

- Check Every 5 Minutes → Get Unread Emails (IMAP)
- Get Unread Emails (IMAP) → 1. Classify Email (Ollama)
- 1. Classify Email (Ollama) → Filter Spam
- Filter Spam → 2. Draft Reply (Ollama)
- 2. Draft Reply (Ollama) → Prepare Draft for Review
