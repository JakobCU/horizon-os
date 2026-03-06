# W8: Final Assembly & Trim

> **Owner**: Coordinator Hub (direct involvement)
> **Supporting Agents**: Compliance Reviewer (final check), Budget Balancer (final numbers)
> **Trigger**: W7 complete, all CRITICAL/MAJOR issues resolved
> **Output**: Submission-ready Part B document

---

## Workflow Steps

### Step 1: Assembly
- **Actor**: Coordinator Hub
- **Action**: Merge all sections into final document structure:
  1. **Part B-1**: Excellence (Section 1) + Impact (Section 2)
  2. **Part B-2**: Implementation (Section 3)
  3. Verify section numbering and headers match the official template
  4. Ensure table of contents (if required) is accurate

### Step 2: Consistency Pass
- **Actor**: Coordinator Hub
- **Checks**:
  - [ ] **Acronym consistency**: All partner acronyms match `partner_matrix.md` throughout
  - [ ] **Terminology**: No conflicting terms for the same concept across sections
  - [ ] **Cross-references**: "As described in Section X.Y" references point to correct locations
  - [ ] **Objective-WP-KER alignment table**: Create or verify a master mapping table
  - [ ] **No placeholder text**: Search for "[TO BE FILLED]", "[TBD]", "XXX", "[INSERT]"
  - [ ] **No tracked changes or comments**: Clean document

### Step 3: Page Limit Enforcement
- **Actor**: Coordinator Hub
- **Action**: Count pages per section against limits from `evals/page_limit_and_formatting.md`:

  | Section | Limit | Current | Status |
  |---------|-------|---------|--------|
  | Part B-1 (Excellence + Impact) | [N] | [N] | OK / OVER by [N] |
  | Part B-2 (Implementation) | [N] | [N] | OK / OVER by [N] |

- **If OVER**: Trim in this priority order:
  1. Remove redundant text (same idea stated twice across sections)
  2. Compress tables (merge rows, abbreviate)
  3. Tighten prose (eliminate filler words, shorten sentences)
  4. Reduce references to most essential only
  5. Move detailed tables to a more compact format
  - **Never trim**: Objectives, methodology core, WP descriptions, budget tables

### Step 4: Fix MINOR Issues
- **Actor**: Coordinator Hub
- **Action**: Address MINOR issues logged in W7:
  - Formatting inconsistencies
  - Missing figure captions
  - Acronym not defined on first use
  - Minor clarity improvements

### Step 5: Final Numbers Lockdown
- **Actor**: Coordinator Hub → Budget Balancer
- **Action**: Lock final budget numbers:
  - [ ] All person-month tables are internally consistent
  - [ ] Budget summary table matches partner-level budgets
  - [ ] Indirect costs calculated correctly
  - [ ] Total matches what will be entered in the portal
  - Output: Final `output/budget_drafts/v_final_person_months.csv`

### Step 6: Abstract & Portal Metadata
- **Actor**: Coordinator Hub
- **Action**: Prepare submission portal inputs:
  - [ ] Abstract (≤2000 characters) — summarize from Excellence + Impact
  - [ ] Keywords for portal search
  - [ ] Ethics self-assessment answers
  - [ ] Call-specific questionnaires (if any)

### Step 7: Final Compliance Sweep
- **Actor**: Coordinator Hub → Compliance Reviewer
- **Action**: Rapid final check (not full review — focused on fixes made since W7):
  - [ ] CRITICAL/MAJOR fixes verified
  - [ ] Page limits met
  - [ ] No new issues introduced during trimming

### Step 8: Submission Package
- **Actor**: Coordinator Hub → User
- **Deliverables**:
  - [ ] Part B-1 (final, within page limit)
  - [ ] Part B-2 (final, within page limit)
  - [ ] Budget tables (final)
  - [ ] Abstract text (final)
  - [ ] Partner matrix (final) — for reference during portal submission
  - [ ] Outstanding items list (LOIs still pending, ethics issues to flag)
  - [ ] Final score estimate and risk assessment

### Step 9: User Submission
- **Actor**: User
- **Action**: User uploads to the Funding & Tenders Portal. The system does NOT submit automatically.

## Exit Criteria
- [ ] All documents finalized and within page limits
- [ ] No placeholder text remaining
- [ ] Budget locked and consistent
- [ ] Abstract prepared
- [ ] Final compliance sweep passed
- [ ] User has received complete submission package
- [ ] `proposal_state.phase` set to `SUBMITTED` (after user confirms upload)
