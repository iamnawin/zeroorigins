# ZO-SEC-005 — Incident Response SOP

---

## 1. Purpose

To respond to security incidents (data breaches, account compromises, system outages) in a structured, time-bound way that minimizes damage and maintains client trust.

---

## 2. Scope

Any security incident affecting ZeroOrigins systems or client data.

---

## 3. Owner

Founder

---

## 4. Trigger

Any of the following:
- Unauthorized access detected on any account
- Suspicious login or password reset email received
- Client data found in wrong location
- n8n or other system sending unexpected outputs
- Phishing email clicked or credential submitted to a fake site

---

## 5. Incident Severity Levels

| Level | Definition | Examples | Response Time |
|-------|-----------|---------|---------------|
| Critical | Client data exposed or likely stolen | Data breach, credential theft, ransomware | Within 2 hours |
| High | ZeroOrigins system compromised | Account takeover, email hack | Within 4 hours |
| Medium | Potential vulnerability identified | Suspicious login attempt, phishing received | Within 24 hours |
| Low | No data affected, informational | Spam increase, odd bounce rate | Within 72 hours |

---

## 6. Incident Response Steps

**Step 1 — CONTAIN (do this first, before investigating)**
- Change all passwords related to the affected system
- Revoke all sessions and API keys
- If client systems are affected: cut access and notify client immediately
- Do not try to understand what happened first — contain it first

**Step 2 — ASSESS**
- What systems were accessed?
- What data was in those systems?
- How long was access possible? (Check audit logs)
- Is the threat still active or contained?

**Step 3 — NOTIFY**
- If client data was affected: call/email the client within 24 hours
- If personal data of Indian individuals: consult legal advisor on DPDPA reporting requirements (72-hour window to authorities)
- If financial data (payment credentials): notify the payment provider (Razorpay/Stripe)

**Step 4 — RECOVER**
- Restore access with new, secure credentials
- Verify all automation workflows are running correctly
- Confirm no data was altered (check recent workflow run logs)

**Step 5 — DOCUMENT**
- Write an incident report (see Section 7)
- Identify the root cause
- Update affected SOPs to prevent recurrence

---

## 7. Incident Report Template

```markdown
# Incident Report — [Date]

## Summary
[1–2 sentence description of what happened]

## Timeline
- [Time] — Incident detected / occurred
- [Time] — Containment steps taken
- [Time] — Client notified (if applicable)
- [Time] — Resolved

## Systems Affected
[List of tools, accounts, data]

## Data Affected
[Type of data, approximate number of records if known]

## Root Cause
[Why did this happen? Missing 2FA? Weak password? Phishing click?]

## Actions Taken
[What was done to contain and recover]

## Prevention
[What process or control is being added to prevent recurrence]

## Client Impact
[None / Notified / Remediation in progress]
```

---

## 8. Client Communication Template (Data Breach)

```
Subject: Important — Security Incident Affecting Your Project

Hi [Client Name],

I'm writing to inform you of a security incident that may have affected data from your project.

What happened: [Brief, factual description — 2–3 sentences]

What data may have been affected: [Type — e.g., "The lead list CSV shared on [date]"]

What we've done: [Containment steps taken]

What we're doing next: [Recovery steps]

I take data security seriously and am committed to full transparency. I'm available to speak by phone or call if you'd like to discuss.

I'm sorry for any concern this causes.

— Naveen
ZeroOrigins
[Phone number]
```

---

## 9. Quality Checklist

- [ ] Incident detected and contained within response time for its severity level
- [ ] Incident report written within 24 hours
- [ ] Client notified if their data was affected
- [ ] Root cause identified
- [ ] Prevention measure added

---

## 10. Approval Required

None — Founder acts immediately; inform clients and legal advisor as required.

---

## 11. Output

- Incident report in Drive
- Updated SOP or process to prevent recurrence
- Client notification sent if applicable

---

## 12. Storage Location

Google Drive → `Security / Incident_Reports / [Date]_[Brief_Description] /`

---

## 13. Risks / Mistakes to Avoid

- **Investigating before containing** — spending 30 minutes figuring out what happened while the attacker still has access; contain first, understand later
- **Not notifying the client** — silence when their data may be affected destroys trust permanently; transparency, even for uncomfortable news, maintains the relationship

---

## 14. Review Frequency

After every incident; review annually to check if response steps are still applicable.
