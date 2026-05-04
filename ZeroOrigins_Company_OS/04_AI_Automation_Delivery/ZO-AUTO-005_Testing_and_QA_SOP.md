# ZO-AUTO-005 — Testing and QA SOP

---

## 1. Purpose

To systematically test every automation workflow before client delivery so that bugs are caught in development, not in production.

---

## 2. Scope

All n8n workflows: custom client builds and internal ZeroOrigins products.

---

## 3. Owner

Founder

---

## 4. Trigger

After build is complete (ZO-AUTO-003) and before client demo (ZO-AUTO-006).

---

## 5. Testing Levels

| Level | What It Tests | When |
|-------|--------------|------|
| Unit Test | Each node individually | During build |
| Integration Test | End-to-end with real tools | After build complete |
| Edge Case Test | Unusual or bad input data | After integration test |
| Load Test | Multiple records at once | For high-volume workflows |
| User Acceptance Test (UAT) | Client tests in their environment | Before final delivery |

---

## 6. Test Data Preparation

Before testing, prepare:
1. **Happy path data** — perfect, complete records that should process successfully
2. **Edge case data** — see list below
3. **Real data samples** — use actual data client provided (anonymized for testing)

**Common edge cases for automation workflows:**

| Scenario | Test Data |
|----------|-----------|
| Empty/blank required field | Record with empty name, email, or phone |
| Special characters | Name: "O'Brien & Associates" |
| International phone format | +1-555-555-5555 vs 9876543210 |
| Very long text | 1000-character message body |
| Duplicate record | Same email submitted twice |
| Invalid email format | "not-an-email" |
| Number as text | "Rs. 50,000" instead of 50000 |
| Null/undefined value | Field exists but is null |
| Rate limit trigger | 100 records in rapid succession |

---

## 7. Step-by-Step Testing Process

### Step 1: Unit Test Each Node

For each node in the workflow:
- [ ] Run node with sample input data
- [ ] Verify output data is correct format
- [ ] Check that the node is NOT generating errors

### Step 2: Integration Test — Happy Path

- [ ] Run the full workflow end-to-end with complete, correct data
- [ ] Verify every integration worked:
  - [ ] Google Sheet row created correctly
  - [ ] Email sent to correct address with correct content
  - [ ] CRM updated correctly
  - [ ] Webhook fired correctly
- [ ] Check all outputs (every place data should land)
- [ ] Time the workflow run — note average execution time

### Step 3: Integration Test — Edge Cases

For each edge case in your list:
- [ ] Run the workflow with that input
- [ ] Document what happened
- [ ] Fix any unhandled edge cases
- [ ] Re-test after fix

### Step 4: Error Handling Test

- [ ] Simulate a broken API connection (use wrong API key temporarily)
- [ ] Verify error workflow fires
- [ ] Verify notification is sent to correct channel
- [ ] Restore correct credentials and verify normal flow resumes

### Step 5: Load Test (For High-Volume Workflows)

- [ ] Submit 50–100 records at once
- [ ] Verify all records processed (no silent drops)
- [ ] Check for rate limit errors
- [ ] Check execution time under load

### Step 6: Document Test Results

Use this format:
```
Test Run: [Date]
Workflow: [Name]
Tester: [Founder]

Test 1: Happy Path — PASS
Test 2: Empty email — HANDLED (skips record, logs to error sheet)
Test 3: Duplicate record — FAIL — duplicate CRM entry created
Fix applied: Added deduplication check on email field
Re-test: PASS

Known Limitations:
- Workflow does not handle records with both email AND phone blank (rare, acceptable)

Overall: READY FOR CLIENT DEMO
```

### Step 7: UAT — Client Testing

After internal tests pass:
- [ ] Deploy to client's environment
- [ ] Send client 3–5 test records to submit
- [ ] Ask client to verify outputs on their end
- [ ] Fix any issues raised by client
- [ ] Confirm: "Are you happy with how this is working?"

---

## 8. Quality Checklist

- [ ] All nodes unit tested
- [ ] Happy path integration test passed
- [ ] All edge cases tested
- [ ] Error handling verified
- [ ] Load test run (if applicable)
- [ ] Test results documented
- [ ] UAT passed by client

---

## 9. Approval Required

Founder sign-off on test results before demo. Client sign-off after UAT.

---

## 10. Output

- Test results document
- List of known limitations (if any)
- Confirmed "Ready for delivery" status

---

## 11. Storage Location

Google Drive → `ZeroOrigins / Clients / [ClientName] / [ProjectName] / 05_Testing /`

---

## 12. Risks / Mistakes to Avoid

- **Testing only the happy path** — production always throws edge cases
- **Skipping UAT** — clients sometimes have different expectations from what you built; UAT catches this before final payment
- **Not documenting test results** — if something breaks post-delivery, documented tests prove what was verified
- **Testing in production environment** — test in dev/sandbox; production failures are visible to real users
- **Not testing error handling** — a workflow with no error handling that fails silently is worse than no workflow at all

---

## 13. Review Frequency

After each project. Update edge case library with new scenarios discovered. Quarterly SOP review.
