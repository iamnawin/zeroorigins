# ZO-AUTO-002 — Workflow Architecture SOP

---

## 1. Purpose

To design a clear, maintainable workflow architecture before building in n8n — so the build is faster, the logic is sound, and the client can understand what was built.

---

## 2. Scope

All automation projects. Architecture happens after requirements are confirmed and before n8n build starts.

---

## 3. Owner

Founder

---

## 4. Trigger

After requirements document is confirmed by client (ZO-AUTO-001).

---

## 5. Architecture Outputs

For every project, produce:
1. **Workflow Logic Diagram** — visual flow showing trigger → nodes → outputs
2. **Node Plan** — list of every n8n node needed
3. **Data Map** — what data fields flow through each stage
4. **Integration List** — tools, APIs, credentials needed

---

## 6. Step-by-Step Process

**Step 1: Draw the workflow on paper or whiteboard (5 minutes)**
- Start with the trigger on the left
- Map each step to the right
- Mark decision points (IF/ELSE forks)
- End with all outputs on the right

**Step 2: Convert to digital diagram**
- Use FigJam, Excalidraw, or Miro
- Use standard shapes:
  - Rectangle: action or process step
  - Diamond: decision / condition
  - Oval: start / end
  - Arrow: data flow direction

**Step 3: Write the Node Plan**
List every n8n node in order:
```
1. Webhook Trigger — receives form data
2. Set — extract and rename fields
3. IF — check if lead score > 70
4. Google Sheets — append to "Hot Leads" sheet (IF true)
5. Gmail — send notification email to founder
6. Google Sheets — append to "Cold Leads" sheet (IF false)
7. HTTP Request — call OpenAI API for lead summary
8. Gmail — send AI summary email to client
```

**Step 4: Define the Data Map**
For each node, note what data comes in and what goes out:
```
Webhook: { name, email, company, message, source }
SET node: { lead_name, lead_email, company_name, inquiry }
IF node: condition = message.length > 50 (basic proxy for serious inquiry)
```

**Step 5: Share architecture with client**
- Send diagram + 5-sentence explanation
- Ask: "Does this match your expectation?"
- Get written confirmation before building

**Step 6: Identify risks**
Before building, flag:
- Any API that has rate limits (OpenAI, Gmail)
- Any data that might be missing (what if name is blank?)
- Any integration that requires enterprise/paid plan

---

## 7. Quality Checklist

- [ ] Workflow diagram created
- [ ] Node plan written in order
- [ ] All integrations identified with API/credential needs
- [ ] Data map covers all key fields
- [ ] Risks identified
- [ ] Architecture shared with and confirmed by client

---

## 8. Approval Required

Client confirmation before build starts.

---

## 9. Output

- Workflow diagram (PDF or shared Figma/Excalidraw)
- Node plan document
- Data map

---

## 10. Storage Location

Google Drive → `ZeroOrigins / Clients / [ClientName] / [ProjectName] / 02_Architecture /`

---

## 11. Risks / Mistakes to Avoid

- **Skipping architecture for "simple" workflows** — even simple workflows need a plan; scope creep catches you off guard
- **Not confirming with client** — clients often have visual expectations that differ from yours

---

## 12. Review Frequency

After each project.
