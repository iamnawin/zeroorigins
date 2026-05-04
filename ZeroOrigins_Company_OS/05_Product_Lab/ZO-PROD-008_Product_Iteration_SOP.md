# ZO-PROD-008 — Product Iteration SOP

---

## 1. Purpose

To define when and how to update, improve, or discontinue a product based on data and feedback.

---

## 2. Scope

All ZeroOrigins digital products and SaaS post-launch.

---

## 3. Owner

Founder

---

## 4. Trigger

After monthly feedback review (ZO-PROD-007) or when a critical bug is found.

---

## 5. When to Iterate vs. When to Kill

| Signal | Action |
|--------|--------|
| Sales stalled, positive feedback | Iterate — marketing problem, not product |
| Sales stalled, negative feedback | Iterate — product problem |
| Sales good, bugs reported | Patch immediately |
| Zero sales after 30 days of marketing | Kill or pivot |
| Sales good, users want more features | Plan v2 |

---

## 6. Versioning Rules

Use semantic versioning: `MAJOR.MINOR.PATCH`

| Version Type | What Changed | Example |
|-------------|--------------|---------|
| Patch (0.0.X) | Bug fix, typo, broken link | v1.0.1 |
| Minor (0.X.0) | New section, bonus added, UX improvement | v1.1.0 |
| Major (X.0.0) | Significant restructure, new core feature | v2.0.0 |

---

## 7. Iteration Process

**Step 1: Decide what to fix**
- Pick top 2 issues from feedback log (ZO-PROD-007)
- Only pick issues affecting more than 2 users OR a critical bug

**Step 2: Scope the fix**
- Write 2–3 lines on what you're changing and why
- Estimate time: Patch = same day, Minor = 1–3 days, Major = treat as new build

**Step 3: Build and test**
- Run QA checklist (ZO-PROD-005) on changed areas
- For digital products: send updated file to 2 early buyers for check

**Step 4: Release**
- Update version number in file name and product listing
- Send update email to all buyers (see template below)

**Step 5: Document**
- Add to changelog

---

## 8. Update Email Template

```
Subject: [Product Name] just got better — here's your update

Hi [Name],

I've updated [Product Name] based on feedback from early buyers.

What changed in v[X.X]:
- [Change 1]
- [Change 2]

Download the latest version here: [Link]

Thanks for helping make this better.

— Naveen
```

---

## 9. Changelog Format

Maintain a `CHANGELOG.md` inside each product folder:

```
## v1.1.0 — [Date]
### Added
- [New content or feature]
### Fixed
- [Bug or broken element]
### Changed
- [Modified section or flow]
```

---

## 10. When to Kill a Product

Kill if ALL three are true:
1. Less than 5 sales in 60 days of active marketing
2. Feedback shows the core use case doesn't resonate
3. You've tried at least 2 positioning/pricing changes

Archive (don't delete) — it may be repurposed later.

---

## 11. Quality Checklist

- [ ] Feedback reviewed before deciding on changes
- [ ] Version number updated
- [ ] QA completed on changes
- [ ] All buyers notified of update
- [ ] Changelog updated

---

## 12. Approval Required

Founder decision on version bump.

---

## 13. Output

- Updated product file or URL
- Changelog entry
- Buyer notification email sent

---

## 14. Storage Location

Google Drive → `Products / [ProductName] / Versions /`

---

## 15. Risks / Mistakes to Avoid

- **Iterating based on one person's feedback** — check if the issue is common before building
- **Never notifying buyers of updates** — buyers who get updates become loyal repeat customers

---

## 16. Review Frequency

Monthly.
