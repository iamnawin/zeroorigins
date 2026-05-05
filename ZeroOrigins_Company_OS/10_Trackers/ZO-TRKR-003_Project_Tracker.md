# ZO-TRKR-003 — Project Tracker

**ID:** ZO-TRKR-003  
**Department:** AI Automation Delivery / Product Lab  
**Version:** 1.0  
**Owner:** Founder  

---

## Purpose

Track all active and completed client projects and internal product builds in one place. Copy this structure into Google Sheets for live use.

---

## Sheet: Project Tracker

### Columns

| Column | Description | Values / Format |
|--------|-------------|-----------------|
| Project ID | Unique project reference | ZO-PROJ-2026-001 |
| Project Name | Short descriptive name | Text |
| Type | Project category | Client Automation / Product Build / Digital Product / Internal / Creative |
| Client / Owner | Client name or "Internal" | Text |
| Lead Ref | Link to Lead ID | ZO-LEAD-XXX |
| Invoice Ref | Link to Invoice ID | ZO-INV-XXXX-XXX |
| Start Date | Actual or planned start | DD-MM-YYYY |
| Target End Date | Agreed delivery deadline | DD-MM-YYYY |
| Actual End Date | Real completion date | DD-MM-YYYY |
| Status | Current project status | Not Started / In Progress / In Review / Delivered / On Hold / Cancelled |
| Phase | Current delivery phase | Discovery / Architecture / Build / Testing / Demo / Deployed / Support |
| Contract Value | Total agreed amount | Rs / USD |
| Amount Invoiced | Total invoiced so far | Rs / USD |
| Amount Received | Total received so far | Rs / USD |
| n8n Workflow URL | Link to n8n workflow (if applicable) | URL |
| Repo / Drive Link | GitHub repo or Google Drive folder | URL |
| Key Deliverables | Bullet list of main outputs | Text |
| Notes | Blockers, risks, client preferences | Text |

---

## Status Definitions

| Status | Meaning |
|--------|---------|
| Not Started | Project confirmed, work not yet begun |
| In Progress | Active work happening |
| In Review | Delivered to client for review / approval |
| Delivered | Client accepted, project complete |
| On Hold | Paused — awaiting client input or payment |
| Cancelled | Terminated before completion |

---

## Weekly Project Review

Review each active project:
- [ ] Is it on track for the deadline?
- [ ] Any blockers requiring client input?
- [ ] Is the current phase aligned with the plan?
- [ ] Any scope creep issues to address?
- [ ] Is the invoice in the Invoice Tracker and up to date?

---

## Project ID Numbering

Format: `ZO-PROJ-[YEAR]-[SEQ]`

Examples:
- `ZO-PROJ-2026-001` — first project in 2026
- `ZO-PROJ-2026-005` — fifth project in 2026

---

*SOP reference: ZO-AUTO-002_Workflow_Architecture_SOP.md, ZO-SALES-004_Client_Onboarding_SOP.md*  
*Version: 1.0 | Created: May 2026 | Owner: Founder, ZeroOrigins*
