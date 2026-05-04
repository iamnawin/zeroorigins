# ZO-SEC-004 — Access Revocation SOP

---

## 1. Purpose

To ensure access to ZeroOrigins systems and client systems is revoked promptly when a project ends, a contractor leaves, or a client relationship closes.

---

## 2. Scope

All access granted to any person (contractor, intern, client) to ZeroOrigins systems, and all access granted to ZeroOrigins by clients to their systems.

---

## 3. Owner

Founder

---

## 4. Trigger

- Project delivery completed (ZO-AUTO-007)
- Contractor engagement ends
- Client relationship terminates

---

## 5. Offboarding Checklist — Client Project End

When a project closes, within 48 hours:

**ZeroOrigins access to client systems:**
- [ ] Remove ZeroOrigins from client Google Workspace (if added)
- [ ] Revoke API keys ZeroOrigins was using on the client's account
- [ ] Remove n8n credentials specific to this client from ZeroOrigins credential store
- [ ] Confirm no ZeroOrigins webhooks remain active in client's tools
- [ ] Delete client credentials from password manager (after final handover confirmed)

**Client access to ZeroOrigins systems:**
- [ ] Remove client from any shared Notion workspaces
- [ ] Revoke any Slack/WhatsApp/Discord channel access if using a shared system
- [ ] If client had read access to ZeroOrigins n8n: revoke

---

## 6. Offboarding Checklist — Contractor End

When a contractor or hired help finishes:

- [ ] Remove from all shared tools: Notion, Slack, GitHub repos
- [ ] Revoke any access to ZeroOrigins Google Drive folders they were added to
- [ ] Change any shared passwords they had access to
- [ ] Remove their devices from any trusted device lists
- [ ] Confirm they have deleted any ZeroOrigins files from personal devices (email confirmation)
- [ ] Collect any ZeroOrigins property (if applicable)

---

## 7. Access Revocation Log

Maintain a simple Google Sheet or Notion table:

| Date | Person/Client | Access Type | Revoked By | Confirmed |
|------|--------------|-------------|-----------|-----------|
| [Date] | [Client Name] | n8n credentials | Founder | Yes |
| [Date] | [Contractor Name] | Notion workspace | Founder | Yes |

---

## 8. Emergency Revocation

If you suspect unauthorized access:
1. Revoke all credentials immediately (don't wait to investigate first)
2. Change all shared passwords
3. Check audit logs for suspicious activity
4. Notify affected client(s) within 24 hours
5. Document what happened in the incident log (ZO-SEC-005)

---

## 9. Quality Checklist

- [ ] Offboarding completed within 48 hours of project close
- [ ] All client credentials removed from ZeroOrigins systems
- [ ] All ZeroOrigins credentials removed from client systems
- [ ] Revocation logged

---

## 10. Approval Required

None — Founder executes directly.

---

## 11. Output

- Updated Access Revocation Log
- Confirmation email to client that ZeroOrigins access has been removed (optional but professional)

---

## 12. Storage Location

Google Drive → `Security / Access_Log.xlsx`

---

## 13. Risks / Mistakes to Avoid

- **Forgetting to revoke access at project end** — old credentials sitting in live systems are a security liability for you and the client
- **Deleting credentials before final handover** — revoke AFTER the client has confirmed everything works, not before

---

## 14. Review Frequency

After every project close and contractor end. Quarterly audit of all access.
