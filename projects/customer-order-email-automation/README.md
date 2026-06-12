# AI-Powered Customer Order Email Automation

## Overview

This workflow automates customer order confirmation, shipping updates, and delivery emails using Airtable, n8n, OpenAI, and Gmail.

## Business Problem

Small businesses often manually send order status emails, which creates delays, missed updates, inconsistent customer communication, and unnecessary admin work.

## Solution

The automation detects new or updated orders in Airtable, checks the order status, generates personalized email content with OpenAI, sends the email through Gmail, and updates Airtable to prevent duplicate messages.

## Tools Used

- n8n
- Airtable
- OpenAI
- Gmail
- JavaScript expressions
- Conditional logic

## Workflow Steps

1. Airtable detects a new or updated order.
2. n8n checks the order status.
3. IF nodes determine whether confirmation, shipping, or delivery email should be sent.
4. OpenAI generates a personalized customer email.
5. Gmail sends the email.
6. Airtable updates the correct email-sent field to prevent duplicates.

## Key Features

- Status-based email automation
- Duplicate email prevention
- AI-generated customer communication
- Airtable record updates
- Clear order lifecycle tracking

## Business Value

- Reduces manual email work
- Improves customer response speed
- Prevents missed order updates
- Creates consistent communication
- Can be adapted for ecommerce, logistics, booking, and service businesses

## Security Notes

All credentials, private URLs, customer data, and API keys have been removed or replaced with placeholders.

## Screenshots

Add screenshots inside the `screenshots/` folder.

Recommended screenshots:

- Full n8n workflow canvas
- Airtable table structure
- IF node logic
- OpenAI prompt node
- Gmail node configuration with sensitive data hidden
- Airtable update node
- Successful execution log
- Sample email output

## Demo

Add your Loom, YouTube, or portfolio video link here.
