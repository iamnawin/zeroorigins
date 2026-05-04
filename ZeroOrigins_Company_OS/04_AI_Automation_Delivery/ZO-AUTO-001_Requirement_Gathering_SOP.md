# ZO-AUTO-001 — Requirement Gathering SOP

---

## 1. Purpose

To gather complete, unambiguous requirements before any automation build begins. Incomplete requirements are the #1 cause of rework, scope creep, and delayed delivery.

---

## 2. Scope

All custom automation builds for clients: n8n workflows, API integrations, AI-powered systems.

---

## 3. Owner

Founder

---

## 4. Trigger

After kickoff call (ZO-SALES-004) and before architecture design (ZO-AUTO-002).

---

## 5. The Requirements Framework

Every automation project needs answers to these categories:

### Category 1: Trigger

What starts this workflow?

- What is the event that kicks things off?
- Is it manual (someone clicks a button), scheduled (runs every day at 9am), or event-based (new form submission, new email, new payment)?
- Is there one trigger or multiple triggers?
- What should NOT trigger this workflow?

**Example questions to ask:**
- "Walk me through: right now, when does this process start? What is the exact first action?"
- "Is there anything that would cause this process NOT to run? Any exceptions?"

---

### Category 2: Data Inputs

What data does this workflow need to work?

- Where does the incoming data come from? (Form, spreadsheet, email, API, CRM, webhook)
- What fields/data points are needed?
- What format is the data in? (Text, JSON, CSV, email body)
- Is the data always structured or sometimes messy/incomplete?
- Are there required fields vs. optional fields?

**Ask:**
- "Can you show me an example of the actual data this process receives? A real record, or a sample?"
- "What happens if some of this information is missing?"

---

### Category 3: Processing / Logic

What decisions or transformations happen?

- Does any data need to be changed, formatted, or extracted?
- Are there conditions? (If X, then Y; else Z)
- Does it need to look up information from another system?
- Does it need to score, rank, or categorize anything?
- Does AI/LLM need to be involved? For what task exactly?
- How many branches can the process take?

**Ask:**
- "In the current manual process, what judgments or decisions does a human make?"
- "Are there any cases where you'd want the workflow to do something different?"

---

### Category 4: Outputs / Actions

What should the workflow do with the processed data?

- Send a notification? (Email, WhatsApp, Slack, SMS)
- Create a record? (Add row to sheet, create CRM entry, create a Notion page)
- Update a record? (Mark as contacted, change status)
- Trigger another system? (Webhook to another tool)
- Generate a document? (PDF, formatted email, report)
- Multiple outputs at once?

**Ask:**
- "At the end of this process, what should exist that doesn't exist today?"
- "Who needs to be notified, and through what channel?"

---

### Category 5: Tools and Integrations

What tools are involved?

- List every tool that needs to be connected
- Do they have APIs? (Most modern tools do)
- Are accounts already set up or do we need to create them?
- Are there any existing workflows we need to integrate with or not break?

**Common tools in ZeroOrigins builds:**
| Tool | Connection Method |
|------|------------------|
| Google Sheets | Google Sheets node in n8n |
| Gmail | Gmail node |
| WhatsApp | Twilio / WhatsApp Business API |
| Notion | Notion node |
| Airtable | Airtable node |
| Slack | Slack node |
| Calendly | Webhooks |
| Typeform / Tally | Webhooks |
| OpenAI | HTTP Request node or OpenAI node |
| Razorpay | Webhooks |
| HubSpot / Pipedrive | Native nodes |

**Ask:**
- "Do you have API access or admin access to all of these tools?"
- "Are there any tools you're planning to switch in the next 3 months?"

---

### Category 6: Volume and Scale

How much data and how often?

- How many records per day / per hour?
- Peak load times?
- Any records per month target?
- How many users will the system serve?

This affects: n8n plan choice, rate limit planning, error handling design.

---

### Category 7: Error Handling Expectations

What should happen when something goes wrong?

- Should workflow stop and alert someone?
- Should it retry?
- Should it skip the failed record and continue?
- Who should be notified of failures? (Email, Slack)
- Is there a fallback manual process?

---

### Category 8: Security and Access

Who can access what?

- Who in the client organization will interact with this system?
- Any data privacy requirements? (Customer PII, financial data, health data)
- Should any data be stored or just passed through?
- India data privacy note: if handling personal data of Indian users, Digital Personal Data Protection Act (DPDPA) 2023 compliance is relevant — consult legal if needed.

---

## 6. Step-by-Step Process

**Step 1:** After kickoff call, send the Requirement Gathering questionnaire (based on the 8 categories above)

**Step 2:** Schedule 45–60 min requirements call to walk through answers together

**Step 3:** During call, ask for examples:
- "Can you show me the form / sheet / email that starts this process?"
- "Can you share a sample data record?"

**Step 4:** Document all requirements in a structured format (use the template below)

**Step 5:** Send Requirements Document to client for confirmation:
> "Here's what I understood from our conversation. Please confirm this is correct before I start building."

**Step 6:** Wait for written confirmation before starting architecture or build.

---

## 7. Requirements Document Template

```
Project: [Client Name] — [Workflow Name]
Date: [Date]
Version: 1.0

TRIGGER: [Exact trigger description]
DATA INPUTS: [Source, fields, format]
PROCESSING LOGIC: [Decision rules, transformations, AI involvement]
OUTPUTS: [What gets created, sent, updated]
TOOLS CONNECTED: [List of tools + connection method]
VOLUME: [Records per day/week/month]
ERROR HANDLING: [What happens on failure]
SECURITY NOTES: [Data sensitivity, access controls]

CONFIRMED BY CLIENT: [Name + Date of email confirmation]
```

---

## 8. Quality Checklist

- [ ] All 8 categories documented
- [ ] Sample data collected for testing
- [ ] Tool access confirmed (API keys available)
- [ ] Volume estimates captured
- [ ] Error handling expectations noted
- [ ] Requirements document sent and confirmed by client in writing

---

## 9. Approval Required

Client written confirmation of requirements document before build begins.

---

## 10. Output

- Signed-off Requirements Document
- Sample data set for testing
- List of all tools and API credentials needed

---

## 11. Storage Location

Google Drive → `ZeroOrigins / Clients / [ClientName] / [ProjectName] / 01_Requirements /`

---

## 12. Risks / Mistakes to Avoid

- **Starting build without written confirmation** — clients forget what they agreed to verbally
- **Not asking for sample data** — assumptions about data format cause errors during testing
- **Missing edge cases** — always ask "what happens if [unusual thing]?"
- **No error handling spec** — every production workflow needs a defined failure mode

---

## 13. Review Frequency

After each project — update question bank with anything you wish you had asked. Quarterly SOP review.
