# Testing Notes

## Test Scenarios

1. Unread normal question email
   - Expected result: email is classified as QUESTION and a reply draft is created.

2. Urgent email
   - Expected result: email is classified as URGENT and a professional reply is drafted.

3. Feedback email
   - Expected result: email is classified as FEEDBACK and a polite response is drafted.

4. Spam email
   - Expected result: spam is detected and should not proceed to reply drafting.

5. Empty email body
   - Expected result: workflow should not fail and should still classify based on subject/from fields.

6. Ollama server offline
   - Expected result: workflow should fail safely and show an error in execution logs.

7. Invalid AI response
   - Expected result: workflow should be reviewed because classification may not match the expected categories.

## Recommended Improvements

- Add error handling for Ollama failures
- Add a human approval step before sending replies
- Log classification and draft history to Airtable, Google Sheets, or a database
- Add priority routing for urgent emails
- Add a confidence score field
- Add automatic read/unread handling after processing
