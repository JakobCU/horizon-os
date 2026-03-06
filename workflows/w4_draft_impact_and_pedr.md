# W4: Draft Impact Section & PEDR Chains

> **Owner**: Coordinator Hub
> **Primary Agent**: Impact Specialist
> **Trigger**: W3 complete (or can run in parallel if Excellence is stable)
> **Output**: `output/current_draft/2_Impact.md`

---

## Workflow Steps

### Step 1: Dispatch Impact Specialist
- **Actor**: Coordinator Hub → Impact Specialist
- **Dispatch**:
  ```
  TO: impact-specialist
  WORKFLOW: w4_draft_impact_and_pedr
  TASK: Draft Part B Section 2 (Impact) with full PEDR chains for each KER
  CONTEXT:
    call_id: "[call ID]"
    relevant_partners: [from partner_matrix.md]
    constraints:
      page_limit: [N pages]
  FILES:
    - knowledge/call_text_live.md
    - knowledge/proposal_concept_live.md
    - knowledge/partner_matrix.md
    - knowledge/definitions/key_impact_pathways.md
    - templates/part_B_2_impact.md
    - templates/pedr_framework.md
    - evals/he_evaluation_criteria.md (Criterion 2)
    - output/current_draft/1_Excellence.md (for consistency)
  ```

### Step 2: Monitor for Gap Detection
- **Actor**: Coordinator Hub
- **Trigger**: Impact Specialist reports `GAP_DETECTED` (typically: missing exploitation owner for a KER)
- **Action**: Same pause/scout/resume protocol as W3 (see W3 Step 2)

### Step 3: PEDR Quality Check
- **Actor**: Coordinator Hub
- **Verify**: Each KER has a complete PEDR chain with:
  - [ ] Named target users (not generic "stakeholders")
  - [ ] Quantified KPIs where possible
  - [ ] Credible exploitation owner (partner in consortium)
  - [ ] Realistic timeline
  - [ ] Link to call expected outcomes

### Step 4: Cross-Reference with Excellence
- **Actor**: Coordinator Hub
- **Verify**:
  - [ ] Every KER in Impact corresponds to a described result in Excellence
  - [ ] Terminology is consistent
  - [ ] TRL claims match
  - [ ] Objective-KER-WP mapping is coherent

### Step 5: Receive Draft & Advance
- **Deliverable**: `output/current_draft/2_Impact.md`
- **Advance to**: W5 (Implementation)

## Exit Criteria
- [ ] `output/current_draft/2_Impact.md` exists and follows template
- [ ] All KERs have PEDR chains
- [ ] Exploitation owners assigned and verified against `partner_matrix.md`
- [ ] Within page budget
- [ ] Cross-referenced with Excellence section — no inconsistencies
