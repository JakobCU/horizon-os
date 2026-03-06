# W6: Iterative Partner Fill (Mid-Draft Scouting)

> **Owner**: Coordinator Hub
> **Primary Agent**: Consortium Scout
> **Trigger**: Any drafting agent (W3/W4/W5) reports `GAP_DETECTED`
> **Output**: Updated `knowledge/partner_matrix.md`, outreach emails in `output/partner_outreach/`

---

## Context

This workflow is the **re-entry point** for consortium scouting during active drafting. Unlike W2 (initial consortium build), W6 is triggered mid-draft when a specific capability gap is discovered by the Excellence Architect, Impact Specialist, or Implementation Manager.

This is the heart of the iterative teaming loop.

## Workflow Steps

### Step 1: Receive Gap Specification
- **Actor**: Coordinator Hub
- **Input**: `GAP_DETECTED` report from a drafting agent containing:
  - Which WP/task needs the capability
  - What the capability is
  - Ideal partner profile (org type, TRL range, country, experience)
  - Urgency level (`blocking_draft` | `nice_to_have` | `strategic`)
- **Action**: Log gap in `partner_matrix.md` Gap Tracker with status `SCOUTING`

### Step 2: Check Existing Candidates
- **Actor**: Coordinator Hub
- **Action**: Before dispatching the Scout, check if an existing partner in the matrix (status: `CANDIDATE` or `OUTREACH_SENT`) could fill this gap. If yes → skip scouting, reassign partner. If no → proceed.

### Step 3: Dispatch Consortium Scout
- **Actor**: Coordinator Hub → Consortium Scout
- **Dispatch**:
  ```
  TO: consortium-scout
  WORKFLOW: w6_iterative_partner_fill
  TASK: Find partners matching gap specification
  GAP:
    wp: "[WP from drafting agent report]"
    capability: "[capability description]"
    ideal_profile: { ... }
    urgency: "[level]"
    budget_ceiling_eur: [amount]
    person_months_max: [PM]
  CONTEXT:
    call_id: "[call ID]"
    current_consortium: [current partners from matrix]
    paused_workflow: "[w3/w4/w5]"
    paused_section: "[section being drafted]"
  ```

### Step 4: Evaluate Scout Results
- **Actor**: Coordinator Hub
- **Action**:
  - `OK` (STRONG_FIT found) → Add candidates to matrix, draft outreach, notify user
  - `PARTIAL_MATCH` → Present GOOD_FIT candidates to user for decision
  - `NO_CANDIDATES` →
    - If Round < 3: Relax constraints, dispatch Scout again (Round 2/3)
    - If Round = 3: Escalate to user with options:
      - Restructure the WP (merge tasks into adjacent WPs)
      - Adjust proposal scope
      - User provides a lead from their own network
      - Accept the gap and write around it (last resort)
  - `BLOCKED` → Clarify gap specification with drafting agent, re-dispatch

### Step 5: Update Partner Matrix
- **Actor**: Coordinator Hub
- **Action**: Merge Scout's matrix update rows into `partner_matrix.md`. Update Gap Tracker status.

### Step 6: Save Outreach Drafts
- **Actor**: Coordinator Hub
- **Action**: Save drafted outreach emails to `output/partner_outreach/[org_acronym]_[country].md`

### Step 7: Resume Paused Workflow
- **Actor**: Coordinator Hub
- **Action**:
  1. Update the paused drafting agent's context with new partner information
  2. Re-dispatch the drafting agent to resume from where they paused
  3. Provide: updated `partner_matrix.md`, the new partner's profile card, specific instructions on how to integrate them into the section being drafted

## Multi-Gap Handling

If multiple gaps are detected simultaneously:
- Triage by urgency: `blocking_draft` first, then `strategic`, then `nice_to_have`
- Scout for `blocking_draft` gaps immediately
- Queue `nice_to_have` gaps for batch scouting after draft sections stabilize
- A single Scout dispatch can include multiple gaps if they share similar profiles

## Exit Criteria
- [ ] Gap status in `partner_matrix.md` updated from `SCOUTING` to `CANDIDATE`/`OUTREACH_SENT` (or `ESCALATED` if no match found)
- [ ] Outreach emails saved (if candidates found)
- [ ] Paused workflow resumed with updated context
- [ ] Coordinator `proposal_state.paused_workflows` cleared
