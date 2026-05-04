# ZO-DIGI-004 — Digital Product Delivery SOP

---

## 1. Purpose

To ensure every digital product buyer receives their purchase reliably, immediately, and with a good first experience.

---

## 2. Scope

All ZeroOrigins digital products delivered via Gumroad or direct link.

---

## 3. Owner

Founder

---

## 4. Trigger

When a new digital product is ready to list, or if delivery issues are reported.

---

## 5. Delivery Methods by Product Type

| Product Type | Delivery Method |
|-------------|----------------|
| PDF / template / guide | Gumroad hosted file (auto-delivered) |
| Notion template | Gumroad delivers a PDF with the Notion duplicate link |
| n8n workflow JSON | Gumroad hosted file (ZIP) |
| Video course | Gumroad hosted video OR link to Loom/private YouTube |
| Done-with-you program | Gumroad delivers welcome PDF + Calendly link |

---

## 6. Delivery Setup Checklist (Per Product)

- [ ] File uploaded to Gumroad product page
- [ ] File is the correct version (check version number)
- [ ] Test purchase completed — confirm file downloads correctly
- [ ] Confirmation email text written and set (Gumroad → "Receipt" settings)
- [ ] Thank-you / welcome email set up in Brevo (triggered by Gumroad webhook or manual tag)
- [ ] Gumroad product page has clear "what you get" description

---

## 7. Welcome Email Template

Send immediately after purchase (triggered via Gumroad or email tool):

```
Subject: Your [Product Name] is ready

Hi [Name],

Thank you for picking up [Product Name].

Here's how to get started:
1. [Step 1 — e.g., Download the file from your Gumroad receipt]
2. [Step 2 — e.g., Duplicate the Notion template using the link inside]
3. [Step 3 — e.g., Read page 1 first — it explains how to use this]

If anything doesn't work, reply to this email.

— Naveen
ZeroOrigins
```

---

## 8. What the Delivery File Must Contain

Every digital product file must include:
- Cover page with product name and version number
- "How to use this" section (first page or first section)
- Contact email for support: naveen.naidu21@gmail.com
- ZeroOrigins branding (logo or name in footer)

---

## 9. Common Delivery Issues and Fixes

| Issue | Fix |
|-------|-----|
| Buyer says file didn't arrive | Ask them to check spam; resend via Gumroad admin |
| File won't open | Check file format; re-export as PDF; re-upload |
| Notion link not working | Check sharing settings — must be "Share to web" enabled |
| Wrong version delivered | Update Gumroad file immediately; email all buyers |

---

## 10. Quality Checklist

- [ ] Test download confirmed before going live
- [ ] Welcome email sends within 5 minutes of purchase
- [ ] File has version number on cover page
- [ ] "How to use" section exists

---

## 11. Approval Required

None — Founder manages directly.

---

## 12. Output

- Live Gumroad listing with working delivery
- Welcome email active

---

## 13. Storage Location

Google Drive → `Products / Digital / [ProductName] / Delivery /`

---

## 14. Risks / Mistakes to Avoid

- **Not test-purchasing before launch** — buyers will be first to discover broken delivery
- **No welcome email** — silence after purchase feels like a scam; always send something

---

## 15. Review Frequency

At launch and after any product update.
