# ZO-TRKR-002 — Invoice Tracker

**ID:** ZO-TRKR-002  
**Department:** Finance  
**Version:** 1.0  
**Owner:** Founder  

---

## Purpose

Track all invoices raised — status, due dates, and payment confirmations. Copy this structure into Google Sheets for live use.

---

## Sheet: Invoice Tracker

### Columns

| Column | Description | Values / Format |
|--------|-------------|-----------------|
| Invoice ID | Invoice number | ZO-INV-2026-001, 002... |
| Date Issued | Date invoice was sent | DD-MM-YYYY |
| Client Name | Full name or company | Text |
| Client Email | Billing email address | Email |
| Project / Service | What the invoice is for | Text |
| Invoice Amount | Total amount billed | Rs / USD |
| Currency | Currency of invoice | INR / USD / AED / AUD |
| GST Amount | GST charged (if applicable) | Rs or 0 |
| Total with GST | Amount including GST | Rs |
| Payment Due Date | When payment is expected | DD-MM-YYYY |
| Payment Method | How client will pay | Razorpay / Stripe / Bank Transfer / UPI / Other |
| Status | Current payment status | Sent / Viewed / Partial / Paid / Overdue / Disputed / Cancelled |
| Payment Received Date | Date money arrived in account | DD-MM-YYYY |
| Amount Received | Actual amount received | Rs / USD |
| Outstanding | Amount still unpaid | Auto-calculated |
| Receipt Sent | Acknowledgement sent to client | Yes / No |
| Notes | Payment refs, disputes, delays | Text |

---

## Status Definitions

| Status | Meaning |
|--------|---------|
| Sent | Invoice emailed, awaiting action |
| Viewed | Client confirmed they received it |
| Partial | Part payment received |
| Paid | Full amount received and confirmed |
| Overdue | Past due date, follow-up required |
| Disputed | Client raised a query or dispute |
| Cancelled | Invoice voided (project cancelled, scope change) |

---

## Monthly Reconciliation Checklist

Run at the end of each month (see ZO-FIN-005):
- [ ] All invoices for the month entered in tracker
- [ ] All Paid invoices cross-checked against bank statement
- [ ] All Overdue invoices followed up (send reminder, log date)
- [ ] GST amounts totalled for filing
- [ ] AR (Accounts Receivable) total calculated = sum of Sent + Overdue invoices
- [ ] Month's revenue total = sum of Amount Received in the month

---

## Invoice Numbering

Format: `ZO-INV-[YEAR]-[SEQ]`

Examples:
- `ZO-INV-2026-001` — first invoice in 2026
- `ZO-INV-2026-012` — twelfth invoice in 2026

Reset sequence each calendar year.

---

## Follow-up Schedule for Overdue Invoices

| Days Overdue | Action |
|--------------|--------|
| 1–3 days | Friendly reminder email |
| 4–7 days | WhatsApp or phone follow-up |
| 8–14 days | Formal reminder with late payment notice |
| 15+ days | Escalate — consider pausing deliverables |

---

*SOP reference: ZO-FIN-002_Payment_Collection_SOP.md*  
*Version: 1.0 | Created: May 2026 | Owner: Founder, ZeroOrigins*
