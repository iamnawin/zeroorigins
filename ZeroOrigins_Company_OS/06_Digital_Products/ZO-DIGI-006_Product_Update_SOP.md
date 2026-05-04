# ZO-DIGI-006 — Product Update SOP

---

## 1. Purpose

To update digital products when content becomes outdated, bugs are found, or a new version is released — and notify all buyers.

---

## 2. Scope

All ZeroOrigins digital products sold via Gumroad.

---

## 3. Owner

Founder

---

## 4. Trigger

- A tool or platform referenced in the product changes significantly
- A buyer reports something broken
- Monthly feedback review flags a common issue (ZO-PROD-007)
- A version upgrade is planned (ZO-PROD-008)

---

## 5. Update Types and Actions

| Update Type | Action |
|-------------|--------|
| Minor fix (typo, broken link) | Fix and re-upload silently; bump to PATCH version |
| Content update (new section, revised steps) | Re-upload; notify buyers via email; bump MINOR version |
| Major revision (restructure, new tools) | Treat as new product version; major email campaign |
| Tool shutdown (e.g., service discontinued) | Urgent fix required; email all buyers within 24 hours |

---

## 6. Update Process

**Step 1:** Make the fix in the source file (Google Docs, Notion, Figma, etc.)  
**Step 2:** Export as PDF or ZIP  
**Step 3:** Version the file: `ProductName_v1.1.pdf`  
**Step 4:** Upload to Gumroad (Product → Edit → Files → Replace)  
**Step 5:** Confirm the new file is downloadable (re-test)  
**Step 6:** Send buyer notification email (see template below)  
**Step 7:** Update changelog in product folder  

---

## 7. Buyer Notification Email Template

```
Subject: [Product Name] has been updated — v[X.X] is ready

Hi [Name],

I've just released an update to [Product Name].

What changed in v[X.X]:
- [Change 1 — e.g., "Updated the n8n setup steps for the new UI"]
- [Change 2 — e.g., "Added a troubleshooting section for common errors"]
- [Change 3 if applicable]

Download the latest version from your Gumroad purchase page:
[Gumroad library link]

As always, if you have questions, reply to this email.

— Naveen
ZeroOrigins
```

---

## 8. Gumroad Buyer Email Steps

1. Log into Gumroad
2. Go to Customers → filter by product
3. Export email list as CSV
4. Import to Brevo as a segment: `[ProductName] Buyers`
5. Send campaign from that segment only

---

## 9. Quality Checklist

- [ ] Updated file tested and downloadable
- [ ] Version number updated (filename and cover page)
- [ ] Changelog updated
- [ ] All buyers notified by email
- [ ] Gumroad product description updated if relevant

---

## 10. Approval Required

None — Founder manages directly.

---

## 11. Output

- Updated file live on Gumroad
- Buyer notification email sent
- Changelog updated

---

## 12. Storage Location

Google Drive → `Products / Digital / [ProductName] / Versions /`

---

## 13. Risks / Mistakes to Avoid

- **Uploading update without testing download** — the new file may be corrupted or incomplete
- **Not notifying buyers** — buyers who discover outdated content on their own leave bad reviews; proactive updates build loyalty

---

## 14. Review Frequency

After every update; quarterly audit of all products for outdated content.
