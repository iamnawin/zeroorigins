# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What This Repository Is

This is the ZeroOrigins master operating system — a strategic planning and brand operations knowledge base, not a software project. There are no build tools, package managers, or test suites.

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

The first revenue path is **ZeroOrigins Studio Services**, starting with the **LeadFlow Setup** offer (lead capture + follow-up automation). Pricing starts at $200. Primary markets: USA → Australia → UAE.

The core automation stack is **n8n** (self-hosted or cloud). It is the shared backend engine across all verticals, not the product itself

## Folder Conventions

Follow the numbered structure defined in `zeroorigins_unified_operating_system.md` §4:
- `00-Company-Core/` — vision, positioning, brand architecture
- `01-Strategy/` — GTM, ICP, pricing
- `02-Studio-Services/` — offers, outreach templates, proposals
- `05-Automation-Systems/n8n/` — workflow exports and docs
- `06-Client-Solutions/` — per-client folders
- `07-Content-and-Media/` — split by vertical
- `08-IgnAIte/` — education vertical (future)

The `ignAIte/Studio-Offers/` folder contains the current IgnAIte service offer docs (`01_offer.md` → `05_demo_flow.md`). These map to the Studio Services concept but are branded under IgnAIte.

## Working Principles

- **Execution over planning.** Recommend the smallest version that can be sold or demonstrated quickly.
- **Keep verticals separate.** AIwithNoBrain, EpicsToYou, and IgnAIte have distinct audiences and tones — do not blend them.
- **Unified backend.** Automation logic, lead routing, CRM structure, and SOPs should be reusable across verticals.
- **Sell outcomes, not tech.** Lead with business outcomes (faster response, fewer missed leads), not AI/n8n terminology.
