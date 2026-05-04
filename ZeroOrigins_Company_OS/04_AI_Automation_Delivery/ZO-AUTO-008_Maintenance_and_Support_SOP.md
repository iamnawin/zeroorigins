# ZO-AUTO-008 — Maintenance and Support SOP

---

## 1. Purpose

To handle post-delivery support requests and maintain ongoing automation systems for retainer clients.

---

## 2. Scope

All post-delivery support: 30-day free bug fix window and ongoing paid retainer maintenance.

---

## 3. Owner

Founder

---

## 4. Support Tiers

| Tier | Response Time | Included In |
|------|--------------|-------------|
| Critical (workflow down) | Same day | All clients |
| High (wrong output, data not saving) | 24 hours | All clients |
| Medium (minor display issues) | 48 hours | Retainer clients |
| Low (new features, enhancements) | Quoted separately | Not included in support |

---

## 5. Step-by-Step Process

**When a support request comes in:**

**Step 1: Acknowledge within response time target**
"Got it — looking into this now."

**Step 2: Reproduce the issue**
- Ask client to share: exact steps, screenshot/video, what they expected vs. what happened
- Check n8n execution log for the failed run

**Step 3: Diagnose**
Common causes:
- API credential expired or revoked
- Third-party service down (check status pages)
- Input data format changed (client changed their form)
- n8n version update broke a node
- Rate limit hit

**Step 4: Fix**
- Fix in dev/test first if possible
- Document what the fix is
- Apply to production

**Step 5: Verify with client**
"Fixed — I've [description of fix]. Can you test and confirm?"

**Step 6: Document**
Add to project notes: what broke, why, how it was fixed.

---

## 6. Retainer Maintenance (Monthly)

For clients on retainer:
- [ ] Review n8n execution history at start of each month
- [ ] Check for any failed executions
- [ ] Check for rate limit warnings
- [ ] Check for API key expiry (Google tokens expire; refresh if needed)
- [ ] Send monthly status report: "Your workflow ran X times this month, all successful."

---

## 7. Quality Checklist

- [ ] Support requests responded to within SLA
- [ ] Root cause identified and documented
- [ ] Fix tested before applying to production
- [ ] Client confirmed fix
- [ ] Retainer clients get monthly health check

---

## 8. Approval Required

None for bug fixes. New feature requests require new proposal and payment.

---

## 9. Output

- Fixed workflow
- Documented issue and resolution

---

## 10. Storage Location

Google Drive → `Clients / [ClientName] / Support_Log /`

---

## 11. Risks / Mistakes to Avoid

- **Scope creep disguised as bug fixes** — "while you're in there, can you also add X?" is a feature request, not a bug fix. Quote it separately.
- **Not logging support issues** — patterns of the same issue = product problem worth fixing at source

---

## 12. Review Frequency

Monthly (review support log). Quarterly SOP review.
