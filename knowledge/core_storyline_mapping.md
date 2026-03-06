# Core Storyline Mapping — The Roter Faden

> **Owner**: Narrative Strategist
> **Status**: LOCKED
> **Locked at**: 2026-03-06
> **Read by**: ALL agents — this is the narrative foundation

---

## One-Sentence Summary

> "CORTEX will deliver the first closed-loop cognitive support system for search-and-rescue operations by fusing real-time responder biosignal monitoring with adaptive human-AI teaming and decision support, enabling safer and more effective disaster response for European first responders and emergency medical services."

## Narrative Arc

| Element | Content |
|---------|---------|
| **Hook** | A SAR robot with full autonomy and a cognitively overloaded operator is not a team — it is two independent agents in a disaster zone. In structural collapse scenarios, the majority of critical decision errors occur not from lack of information, but from cognitive overload. The next generation of SAR technology must support the rescuer's cognition before it can rescue anyone else. |
| **Tension** | A decade of EU-funded SAR innovation has produced better drones, smarter robots, and more sensors — but the human operating them is still unsupported. Biosignal monitoring ends at a dashboard nobody watches. Robot autonomy is binary: teleoperated or fully autonomous. Interfaces remain static regardless of operator state. The result: a growing gap between what technology can do and what human-robot teams actually achieve under stress. |
| **Turning Point** | CORTEX introduces the missing layer — a Cognitive Twin for every responder and an Adaptive Autonomy Manager for every robot, connected through a decision-support C2 overlay that works with existing systems. For the first time, responder physiological/cognitive state becomes the control signal that governs information flow, autonomy allocation, and team management — closing the loop that 15 prior EU projects left open. |
| **Resolution** | Post-CORTEX, incident commanders have objective data for team rotation decisions, responders work alongside robots that adapt to their cognitive state, and the C2 system surfaces only what matters when it matters. Validated at TRL 7-8 across three multinational field exercises in real SAR conditions. |
| **Coda** | CORTEX is platform-agnostic middleware — it works with whatever robots and C2 systems agencies already own. This dramatically lowers the adoption barrier and enables scaling across European civil protection without hardware lock-in. |

## Problem Chain

| ID | Problem Statement | Evidence | Urgency |
|----|-------------------|----------|---------|
| P1 | SAR responders experience cognitive overload and fatigue during extended operations, leading to critical decision errors | Documented in SHOTPROS, MED1stMR research; 72-hour SAR rotations common in earthquake/wildfire response; fatigue-driven errors are a known but unquantified problem | Climate-driven increase in wildfire, flood, and multi-hazard disasters means longer, more complex SAR operations |
| P2 | Human-robot teaming in SAR is dysfunctional — robots operate independently or under full manual control, with no adaptation to operator state | TRIFFID, HURRICANE, PROACTIF all focus on robot autonomy; the human side is treated as a static remote operator | Autonomous SAR robots are arriving (TRL 6-7) but integration with human teams is the new bottleneck |
| P3 | C2 systems present all information equally regardless of the operator's capacity to process it, causing information overload during mass casualty / multi-hazard events | End-user feedback from EMS commanders; no adaptive information prioritization in operational C2 tools | Increasing scale and complexity of disasters (cascading, multi-hazard) overwhelms existing C2 approaches |
| P4 | Responders have never trained for human-AI teaming — they don't know how to work alongside adaptive autonomous systems | No XR or simulation training for human-robot collaboration in SAR exists; trust calibration is absent | As autonomous systems deploy, untrained human-robot interaction becomes a safety risk |

## Gap Chain

| ID | Problem | Innovation Gap | Source |
|----|---------|---------------|--------|
| G1 | P1 | Biosignal monitoring of SAR responders exists (SIXTHSENSE, FASTER, RESCUER) but is NOT integrated into C2 decision-making in a closed loop — monitoring stops at a dashboard | SotA Research: no project has demonstrated biosignal-to-C2-to-action closed loop |
| G2 | P2 | Human-AI teaming in SAR is robot-centric — no adaptive autonomy based on operator cognitive/physical state; autonomy is all-or-nothing | SotA Research: TRIFFID, HURRICANE, PROACTIF focus on robot capability, not human-centered teaming |
| G3 | P3 | Adaptive interfaces based on cognitive state are nascent (RESCUER reached TRL 5-6 with limited AR adaptation) — no operational C2 systems adapt information delivery to operator state | SotA Research: CODA does this for air traffic control but nobody has transferred it to SAR/disaster C2 |
| G4 | P4 | XR training covers individual and team skills (SHOTPROS, MED1stMR) but NOT human-AI teaming — no training exists for trust calibration, shared mental models, or adaptive autonomy interaction | SotA Research: gap confirmed across all reviewed projects |

