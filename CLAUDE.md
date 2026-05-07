# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What This Repository Is

This is the ZeroOrigins master operating system — a strategic planning, brand operations, and knowledge-base repository. There are no build tools, package managers, or test suites. Work here means creating, editing, and organizing Markdown documents, HTML pages, n8n workflow JSON files, and brand assets.

The authoritative strategy document is [zeroorigins_unified_operating_system.md](zeroorigins_unified_operating_system.md). Read it before making any structural decisions.

## Brand Architecture

```
ZeroOrigins (parent umbrella)
├── Studio / Services     — AI automation services, client work, n8n workflows
├── SaaS / Products       — productized software
├── Apps / Tools          — demos, MVPs, prototypes
├── Automation Systems    — reusable n8n backend logic
├── Client Solutions      — per-client delivery artifacts
├── AIwithNoBrain         — AI music, creative/viral content
├── EpicsToYou            — AI video, cinematic storytelling
└── ignAIte               — future academy/workshop vertical (not main brand)
```

**ZeroOrigins is the main operating brand.** Do not default content or systems to IgnAIte — that is reserved for education/training verticals later.

## Current Priority

First revenue path: **ZeroOrigins Studio Services** → **LeadFlow Setup** offer (lead capture + follow-up automation). Pricing: $200 / Rs. 15,000. Primary markets: USA → Australia → UAE.

Core automation stack is **n8n** (self-hosted or cloud) — the shared backend engine across all verticals, not the product itself.

## Actual Folder Structure

```
zeroOrigins/
├── zeroorigins_unified_operating_system.md   ← authoritative strategy doc
├── ZeroOrigins_Company_OS/                   ← main operational OS (72 docs)
│   ├── INDEX.md                              ← find any SOP by ID or topic
│   ├── START_HERE.md                         ← founder's first-30-days checklist
│   ├── 30_Day_Execution_Plan.md
│   ├── 01_Company_and_Compliance/            ← legal, MCA, GST, registration SOPs
│   ├── 02_Finance/                           ← invoicing, payments, accounting SOPs
│   ├── 03_Sales_and_Client_Operations/       ← lead→close, onboarding, communication
│   ├── 04_AI_Automation_Delivery/            ← n8n build, testing, deployment SOPs
│   ├── 05_Product_Lab/                       ← product validation, build, QA, launch
│   ├── 06_Digital_Products/                  ← Gumroad listings, template strategy
│   ├── 07_Marketing_and_Content/             ← LinkedIn, email, SEO, paid ads SOPs
│   ├── 08_Security_and_Access/               ← credential hygiene, incident response
│   ├── 09_Templates/                         ← fill-in-blank: proposal, invoice, NDA
│   ├── 10_Trackers/                          ← copy to Google Sheets: leads, invoices
│   ├── 11_Policies/                          ← privacy, IP, refund, contractor policy
│   └── 12_Archive/                           ← deprecated files
├── ignAIte/                                  ← education vertical
│   ├── Studio-Offers/                        ← 01_offer.md → 05_demo_flow.md
│   └── *.html                                ← course pages, brochures, ads
├── AIwithnoBrain/                            ← AI music/creative vertical (HTML)
├── EpicsToYou/                               ← AI video vertical
├── ZeroOrigins – Workflow Starter Kit/       ← digital product: Guide/, Workflows/
├── zeroOrigins Files/                        ← brand assets, logos, GTM plan
└── Assests/                                  ← additional brand/visual assets
```

## SOP Naming Convention

`ZO-[DEPT]-[NUMBER]_[SOP_Name].md`

Dept codes: `COMP` `FIN` `SALES` `AUTO` `PROD` `DIGI` `MKT` `SEC` `TMPL` `TRKR` `POL`

Example: `ZO-AUTO-003_n8n_Build_SOP.md`

When adding a new SOP: assign the next sequential number in the department, create the file, and add an entry to `ZeroOrigins_Company_OS/INDEX.md`.

## Key Navigation

- **Finding any document:** use `ZeroOrigins_Company_OS/INDEX.md` — all 72 docs indexed by ID and topic.
- **New to the OS:** start with `ZeroOrigins_Company_OS/START_HERE.md` then `30_Day_Execution_Plan.md`.
- **n8n workflow delivery:** SOPs are in `04_AI_Automation_Delivery/` (ZO-AUTO-001 through 008).
- **Client-facing docs:** proposals in `09_Templates/ZO-TMPL-001_Proposal_Template.md`, invoices in `ZO-TMPL-002`.
- **Trackers** (Lead, Invoice, Project, Content, Expense) live in `10_Trackers/` — export to Google Sheets for live use.

## Working Principles

- **Execution over planning.** Recommend the smallest version that can be sold or demonstrated quickly.
- **Keep verticals separate.** AIwithNoBrain, EpicsToYou, and ignAIte have distinct audiences and tones — do not blend them.
- **Unified backend.** Automation logic, lead routing, CRM structure, and SOPs should be reusable across verticals.
- **Sell outcomes, not tech.** Lead with business outcomes (faster response, fewer missed leads), not AI/n8n terminology.
- **IP ownership:** ZeroOrigins retains all AI systems, prompts, and automation logic. Do not move AI assets to third-party-controlled repos without legal sign-off.
