# Horizon Europe OS — Start Here

## What is this?

A **360-degree, multi-agent system** for identifying EU funding calls (Cluster 3: Civil Security for Society), building consortia, and iteratively drafting winning Horizon Europe proposals.

## Why a multi-agent system?

Standard linear AI writing workflows fail for EU grants because **consortium building and proposal drafting are deeply intertwined and highly iterative**. You rarely have the perfect 10-partner team on Day 1. This system uses a **Hub-and-Spoke architecture** where drafting agents can pause mid-section, trigger consortium scouting, and resume with updated partner context.

## Architecture Overview

```
                    ┌──────────────────────┐
                    │    COORDINATOR HUB    │  ← Central state manager
                    │    (Global State)     │
                    └──────────┬───────────┘
                               │
        ┌──────────────────────┼──────────────────────┐
        │                      │                      │
   ─ ─ ─ ─ ─ ─ ─ ─     ─ ─ ─ ─ ─ ─ ─ ─     ─ ─ ─ ─ ─ ─ ─ ─
  │ BRAIN TRUST (W0) │  │ DRAFTING (W3-5) │  │ QUALITY (W7-8) │
   ─ ─ ─ ─ ─ ─ ─ ─     ─ ─ ─ ─ ─ ─ ─ ─     ─ ─ ─ ─ ─ ─ ─ ─
  │                 │  │                 │  │                 │
  │ SotA Researcher │  │ Excellence      │  │ Compliance      │
  │ Tech Scout      │  │   Architect     │  │   Reviewer      │
  │ Visionary       │  │ Impact          │  │ Narrative       │
  │   Ideator       │  │   Specialist    │  │   Strategist    │
  │ End-User        │  │ Implementation  │  │ End-User        │
  │   Simulator     │  │   Manager       │  │   Simulator     │
  │ Narrative       │  │                 │  │                 │
  │   Strategist    │  │   GAP_DETECTED──┼──┼──► Consortium   │
   ─ ─ ─ ─ ─ ─ ─ ─     ─ ─ ─ ─ ─ ─ ─ ─  │ │     Scout      │
                                           │  ─ ─ ─ ─ ─ ─ ─ ─
        ┌──────────────────────────────────┘
        │
  ┌─────▼──────────────────┐     ┌────────────────────────────┐
  │  partner_matrix.md     │     │ core_storyline_mapping.md  │
  │  (Consortium Memory)   │     │ (The Roter Faden)          │
  └────────────────────────┘     └────────────────────────────┘

  Support: Call Strategist, Budget Balancer, IP & Legal Expert, Consortium Scout
```

## The Iterative Teaming Loop

1. A **drafting agent** (Excellence, Impact, or Implementation) is writing a section
2. It discovers a capability gap — a WP needs expertise the consortium doesn't have
3. It reports `GAP_DETECTED` to the **Coordinator Hub**
4. Coordinator **pauses** the draft and dispatches the **Consortium Scout**
5. Scout returns candidate partners with profile cards and outreach emails
6. Coordinator updates `partner_matrix.md` and **resumes** the draft with new context

## Workflow Sequence

| # | Workflow | Agents | Description |
|---|---------|--------|-------------|
| **W-pre** | `w_pre_applicant_onboarding` | User (interview) | One-time team profile: who you are, what you bring, your track record |
| **W0** | `w0_ideation_and_gap_analysis` | SotA Researcher, Tech Scout, Visionary Ideator, End-User Simulator | Deep research, solution design, creative ideation, reality check |
| **W0.5** | `w0_5_storyline_lock` | Narrative Strategist | Lock the Roter Faden — the Red Thread all agents follow |
| W1 | `w1_call_discovery` | Call Strategist | Parse and assess the call |
| W2 | `w2_consortium_scouting_loop` | Consortium Scout | Initial consortium assembly |
| W3 | `w3_draft_excellence` | Excellence Architect | Draft Part B Section 1 |
| W4 | `w4_draft_impact_and_pedr` | Impact Specialist | Draft Part B Section 2 |
| W5 | `w5_draft_implementation_wp` | Implementation Manager | Draft Part B Section 3 |
| W6 | `w6_iterative_partner_fill` | Consortium Scout | Mid-draft partner scouting (re-entry) |
| W7 | `w7_red_team_review` | Compliance Reviewer + Narrative Strategist | Score, critique, coherence audit |
| W8 | `w8_final_assembly_and_trim` | Coordinator Hub | Final assembly, page trim, submission package |
| **W9** | `w9_post_submission` | Coordinator Hub | Rebuttal prep, evaluation analysis, lessons learned |

**Not linear** — W6 can be triggered at any point during W3-W5. W7 can be run per-section or at the end. W0/W0.5 always run first.

## Quick Start

### 1. Set up your team profile (once)

If this is your first time using the system, the Coordinator will walk you through **W-pre: Applicant Onboarding** — a short interview about your organisation, team, track record, and strategic focus. This populates `knowledge/applicant_profile.md` and is reused across all future proposals.

