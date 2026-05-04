# IgnAIte — Demo Flow

## What To Demo

**Workflow: Lead Capture → Auto Follow-up**

This is the simplest flow to show. Every client immediately understands it.
Run this demo on every first call.

---

## The Flow (Step by Step)

### Step 1 — Lead Submits a Form
- Tool: Tally.so or Google Form or Typeform
- Lead fills in: Name, Phone, Email, Interest/Query
- This triggers a webhook to n8n instantly

### Step 2 — n8n Receives the Webhook
- n8n workflow activates the moment the form is submitted
- No delay, no manual check

### Step 3 — Lead Data Saved to Google Sheet
- Lead name, contact, query, timestamp saved automatically
- Status column set to: `New`
- Row added in under 2 seconds

### Step 4 — Auto Email Sent to Lead
- Subject: "We received your enquiry — here's what happens next"
- Body: Personalized with their name and query
- Sent from the business email via Gmail node

### Step 5 — Internal WhatsApp or Slack Alert Sent to Owner
- Message: "New lead from [Name] — [Phone] — [Query]"
- Owner sees it immediately on phone

### Step 6 — Follow-up Reminder Created
- n8n schedules a reminder for 24 hours later
- If lead status is still `New` in the sheet, owner gets another alert
- Message: "You haven't followed up with [Name] yet"

### Step 7 — Lead Tagged With Status
- After owner responds or updates, status changes in the sheet
- Options: `New` → `Contacted` → `Demo Booked` → `Closed` → `Lost`

---

## What To Show During The Demo Call

1. Open the Tally form — fill it in live on screen
2. Switch to n8n — show the workflow activate in real time
3. Switch to Google Sheet — show the row appear
4. Check email inbox — show the confirmation email arrive
5. Show the WhatsApp / Slack alert received
6. Show the 24-hour follow-up reminder set in the workflow

Total demo time: **8–12 minutes**

---

## What To Say During The Demo

> "Right now, every time someone enquires from you — this is what happens automatically. No manual work. No delays. No leads slipping through."

> "This same system can be connected to your existing form, your WhatsApp, your Gmail, and your spreadsheet. We just wire it up for you."

---

## Tools Needed To Run This Demo

| Tool          | Purpose                    | Cost      |
|---------------|----------------------------|-----------|
| Tally.so      | Form trigger               | Free      |
| n8n (cloud)   | Workflow automation        | Free tier |
| Google Sheets | Lead storage               | Free      |
| Gmail         | Auto email                 | Free      |
| Slack or WA   | Internal alert             | Free      |

---

## After The Demo

Ask the client:
1. "Do you currently have a system like this?"
2. "How many leads do you lose per week because of no follow-up?"
3. "What tools are you already using that we can connect to?"

Then map it to a package.
