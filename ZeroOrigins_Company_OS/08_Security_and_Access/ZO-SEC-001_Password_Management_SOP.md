# ZO-SEC-001 — Password Management SOP

---

## 1. Purpose

To ensure all ZeroOrigins accounts are protected by strong, unique passwords stored securely — and never in a spreadsheet, sticky note, or memory.

---

## 2. Scope

All ZeroOrigins accounts: SaaS tools, cloud platforms, client portals, payment systems, social media.

---

## 3. Owner

Founder

---

## 4. Trigger

Immediately on setup of any new account; reviewed quarterly.

---

## 5. Password Manager

Use **1Password** or **Bitwarden** (both are acceptable; pick one and never switch).

| Feature | 1Password | Bitwarden |
|---------|-----------|-----------|
| Cost | ~$3/month | Free (or $10/year premium) |
| Security | Excellent | Excellent |
| Browser extension | Yes | Yes |
| Mobile app | Yes | Yes |
| Recommended for | Ease of use | Budget-first |

**Setup steps:**
1. Create account with a strong master password (20+ characters, written down and stored offline in a safe place)
2. Install browser extension
3. Install mobile app
4. Enable two-factor authentication (2FA) on the password manager itself using an authenticator app (not SMS)

---

## 6. Password Rules

| Rule | Standard |
|------|----------|
| Length | Minimum 16 characters |
| Generation | Always use password manager generator |
| Reuse | Never — every account gets a unique password |
| Storage | Password manager only — never in Notion, Google Sheets, or messages |
| Sharing | Never share via WhatsApp/email; use 1Password/Bitwarden secure sharing feature |

---

## 7. Two-Factor Authentication (2FA)

Enable 2FA on every account that supports it.

Priority accounts (mandatory 2FA):
- [ ] Google / Gmail
- [ ] GitHub
- [ ] AWS / GCP / Azure
- [ ] Stripe / Razorpay / Wise
- [ ] Gumroad
- [ ] n8n cloud
- [ ] LinkedIn
- [ ] Domain registrar / DNS

Use an authenticator app (Google Authenticator, Authy, or 1Password built-in TOTP) — not SMS.

Store backup codes in the password manager (as a secure note).

---

## 8. Account Inventory

Maintain a list of all accounts in the password manager organized by category:

| Category | Examples |
|----------|---------|
| Business accounts | Google Workspace, GitHub, Notion |
| Financial | Razorpay, Stripe, Wise, HDFC NetBanking |
| Cloud / Hosting | AWS, Vercel, Railway, Cloudflare |
| Marketing | LinkedIn, Brevo, Buffer |
| Products | Gumroad, Lemon Squeezy |
| Client-specific | Add per project, remove after offboarding |

---

## 9. When an Account Is Compromised

1. Change the password immediately
2. Enable/verify 2FA
3. Check all active sessions and revoke unknown devices
4. Check if other accounts use the same password (they shouldn't — this is why uniqueness matters)
5. If a client credential is involved, notify the client same day

---

## 10. Quality Checklist

- [ ] Password manager set up with 2FA on the manager itself
- [ ] All critical accounts have unique passwords in the manager
- [ ] 2FA enabled on all priority accounts
- [ ] Master password written and stored offline (not digitally)
- [ ] Quarterly: audit for weak/reused passwords using password manager health report

---

## 11. Approval Required

None — Founder manages directly.

---

## 12. Output

- Complete account inventory in password manager
- 2FA enabled on all critical accounts

---

## 13. Storage Location

Password manager (not Google Drive — passwords are not documents).

---

## 14. Risks / Mistakes to Avoid

- **Master password stored in the same digital system** — if your computer is compromised, the attacker gets everything
- **Using SMS for 2FA** — SIM swap attacks are common; use an authenticator app
- **Sharing passwords via WhatsApp** — messages are not encrypted end-to-end for attachments

---

## 15. Review Frequency

Quarterly password health audit; immediately after any account compromise.
