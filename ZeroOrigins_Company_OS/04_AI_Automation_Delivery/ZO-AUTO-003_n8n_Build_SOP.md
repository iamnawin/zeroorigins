# ZO-AUTO-003 — n8n Build SOP

---

## 1. Purpose

To build n8n workflows correctly, efficiently, and in a way that is maintainable after delivery.

---

## 2. Scope

All n8n workflow builds for clients and internal ZeroOrigins products.

---

## 3. Owner

Founder

---

## 4. Trigger

After architecture is confirmed (ZO-AUTO-002).

---

## 5. Build Environment Setup

**Development workflow (before touching client's live environment):**
1. Build and test in a separate n8n instance (personal cloud or local Docker)
2. Only deploy to client's environment after full testing passes (ZO-AUTO-005)

**n8n Deployment Options:**
| Option | Best For |
|--------|---------|
| n8n Cloud | Client-managed, easiest setup |
| n8n self-hosted (Railway, Render) | Cost control, more flexibility |
| n8n self-hosted (Docker, VPS) | Full control, enterprise clients |

---

## 6. Build Standards

### Naming Conventions

**Workflow names:** `[Client]_[Purpose]_[Version]`
Example: `Acme_LeadCapture_v1`

**Node names:** Describe what the node does, not what type it is
- Good: `Append Lead to Hot Leads Sheet`
- Bad: `Google Sheets1`

**Sticky notes:** Add sticky note at start of workflow explaining:
- What it does (1 sentence)
- Trigger source
- Key logic branches

### Error Handling Standards

Every production workflow must have:
1. **Error workflow connected** — set in n8n Workflow Settings → "Error Workflow"
2. **Try/Catch structure** — for critical HTTP requests, wrap in error handler
3. **Failure notification** — send email or Slack alert to founder@zeroorigins.ai when workflow fails

### Performance Standards

- Avoid loops over large datasets — batch operations where possible
- Set `Batch Size` appropriately in Sheets and database nodes
- Add Wait nodes where APIs have rate limits (e.g., OpenAI: add 1-second wait between rows)
- Set timeout on HTTP Request nodes (default: 10 seconds)

---

## 7. Step-by-Step Build Process

**Step 1: Set up credentials first**
- Follow ZO-AUTO-004 for API key handling
- Test each credential with a simple test run before building the full workflow

**Step 2: Build the happy path**
- Build the main flow without conditions or error handling
- Run with sample data from requirements
- Confirm data flows through each node correctly

**Step 3: Add conditional logic**
- Implement IF/ELSE branches
- Test each branch with appropriate sample data

**Step 4: Add error handling**
- Connect error workflow
- Add failure notification node

**Step 5: Add sticky notes for documentation**
- One note at the start of workflow
- One note at each major section (trigger, processing, output)

**Step 6: Run full test**
- Follow ZO-AUTO-005 Testing SOP
- Fix all bugs before client demo

**Step 7: Export workflow JSON**
- Export as JSON file for backup
- Store in Google Drive: `Clients / [Client] / [Project] / 04_Build /`

---

## 8. Quality Checklist

- [ ] All nodes descriptively named
- [ ] Sticky notes explain workflow logic
- [ ] Happy path tested with real sample data
- [ ] All conditional branches tested
- [ ] Error workflow connected
- [ ] Failure notification configured
- [ ] Workflow JSON exported and backed up
- [ ] Performance: no unnecessarily slow operations

---

## 9. Approval Required

Founder reviews and approves before client demo.

---

## 10. Output

- Working n8n workflow (tested)
- Exported JSON backup
- Workflow documentation notes

---

## 11. Storage Location

Google Drive → `ZeroOrigins / Clients / [ClientName] / [ProjectName] / 04_Build /`

---

## 12. Risks / Mistakes to Avoid

- **Building without testing credentials** — if the API key is wrong, you'll waste 2 hours debugging
- **No error handling** — production workflows break; you need to know when they do
- **Unnamed nodes** — makes debugging impossible and handover confusing
- **Building directly in client environment** — always build and test in dev first

---

## 13. Review Frequency

Quarterly (update with new n8n features).
