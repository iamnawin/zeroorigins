# ZO-PROD-003 — Prototype Build SOP

---

## 1. Purpose

To build working prototypes quickly for validation, investor demos, or internal testing without over-engineering.

---

## 2. Scope

All product prototypes before full build.

---

## 3. Owner

Founder

---

## 4. Trigger

After PRD is locked (ZO-PROD-002).

---

## 5. Prototype Philosophy

A prototype should answer one question: "Does this idea work in practice?"

It does NOT need to:
- Handle edge cases
- Scale to 1000 users
- Look pixel-perfect
- Have authentication unless that's the core feature

It DOES need to:
- Demonstrate the core user flow
- Be testable by a real user
- Work enough to get meaningful feedback

---

## 6. Prototype Toolstack for ZeroOrigins

| Type | Tools |
|------|-------|
| UI / Clickable mock | Framer, Figma prototype mode |
| Web app (fast) | Bolt.new, Replit, Lovable.dev |
| n8n workflow | n8n cloud (test mode) |
| Landing page | Framer, Carrd, Typedream |
| AI product | Claude API + simple Node/Python wrapper |
| Data product | Google Sheets + Zapier/n8n + simple frontend |

---

## 7. Step-by-Step Process

**Step 1: Build only the core feature**
- Open PRD — implement only the "Must" features
- Skip auth, settings, admin panel for now

**Step 2: Time-box the build**
- Set a deadline: max 3–5 days for a prototype
- If you can't finish the core in 5 days, the scope is too big — cut it

**Step 3: Test internally**
- Use the prototype yourself for 30 minutes
- Note: what's confusing, what broke, what feels good

**Step 4: Get 3 external testers**
- Share with 3 potential users (not friends who'll say it's great)
- Ask: "Can you try to [core task] and tell me what happens?"
- Watch them struggle — don't explain anything

**Step 5: Document learnings**
- What worked?
- What didn't?
- What questions came up that you didn't anticipate?

**Step 6: Go/Iterate/Pivot decision**
- Go: feedback is positive, core flow works → move to full build
- Iterate: core works but needs refinement → build v2 prototype
- Pivot: core assumption was wrong → back to validation

---

## 8. Quality Checklist

- [ ] Core user flow is demonstrable end-to-end
- [ ] Built within time box (3–5 days)
- [ ] Tested by 3+ external users
- [ ] Learnings documented
- [ ] Go/Iterate/Pivot decision made

---

## 9. Output

- Working prototype
- Prototype test notes

---

## 10. Storage Location

Google Drive → `ZeroOrigins / Products / [ProductName] / Prototype /`

---

## 11. Risks / Mistakes to Avoid

- **Over-polishing prototype** — it's a test, not a product; don't spend 2 weeks making it pretty
- **Testing only with friends** — they'll say it's great to be supportive; test with strangers who have the actual problem

---

## 12. Review Frequency

Per product build.
