# ZO-SEC-003 — Client Data Handling SOP

---

## 1. Purpose

To define how ZeroOrigins receives, stores, uses, and deletes client data — protecting clients and ensuring ZeroOrigins stays compliant with India's Digital Personal Data Protection Act (DPDPA 2023) and international standards.

---

## 2. Scope

All client data received during project delivery: contact lists, business data, login credentials, API keys, customer records, or any data that belongs to the client.

---

## 3. Owner

Founder

---

## 4. Trigger

At the start of every client project, before any data is received.

---

## 5. Types of Client Data ZeroOrigins Handles

| Data Type | Examples | Risk Level |
|-----------|---------|------------|
| Business data | Revenue figures, sales data, pipeline | Medium |
| Contact lists | Lead lists, customer emails, phone numbers | High |
| Login credentials | Admin logins, API keys, OAuth tokens | High |
| Personal data | Names, emails, phone numbers of their customers | High |
| Financial data | Invoice data, payment records | High |
| Internal documents | SOPs, proposals, pricing | Medium |

---

## 6. Data Minimization Principle

**Only receive the data you actually need.**

Before accepting any data from a client:
1. Ask: "Do I need this specific data to complete the work?"
2. If no: do not accept it. Ask for a sample or anonymized version instead.
3. If yes: accept it with a clear agreement on how it will be used and deleted.

Example: If building a lead follow-up automation, you need the automation logic and field names — not the actual 5,000 leads in the CRM. Request test data (anonymized or a 10-row sample) for testing.

---

## 7. Data Receipt Protocol

When a client sends data:

**Step 1: Acknowledge receipt**
```
"Received. I'll use this only for [specific purpose] and delete it after delivery."
```

**Step 2: Store it correctly**
- Store in Google Drive in a **client-specific folder** with restricted access (not a shared folder)
- If credentials: store in 1Password/Bitwarden under a project-specific vault
- Never store data in personal email, WhatsApp files, or local downloads folder without backup

**Step 3: Document what you received**
- Log in the Client Data Register (see Section 9)

---

## 8. Data Storage Rules

| Rule | Requirement |
|------|-------------|
| Location | Google Drive (client folder) or password manager (credentials only) |
| Access | Founder only — no third-party access unless absolutely required |
| Encryption | Google Drive encrypts at rest — do not export to unencrypted local storage |
| Backup | Do not create unnecessary copies of client data |
| Sharing with subcontractors | Only with explicit client consent and an NDA with the subcontractor |

---

## 9. Client Data Register

Maintain a Google Sheet: `Client_Data_Register.xlsx`

| Client | Project | Data Type | Received Date | Purpose | Storage Location | Deletion Date |
|--------|---------|-----------|--------------|---------|-----------------|---------------|
| [Name] | [Project] | Lead list (CSV) | [Date] | Testing automation | Drive → /Clients/[Name]/ | On delivery |
| [Name] | [Project] | API keys | [Date] | Live automation access | 1Password | On offboarding |

---

## 10. Data Usage Rules

Client data may ONLY be used for:
- The specific project it was received for
- Nothing else

Client data may NOT be used to:
- Train AI models
- Build product examples (even anonymized, without consent)
- Share with any other party
- Reference in marketing or case studies (without explicit written consent)

---

## 11. DPDPA 2023 Compliance (India)

India's Digital Personal Data Protection Act 2023 applies when handling personal data of Indian individuals.

Key obligations for ZeroOrigins as a "Data Fiduciary" (when processing personal data on behalf of clients):

| Obligation | What to Do |
|-----------|-----------|
| Purpose limitation | Only use data for the stated purpose — document this |
| Data minimization | Don't collect more than needed — see Section 6 |
| Consent | Client must have consent from their data subjects before sharing with you |
| Retention limit | Delete data after the project purpose is fulfilled |
| Security safeguards | Use encrypted storage; control access |
| Breach notification | If data is compromised, notify the client within 72 hours |

**Consult a legal advisor** before handling personal data at scale (e.g., processing lists with 1,000+ records). DPDPA penalties are significant.

---

## 12. GDPR (For European Clients)

If working with clients whose end customers are in the EU:
- A Data Processing Agreement (DPA) is legally required
- Contact a legal advisor to prepare a standard DPA template before taking EU-data clients
- GDPR breach notification: 72 hours to the supervisory authority

---

## 13. Data Deletion Protocol

At project end (within 5 days of final delivery):

- [ ] Delete all client data files from Google Drive
- [ ] Remove client API keys and credentials from password manager
- [ ] Purge any test data from n8n workflow test history
- [ ] Confirm deletion in the Client Data Register (add "Deleted: [Date]")
- [ ] Send confirmation to client: "All data received during this project has been deleted from our systems."

**Exceptions:** If a retainer agreement is in place, data may be retained for the duration of the retainer — document this in the agreement.

---

## 14. Data Breach Response (Summary)

If client data is exposed, lost, or accessed without authorization:

1. Contain the breach immediately (revoke access, change credentials)
2. Notify the client within 24 hours (not 72 — be faster than legally required)
3. Document: what happened, when, what data, how many records
4. Consult a legal advisor on DPDPA reporting obligations
5. Improve the process to prevent recurrence (see ZO-SEC-005)

Full incident response in ZO-SEC-005.

---

## 15. Quality Checklist

- [ ] Client data register updated at project start
- [ ] Only minimum necessary data received
- [ ] Data stored in correct location (Drive or password manager)
- [ ] Data deleted within 5 days of project close
- [ ] Deletion confirmed in Client Data Register

---

## 16. Approval Required

Founder review before receiving any high-risk data (contact lists with 1,000+ records, financial data, health data).

---

## 17. Output

- Updated Client Data Register
- Deletion confirmation sent to client
- No client data retained beyond project close date

---

## 18. Storage Location

Google Drive → `Security / Client_Data_Register.xlsx`
Google Drive → `Clients / [ClientName] / Data /` (for project duration only)

---

## 19. Risks / Mistakes to Avoid

- **Storing credentials in WhatsApp or email** — messaging apps are not secure credential stores; a hacked phone or email exposes all client credentials
- **Not deleting data after project** — forgotten data is a liability; old client data sitting in Drive that you've forgotten about is a breach waiting to happen
- **Using client contact lists for your own outreach** — this violates the data purpose agreement and could expose ZeroOrigins to legal action
- **Receiving more data than needed** — "just in case" data collection violates DPDPA data minimization requirements; only accept what is needed for the specific project task

---

## 20. Review Frequency

At every project start and close. Full SOP review annually.
