# CORTEX — Cognitive Resilient Teaming for Extreme Search and Rescue

## Internal Pitch Document | AIT Center for Technology Experience

---

### The Opportunity

| Field | Detail |
|-------|--------|
| **Call** | HORIZON-CL3-2026-01-DRS-03 |
| **Topic** | Innovative tools & technologies for search and rescue in hazardous conditions |
| **Instrument** | Innovation Action (IA) |
| **EU Contribution** | ~EUR 4M per project (2 projects funded) |
| **AIT Budget Target** | ~EUR 900k |
| **Deadline** | 5 November 2026 |
| **TRL Target** | 7-8 |
| **Duration** | 36 months |

### The Problem

Search-and-rescue operations in disaster environments (structural collapse, wildfire, earthquake) push human responders to their cognitive and physical limits. A decade of EU-funded innovation has produced better drones, smarter robots, and more sensors — but the human operating them is still unsupported:

- **No closed loop.** Biosignal monitoring of responders exists (SIXTHSENSE, FASTER, RESCUER) but stops at a dashboard nobody watches during a crisis. It never feeds back into operational decisions.
- **All-or-nothing autonomy.** SAR robots are either teleoperated or fully autonomous. There is no adaptation based on the operator's current cognitive capacity.
- **Static interfaces.** C2 systems present all information equally, regardless of whether the commander is fresh or overwhelmed.
- **No training for human-AI teams.** Responders have never practiced working alongside adaptive autonomous systems.

### Our Solution: The Missing Human-AI Teaming Layer

CORTEX closes the loop between the responder, the robot, and the command post — for the first time.

```
  RESPONDER                COMMAND POST               TRAINING
  +-----------+           +------------------+        +----------+
  | Wearable  |--edge---->| Adaptive         |        | XR Human-|
  | Biosensors|  node     | Autonomy Manager |        | AI Team  |
  | (PPE-     |  (real-   | (advisory mode:  |        | Trainer  |
  |  embedded)|  time)    |  human confirms) |        +----------+
  +-----------+           +--------+---------+
                                   |
                          +--------v---------+
                          | Adaptive C2      |
                          | Dashboard        |
                          | (overlay on      |
                          |  existing C2)    |
                          +--------+---------+
                                   |
                          +--------v---------+
                          | Robot/Drone Fleet|        Ethics &
                          | (partner-provided|        Governance
                          |  platforms)      |        (cross-cutting)
                          +------------------+
```

**Five Key Exploitable Results:**

1. **Cognitive Twin Engine** — Real-time responder state inference (stress, fatigue, cognitive load) from PPE-embedded biosensors. Predicts degradation before the responder notices it.
2. **Adaptive Autonomy Manager** — Middleware that adjusts robot/drone autonomy based on operator cognitive state. Advisory mode: the system recommends, the human confirms.
3. **Adaptive C2 Overlay** — Plugin for existing C2/CAD systems that prioritizes information based on commander state. Stable layout, adaptive content.
4. **XR Training for Human-AI Teaming** — VR/MR scenarios where responders practice trust calibration and collaboration with adaptive autonomous systems.
5. **Mission Replay Tool** — "Black box for responders" — synchronized post-mission cognitive-operational after-action review.

### Why AIT CTE Should Lead This

- **Direct lineage from SHOTPROS + MED1stMR** — XR training, biosignal measurement, human performance under stress. CORTEX is the natural next step.
- **We own the innovation gap.** 15 EU projects mapped — nobody has closed the biosignal-to-C2-to-autonomy loop. The robotics side is saturated (TRIFFID, HURRICANE, PROACTIF). The human side is wide open.
- **5 of 9 consortium partners are warm contacts** from our past projects (PLUX, Campus Vesta, SAMUR-PC, Region Jamtland, Univ. Twente).
- **We lead 4 of 8 WPs** — WP1 (Management), WP2 (Cognitive Twin), WP3 co-lead (Adaptive Autonomy), WP4 co-lead (C2 Overlay), WP5 (XR Training). This is our project.
- **Platform-agnostic middleware** — high exploitation potential. Works with any robot and any C2 system. No hardware lock-in.

