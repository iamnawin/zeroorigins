# ZO-AUTO-007 — Deployment SOP

---

## 1. Purpose

To deploy automation workflows to the client's production environment correctly, safely, and with a complete handover.

---

## 2. Scope

All workflow deployments to client environments.

---

## 3. Owner

Founder

---

## 4. Trigger

After client demo approval (ZO-AUTO-006).

---

## 5. Step-by-Step Process

**Step 1: Pre-deployment checklist**
- [ ] All tests passed in dev environment
- [ ] Client has confirmed approval
- [ ] Final payment invoice raised
- [ ] Client has their own n8n account set up (or ZeroOrigins account if on retainer)
- [ ] All credentials are in client's n8n (not ZeroOrigins dev)

**Step 2: Export workflow from dev**
- In dev n8n: open workflow → Settings → Download
- Save JSON as: `[ClientName]_[WorkflowName]_v1.0.json`
- Store in Google Drive

**Step 3: Import to production**
- In client's n8n: go to Workflows → Import
- Upload the JSON file
- Verify all nodes loaded correctly

**Step 4: Configure credentials in production**
- Re-configure all credentials in production n8n using client's own accounts
- Follow ZO-AUTO-004 for credential handling
- Test each credential in production

**Step 5: Update webhook URLs (critical)**
- n8n webhook URLs are environment-specific
- If workflow uses webhook trigger: copy new production webhook URL
- Update all places that POST to this webhook (forms, CRMs, etc.)
- Test that webhooks fire correctly

**Step 6: Run production smoke test**
- Submit one real test record through the full flow in production
- Confirm all outputs (sheet, email, CRM) worked correctly
- Check n8n execution log for any errors

**Step 7: Enable workflow**
- Toggle workflow to "Active" in production n8n
- Confirm status is green/active

**Step 8: Send handover package to client**
Email with:
- Workflow documentation (what it does, when it runs, what it outputs)
- Credentials guide (what APIs are connected, who owns them)
- How to turn it on/off
- What to do if something breaks (see ZO-AUTO-008)
- n8n access instructions (how to view execution history)

**Step 9: Monitor for 24–48 hours**
- Check execution log the next morning
- Verify first real records processed successfully
- Notify client: "I checked this morning — your first [X] leads have been processed. Everything is working."

---

## 6. Quality Checklist

- [ ] Workflow JSON exported from dev
- [ ] Workflow imported to production n8n
- [ ] All credentials re-configured in production
- [ ] Webhook URLs updated everywhere they're referenced
- [ ] Production smoke test passed
- [ ] Workflow set to Active
- [ ] Handover package sent to client
- [ ] First 24h monitoring done

---

## 7. Approval Required

Client confirms they have received handover package.

---

## 8. Output

- Live workflow in client's n8n
- Handover package delivered
- 30-day support window started

---

## 9. Storage Location

Google Drive → `ZeroOrigins / Clients / [ClientName] / [ProjectName] / 06_Deployment /`

---

## 10. Risks / Mistakes to Avoid

- **Not updating webhook URLs** — most common deployment failure. Always update every webhook URL.
- **Using dev credentials in production** — client must own all credentials in their production environment
- **Not monitoring after go-live** — first few real records often reveal edge cases not in test data
- **Deploying without handover documentation** — clients who don't understand the system create support debt

---

## 11. Review Frequency

After each deployment. Quarterly SOP review.
