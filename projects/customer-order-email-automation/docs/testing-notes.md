# Testing Notes

## Test Scenarios

1. New order is created with `Status = In Progress`
   - Expected result: confirmation email is sent once.

2. Order status changes to `Shipped`
   - Expected result: shipping email is sent once.

3. Order status changes to `Delivered`
   - Expected result: delivery email is sent once.

4. Email-sent field is already true
   - Expected result: no duplicate email is sent.

5. Missing customer email
   - Expected result: workflow should stop or route to manual review.

6. OpenAI returns invalid JSON
   - Expected result: workflow should handle the error safely.

## Notes

Use fake customer records during testing. Never test with real customer information in a public portfolio repository.