### Innovation Positioning

| What competitors will propose | What CORTEX proposes |
|-------------------------------|---------------------|
| "Better robots save more lives" | "Better-supported humans, teamed with robots, save more lives" |
| New drone/UGV platforms (TRL 4-5 to 7) | Middleware layer that works with existing platforms (lower risk) |
| Human factors as a token WP | Human state as the central control signal of the architecture |
| End-users test at the end | End-users co-design from Month 1 (5 warm contacts) |
| Silent on AI Act | Compliance by architecture — human-in-the-loop, advisory mode |

### Consortium (Proposed, 9 Partners, 8 Countries)

| Partner | Country | Type | Role | Warm? |
|---------|---------|------|------|-------|
| **AIT CTE** | Austria | RTO | Coordinator, WP1/2/3/4/5 | — |
| Robotnik Automation | Spain | SME | Robotics (UGV/UAV) | |
| IES / Webgenesys | Italy | SME | C2 platform (JIXEL) | |
| PLUX Biosignals | Portugal | SME | Wearable biosensors | MED1stMR |
| Campus Vesta | Belgium | Public Body | Fire/rescue end-user, exercises | SHOTPROS + MED1stMR |
| Feuerwehr Dortmund / IFR | Germany | Public Body | Fire/USAR end-user, exercises | |
| SAMUR-PC Madrid | Spain | Public Body | Medical emergency authority | MED1stMR |
| Region Jamtland Harjedalen | Sweden | Public Body | Medical/EMS authority | MED1stMR |
| Univ. Twente | Netherlands | University | ELSI / ethics | TechEthos with AIT |

40+ backup candidates identified across all positions. Budget headroom (~500k) for a 10th partner (recommended: CNBOP-PIB, Poland — widening country bonus).

### Budget Overview

| Category | EUR | % |
|----------|-----|---|
| AIT CTE | 900,000 | 23% |
| Technology SMEs (Robotnik, IES, PLUX) | 1,250,000 | 31% |
| End-users (4 orgs) | 1,100,000 | 28% |
| ELSI (Univ. Twente) | 250,000 | 6% |
| **Subtotal** | **3,500,000** | **88%** |
| Headroom (10th partner or buffer) | 500,000 | 12% |
| **Total** | **~4,000,000** | 100% |

Note: IA funding rate is 70% (100% for non-profit). AIT as RTO qualifies for 100%. Lump sum grant.

### Timeline

| Phase | Months | Key Activities |
|-------|--------|---------------|
| Now - Nov 2026 | Pre-submission | Internal approval, consortium outreach, proposal writing |
| May 2026 | Call opens | — |
| **Nov 2026** | **Deadline** | **Submission** |
| ~Jun 2027 | Expected start | If funded |
| M1-M12 | Component maturation | Lab validation, co-design with end-users, DPIA |
| M13-M24 | Integration | Subsystem integration, indoor testbed, first integrated demo |
| M25-M36 | Field validation | 3 multinational field exercises (TRL 7-8) |

### What We Need to Proceed

1. **Internal GO decision** to invest pre-proposal effort (~3-5 PM for concept development and proposal writing over 8 months)
2. **Approval to coordinate** (AIT CTE as lead beneficiary)
3. **Green light for outreach** to consortium partners (starting with 5 warm contacts)

### Key Risk & Mitigation

| Risk | Mitigation |
|------|-----------|
| Biosignal reliability under SAR conditions | Multi-modal fusion (no single-sensor dependency); confidence scoring; graceful degradation |
| Responder/union acceptance of monitoring | Co-design from M1; advisory-only; data stays on-device; works council engagement in timeline |
| Adaptive autonomy validation | Wizard-of-Oz before automation; conservative policy with safety constraints; A/B evaluation design |
| Competition (~8-13% success rate) | Human-centered angle is unique; 5 warm contacts de-risk consortium; strong AIT pedigree |

---

*Prepared by Horizon Europe OS | 2026-03-06*
*Contact: [PI] — AIT Center for Technology Experience*
