# W0: Ideation & Gap Analysis

> **Owner**: Coordinator Hub
> **Primary Agents**: SotA Researcher, Tech Scout, Visionary Ideator, End-User Simulator
> **Trigger**: User has a rough proposal idea + a candidate call topic (or wants to explore)
> **Output**: Populated `knowledge/core_storyline_mapping.md`, `knowledge/tech_radar/`, Innovation Gap Report, Solution Architecture, Idea Cards
> **Runs BEFORE**: W1 (Call Discovery) — this is the creative foundation phase

---

## Why W0 Exists

Most proposal systems start at "write Section 1." That's too late. By the time you're writing, you should already know:
- What the real problem is (not your assumption of the problem)
- What's been tried before and why it failed or fell short
- Where the precise innovation gap sits
- What technological building blocks could cross that gap
- What creative angle makes your proposal stand out
- Whether a real practitioner would actually want what you're proposing

W0 answers all of this before a single line of proposal text is written.

## Workflow Steps

### Step 1: Concept Intake
- **Actor**: User → Coordinator Hub
- **Input**: User provides initial concept — can be as rough as a paragraph or as developed as a full concept note
- **Action**: Coordinator populates (or reviews existing) `knowledge/proposal_concept_live.md` with:
  - Problem area
  - Initial solution idea
  - Target end-users
  - Candidate call topic(s) if known
  - Any existing partners

### Step 2: State-of-the-Art Deep Dive (Pass 1 — Landscape Scan)
- **Actor**: Coordinator Hub → SotA Researcher (orchestrator)
- **Dispatch**:
  ```
  TO: sota-researcher
  WORKFLOW: w0_ideation_and_gap_analysis
  PASS: 1_landscape
  TASK:
    - Define search domains from concept and call text
    - Dispatch sub-agents in parallel:
      → sota-literature: academic papers, benchmarks, research groups
      → sota-commercial: products, platforms, companies, open-source
      → sota-eu-projects: CORDIS past/ongoing projects, duplication risk
      → sota-regulatory: standards, regulations, patents, ethical frameworks
    - Cross-reference and synthesize into Innovation Gap definitions
    - Populate knowledge files (past_cordis_abstracts, competitor_landscape,
      sota_literature, sota_commercial, sota_regulatory)
  CONTEXT:
    concept: [from proposal_concept_live.md]
    candidate_call: [if known]
  ```
- **Output**: Innovation Gap Report with structured gap definitions from all four source types
- **Note**: A deeper Pass 2 (per-WP deep dive) runs before W3 drafting to produce citable SotA briefs for the Excellence Architect

### Step 3: Solution Architecture (parallel with Step 4)
- **Actor**: Coordinator Hub → Tech Scout
- **Dispatch**:
  ```
  TO: tech-scout
  WORKFLOW: w0_ideation_and_gap_analysis
  TASK:
    - Take Innovation Gaps from SotA Researcher
    - Design solution building blocks for each gap
    - Assess TRL pathways
    - Identify capability gaps (feed consortium scouting)
    - Populate knowledge/tech_radar/ with technology assessments
  CONTEXT:
    gaps: [from SotA Researcher output]
    concept: [from proposal_concept_live.md]
  ```
- **Output**: Solution Architecture Report with building blocks, risks, capability gaps

### Step 4: Creative Ideation (parallel with Step 3)
- **Actor**: Coordinator Hub → Visionary Ideator
- **Dispatch**:
  ```
  TO: visionary-ideator
  WORKFLOW: w0_ideation_and_gap_analysis
  TASK:
    - Review Innovation Gaps and initial concept
    - Generate 3-5 novel angles / X-factors
    - Identify differentiators vs. likely competing proposals
    - Suggest narrative hooks
  CONTEXT:
    gaps: [from SotA Researcher output]
    concept: [from proposal_concept_live.md]
    competitor_landscape: [from SotA Researcher]
  ```
- **Output**: Ideation Report with scored idea cards

### Step 5: Practitioner Reality Check
- **Actor**: Coordinator Hub → End-User Simulator
- **Dispatch**:
  ```
  TO: end-user-simulator
  WORKFLOW: w0_ideation_and_gap_analysis
  TASK:
    - Adopt relevant practitioner persona(s)
    - Review the proposed concept and solution architecture
    - Flag operational impossibilities
    - Validate that the problem is real from a practitioner perspective
    - Validate that the proposed solution would be wanted/used
  CONTEXT:
    concept: [from proposal_concept_live.md]
    solution_architecture: [from Tech Scout]
    target_users: [from concept note]
  ```
- **Output**: Practitioner Review with persona-based feedback

### Step 6: Synthesis & Concept Refinement
- **Actor**: Coordinator Hub
- **Action**: Synthesize all four inputs:
  1. **Refine the concept** — Update `proposal_concept_live.md` based on:
     - SotA Researcher's gap definitions → sharper objectives
     - Tech Scout's building blocks → clearer methodology preview
     - Ideator's best ideas → unique selling proposition
     - End-User feedback → realistic scope and validation approach
  2. **Initial storyline** — Begin drafting `knowledge/core_storyline_mapping.md`:
     - Problem chain ← user concept + SotA evidence
     - Gap chain ← SotA Researcher
     - Objective chain ← refined concept
     - Methodology chain ← Tech Scout blocks
     - (Result and Impact chains are filled later during drafting)
  3. **Partner requirements** — From Tech Scout's capability gaps, compile initial partner requirements for W2
  4. **Decision point**: Present to user:
     - "Here's what we found. Here's where the innovation gap is. Here's our proposed angle. Here's what a practitioner thinks. Do you want to proceed?"

### Step 7: User Go/No-Go
- **Actor**: User
- **Decision**:
  - **GO** → Advance to W0.5 (Storyline Lock), then W1 (Call Discovery)
  - **PIVOT** → User provides new direction; return to Step 2 with refined scope
  - **ABORT** → The concept doesn't have enough innovation gap or the competition is too strong

## Exit Criteria
- [ ] SotA Research Pass 1 complete — Innovation Gaps defined from all four source types
- [ ] `knowledge/past_cordis_abstracts.md` populated (EU Project Reviewer)
- [ ] `knowledge/sota_literature.md` populated (Literature Reviewer)
- [ ] `knowledge/sota_commercial.md` populated (Commercial Reviewer)
- [ ] `knowledge/sota_regulatory.md` populated (Regulatory Reviewer)
- [ ] `knowledge/competitor_landscape.md` populated
- [ ] Solution Architecture designed — building blocks, TRL pathways, risks identified
- [ ] Creative ideas generated and feasibility-assessed
- [ ] Practitioner review completed — no showstoppers (or showstoppers addressed)
- [ ] `knowledge/proposal_concept_live.md` updated with refined concept
- [ ] `knowledge/core_storyline_mapping.md` initialized (Problem → Gap → Objective → Methodology chains)
- [ ] `knowledge/tech_radar/` populated with key technology assessments
- [ ] User has approved the refined concept (GO decision)
