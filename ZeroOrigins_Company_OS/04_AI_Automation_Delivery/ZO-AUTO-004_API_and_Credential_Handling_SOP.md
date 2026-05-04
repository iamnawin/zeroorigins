# ZO-AUTO-004 — API and Credential Handling SOP

---

## 1. Purpose

To handle API keys, access tokens, and client credentials securely so that no credentials are lost, leaked, or misused — and so that ZeroOrigins maintains professional security practices.

---

## 2. Scope

All API keys, OAuth tokens, passwords, webhooks, and access credentials handled by ZeroOrigins: both our own and our clients'.

---

## 3. Owner

Founder

---

## 4. Trigger

When a new project starts, when a client shares credentials, or when a new tool is integrated.

---

## 5. Key Principles

1. **Never store credentials in n8n workflow JSON files** — n8n stores credentials separately. Exported workflow JSONs should never contain raw keys.
2. **Never store credentials in plain text files, Google Docs, or email** — use a password manager.
3. **Never share credentials via WhatsApp or SMS** — use secure channels only.
4. **Minimum access** — only request the permissions needed. Don't use admin API keys when a read-only key will do.
5. **Revoke after use** — if a credential was created for testing, revoke it after the project.

---

## 6. Tools for Credential Management

| Tool | Use |
|------|-----|
| 1Password (recommended) | Master password manager for all credentials |
| Bitwarden (free alternative) | Open-source, self-hostable |
| n8n Credentials panel | Store credentials within n8n (encrypted at rest) |
| Google Drive (for sharing) | Only for non-sensitive documents — NOT for credentials |

---

## 7. Step-by-Step Process

### Receiving Credentials from Clients

**Step 1: Request credentials via secure channel**
- Never ask for credentials over WhatsApp/SMS
- Ask via encrypted email or use a secure form
- Preferred method: ask client to add credentials directly in their n8n instance (ZeroOrigins never touches the raw key)
- If you must receive keys: use 1Password's share feature or a secure notes link

**Step 2: Receive and immediately store in 1Password**
- Create a 1Password entry named: `[Client Name] — [Tool Name] — [Purpose]`
- Example: `Acme Corp — OpenAI API — Lead Qualifier Workflow`
- Fields to save: API key, endpoint, any associated email/account, expiry date if applicable

**Step 3: Add to n8n credentials panel**
- Go to n8n → Credentials → New Credential
- Name it: `[Client] — [Service]` (e.g., "Acme — Gmail")
- Enter credentials
- Test connection before closing
- Do NOT export credentials — they stay in n8n

**Step 4: Do NOT store in workflow JSON**
- When exporting workflow JSON for backup, verify no raw credentials appear in the JSON
- n8n substitutes credential IDs, not values, in exports — verify this

**Step 5: Document what credentials are in use**
Add to project notes:
```
Credentials used in this project:
- Gmail: Acme's company Gmail (client configured directly)
- OpenAI: ZeroOrigins API key (revoke after project if client wants their own)
- Google Sheets: OAuth via Acme's Google account
- Webhook: n8n cloud webhook URL (changes with each deploy)
```

---

### Managing ZeroOrigins Own API Keys

**Step 1: Create service-specific API keys where possible**
- OpenAI: Create separate project key per client or per product
- AWS: Create IAM user with minimum permissions per use case
- Don't reuse one master key across everything

**Step 2: Set usage limits**
- OpenAI: set monthly spend limits per project key
- AWS: set billing alerts

**Step 3: Rotate keys periodically**
- Review and rotate long-lived API keys every 90 days
- Immediately rotate any key you suspect was exposed

**Step 4: Track all active keys**
Maintain a credential inventory in 1Password:
| Key Name | Service | Owner | Created | Last Rotated | Expiry |
|----------|---------|-------|---------|--------------|--------|
| ZO-OpenAI-Prod | OpenAI | ZeroOrigins | Jan 2026 | — | — |
| ZO-Gmail-Admin | Gmail | ZeroOrigins | Jan 2026 | — | — |

---

### Secure Transmission of Credentials

**Acceptable methods:**
- 1Password's secure sharing link (time-limited)
- Ask client to paste directly into n8n's credential panel during a screen share session
- Bitwarden send (time-limited encrypted link)

**Never acceptable:**
- WhatsApp, Telegram, SMS
- Plain email body
- Google Docs
- Slack (unless encrypted and self-hosted)
- Screenshots in email

---

### Project End / Client Offboarding

**Step 1:** Confirm client has all their own credentials
**Step 2:** Remove ZeroOrigins credentials from client's n8n if any were added
**Step 3:** Archive the credential record in 1Password (don't delete — needed for support reference)
**Step 4:** If ZeroOrigins API keys were used for a client project: revoke or reassign them

---

## 8. Quality Checklist

- [ ] All credentials stored in 1Password, never in plain text
- [ ] n8n credentials named clearly per client and service
- [ ] No raw API keys in exported workflow JSONs
- [ ] Usage limits set on OpenAI/cloud services
- [ ] Credential inventory log maintained
- [ ] Project-end credential cleanup completed
- [ ] Keys not older than 90 days without rotation

---

## 9. Approval Required

Founder reviews all credential access requests from collaborators.

---

## 10. Output

- Credential inventory in 1Password
- Secure project credentials in n8n
- Clean export JSONs (no embedded keys)

---

## 11. Storage Location

- Credentials: 1Password vault (not Google Drive)
- Credential inventory log: 1Password secure notes or encrypted sheet

---

## 12. Risks / Mistakes to Avoid

- **API keys in n8n workflow JSON exports** — check every export before sharing
- **One key for everything** — if one key is compromised, your entire operation is exposed
- **Not revoking after project** — accumulation of stale keys is a security risk
- **Receiving client credentials over WhatsApp** — creates liability. Always use secure channel.
- **Not setting spending limits on LLM APIs** — a runaway loop can generate massive API bills in minutes

---

## 13. Review Frequency

Quarterly (rotate keys, review inventory, check for unused credentials).
