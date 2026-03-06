# W1: Call Discovery & Strategic Assessment

> **Owner**: Coordinator Hub
> **Primary Agent**: Call Strategist
> **Trigger**: User provides a call ID or raw call text
> **Output**: Populated `knowledge/call_text_live.md`

---

## Workflow Steps

### Step 1: Receive Call Input
- **Input**: User pastes raw call text or provides a Funding & Tenders Portal link
- **Actor**: User → Coordinator Hub

### Step 2: Parse & Structure Call
- **Actor**: Coordinator Hub → Call Strategist
- **Action**: Call Strategist parses the raw text and populates `knowledge/call_text_live.md`:
  - Metadata (call ID, instrument, deadline, budget)
  - Expected outcomes (verbatim from call)
  - Scope (verbatim from call)
  - Specific conditions (page limits, consortium requirements, TRL, security)
  - Keyword extraction with frequency analysis
  - Mandatory vs. optional elements table

### Step 3: Strategic Assessment
- **Actor**: Call Strategist
- **Action**: Produce strategic assessment:
  - Fit score (1-5) based on user's domain and capabilities
  - Competitive landscape (expected number of proposals, budget per grant)
  - Recommended positioning angle
  - Key risks and red flags
  - Consortium requirements analysis (minimum partners, mandatory LEA involvement, widening)

### Step 4: Alignment Check (if proposal concept exists)
- **Actor**: Call Strategist
- **Action**: If `knowledge/proposal_concept_live.md` already has content, cross-reference against call requirements:
  - Map proposal objectives to call expected outcomes
  - Identify any expected outcome NOT addressed by the concept
  - Flag any proposal element NOT requested by the call (scope creep risk)

### Step 5: Report to Coordinator
- **Actor**: Call Strategist → Coordinator Hub
- **Status**: `OK` (call is suitable) | `MISALIGNMENT_DETECTED` (concept doesn't match call) | `CALL_NOT_SUITABLE` (poor fit)
- **Coordinator Action**: Update `proposal_state`, report to user, recommend next step (typically W2 or concept revision)

## Exit Criteria
- [ ] `knowledge/call_text_live.md` is fully populated
- [ ] Strategic assessment delivered to Coordinator
- [ ] User has confirmed proceed/abort decision
- [ ] If proceeding: Coordinator advances to W2 (consortium scouting) or W3 (drafting if consortium exists)
