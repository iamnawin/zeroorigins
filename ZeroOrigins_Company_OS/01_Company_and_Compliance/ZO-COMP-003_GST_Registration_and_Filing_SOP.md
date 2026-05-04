# ZO-COMP-003 — GST Registration and Filing SOP

> **Consult CA/CS for GST compliance. Rules change frequently. This SOP provides an operational guide only.**

---

## 1. Purpose

To register ZeroOrigins for GST and maintain timely monthly and annual GST filings.

---

## 2. Scope

Applies to all GST registration, invoicing compliance, return filing, and ITC (Input Tax Credit) management for ZeroOrigins.

---

## 3. Owner

Founder (with CA executing filings)

---

## 4. Trigger

- Registration: triggered at incorporation or when turnover exceeds Rs. 20L (services) or Rs. 40L (goods)
- Recommended: register from day 1 for B2B credibility (clients need your GSTIN to claim ITC)

---

## 5. Inputs Required

- Company PAN
- Certificate of Incorporation
- Proof of registered address (rent agreement + NOC or ownership proof)
- Utility bill for address
- Cancelled cheque or bank statement
- Photo of authorized signatory
- Digital signature

---

## 6. Step-by-Step Process

### GST Registration

**Step 1: Apply on GST portal**
- Go to: gstin.gov.in → New Registration → Register as Taxpayer
- Select: Regular Taxpayer
- Enter PAN, mobile, email → verify OTP
- Fill Part A (basic details) → save TRN (Temporary Reference Number)

**Step 2: Fill Part B**
- Business details, address, bank details
- Upload required documents
- Select HSN/SAC codes for your services:

| Service | SAC Code |
|---------|----------|
| IT / software services | 998314 |
| Management consulting | 998311 |
| Online courses / training | 999293 |
| Digital content / creative services | 998912 |
| AI/automation development | 998314 |

**Step 3: Submit and verify**
- Submit with DSC
- GST officer reviews and approves (typically 3–7 working days)
- You receive GSTIN (15-digit number)

**GSTIN format:** 29AAAAA0000A1Z5
- First 2 digits: state code
- Next 10: PAN of company
- Next: entity number
- Last: checksum

### GST on Invoices

All GST invoices must include:
- Your GSTIN
- Client's GSTIN (for B2B)
- Invoice number (sequential, no gaps)
- Invoice date
- SAC code
- Taxable value
- GST rate and amount (CGST + SGST for intra-state; IGST for inter-state)
- Place of supply

**GST rates for ZeroOrigins services:** 18% (most IT and professional services)

**Intra-state:** CGST 9% + SGST 9%
**Inter-state (including international): IGST 18%**

**Export of services (clients outside India):**
- Zero-rated supply — 0% GST
- Issue Letter of Undertaking (LUT) at start of each FY to export without paying IGST
- File LUT on GST portal before first export invoice

### Monthly GST Filing

**GSTR-1 (Outward Supplies — Sales)**
- Due: 11th of the following month (if turnover > Rs. 5Cr) or quarterly (if < Rs. 5Cr with QRMP scheme)
- List all sales invoices issued in the month

**GSTR-3B (Summary Return + Tax Payment)**
- Due: 20th of the following month
- Pay any tax liability before filing

**Steps each month:**
1. Download all sales invoices for the month from accounting software
2. Reconcile with payment received
3. Check GSTR-2B (auto-generated ITC statement) for input credits
4. Share data with CA by 5th of following month
5. CA files GSTR-1 by 11th
6. Review GSTR-3B draft with CA
7. Pay GST liability via net banking by 20th
8. CA files GSTR-3B

### Annual GST Return

- GSTR-9 (Annual Return): due 31 December after FY end
- Reconciles all monthly returns for the year
- CA will prepare and file

### Input Tax Credit (ITC)

You can claim ITC on:
- Software subscriptions (n8n, AWS, tools)
- Professional services (CA, legal)
- Office supplies and equipment
- Any purchase/expense with a GST invoice in company's name

Rules:
- Vendor must have filed their GSTR-1 for the credit to appear in your GSTR-2B
- ITC must be claimed within the time limit (typically same FY or before September of next FY)
- Keep all invoices with GSTIN, SAC code, and amounts

---

## 7. Quality Checklist

- [ ] GSTIN obtained and displayed on all invoices
- [ ] LUT filed for export services before first foreign invoice
- [ ] All invoices use correct SAC codes
- [ ] GSTR-1 filed by 11th each month
- [ ] GSTR-3B filed and tax paid by 20th each month
- [ ] ITC reconciled monthly against GSTR-2B
- [ ] GSTR-9 filed annually
- [ ] All GST invoices stored digitally for 7 years

---

## 8. Approval Required

Founder approves tax payment before CA files GSTR-3B.

---

## 9. Output

- Active GSTIN
- Monthly filed GSTR-1 and GSTR-3B
- Annual GSTR-9
- ITC ledger maintained

---

## 10. Storage Location

- All GST filings: Google Drive → `ZeroOrigins / Finance / GST /`
- Invoices: `ZeroOrigins / Finance / Invoices / [Year-Month] /`

---

## 11. Risks / Mistakes to Avoid

- **Missing LUT for foreign clients** — if you forget LUT, you must pay IGST on exports and then claim refund (slow and painful)
- **Wrong place of supply** — determines IGST vs CGST/SGST split
- **Not filing GSTR-1 on time** — clients cannot see your invoices in their GSTR-2B, which blocks their ITC and creates friction
- **Mixing personal and business expenses** — only company expenses with GSTIN in company name are eligible for ITC

---

## 12. Review Frequency

Monthly (aligned with filing schedule). Review annual compliance in April.
