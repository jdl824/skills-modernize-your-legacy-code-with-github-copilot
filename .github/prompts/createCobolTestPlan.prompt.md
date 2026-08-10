---
agent: 'agent'
model: gpt-4.1
description: 'Generate a comprehensive test plan for the COBOL accounting system and save it to docs/TESTPLAN.md'
---

Analyze the current COBOL accounting application in this repository and generate a complete Markdown test plan for its business logic.

The test plan should:

1. Cover the legacy app's current features and edge cases, including:
   - application startup and menu navigation
   - viewing the current balance
   - crediting funds and updating balance
   - debiting funds and rejecting overdrafts
   - handling invalid or non-numeric input
   - exiting the application cleanly
2. Use the following headings and store the output in `docs/TESTPLAN.md`:
   1. Test Case ID
   2. Test Case Description
   3. Pre-conditions
   4. Test Steps
   5. Expected Result
   6. Actual Result
   7. Status (Pass/Fail)
   8. Comments
3. Present the test plan as a Markdown table.
4. Focus on the current application behavior and business rules only; do not propose new features.
5. Keep each test case clear, actionable, and easy to validate.
