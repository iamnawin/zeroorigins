# Setup Guide — ZeroOrigins Workflow Starter Kit

**Time required:** 30–60 minutes  
**Skill level:** Beginner-friendly — no coding required  
**Support:** hello@zeroorigins.in | https://calendly.com/zeroorigins

---

## Before You Start

You need three accounts set up before importing anything:

| Tool | Why you need it | Get it at |
|---|---|---|
| n8n | Runs your automations | n8n.io (free cloud tier available) |
| Google account | Sheets (lead tracker) + Gmail (emails) | google.com |
| Form tool | To collect leads on your site | tally.so (free) or any webhook-capable form |

All three have free tiers. You do not need to pay for any of them to run this kit.

---

## Step 1 — Create Your Google Sheet

1. Go to [sheets.google.com](https://sheets.google.com) and create a new blank spreadsheet.
2. Name it: **ZeroOrigins Leads** (or anything you prefer).
3. Click on **Sheet1** tab at the bottom and rename it to: **Leads**
4. In **row 1**, type each column header exactly as written (one per cell, starting from A1):

```
Timestamp | Name | Email | Business | Message | Source | Status | Followup Sent | Followup Date
```

5. Copy the Spreadsheet ID from the URL bar:
   - URL looks like: `docs.google.com/spreadsheets/d/[SPREADSHEET_ID]/edit`
   - The ID is the long string between `/d/` and `/edit`
   - Save it somewhere — you'll paste it into n8n shortly.

---

## Step 2 — Import Workflows into n8n

1. Log in to your n8n instance (cloud or self-hosted).
2. Click the **+** button to create a new workflow.
3. Click the three-dot menu (⋯) in the top right → **Import from file**.
4. Select `Workflows/lead_capture.json` from this kit.
5. The workflow will open. Do **not** activate it yet.
6. Repeat steps 2–5 for `Workflows/followup_flow.json`.

---

## Step 3 — Connect Google Sheets

Do this inside **both** workflows:

1. Click the **"Log Lead to Sheet"** node (in lead_capture) or **"Read Pending Leads"** node (in followup_flow).
2. Click **"Credential for Google Sheets"** → **Create new credential**.
3. Click **Sign in with Google** and authorise n8n to access your Google account.
4. After connecting, paste your **Spreadsheet ID** into the Spreadsheet ID field.
5. Make sure the Sheet Name field shows **Leads**.
6. Click Save.

---

## Step 4 — Connect Gmail

Do this inside **both** workflows:

1. Click any Gmail node (e.g., "Notify Owner" in lead_capture).
2. Click **"Credential for Gmail"** → **Create new credential**.
3. You can reuse the same Google credential you created for Sheets if it has Gmail scope.
4. In the **"Notify Owner"** node, update the **To** field with your own email address.
5. In both Gmail nodes, update the **Sender Name** from "ZeroOrigins" to your business name (optional).

---

## Step 5 — Personalise the Email Copy

Open each Gmail node and update:

**"Send Confirmation to Lead"** (in lead_capture):
- Update the booking link if you have a custom Calendly URL
- Update the sign-off name from "Naveen" to your name
- Update the email address in the signature

**"Send Follow-Up Email"** (in followup_flow):
- Same — update name, email, and booking link
- Personalise the message body if needed

---

## Step 6 — Activate the Lead Capture Workflow

1. Open the `lead_capture` workflow.
2. Click **Activate** (toggle at the top right of the canvas).
3. Click the **Webhook** node — you'll see the **Production URL** appear.
4. Copy that URL — this is your webhook endpoint.

The URL will look like:
```
https://your-n8n-instance.app.n8n.cloud/webhook/lead-capture
```

---

## Step 7 — Connect Your Form

In your form tool (Tally, Typeform, Google Forms with Apps Script, etc.):

1. Go to the form's **settings → integrations → webhook**.
2. Paste the webhook URL you copied.
3. Map your form fields to these field names (case-insensitive):
   - Full name → `name` or `full_name`
   - Email → `email`
   - Company/Business → `business` or `company`
   - Message/Question → `message`
4. Save and enable the integration.

---

## Step 8 — Activate the Follow-Up Workflow

1. Open the `followup_flow` workflow.
2. Check the **Schedule Trigger** node — default is daily at 9:00 AM UTC.
   - Adjust the cron expression if needed (e.g., `0 9 * * *` = 9AM every day).
3. Click **Activate**.

---

## Step 9 — Test the Full System

1. Open your form and submit a test entry using your own email.
2. Within 30 seconds, check:
   - Your Google Sheet — a new row should appear with your test data.
   - Your inbox — you should receive the owner notification email.
   - The email you submitted — you should receive the confirmation email.
3. If all three work, your system is live.

---

## Troubleshooting

**No data in Google Sheet:**
- Check the Google Sheets credential is properly connected
- Confirm the Sheet name is exactly "Leads" (case-sensitive)
- Check n8n execution log — click the workflow → Executions tab

**Email not received:**
- Check Gmail credential is authorised
- Check spam folder
- In the workflow execution log, click the Gmail node to see the response

**Webhook not receiving data:**
- Make sure the workflow is **active** (not just saved)
- Check that you're using the **Production URL**, not the Test URL
- Confirm your form tool is sending a POST request (not GET)

---

## What's Next

Once this is running, you can extend it:
- Add Slack or WhatsApp notifications for new leads
- Connect to a CRM (HubSpot, Notion, Airtable)
- Add lead scoring logic based on business size or message keywords
- Build a multi-step nurture sequence instead of one follow-up

To build any of these, book a setup call:
**https://calendly.com/zeroorigins**

---

*ZeroOrigins AI — hello@zeroorigins.in*