### 2. Set up your proposal

Edit these files with your information:
- `knowledge/proposal_concept_live.md` — your proposal idea (even a rough paragraph is enough to start)
- `knowledge/partner_matrix.md` — any partners you already have (can be empty)

### 3. Activate the Coordinator Hub

Load `agents/coordinator-hub.md` as the system prompt for your central agent. It will:
1. Check for an applicant profile (if missing, starts W-pre onboarding)
2. Read your concept (and call text if you have one)
3. Assess what phase you're in
4. Recommend the next workflow step
5. Begin orchestrating

### 4. The system guides you

The Coordinator will take you through the full lifecycle:
- **W0**: The "Brain Trust" researches the landscape, designs the solution, brainstorms angles, and reality-checks with a practitioner persona
- **W0.5**: The Narrative Strategist locks the Red Thread so all agents tell the same story
- **W1-W2**: Call analysis and consortium building
- **W3-W5**: Section drafting (with automatic W6 partner scouting loops when gaps appear)
- **W7-W8**: Red Team review, final assembly, submission package
- **W9**: Post-submission analysis and lessons learned

You'll be asked for input at key decision points (concept approval, partner approvals, scope decisions, budget sign-offs, storyline lock).

## Directory Structure

```
horizon-os/
├── agents/                ← System prompts for all agents
│   ├── coordinator-hub        (central orchestrator)
│   ├── sota-researcher        (SotA orchestrator — dispatches sub-agents)
│   │   ├── sota-literature    (scientific papers, benchmarks, research groups)
│   │   ├── sota-commercial    (products, platforms, companies, open-source)
│   │   ├── sota-eu-projects   (CORDIS, EU project landscape, duplication risk)
│   │   └── sota-regulatory    (standards, regulations, patents, ethics)
│   ├── tech-scout             (solution architecture)
│   ├── visionary-ideator      (creative X-factor)
│   ├── narrative-strategist   (Red Thread / Roter Faden guardian)
│   ├── end-user-simulator     (practitioner reality check)
│   ├── call-strategist        (call parsing + strategy)
│   ├── consortium-scout       (partner search + outreach)
│   ├── excellence-architect   (Part B Section 1)
│   ├── impact-specialist      (Part B Section 2)
│   ├── implementation-manager (Part B Section 3)
│   ├── compliance-reviewer    (Red Team evaluator)
│   ├── budget-balancer        (budget construction + validation)
│   └── ip-legal-expert        (IP, GDPR, ethics, legal)
├── evals/                 ← Evaluation checklists (Red Team uses these)
├── knowledge/             ← Living knowledge base
│   ├── core_storyline_mapping.md  ← THE RED THREAD (Problem→Gap→Obj→Impact)
│   ├── competitor_landscape.md    ← Competing consortia intelligence
│   ├── stakeholder_map.md        ← Full ecosystem mapping
│   ├── applicant_profile.md         ← Your team: who you are, what you bring
│   ├── partner_matrix.md         ← Living consortium roster
│   ├── proposal_concept_live.md  ← Evolving concept note
│   ├── call_text_live.md         ← Parsed call text
│   ├── past_cordis_abstracts.md  ← EU project reference database
│   ├── sota_literature.md       ← Scientific literature per domain
│   ├── sota_commercial.md       ← Products & market landscape per domain
│   ├── sota_regulatory.md       ← Standards, regulations, patents
│   ├── tech_radar/               ← Technology landscape assessments
│   ├── definitions/              ← Reference materials (TRL, taxonomy, open science)
│   ├── eu_policies/              ← Relevant EU policy summaries
│   └── work_programmes/          ← CL3 work programme summaries
├── output/                ← Generated artifacts
│   ├── current_draft/     ← Part B sections (Excellence, Impact, Implementation)
│   ├── budget_drafts/     ← Budget iterations
│   └── partner_outreach/  ← Drafted outreach emails
├── templates/             ← Structural templates for all outputs
└── workflows/             ← Step-by-step workflow definitions (W0 → W9)
```

## Key Design Principles

1. **Think Before You Write** — W0 (Brain Trust) researches, designs, and ideates BEFORE any drafting begins
2. **The Roter Faden** — One Red Thread connects Problem → Gap → Objectives → Methodology → Results → Impact. The Narrative Strategist guards it.
3. **Iterative Teaming** — Consortium building loops back during drafting, not just upfront
4. **Practitioner-First** — The End-User Simulator ensures the proposal works in the field, not just on paper
5. **Strict EU Compliance** — Every eval criterion, formatting rule, and cross-cutting theme is checklistified
6. **Markdown-Driven** — Everything is a readable, versionable Markdown file
7. **Separation of Concerns** — 14 specialist agents + 4 SotA sub-agents; only the Coordinator sees the full picture
8. **Human in the Loop** — The system researches, drafts, and recommends; you decide and submit
