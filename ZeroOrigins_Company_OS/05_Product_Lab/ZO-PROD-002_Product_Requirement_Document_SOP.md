# ZO-PROD-002 — Product Requirement Document SOP

---

## 1. Purpose

To write a Product Requirement Document (PRD) before building any product so that scope is clear, build is focused, and there's no mid-build confusion.

---

## 2. Scope

All internal ZeroOrigins products.

---

## 3. Owner

Founder

---

## 4. Trigger

After product idea is validated (ZO-PROD-001).

---

## 5. PRD Template

```markdown
# Product Name — PRD v1.0

## 1. Problem
One sentence: what problem does this solve and for whom?

## 2. Target User
Who is this for? Be specific: "Solo founders running service businesses" not "everyone."

## 3. Core Use Cases (Max 3)
What are the 3 things a user should be able to do with this product?
1. [Use case 1]
2. [Use case 2]
3. [Use case 3]

## 4. What's NOT In v1 (Explicitly)
List features that are out of scope for the first version.

## 5. MVP Feature List
List every feature needed for v1. Mark priority: Must / Should / Could
| Feature | Priority | Notes |
|---------|---------|-------|
| [Feature] | Must | |

## 6. Success Metric
How will you know v1 is working?
- [Metric 1]: e.g., 10 users use it in first week
- [Metric 2]: e.g., average session time > 5 minutes

## 7. Tech Stack
What technologies will be used?

## 8. Estimated Build Time
Honest estimate in days.

## 9. Risks
What could go wrong?

## 10. Launch Plan
Where will you launch? When?
```

---

## 6. Step-by-Step Process

**Step 1:** Copy the PRD template above
**Step 2:** Fill every section — do not leave any blank
**Step 3:** Review the "Not In v1" section carefully — cut anything not essential
**Step 4:** Share with 1–2 trusted people for feedback
**Step 5:** Lock the PRD before starting build — changes after this require a new version

---

## 7. Quality Checklist

- [ ] Problem statement is one sentence
- [ ] "Not in v1" section explicitly written
- [ ] All Must features are truly essential (test: would the product be unusable without it?)
- [ ] Success metric is measurable
- [ ] Build estimate is realistic (multiply first estimate by 1.5 for buffer)

---

## 8. Approval Required

Founder sign-off before build.

---

## 9. Output

- Locked PRD document (v1.0)

---

## 10. Storage Location

Google Drive → `ZeroOrigins / Products / [ProductName] / PRD_v1.md`

---

## 11. Risks / Mistakes to Avoid

- **Too many "Must" features** — if everything is Must, nothing gets prioritized
- **Not defining success metric** — you won't know if the product is working
- **PRD that grows during build** — lock it; create v2.0 for next iteration

---

## 12. Review Frequency

Once per product before build. Create new version for major iterations.
