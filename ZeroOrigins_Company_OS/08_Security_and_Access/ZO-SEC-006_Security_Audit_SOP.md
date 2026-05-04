# ZO-SEC-006 — Security Audit SOP

---

## 1. Purpose

To run a quarterly review of all ZeroOrigins security practices — catching gaps before they become incidents.

---

## 2. Scope

All ZeroOrigins systems, accounts, credentials, and data handling practices.

---

## 3. Owner

Founder

---

## 4. Trigger

Quarterly — January, April, July, October. Also run after any security incident.

---

## 5. Quarterly Security Audit Checklist

Set aside 2 hours each quarter. Go through each section:

### 5.1 Account Security

- [ ] Password manager health check — any weak or reused passwords? Fix now.
- [ ] 2FA enabled on all critical accounts (Google, GitHub, payment, cloud)?
- [ ] Any unused accounts that should be deleted?
- [ ] Any accounts shared with contractors who have since left?

### 5.2 Credential Inventory

- [ ] Open Access Log (ZO-SEC-004) — any credentials outstanding for closed projects?
- [ ] Any client API keys still active that should have been revoked?
- [ ] Any old API keys in n8n for workflows that are no longer active?

### 5.3 Device Security

- [ ] Disk encryption enabled on all devices?
- [ ] All devices have current OS and software updates applied?
- [ ] VPN installed and functioning?
- [ ] Any devices added in the last quarter that need security baseline (ZO-SEC-002)?

### 5.4 Data Handling

- [ ] Client Data Register (ZO-SEC-003) — any data that should have been deleted that hasn't been?
- [ ] Any client folders in Drive that are no longer needed?
- [ ] Check Google Drive sharing settings — any files shared publicly by accident?

### 5.5 n8n and Automation Security

- [ ] No API keys or passwords hardcoded in any workflow? (Check with "Search" in n8n)
- [ ] All credentials stored in n8n Credentials panel (not in node fields directly)?
- [ ] Error workflows active and logging failures?
- [ ] Webhook URLs changed if they were shared unnecessarily?

### 5.6 Third-Party Services

- [ ] Review list of all SaaS tools actively used — any that can be cancelled?
- [ ] Check OAuth authorizations on Google account — revoke any unknown apps
- [ ] Any trial accounts that converted to paid without your knowledge?

---

## 6. Audit Report Format

After completing the checklist, write a 1-page summary:

```markdown
# Security Audit — [Quarter] [Year]

Date: [Date]
Auditor: Naveen (Founder)

## Summary
[1–2 sentences on overall security posture]

## Issues Found
| Issue | Severity | Status |
|-------|----------|--------|
| [Issue 1] | High | Fixed |
| [Issue 2] | Medium | In Progress |

## Actions Taken
[List of fixes made during or after the audit]

## No Issues Found In
[Areas that checked out clean]

## Next Audit Date
[Date of next quarterly audit]
```

---

## 7. Quality Checklist

- [ ] Audit completed within the first week of January, April, July, October
- [ ] All High issues resolved within 48 hours of discovery
- [ ] Audit report written and saved
- [ ] Calendar reminder set for next quarter's audit

---

## 8. Approval Required

None — Founder manages directly.

---

## 9. Output

- Quarterly Security Audit Report (Google Drive)
- All found issues resolved or logged with a fix timeline

---

## 10. Storage Location

Google Drive → `Security / Audit_Reports / Q[X]_[Year]_Security_Audit.md`

---

## 11. Risks / Mistakes to Avoid

- **Skipping the audit when nothing seems wrong** — incidents are usually discovered during audits, not in real time
- **Logging issues but not fixing them** — an audit with unresolved issues is worse than no audit (you now know about the risk and did nothing)

---

## 12. Review Frequency

Quarterly (this SOP itself reviewed annually).
