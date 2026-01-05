# AI Email Action Summary Automation (Mocked AI)

## Overview
This project is an automation workflow built with **n8n** that collects weekend emails and sends a summarized list of action items every Monday morning.

The workflow is designed to be **AI-ready**, with the AI analysis layer currently mocked due to API access limitations. The mock simulates structured LLM output and can be easily replaced with a real AI model.

---

## Problem
Managing emails received over the weekend can be overwhelming and often leads to missed tasks and delayed responses.

---

## Solution
An automated workflow that:
- Fetches weekend emails from Gmail
- Analyzes emails to extract action items (mocked AI)
- Sends a clean summary email every Monday morning

---

## Workflow
1. Monday Morning Trigger
2. Fetch weekend emails from Gmail
3. Mock AI analysis using a Code node
4. Send summarized action items via email

---

## Tech Stack
- n8n (workflow automation)
- Gmail API
- JavaScript (Code node)
- AI-ready architecture (mocked LLM output)

---

## AI Layer (Mocked)
The AI analysis step is simulated using a **Code node** that returns structured JSON similar to an LLM response.  
This approach allows:
- Testing without API dependency
- Clear data contracts
- Easy replacement with OpenAI or other LLMs in the future

---

## Sample AI Output (Mocked)
```json
{
  "summary": "You received important emails over the weekend.",
  "action_items": [
    { "task": "Reply to client about unpaid invoice", "priority": "High" },
    { "task": "Confirm meeting with design team", "priority": "Medium" },
    { "task": "Read newsletter from skate brand", "priority": "Low" }
  ]
}
