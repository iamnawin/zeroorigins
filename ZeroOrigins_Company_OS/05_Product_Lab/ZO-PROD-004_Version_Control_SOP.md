# ZO-PROD-004 — Version Control SOP

---

## 1. Purpose

To maintain code and configuration version history for all ZeroOrigins products so that changes are trackable and rollback is possible.

---

## 2. Scope

All software products, n8n workflow JSON files, and AI prompts.

---

## 3. Owner

Founder

---

## 4. Trigger

When starting any new product or making significant changes.

---

## 5. Version Control by Asset Type

| Asset | Tool |
|-------|------|
| Code (web app, API) | Git + GitHub |
| n8n workflows | JSON export + Google Drive versioned folders |
| AI prompts | Google Drive + manual versioning |
| Design files | Figma (version history built in) |
| Documents | Google Drive (version history built in) |

---

## 6. Git Workflow for Code Products

**Branching:**
- `main` — production only, always deployable
- `dev` — active development
- `feature/[name]` — new features
- `fix/[name]` — bug fixes

**Commit message format:**
```
feat: add lead scoring function
fix: correct email template for empty name
docs: update API setup instructions
```

**Before merging to main:**
- [ ] All tests passing
- [ ] Code reviewed (at least self-review)
- [ ] No hardcoded secrets

**Tagging releases:**
- Tag every release: `git tag v1.0.0`
- Use semantic versioning: `MAJOR.MINOR.PATCH`
  - Major: breaking changes
  - Minor: new features
  - Patch: bug fixes

---

## 7. n8n Workflow Versioning

- Export workflow JSON after every significant change
- Naming: `WorkflowName_v1.0.json`, `WorkflowName_v1.1.json`
- Store in Google Drive in dated folder
- Never overwrite old versions — always save as new file

---

## 8. Quality Checklist

- [ ] All products have a Git repository (GitHub)
- [ ] README exists in every repo
- [ ] No secrets in git history
- [ ] n8n workflows exported after every change
- [ ] Version numbers updated on releases

---

## 9. Output

- Git repository with clean history
- n8n workflow version archive

---

## 10. Storage Location

- Code: GitHub (github.com/[org]/[repo])
- n8n JSONs: Google Drive → `Products / [ProductName] / Workflow_Versions /`

---

## 11. Risks / Mistakes to Avoid

- **Committing .env or API keys to git** — use .gitignore; use GitHub secret scanning
- **No commit messages** — git history without messages is useless

---

## 12. Review Frequency

Per product. Quarterly audit of all repositories.
