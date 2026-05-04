# ZO-FIN-001 — Invoice Creation SOP

---

## 1. Purpose

To ensure every ZeroOrigins invoice is legally compliant (GST-compliant), professionally presented, correctly numbered, and sent on time so that payment collection is smooth and our books stay clean.

---

## 2. Scope

Applies to all client invoices: domestic (India) and international (export of services). Applies to both service billing and digital product billing.

---

## 3. Owner

Founder

---

## 4. Trigger

- On project completion or milestone completion
- On monthly retainer cycle (raise on 1st of each month)
- On sale of a digital product (can be auto-generated via Gumroad)
- Immediately after written confirmation of work scope

---

## 5. Inputs Required

- Client's legal name and billing address
- Client's GSTIN (for Indian B2B clients)
- Agreed scope and price
- Invoice number (next in sequence)
- Your company's GSTIN, bank account details, PAN
- Service description and SAC code

---

## 6. Mandatory Fields on Every Invoice

### For Indian B2B Clients (GST Invoice)

| Field | Details |
|-------|---------|
| Invoice Number | Sequential — e.g., ZO-INV-2026-001 |
| Invoice Date | Date of raising |
| Your Company Name | ZeroOrigins Technologies Private Limited |
| Your GSTIN | e.g., 29AAAAA0000A1Z5 |
| Your Address | Registered address |
| Your PAN | Company PAN |
| Client Name | Full legal name |
| Client GSTIN | Mandatory for B2B |
| Client Address | Billing address |
| Place of Supply | Client's state |
| SAC Code | e.g., 998314 for IT services |
| Description of Service | Clear, specific |
| Taxable Amount | Amount before GST |
| GST Rate | 18% |
| CGST + SGST (intra-state) | 9% each |
| IGST (inter-state) | 18% |
| Total Amount | Amount after GST |
| Payment Terms | e.g., Net 7, Net 15 |
| Bank Account | Account No., IFSC, Bank, Branch |
| UPI ID | For quick payment |

### For International Clients (Export Invoice)

| Field | Details |
|-------|---------|
| Invoice Number | Sequential — e.g., ZO-EXP-2026-001 (use separate series for exports) |
| Currency | USD / AUD / AED — as agreed |
| Exchange rate reference | Optional, useful for accounting |
| GST | 0% (zero-rated export) — state "Zero-Rated Supply — LUT Reference No. XXXXX" |
| LUT Reference | File LUT before first export invoice — consult CA |
| SWIFT / Wire details | For international transfers |
| PayPal / Stripe link | For digital product buyers abroad |

---

## 7. Invoice Numbering System

Never reuse or skip invoice numbers. Use a consistent format:

- Domestic: `ZO-INV-YYYY-NNN` (e.g., ZO-INV-2026-001)
- Export: `ZO-EXP-YYYY-NNN` (e.g., ZO-EXP-2026-001)
- Digital products (Gumroad auto): tracked separately, no manual number needed

Reset NNN to 001 on 1 April each financial year.

---

## 8. Step-by-Step Process

**Step 1: Verify scope is agreed and signed**
- Do not raise invoice until client has approved the project scope or milestone
- Have at least a written email or WhatsApp confirmation of scope and price
- For large projects, use a formal contract (see ZO-SALES-005)

**Step 2: Collect client billing details**
- Request client's legal name, billing address, GSTIN
- For international: get client's full company name, billing country, currency preference

**Step 3: Assign invoice number**
- Open the Invoice Tracker (`10_Trackers/Invoice_Tracker.md`)
- Find the last invoice number and increment by 1
- Example: last was ZO-INV-2026-004 → new is ZO-INV-2026-005

**Step 4: Create the invoice**
- Use the invoice template in `09_Templates/Invoice_Checklist_Template.md`
- Tools: Google Docs / Zoho Invoice / Wave Accounting (free) / QuickBooks
- Fill all mandatory fields (Section 6 above)
- Double-check: amount, GST calculation, client GSTIN, place of supply

**Step 5: Review before sending**
Review checklist:
- [ ] Correct client name and GSTIN
- [ ] Correct service description
- [ ] Correct SAC code
- [ ] Correct GST split (CGST+SGST vs IGST)
- [ ] Bank details are correct
- [ ] Invoice number is sequential
- [ ] Payment terms clearly stated

**Step 6: Send invoice**
- Email with subject: `Invoice #ZO-INV-2026-005 — [Company Name] — [Service Name]`
- Attach as PDF (never editable Word or Excel)
- CC your admin email for records
- For large invoices (>Rs. 50,000 or >$500), send via email AND WhatsApp

**Step 7: Update Invoice Tracker**
- Add row to Invoice Tracker with:
  - Invoice number
  - Client name
  - Date sent
  - Amount
  - Due date
  - Status: Sent

**Step 8: Follow up on payment**
- If not paid by due date: follow up on Day 1 overdue, Day 7, Day 14
- See ZO-FIN-002 for payment collection SOP

**Step 9: Mark as paid**
- When payment received, update Invoice Tracker: Status → Paid, Payment Date
- File invoice in Google Drive: `Finance / Invoices / FY2026-27 / Month /`

---

## 9. Quality Checklist

- [ ] Invoice number is next in sequence (no gaps)
- [ ] Client GSTIN verified (check gstin.gov.in/search)
- [ ] GST type correct (CGST+SGST for same state; IGST for different state or international)
- [ ] Amount matches agreed price
- [ ] Payment terms clearly stated
- [ ] Bank details included
- [ ] Sent as PDF
- [ ] Invoice Tracker updated
- [ ] Copy stored in Google Drive

---

## 10. Approval Required

Invoices above Rs. 1,00,000 or $1,000: founder reviews before sending.

---

## 11. Output

- Sent invoice (PDF)
- Invoice Tracker updated
- Invoice filed in Google Drive

---

## 12. Storage Location

- Google Drive → `ZeroOrigins / Finance / Invoices / FY2026-27 / [Month] /`
- Invoice Tracker → Google Sheets (live document)

---

## 13. Risks / Mistakes to Avoid

- **Wrong GST type** — IGST vs CGST+SGST: if client is in same state, use CGST+SGST. If different state or export, use IGST. Wrong split means incorrect GST filing.
- **Missing client GSTIN** — B2B clients cannot claim ITC without your GSTIN on the invoice, which creates friction.
- **Sending editable files** — always send PDF. Editable invoices can be altered.
- **Gap in invoice numbering** — GST auditors look for this; always use next in sequence.
- **Late invoicing** — raise invoices within 24 hours of project completion or milestone. Delays lead to delayed payments.
- **Forgetting payment terms** — if not stated, clients default to paying whenever they want.

---

## 14. Review Frequency

Monthly (check Invoice Tracker). Review SOP quarterly.
