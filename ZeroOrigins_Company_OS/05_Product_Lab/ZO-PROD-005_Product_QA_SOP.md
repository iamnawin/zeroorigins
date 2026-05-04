# ZO-PROD-005 — Product QA SOP

---

## 1. Purpose

To test internal products before launch and before each major release.

---

## 2. Scope

All ZeroOrigins internal product builds.

---

## 3. Owner

Founder

---

## 4. Trigger

After prototype or feature build is complete, before launch or release.

---

## 5. QA Checklist by Type

### Web App QA

**Functionality:**
- [ ] All core user flows work end-to-end
- [ ] All buttons and links work
- [ ] Forms submit correctly
- [ ] Error states handled (empty form, wrong input)
- [ ] Loading states shown

**Compatibility:**
- [ ] Tested on Chrome, Safari, Firefox
- [ ] Tested on mobile (iOS Safari, Android Chrome)
- [ ] Tested at 375px (mobile), 768px (tablet), 1280px (desktop)

**Performance:**
- [ ] Pages load under 3 seconds
- [ ] No console errors in browser DevTools

**Security:**
- [ ] No API keys in frontend code
- [ ] Auth works correctly (if applicable)

### n8n Workflow / Automation Product QA

- [ ] Happy path tested
- [ ] Edge cases tested (see ZO-AUTO-005)
- [ ] Error handling verified
- [ ] Rate limits tested

### Digital Product / Template QA

- [ ] All links in the document work
- [ ] Formatting renders correctly (on Mac and Windows)
- [ ] All placeholder text replaced with instructions
- [ ] Download and open test completed

---

## 6. QA Sign-Off

Before launch, record:
```
QA Sign-Off
Product: [Name]
Version: [Version]
Date: [Date]
Tester: Founder
Status: PASS / FAIL
Issues Found: [List any]
Issues Fixed: [List any]
```

---

## 7. Quality Checklist

- [ ] Full QA checklist completed for product type
- [ ] No P0 bugs (breaking issues) remaining
- [ ] QA sign-off recorded

---

## 8. Approval Required

Founder sign-off before launch.

---

## 9. Output

- QA sign-off document
- Confirmed launch-ready status

---

## 10. Storage Location

Google Drive → `Products / [ProductName] / QA /`

---

## 11. Review Frequency

Before every release.
