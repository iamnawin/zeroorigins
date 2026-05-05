# ZO-POL-002 — Data Protection Policy

**ID:** ZO-POL-002  
**Department:** Security & Compliance  
**Version:** 1.0  
**Owner:** Founder  
**Effective Date:** May 2026  

---

## 1. Purpose

This policy defines how ZeroOrigins handles, stores, and protects personal and confidential data — whether belonging to clients, prospects, contractors, or internal operations.

---

## 2. Scope

Applies to:
- All ZeroOrigins team members (employees and contractors)
- All data processed in connection with ZeroOrigins projects and services
- All systems and tools used by ZeroOrigins (see ZO-SEC-001 for the approved tools list)

---

## 3. Data Classification

| Class | Description | Examples |
|-------|-------------|----------|
| **Confidential** | Highly sensitive — restricted access | Client credentials, API keys, payment data, legal documents |
| **Internal** | Internal use only — not for public sharing | Client project files, business financials, lead data, contracts |
| **General** | Can be shared publicly or with clients | Service descriptions, published case studies, website content |

---

## 4. Handling Rules by Classification

### Confidential Data
- Store only in approved secure locations (password manager, encrypted Drive folder)
- Never share via unencrypted email or WhatsApp
- Never store in n8n workflow nodes as plain text — use environment variables
- Access limited to founder only, unless explicit need exists
- Rotate credentials every 90 days or immediately after a team member departs

### Internal Data
- Store in ZeroOrigins Google Drive workspace
- Share only with the people who need it for a specific project
- Do not store on personal devices without approval
- Contractors receive access only to files needed for their task

### General Data
- No restrictions — but review before publishing to ensure no accidentally included confidential info

---

## 5. Client Data Rules

1. Do not use client data for any purpose outside the agreed project scope.
2. Do not pass client data to third-party AI tools (OpenAI, Anthropic, etc.) without written consent. If AI processing is part of the service, disclose this clearly in the proposal.
3. Do not retain client credentials (passwords, tokens) after a project closes — delete or return them.
4. Store client files in a dedicated folder: `ZeroOrigins / 06-Client-Solutions / [ClientName] / [Project]`

---

## 6. Contractor and Team Member Obligations

Before accessing any client data or internal systems:
- Sign the ZeroOrigins NDA (ZO-TMPL-004_NDA_Template.md)
- Receive a security briefing covering this policy and ZO-SEC-001
- Be granted only the minimum access required for their work

On offboarding:
- All access revoked immediately (follow ZO-SEC-004_Access_Revocation_SOP.md)
- All company data removed from personal devices
- Passwords and credentials changed for all shared accounts they had access to

---

## 7. Data Breach Response

If a data breach or security incident is suspected:
1. Stop the suspected breach immediately (disconnect system, revoke access)
2. Document what happened and when
3. Follow ZO-SEC-005_Incident_Response_SOP.md
4. Notify affected clients within 72 hours if their data was exposed
5. Review and fix the root cause before resuming operations

---

## 8. Training

All team members must review this policy before starting work. Annual review recommended or whenever a significant new tool or process is introduced.

---

*Version: 1.0 | Created: May 2026 | Owner: Founder, ZeroOrigins*
