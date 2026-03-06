# Horizon Europe OS — Start Here

## What is this?

A **360-degree, multi-agent system** for identifying EU funding calls (Cluster 3: Civil Security for Society), building consortia, and iteratively drafting winning Horizon Europe proposals.

## Why a multi-agent system?

Standard linear AI writing workflows fail for EU grants because **consortium building and proposal drafting are deeply intertwined and highly iterative**. You rarely have the perfect 10-partner team on Day 1. This system uses a **Hub-and-Spoke architecture** where drafting agents can pause mid-section, trigger consortium scouting, and resume with updated partner context.

## Architecture Overview

```
                        ┌─────────────────┐
                        │  COORDINATOR HUB │  ← Central state manager
                        │  (Global State)  │
                        └────────┬────────┘
                                 │
          ┌──────────────────────┼──────────────────────┐
          │                      │                      │
    ┌─────▼─────┐         ┌─────▼─────┐         ┌─────▼─────┐
    │ EXCELLENCE │         │  IMPACT   │         │IMPLEMENTA-│
    │ ARCHITECT  │         │SPECIALIST │         │TION MANAGER│
    └─────┬─────┘         └─────┬─────┘         └─────┬─────┘
          │                      │                      │
          │     GAP_DETECTED     │    GAP_DETECTED      │    GAP_DETECTED
          │─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─│─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─│
          │                      │                      │
          └──────────────────────┼──────────────────────┘
                                 │
                        ┌────────▼────────┐
                        │ CONSORTIUM SCOUT│  ← Triggered on gaps
                        │ (Partner Search)│
                        └────────┬────────┘
                                 │
                        ┌────────▼────────┐
                        │ partner_matrix.md│  ← Living memory
                        │ (Shared State)   │
                        └─────────────────┘

  Support agents: Call Strategist, Compliance Reviewer, Budget Balancer, IP & Legal Expert
```

## The Iterative Teaming Loop

1. A **drafting agent** (Excellence, Impact, or Implementation) is writing a section
2. It discovers a capability gap — a WP needs expertise the consortium doesn't have
3. It reports `GAP_DETECTED` to the **Coordinator Hub**
4. Coordinator **pauses** the draft and dispatches the **Consortium Scout**
5. Scout returns candidate partners with profile cards and outreach emails
6. Coordinator updates `partner_matrix.md` and **resumes** the draft with new context

## Workflow Sequence

| # | Workflow | Agent | Description |
|---|---------|-------|-------------|
| W1 | `w1_call_discovery` | Call Strategist | Parse and assess the call |
| W2 | `w2_consortium_scouting_loop` | Consortium Scout | Initial consortium assembly |
| W3 | `w3_draft_excellence` | Excellence Architect | Draft Part B Section 1 |
| W4 | `w4_draft_impact_and_pedr` | Impact Specialist | Draft Part B Section 2 |
| W5 | `w5_draft_implementation_wp` | Implementation Manager | Draft Part B Section 3 |
| W6 | `w6_iterative_partner_fill` | Consortium Scout | Mid-draft partner scouting (re-entry) |
| W7 | `w7_red_team_review` | Compliance Reviewer | Score and critique all sections |
| W8 | `w8_final_assembly_and_trim` | Coordinator Hub | Final assembly, page trim, submission package |

**Not linear** — W6 can be triggered at any point during W3-W5. W7 can be run per-section or at the end.

## Quick Start

### 1. Set up your proposal

Edit these files with your information:
- `knowledge/proposal_concept_live.md` — your proposal idea, objectives, WP overview
- `knowledge/partner_matrix.md` — any partners you already have

### 2. Provide a call text

Paste the raw call text from the Funding & Tenders Portal into `knowledge/call_text_live.md` (or give it to the Coordinator to dispatch to the Call Strategist).

### 3. Activate the Coordinator Hub

Load `agents/coordinator-hub.md` as the system prompt for your central agent. It will:
1. Read your concept and call text
2. Assess consortium readiness
3. Recommend the next workflow step
4. Begin orchestrating

### 4. Follow the workflow

The Coordinator will guide you through W1→W8, pausing for your input when needed (partner approvals, scope decisions, budget sign-offs).

## Directory Structure

```
horizon-os/
├── agents/              ← System prompts for each agent
├── evals/               ← Evaluation checklists (Red Team uses these)
├── knowledge/           ← Living knowledge base (call text, partners, concept)
│   ├── definitions/     ← Reference materials (TRL, taxonomy, open science)
│   ├── eu_policies/     ← Relevant EU policy summaries
│   └── work_programmes/ ← CL3 work programme summaries
├── output/              ← Generated artifacts
│   ├── current_draft/   ← Part B sections (Excellence, Impact, Implementation)
│   ├── budget_drafts/   ← Budget iterations
│   └── partner_outreach/← Drafted outreach emails
├── templates/           ← Structural templates for all outputs
└── workflows/           ← Step-by-step workflow definitions
```

## Key Design Principles

1. **Iterative Teaming** — Consortium building loops back during drafting, not just upfront
2. **Strict EU Compliance** — Every eval criterion, formatting rule, and cross-cutting theme is checklistified
3. **Markdown-Driven** — Everything is a readable, versionable Markdown file
4. **Separation of Concerns** — Agents are specialists; only the Coordinator sees the full picture
5. **Human in the Loop** — The system drafts and recommends; you decide and submit
