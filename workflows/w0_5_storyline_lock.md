# W0.5: Storyline Lock

> **Owner**: Coordinator Hub
> **Primary Agent**: Narrative Strategist
> **Trigger**: W0 complete, user has given GO decision
> **Output**: Locked `knowledge/core_storyline_mapping.md` — the authoritative Red Thread
> **Runs AFTER W0, BEFORE W1**

---

## Why This Exists

Between ideation (W0) and drafting (W3-W5), there's a critical moment where the proposal's core narrative must be **locked**. Without this, three drafting agents write three different stories. The Narrative Strategist finalizes the Red Thread here, and all subsequent agents are bound by it.

"Lock" doesn't mean "frozen forever" — it means "changes require explicit approval and ripple-through assessment."

## Workflow Steps

### Step 1: Assemble Inputs
- **Actor**: Coordinator Hub → Narrative Strategist
- **Dispatch**:
  ```
  TO: narrative-strategist
  WORKFLOW: w0_5_storyline_lock
  TASK:
    - Finalize the core storyline mapping
    - Verify completeness of Problem → Gap → Objective → Methodology chains
    - Define the narrative arc (hook, tension, turning point, resolution)
    - Define the one-sentence summary
    - Produce the traceability matrix
    - Lock the storyline
  FILES:
    - knowledge/core_storyline_mapping.md (draft from W0)
    - knowledge/proposal_concept_live.md (refined in W0)
    - knowledge/call_text_live.md (if available — may be populated in W1)
    - knowledge/past_cordis_abstracts.md
    - SotA Researcher Innovation Gap Report (from W0)
    - Tech Scout Solution Architecture Report (from W0)
    - Visionary Ideator best ideas (from W0)
    - End-User Simulator feedback (from W0)
  ```

### Step 2: Storyline Finalization
- **Actor**: Narrative Strategist
- **Action**:
  1. **Complete all chains** — Ensure Problem → Gap → Objective → Methodology is fully traced. Flag any chain that ends prematurely (e.g., gap without objective).
  2. **Integrate Ideator's X-Factor** — Select the 1-2 best ideas from the Visionary Ideator and embed them in the narrative (typically as a methodology twist or ambition hook).
  3. **Validate against practitioner feedback** — Ensure the storyline reflects End-User Simulator concerns (e.g., if the Simulator flagged "offline-first architecture," this should appear in the methodology chain).
  4. **Write the one-sentence summary** — The acid test of storyline clarity:
     > "[ACRONYM] will [action verb] [what] to [solve problem] by [novel approach], enabling [specific impact] for [specific users]."
  5. **Define the narrative arc** — How the proposal reads as a story:
     - **Hook** (first paragraph of Excellence): [concrete scenario]
     - **Tension** (SotA / Gap): [what's failing and getting worse]
     - **Turning point** (Objectives / Methodology): [our unique approach]
     - **Resolution** (Impact): [the world after this project]
  6. **Build traceability matrix** — The master mapping table

### Step 3: Traceability Matrix

| Problem | Gap | Objective | Methodology/WP | Building Block | Deliverable | KER | KPI | Impact |
|---------|-----|-----------|----------------|----------------|-------------|-----|-----|--------|
| P1 | G1 | O1 | WP3/T3.1 | BLOCK-001a | D3.2 | KER1 | KPI-1 | I1 |
| P1 | G2 | O2 | WP4/T4.1 | BLOCK-002a | D4.1 | KER2 | KPI-2 | I2 |
| P2 | G3 | O3 | WP5/T5.2 | BLOCK-003a | D5.3 | KER3 | KPI-3 | I3 |

**Every row must be complete.** Empty cells = broken thread.

### Step 4: User Review & Lock
- **Actor**: Coordinator Hub → User
- **Action**: Present the finalized storyline for user approval:
  - One-sentence summary
  - Narrative arc
  - Traceability matrix
  - Any unresolved issues (incomplete chains, competing narratives)
- **Decision**:
  - **APPROVED** → Storyline is LOCKED. Timestamp recorded. All drafting agents receive this as their narrative foundation.
  - **REVISE** → User requests changes. Narrative Strategist revises. Return to Step 2.

### Step 5: Distribute Locked Storyline
- **Actor**: Coordinator Hub
- **Action**: When storyline is locked:
  1. Mark `knowledge/core_storyline_mapping.md` as `STATUS: LOCKED` with timestamp
  2. All subsequent agent dispatches include the locked storyline as mandatory context
  3. Any agent proposing changes to objectives, methodology structure, or impact pathways must route through the Narrative Strategist for ripple-through assessment

## Post-Lock Change Protocol

If a change is needed after lock (e.g., a new partner changes the WP structure, or W1 call analysis reveals a misalignment):

1. **Requesting agent** sends change request to Coordinator
2. **Coordinator** dispatches to Narrative Strategist with the proposed change
3. **Narrative Strategist** performs ripple-through assessment:
   - Which chains are affected?
   - Which sections need updating?
   - Is the one-sentence summary still valid?
   - Does the change break the narrative arc?
4. **Narrative Strategist** reports: `CHANGE_ABSORBED` (minor, no ripple) or `RIPPLE_DETECTED` (lists all affected elements)
5. **Coordinator** manages the updates across affected agents

## Exit Criteria
- [ ] `knowledge/core_storyline_mapping.md` complete with all chains
- [ ] One-sentence summary defined and approved by user
- [ ] Narrative arc defined (hook, tension, turning point, resolution)
- [ ] Traceability matrix complete — no empty cells in any row
- [ ] User has approved and locked the storyline
- [ ] STATUS: LOCKED with timestamp in core_storyline_mapping.md
- [ ] All agents notified of the locked storyline
