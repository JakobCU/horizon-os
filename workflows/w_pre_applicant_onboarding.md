# W-pre: Applicant Onboarding

> **Owner**: Coordinator Hub
> **Primary Actor**: User (interview-driven)
> **Trigger**: First use of the system by a new team, or when no `knowledge/applicant_profile.md` exists
> **Output**: Populated `knowledge/applicant_profile.md`
> **Runs BEFORE**: Everything else — this is the foundation layer

---

## Why This Exists

The system can research calls, design solutions, and draft proposals — but it cannot do any of this well without knowing **who you are**. Your organisation's strengths, track record, team, and strategic focus shape every decision: which calls to pursue, which partners to scout, how to position the consortium, and what to claim in the proposal.

This workflow runs **once per team** (not per proposal). The resulting profile is reused across all future proposals and updated as your organisation evolves.

## Workflow Steps

### Step 1: Check for Existing Profile
- **Actor**: Coordinator Hub
- **Action**: Check if `knowledge/applicant_profile.md` has been populated beyond the template
- **If populated**: Ask the user if they want to review/update it, or proceed with the existing profile
- **If empty/template**: Begin the onboarding interview (Step 2)

### Step 2: Structured Interview
- **Actor**: Coordinator Hub → User
- **Action**: Walk the user through the following question blocks. Ask conversationally, not as a form dump. Adapt follow-up questions based on answers.

#### Block A: Organisation Basics
- Organisation name, type (university, RTO, SME, large industry, public body, NGO), country
- PIC number (if registered on EU Funding & Tenders Portal)
- Brief description (1-2 sentences: what do you do?)

#### Block B: Strategic Focus
- Core research/business domains (e.g., "cybersecurity, critical infrastructure protection, AI for public safety")
- Key technologies and methods you specialise in
- Strategic priorities for the coming years — what kind of projects do you *want* to do?
- Are there topics or domains you explicitly want to avoid?

#### Block C: Key Personnel
- Who are the 3-5 people most likely to be involved in proposals?
- For each: name, role/title, core expertise, notable publications or project roles
- Who would typically be the PI / scientific coordinator?

#### Block D: Track Record
- Past EU-funded projects (name, programme, role: coordinator/partner, topic area)
- Other relevant funded projects (national, bilateral, industry)
- Success rate if known (proposals submitted vs. funded in the last 3-5 years)
- Key results, demonstrators, or outputs from past projects that could be referenced

#### Block E: Assets & Infrastructure
- Labs, testbeds, datasets, platforms, or tools you can contribute to proposals
- Existing IP, patents, or licensed technologies relevant to your domains
- Access to end-user networks, living labs, or pilot sites

#### Block F: Network & Partnerships
- Trusted partners you've worked with before (name, country, type, relationship strength)
- Cluster memberships, associations, or networks (e.g., ECSO, EOS, EARTO)
- Advisory board members or policy contacts

#### Block G: Practical Constraints
- Typical person-month capacity available for EU projects per year
- Preferred role in consortia (coordinator vs. partner)
- Budget preferences (typical contribution range per project)
- Overhead/indirect cost rate (if known)

### Step 3: Populate Profile
- **Actor**: Coordinator Hub
- **Action**: From the interview answers, populate `knowledge/applicant_profile.md` using the template structure
- Present the completed profile to the user for review

### Step 4: User Confirmation
- **Actor**: User
- **Decision**:
  - **APPROVED** — Profile is saved. Proceed to W0 or W1 depending on what's available.
  - **REVISE** — User provides corrections. Coordinator updates and re-presents.

## How Agents Use the Profile

| Agent | What They Need From the Profile |
|-------|-------------------------------|
| Call Strategist | Domain focus, strategic priorities → fit scoring |
| SotA Researcher | Track record, past projects → positioning vs. competitors |
| Consortium Scout | Your capabilities, network → find complementary partners |
| Excellence Architect | Team expertise, track record → "consortium brings..." |
| Impact Specialist | Assets, networks → exploitation and dissemination capacity |
| Implementation Manager | PM capacity, infrastructure → realistic WP planning |
| Budget Balancer | Overhead rate, budget preferences → cost model |

## Maintenance

- Review and update the profile at the start of each new proposal cycle
- After each completed project, add it to the track record
- After team changes, update key personnel

## Exit Criteria
- [ ] All interview blocks (A-G) addressed (some may be "not applicable")
- [ ] `knowledge/applicant_profile.md` populated and saved
- [ ] User has approved the profile
