# Workflow Diagram

Replace this markdown file with a PNG diagram when ready.

```text
Airtable Order Created/Updated
        ↓
Check Order Status
        ↓
IF In Progress + Confirmation Email Sent = false
        ↓
OpenAI Generates Confirmation Email
        ↓
Gmail Sends Email
        ↓
Airtable Updates Confirmation Email Sent = true

IF Shipped + Shipping Email Sent = false
        ↓
OpenAI Generates Shipping Email
        ↓
Gmail Sends Email
        ↓
Airtable Updates Shipping Email Sent = true

IF Delivered + Delivery Email Sent = false
        ↓
OpenAI Generates Delivery Email
        ↓
Gmail Sends Email
        ↓
Airtable Updates Delivery Email Sent = true
```
