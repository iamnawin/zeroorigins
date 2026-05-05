# ZO-TRKR-005 — Expense Tracker

**ID:** ZO-TRKR-005  
**Department:** Finance  
**Version:** 1.0  
**Owner:** Founder  

---

## Purpose

Record all business expenses monthly for accounting closure, GST input credit, and tax filing. Copy this structure into Google Sheets for live use.

---

## Sheet: Expense Tracker

### Columns

| Column | Description | Values / Format |
|--------|-------------|-----------------|
| Expense ID | Unique reference | ZO-EXP-2026-001 |
| Date | Date of expense | DD-MM-YYYY |
| Vendor / Payee | Who was paid | Text |
| Category | Expense category (see below) | Category |
| Description | What was purchased | Text |
| Amount | Amount paid | Rs / USD |
| Currency | Currency | INR / USD / Other |
| INR Equivalent | Converted to INR | Rs |
| Payment Method | How it was paid | UPI / Credit Card / Bank Transfer / Cash / Stripe / PayPal |
| GST Paid | GST included in amount | Rs or 0 |
| GST Claimable | Can claim as input credit | Yes / No |
| Receipt Available | Is a receipt saved? | Yes / No |
| Receipt Location | Where the receipt is stored | Google Drive link or folder path |
| Project / Vertical | Which project or vertical this is for | Client Project ID / ZeroOrigins / AIwithNoBrain / etc. |
| Notes | Any context | Text |

---

## Expense Categories

| Category | Examples |
|----------|----------|
| Software & Tools | n8n Cloud, Notion, Figma, Adobe, GitHub, Vercel, Supabase |
| Cloud & Hosting | AWS, GCP, DigitalOcean, Railway |
| AI & API Costs | OpenAI, Anthropic, ElevenLabs, Replicate, Kling |
| Domain & Website | Domain renewals, Webflow, hosting |
| Marketing & Ads | LinkedIn Ads, Meta Ads, Google Ads, sponsored posts |
| Design & Media | Canva Pro, stock photos, video tools |
| Legal & Compliance | CA fees, CS fees, MCA filings, trademark |
| Banking & Payments | Razorpay fees, Stripe fees, wire transfer charges |
| Office & Equipment | Hardware, peripherals, stationery |
| Travel | Client meetings, events, co-working |
| Contractors | Freelancers, developers, designers paid for specific work |
| Training & Learning | Courses, books, conferences |
| Miscellaneous | Anything that doesn't fit above |

---

## Monthly Totals Summary (add at bottom of sheet)

| Month | Total Expenses (INR) | GST Claimable | Net Expense |
|-------|----------------------|---------------|-------------|
| Jan 2026 | | | |
| Feb 2026 | | | |
| ... | | | |

---

## Receipt Storage Convention

Save receipts in Google Drive at:
`ZeroOrigins / Finance / Receipts / [YYYY-MM] / [Vendor]_[Date].[pdf/jpg]`

Example: `ZeroOrigins / Finance / Receipts / 2026-05 / OpenAI_2026-05-01.pdf`

---

*SOP reference: ZO-FIN-003_Expense_Tracking_SOP.md, ZO-FIN-005_Monthly_Accounting_Closure_SOP.md*  
*Version: 1.0 | Created: May 2026 | Owner: Founder, ZeroOrigins*
