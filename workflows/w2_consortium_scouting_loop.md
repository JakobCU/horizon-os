# W2: Consortium Scouting Loop (Initial Build)

> **Owner**: Coordinator Hub
> **Primary Agent**: Consortium Scout
> **Trigger**: W1 complete; user has confirmed the call; initial consortium needs to be assembled
> **Output**: Populated `knowledge/partner_matrix.md` with initial consortium

---

## Workflow Steps

### Step 1: Define Consortium Requirements
- **Actor**: Coordinator Hub
- **Action**: Based on `knowledge/call_text_live.md` and `knowledge/proposal_concept_live.md`, define:
  - Minimum number of partners (call requirement, typically ≥3 from different EU MS)
  - Required organization types (LEAs, SMEs, universities/RTOs)
  - Required capabilities per WP (from preliminary WP overview)
  - Geographic requirements (widening, diversity)
  - Budget envelope per partner type
  - Any mandatory partner types specified in the call

### Step 2: Identify Known Partners
- **Actor**: Coordinator Hub (with user input)
- **Action**: Add any partners the user already has to `partner_matrix.md` with status `CONFIRMED` or `CANDIDATE`. These are the starting point.

### Step 3: Gap Analysis
- **Actor**: Coordinator Hub
- **Action**: Compare current consortium against requirements from Step 1. Generate gap specifications for each unfilled need.

### Step 4: Dispatch Consortium Scout
- **Actor**: Coordinator Hub → Consortium Scout
- **Action**: For each gap, dispatch the Scout with a structured gap specification:
  ```
  TO: consortium-scout
  WORKFLOW: w2_consortium_scouting_loop
  TASK: Find partners matching gap specification
  GAP:
    wp: "[WP]"
    capability: "[description]"
    ideal_profile: { ... }
    urgency: "blocking_draft"
    budget_ceiling_eur: [amount]
    person_months_max: [PM]
  ```

### Step 5: Evaluate Scout Results
- **Actor**: Coordinator Hub
- **Action**: Review partner profile cards returned by the Scout:
  - `STRONG_FIT` → Add to matrix as `CANDIDATE`, prepare outreach
  - `GOOD_FIT` → Add to matrix as `CANDIDATE`, flag for user review
  - `CONDITIONAL` → Present to user for decision
  - `NOT_RECOMMENDED` → Discard with reason logged

### Step 6: Outreach Decision
- **Actor**: User (via Coordinator Hub)
- **Action**: User reviews candidates and approves/rejects outreach. Approved candidates move to `OUTREACH_SENT`.

### Step 7: Consortium Assessment
- **Actor**: Coordinator Hub
- **Action**: Assess consortium completeness:
  - All mandatory partner types present? (if not → repeat Step 4 with refined gaps)
  - Geographic diversity sufficient?
  - Budget envelope realistic?
  - End-user involvement adequate?

### Step 8: Ready for Drafting?
- **Decision point**:
  - **YES**: At least 6-8 core partners identified (confirmed or outreach sent). Enough to begin drafting with placeholders. → Advance to W3.
  - **NO**: Critical gaps remain. → Return to Step 4 with refined gap specifications.
  - **PARTIAL**: Can begin drafting some sections. → Advance to W3 but flag that W6 (iterative fill) will be needed.

## Loop Limit
- Maximum 3 full scouting rounds per gap before escalating to user
- If consortium cannot be assembled after 3 rounds across all gaps, Coordinator recommends aborting or fundamentally restructuring the proposal

## Exit Criteria
- [ ] `partner_matrix.md` has ≥6 partners in status `CONFIRMED`, `LOI_RECEIVED`, or `OUTREACH_SENT`
- [ ] All mandatory partner types are covered (or explicitly waived by user)
- [ ] Gap tracker shows no `blocking_draft` gaps remaining
- [ ] User has approved the consortium composition (or approved proceeding with caveats)
- [ ] Balance dashboard meets minimum thresholds (≥3 countries, ≥1 widening, org type mix)
