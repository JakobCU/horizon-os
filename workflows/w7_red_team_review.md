# W7: Red Team Review

> **Owner**: Coordinator Hub
> **Primary Agent**: Compliance Reviewer
> **Supporting Agents**: Budget Balancer (budget check), IP & Legal Expert (if triggered)
> **Trigger**: All three sections drafted (W3+W4+W5 complete), or on-demand per section
> **Output**: Issue list with severity ratings and fix recommendations

---

## Workflow Steps

### Step 1: Pre-Flight Check
- **Actor**: Coordinator Hub
- **Action**: Verify all three draft sections exist in `output/current_draft/`:
  - [ ] `1_Excellence.md`
  - [ ] `2_Impact.md`
  - [ ] `3_Implementation.md`
- If any section is missing, the review can proceed on available sections but must be repeated when complete.

### Step 2: Dispatch Compliance Reviewer
- **Actor**: Coordinator Hub → Compliance Reviewer
- **Dispatch**:
  ```
  TO: compliance-reviewer
  WORKFLOW: w7_red_team_review
  TASK: Full Red Team review of all Part B sections
  FILES:
    - output/current_draft/1_Excellence.md
    - output/current_draft/2_Impact.md
    - output/current_draft/3_Implementation.md
    - knowledge/call_text_live.md (for call alignment check)
    - knowledge/partner_matrix.md (for consortium consistency check)
    - evals/he_evaluation_criteria.md
    - evals/page_limit_and_formatting.md
    - evals/dnsh_and_gender_checklist.md
    - evals/security_scrutiny_checklist.md
  ```

### Step 3: Parallel Budget Audit
- **Actor**: Coordinator Hub → Budget Balancer
- **Action**: Final budget validation (runs in parallel with Compliance Review)
- **Checks**: All budget rules from `templates/budget_calculator_RIA.md`

### Step 4: Receive Review Results
- **Actor**: Compliance Reviewer → Coordinator Hub
- **Output**: Scored evaluation with issues list (CRITICAL / MAJOR / MINOR)

### Step 5: Triage Issues
- **Actor**: Coordinator Hub
- **Action**: Sort issues by severity and route to responsible agent:

  | Severity | Action |
  |----------|--------|
  | CRITICAL | Must fix before submission. Dispatch to responsible drafting agent immediately. |
  | MAJOR | Should fix. Dispatch to responsible agent with priority. |
  | MINOR | Fix during W8 (final assembly). Log for later. |

### Step 6: Fix Cycle
- **Actor**: Coordinator Hub → [relevant drafting agents]
- **Action**: For each CRITICAL/MAJOR issue:
  1. Dispatch the responsible agent with the specific issue and suggested fix
  2. Agent revises the section
  3. Coordinator verifies the fix
  4. If fix introduces new issues → re-run partial review on that section
- **Limit**: Maximum 2 full review cycles. After that, only CRITICAL issues block submission.

### Step 7: Final Score Estimate
- **Actor**: Coordinator Hub
- **Action**: After fixes, compile final estimated scores:
  - Excellence: X/5
  - Impact: X/5
  - Implementation: X/5
  - Total: X/15
  - Threshold met? (typically 12/15 with 4/5 per criterion)
- Report to user with recommendation: SUBMIT / REVISE / ABORT

## Exit Criteria
- [ ] All CRITICAL issues resolved
- [ ] All MAJOR issues resolved or explicitly accepted by user
- [ ] MINOR issues logged for W8
- [ ] Final score estimate ≥ threshold (or user accepts risk)
- [ ] Budget audit passed
- [ ] Advance to W8