## Objective Chain

| ID | Gap | Objective (SMART) | Verification |
|----|-----|-------------------|--------------|
| O1 | G1 | Develop and validate a real-time Cognitive Twin system that fuses multi-modal biosignal data into a Responder State Vector (cognitive load, stress, fatigue) with >80% accuracy, integrated into C2 decision support, by M30 | Field exercise validation: RSV accuracy against NASA-TLX ground truth; C2 integration demonstrated |
| O2 | G2 | Design and validate an Adaptive Autonomy Manager that adjusts robot/drone autonomy levels based on operator cognitive state, operating as advisory/confirmable (not automatic override), demonstrating measurable improvement in team performance vs. fixed autonomy, by M33 | A/B comparison in field exercises: task completion, errors, missed victims, subjective workload |
| O3 | G3 | Deliver an adaptive C2 overlay (compatible with existing C2/CAD systems) that prioritizes information, alerts, and recommendations based on incident commander cognitive state — maintaining stable layout while adapting content priority, by M30 | Usability evaluation with incident commanders in multi-agency exercises; reduced decision latency measured |
| O4 | G4 | Create an XR-based training curriculum for human-AI teaming in SAR, including trust calibration, shared mental model building, and autonomy transition familiarization, validated with measurable learning outcomes, by M33 | Pre/post training assessment; transfer to field exercise performance |
| O5 | G1-G3 | Deliver a post-mission cognitive replay ("Black Box for Responders") that synchronizes biosignal, robot telemetry, C2 actions, and communication into an after-action review tool, by M30 | Demonstrated use in after-action review following each field exercise |

## Methodology Chain

| ID | Objective | Approach | WP | Building Blocks |
|----|-----------|----------|-----|-----------------|
| M1 | O1 | Multi-modal biosignal fusion (ECG, EDA, SpO2, respiration, motion) in PPE-compatible form factors; edge-cloud inference pipeline; Cognitive Twin computation | WP2 | BB1 (Wearable Biosignal Platform), BB2 (Edge-Cloud Inference Engine) |
| M2 | O2 | POMDP-based autonomy policy engine; advisory mode with human confirmation; Sheridan 4-level autonomy scale; safety constraints; Wizard-of-Oz validation before automation | WP3 | BB3 (Adaptive Autonomy Manager), BB5 (Robot/Drone Platforms) |
| M3 | O3 | C2 overlay module (not standalone); stable layout with adaptive content prioritization; audio alerts via earpiece; eye-tracking for commander state; integration via EDXL/CAP standards | WP4 | BB4 (Adaptive C2 Dashboard) |
| M4 | O4 | VR/MR training scenarios for human-AI teaming; trust calibration exercises; CRM-adapted protocols for human-robot crews; synthetic biosignal data generation for model improvement | WP5 | BB6 (XR Human-AI Teaming Trainer) |
| M5 | O5 | Multi-modal data fusion and timeline visualization; synchronized replay of biosignal + telemetry + comms + C2 actions | WP4 | BB4 (extended) |
| M6 | O1-O5 | Co-design with end-users from M1; DPIA and works council engagement from M1; AI Act compliance assessment; progressive field validation across 3 exercises in 3+ countries | WP1 (Management), WP6 (Ethics/ELSI) | BB7 (Ethical Governance Framework) |
| M7 | All | Three multinational field exercises at realistic scale: urban SAR (M26), industrial accident (M30), earthquake/collapse (M33); multi-agency, 10+ responders + robots per exercise | WP7 | All BBs integrated |

## Result Chain

