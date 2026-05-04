# ZO-AUTO-006 — Client Demo SOP

---

## 1. Purpose

To demonstrate the completed workflow to the client in a way that builds confidence, confirms the solution works as expected, and gets approval for final delivery.

---

## 2. Scope

All client demos for automation workflows before final delivery.

---

## 3. Owner

Founder

---

## 4. Trigger

After testing is complete and passed (ZO-AUTO-005).

---

## 5. Step-by-Step Process

**Step 1: Prepare demo script (30 minutes before)**
- Open a Google Doc with the demo flow:
  1. Remind client of the problem they had
  2. Show the solution (run live)
  3. Walk through what happened behind the scenes
  4. Show the outputs (sheet, email, notification)
  5. Answer questions
  6. Confirm acceptance

**Step 2: Prepare demo data**
- Use realistic but non-sensitive test data
- Example: test lead named "Demo Lead" with your own email for notifications

**Step 3: Run the demo (30 minutes)**

Open: "Before I run it, let me remind you what we set out to solve: [their original problem]. Here's what the system now does automatically."

Show the trigger:
- Submit the test form / send the test data
- "I just submitted a test lead."

Show the processing:
- Open n8n and show the execution running in real time
- "Here you can see it's capturing the data, scoring it, and routing it."

Show the outputs:
- Open the Google Sheet: "The lead just appeared in your sheet."
- Open Gmail: "The notification email landed in your inbox."
- Show any other outputs

**Step 4: Explain what they're in control of**
- "You can edit this Google Sheet directly."
- "If you want to change the email template, it's just this one field."
- "I'll show you how to turn it on/off."

**Step 5: Ask for questions and feedback**
- "Does this match what you expected?"
- "Is there anything that doesn't look right?"
- "Any questions before we finalize?"

**Step 6: Confirm acceptance**
- Ask: "Are you happy to go live with this?"
- If yes: proceed to deployment (ZO-AUTO-007)
- If changes needed: document them, scope them, confirm if in scope or change request

---

## 6. Quality Checklist

- [ ] Demo script prepared
- [ ] Test data ready
- [ ] Workflow tested fresh (run one last test the morning of the demo)
- [ ] Screen share working before call starts
- [ ] All outputs checked and visible
- [ ] Client confirmed acceptance

---

## 7. Approval Required

Client verbal or written confirmation of acceptance during demo.

---

## 8. Output

- Accepted workflow ready for deployment
- Change requests noted (if any)

---

## 9. Storage Location

Demo recording (if recorded): Google Drive → `Clients / [ClientName] / Demo_Recording /`

---

## 10. Risks / Mistakes to Avoid

- **Live bugs during demo** — run a full test the morning of the demo
- **Not showing outputs** — clients need to see the end result (email, sheet, notification), not just the n8n workflow
- **Skipping the "what you control" explanation** — clients who don't understand the system call you for every small change

---

## 11. Review Frequency

Quarterly.
