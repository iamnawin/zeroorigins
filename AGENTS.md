# AGENTS.md

This repository is the ZeroOrigins master operating system: a strategic planning,
brand operations, and knowledge-base repo. There are no build tools, package
managers, or test suites by default. Work here means creating, editing, and
organizing Markdown documents, HTML pages, n8n workflow JSON files, ZIP/package
artifacts, and brand assets.

Before making structural decisions, read:

- `CLAUDE.md`
- `zeroorigins_unified_operating_system.md`
- `ZeroOrigins_Company_OS/INDEX.md`

## Brand Architecture

ZeroOrigins is the main operating brand. Do not default content or systems to
IgnAIte; IgnAIte is reserved for the education and training vertical.

Primary verticals:

- ZeroOrigins Studio / Services: AI automation services and client work.
- ZeroOrigins SaaS / Products: productized software.
- ZeroOrigins Apps / Tools: demos, MVPs, and prototypes.
- Automation Systems: reusable n8n backend logic.
- Client Solutions: per-client delivery artifacts.
- AIwithNoBrain: AI music and creative content.
- EpicsToYou: AI video and cinematic storytelling.
- ignAIte: future academy/workshop vertical.

## Current Priority

The first revenue path is ZeroOrigins Studio Services through the LeadFlow Setup
offer: lead capture plus follow-up automation. The reference pricing is
`$200 / Rs. 15,000`, with target markets in this order: USA, Australia, UAE.

n8n is the core automation stack and shared backend engine across verticals. It
is not the product itself.

## Main Structure

- `zeroorigins_unified_operating_system.md`: authoritative strategy document.
- `ZeroOrigins_Company_OS/`: main operational OS.
- `ZeroOrigins_Company_OS/INDEX.md`: primary navigation index.
- `ZeroOrigins_Company_OS/START_HERE.md`: founder first-30-days entry point.
- `ZeroOrigins_Company_OS/04_AI_Automation_Delivery/`: n8n delivery SOPs.
- `ZeroOrigins_Company_OS/09_Templates/`: proposals, invoices, NDAs, and other templates.
- `ZeroOrigins_Company_OS/10_Trackers/`: tracker templates intended for Google Sheets.
- `ignAIte/`: education vertical.
- `AIwithnoBrain/`: AI music and creative vertical.
- `EpicsToYou/`: AI video vertical.
- `ZeroOrigins - Workflow Starter Kit/`: digital product package.
- `zeroOrigins Files/`: brand assets, logos, and GTM materials.
- `Assests/`: additional brand and visual assets.

## SOP Naming

Use this naming convention for new SOPs:

```text
ZO-[DEPT]-[NUMBER]_[SOP_Name].md
```

Department codes:

```text
COMP FIN SALES AUTO PROD DIGI MKT SEC TMPL TRKR POL
```

When adding a new SOP:

1. Find the next sequential number in the department.
2. Create the file in the correct department folder.
3. Add the entry to `ZeroOrigins_Company_OS/INDEX.md`.

## Working Principles

- Prefer the smallest version that can be sold, demonstrated, or used quickly.
- Keep verticals separate; do not blend their audiences, positioning, or tone.
- Reuse backend automation logic, lead routing, CRM structure, and SOP patterns
  across verticals where appropriate.
- Sell outcomes, not implementation details. Lead with business results such as
  faster response and fewer missed leads, not AI/n8n terminology.
- ZeroOrigins retains all AI systems, prompts, and automation logic. Do not move
  AI assets to third-party-controlled repositories without legal sign-off.
- Keep diffs small, reviewable, and reversible.
- Avoid new dependencies unless explicitly requested.

## Verification

There is no universal test command for this repository. Verify changes according
to the artifact type:

- Markdown/text: review headings, links, naming, spelling, and consistency with
  the brand architecture.
- JSON workflows: validate JSON syntax after edits.
- HTML: open or inspect locally when visual/layout behavior matters.
- Packages/ZIPs: confirm expected files are present before reporting completion.

Final reports should include changed files, verification performed, and any
remaining risks or gaps.
