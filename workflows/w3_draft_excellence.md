# W3: Draft Excellence Section

> **Owner**: Coordinator Hub
> **Primary Agent**: Excellence Architect
> **Trigger**: W2 complete (or sufficient consortium to begin); call text parsed
> **Output**: `output/current_draft/1_Excellence.md`

---

## Workflow Steps

### Step 1: Dispatch Excellence Architect
- **Actor**: Coordinator Hub → Excellence Architect
- **Dispatch**:
  ```
  TO: excellence-architect
  WORKFLOW: w3_draft_excellence
  TASK: Draft Part B Section 1 (Excellence)
  CONTEXT:
    call_id: "[call ID]"
    relevant_partners: [from partner_matrix.md]
    constraints:
      page_limit: [N pages]
      formatting: "see evals/page_limit_and_formatting.md"
  FILES:
    - knowledge/call_text_live.md
    - knowledge/proposal_concept_live.md
    - knowledge/partner_matrix.md
    - knowledge/past_cordis_abstracts.md
    - templates/part_B_1_excellence.md
    - evals/he_evaluation_criteria.md (Criterion 1)
    - evals/dnsh_and_gender_checklist.md
  ```

### Step 2: Monitor for Gap Detection
- **Actor**: Coordinator Hub
- **Trigger**: Excellence Architect reports `GAP_DETECTED`
- **Action**:
  1. Pause W3
  2. Log the gap in `partner_matrix.md` Gap Tracker
  3. Dispatch W6 (Iterative Partner Fill)
  4. Wait for W6 to complete
  5. Update partner context
  6. Resume W3 by re-dispatching Excellence Architect with updated context

### Step 3: Receive Draft
- **Actor**: Excellence Architect → Coordinator Hub
- **Status**: `OK` (draft complete) or `REVIEW_NEEDED` (draft complete with concerns)
- **Deliverable**: `output/current_draft/1_Excellence.md`

### Step 4: Quick Compliance Check
- **Actor**: Coordinator Hub
- **Action**: Before advancing, verify:
  - [ ] Page count is within budget
  - [ ] All Criterion 1 sub-criteria are addressed
  - [ ] Partner references match `partner_matrix.md`
  - [ ] Objectives are SMART
  - [ ] Gender dimension is addressed
  - [ ] Open science practices described
  - If issues found → return to Excellence Architect for revision

### Step 5: Advance
- **Actor**: Coordinator Hub
- **Action**: Mark Excellence as `review` (pending full Red Team) or `complete` (if quick check passed cleanly). Advance to W4.

## Pause/Resume Protocol
If W3 is paused for gap scouting:
- Save the current draft state (even partial)
- Record which sub-section the Architect was working on
- When resuming, provide the Architect with:
  - The partial draft
  - The new partner information
  - Instruction to continue from where they left off

## Exit Criteria
- [ ] `output/current_draft/1_Excellence.md` exists and follows template structure
- [ ] Within page budget
- [ ] No unresolved `GAP_DETECTED` flags
- [ ] Quick compliance check passed
