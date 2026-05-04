# Onboarding Checklist — ZeroOrigins Workflow Starter Kit

Use this to confirm everything is working before you consider setup complete.
Check each item only after you've actually verified it.

---

## Accounts & Prerequisites

- [ ] n8n account created (cloud or self-hosted)
- [ ] Google account ready (Sheets + Gmail access)
- [ ] Form tool chosen and set up (Tally / Typeform / other)

---

## Google Sheet

- [ ] New Google Sheet created
- [ ] Sheet tab renamed to: **Leads**
- [ ] Row 1 headers added in correct order:
  `Timestamp | Name | Email | Business | Message | Source | Status | Followup Sent | Followup Date`
- [ ] Spreadsheet ID copied and saved somewhere

---

## Workflows Imported

- [ ] `lead_capture.json` imported into n8n
- [ ] `followup_flow.json` imported into n8n

---

## Credentials Connected

- [ ] Google Sheets credential created and connected (in both workflows)
- [ ] Gmail credential created and connected (in both workflows)
- [ ] Spreadsheet ID pasted into all Google Sheets nodes
- [ ] "Notify Owner" email address updated to YOUR email

---

## Email Copy Updated

- [ ] Confirmation email: name and booking link updated
- [ ] Follow-up email: name, email, and booking link updated

---

## Workflows Activated

- [ ] `lead_capture` workflow is **Active**
- [ ] Webhook Production URL copied
- [ ] `followup_flow` workflow is **Active**
- [ ] Schedule trigger timezone/time confirmed

---

## Form Connected

- [ ] Webhook URL pasted into form tool
- [ ] Field mapping confirmed (name, email, business, message)
- [ ] Form integration enabled/saved

---

## End-to-End Test

- [ ] Test form submission sent with real email address
- [ ] New row appeared in Google Sheet within 30 seconds
- [ ] Owner notification email received
- [ ] Confirmation email received at the submitted address
- [ ] No error messages in n8n Executions log

---

## All boxes checked?

Your system is live. You can start sending real traffic to your form.

---

**Need help with any step?**  
Email: hello@zeroorigins.in  
Book a call: https://calendly.com/zeroorigins