| ID | Methodology | Key Exploitable Result | Deliverable | Owner |
|----|-------------|----------------------|-------------|-------|
| R1 | M1 | Cognitive Twin Engine — real-time responder state inference software + PPE-compatible biosignal hardware | D2.3 | AIT (software), Biosignal Partner (hardware) |
| R2 | M2 | Adaptive Autonomy Manager — middleware for biosignal-driven autonomy allocation with robot API | D3.3 | AIT + Robotics Partner |
| R3 | M3 | Adaptive C2 Overlay — plugin module for existing C2/CAD systems | D4.3 | AIT + C2 Integrator |
| R4 | M4 | XR SAR Training Curriculum — human-AI teaming training environment and validated curriculum | D5.2 | AIT |
| R5 | M5 | Mission Replay Tool — post-mission cognitive-operational after-action review system | D4.4 | AIT |
| R6 | M6 | CORTEX Ethical Governance Framework — DPIA template, AI Act compliance checklist, biosignal data policy | D6.2 | ELSI Partner |
| R7 | M7 | Field Validation Reports — TRL 7-8 evidence across 3 exercises | D7.3 | All |

## Impact Chain

| ID | Result | PEDR Pathway | KPI | Timeline |
|----|--------|-------------|-----|----------|
| I1 | R1 | Exploitation: license Cognitive Twin to PPE manufacturers and C2 vendors | Responder fatigue incidents reduced by 30% in adopting organizations | 3-5 years post-project |
| I2 | R2 | Exploitation: open-source AAM middleware adopted by EU SAR robotics projects | Human-robot team performance improved by 25% (measured in exercises) | During project + 2 years |
| I3 | R3 | Exploitation: C2 overlay commercially deployed via C2 integrator partner | Decision latency reduced by 20% for incident commanders during MCI | 2-4 years post-project |
| I4 | R4 | Dissemination: training curriculum shared via CEPOL, UCPM training networks | 500+ responders trained in human-AI teaming within 3 years of project end | 1-3 years post-project |
| I5 | R6 | Policy: ethical framework adopted as reference by EU AI Office for safety-critical biosignal systems | Framework cited in 3+ national/EU policy documents | 2-5 years post-project |
| I6 | R1-R5 | Societal: strengthened European disaster response capacity; alignment with UCPM/rescEU capacity goals | Contribution to ECPP capacity gap reduction documented | During project |

## Traceability Matrix

| Problem | Gap | Objective | Methodology/WP | Block | Deliverable | KER | KPI | Impact |
|---------|-----|-----------|----------------|-------|-------------|-----|-----|--------|
| P1 | G1 | O1 | WP2/M1 | BB1, BB2 | D2.3 | R1 | Fatigue incidents -30% | I1 |
| P2 | G2 | O2 | WP3/M2 | BB3, BB5 | D3.3 | R2 | Team performance +25% | I2 |
| P3 | G3 | O3 | WP4/M3 | BB4 | D4.3 | R3 | Decision latency -20% | I3 |
| P4 | G4 | O4 | WP5/M4 | BB6 | D5.2 | R4 | 500+ responders trained | I4 |
| P1-P3 | G1-G3 | O5 | WP4/M5 | BB4 ext. | D4.4 | R5 | After-action data quality | I1, I6 |
| All | All | All | WP6/M6 | BB7 | D6.2 | R6 | 3+ policy citations | I5 |
| All | All | All | WP7/M7 | All | D7.3 | R7 | TRL 7-8 validated | I6 |

**Rule: Every row is complete. No broken threads.**

## X-Factor / Differentiators

| ID | Differentiator | Where it appears |
|----|---------------|-----------------|
| X1 | **Cognitive Twin** — real-time computational mirror of each responder's cognitive-physiological state, predicting performance degradation before the responder notices | WP2, Section 1.1 (Excellence hook), throughout |
| X2 | **Autonomy as a Dial, Not a Switch** — continuous biosignal-driven autonomy adjustment, zero manual mode-switching | WP3, Section 1.3 (Methodology) |
| X3 | **CRM for Human-Robot Teams** — aviation Crew Resource Management adapted for mixed human-AI SAR crews | WP5 (training design), Section 1.1 |
| X4 | **Platform-Agnostic Middleware** — works with any robot and any C2 system, lowering adoption barrier | Exploitation strategy, Section 2 (Impact) |
| X5 | **Black Box for Responders** — post-mission cognitive-operational replay for after-action review | WP4, Section 2 (Impact) |

## Revision Log (Post-Lock Only)

| Date | Change | Requested By | Ripple Assessment | Affected Sections |
|------|--------|-------------|-------------------|-------------------|
| — | — | — | — | — |
