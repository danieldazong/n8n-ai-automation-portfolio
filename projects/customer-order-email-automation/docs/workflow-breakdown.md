# Workflow Breakdown

## Trigger

The workflow begins when an Airtable order record is created or updated.

## Status Checks

The workflow checks the order status and email-sent tracking fields.

Example status fields:

- In Progress
- Shipped
- Delivered
- Cancelled

Example tracking fields:

- Confirmation Email Sent
- Shipping Email Sent
- Delivery Email Sent

## AI Email Generation

OpenAI generates a clear and personalized customer email based on the order details.

The AI output should return structured JSON, for example:

```json
{
  "subject": "Your order has been received",
  "message": "Hi Sarah, thank you for your order..."
}
```

## Email Delivery

Gmail sends the generated message to the customer.

## Record Update

Airtable is updated after the email is sent to prevent duplicate messages.
