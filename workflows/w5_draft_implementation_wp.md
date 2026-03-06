# W5: Draft Implementation & Work Packages

> **Owner**: Coordinator Hub
> **Primary Agent**: Implementation Manager
> **Supporting Agents**: Budget Balancer, IP & Legal Expert
> **Trigger**: W3 and W4 complete (or sufficiently stable)
> **Output**: `output/current_draft/3_Implementation.md`, `output/budget_drafts/v[N]_person_months.csv`

---

## Workflow Steps

### Step 1: Dispatch Implementation Manager
- **Actor**: Coordinator Hub → Implementation Manager
- **Dispatch**:
  ```
  TO: implementation-manager
  WORKFLOW: w5_draft_implementation_wp
  TASK: Draft Part B Section 3 (Implementation) — WPs, governance, consortium, resources
  CONTEXT:
    call_id: "[call ID]"
    partners: [full partner_matrix.md]
    constraints:
      page_limit: [N pages]
      duration: [months]
      total_budget: EUR [amount]
  FILES:
    - knowledge/call_text_live.md
    - knowledge/proposal_concept_live.md
    - knowledge/partner_matrix.md
    - templates/part_B_3_implementation.md
    - templates/budget_calculator_RIA.md
    - evals/he_evaluation_criteria.md (Criterion 3)
    - evals/security_scrutiny_checklist.md
    - output/current_draft/1_Excellence.md (methodology → WP mapping)
    - output/current_draft/2_Impact.md (KERs → deliverable mapping)
  ```

### Step 2: Monitor for Gap Detection
- **Actor**: Coordinator Hub
- **Trigger**: Implementation Manager reports `GAP_DETECTED`
- **Note**: This is the MOST COMMON trigger for W6. Implementation is where capability gaps become concrete because you must assign real tasks to real partners.
- **Action**: Same pause/scout/resume protocol

### Step 3: Budget Construction
- **Actor**: Coordinator Hub → Budget Balancer
- **Trigger**: Implementation Manager has produced PM allocation tables
- **Action**: Budget Balancer builds the full budget from PMs and validates against rules
- **Output**: `output/budget_drafts/v[N]_person_months.csv`
- **Iterate**: If budget is over ceiling or imbalanced, coordinate with Implementation Manager to adjust

### Step 4: IP & Security Review
- **Actor**: Coordinator Hub → IP & Legal Expert (on demand)
- **Trigger**: If the Implementation section describes data handling, IP-generating tasks, or sensitive operations
- **Action**: IP & Legal Expert reviews and advises on:
  - IP ownership per deliverable
  - Data protection roles
  - Security handling plan text

### Step 5: Cross-Reference Check
- **Actor**: Coordinator Hub
- **Verify**:
  - [ ] Every objective (Excellence) maps to at least one WP
  - [ ] Every KER (Impact) maps to at least one deliverable
  - [ ] Every partner in `partner_matrix.md` with status `CONFIRMED` or `LOI_RECEIVED` appears in at least 2 WPs
  - [ ] Person-months sum correctly
  - [ ] Budget sums match across tables

### Step 6: Receive Draft & Advance
- **Deliverable**: `output/current_draft/3_Implementation.md`
- **Advance to**: W7 (Red Team Review)

## Exit Criteria
- [ ] `output/current_draft/3_Implementation.md` complete with all WP descriptions
- [ ] Budget validated by Budget Balancer
- [ ] No unresolved `GAP_DETECTED` flags
- [ ] Cross-references verified (Objectives ↔ WPs ↔ KERs ↔ Deliverables)
- [ ] Security handling plan included
- [ ] Within page budget
