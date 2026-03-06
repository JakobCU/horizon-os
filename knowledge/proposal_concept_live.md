# Proposal Concept — Living Document

> **Owner**: Coordinator Hub
> **Updated by**: Coordinator Hub (on scope changes), User (initial input)
> **Read by**: All agents

## Proposal Identity

- **Acronym**: CORTEX
- **Full Title**: Cognitive Resilient Teaming for Extreme Search and Rescue
- **Call ID**: HORIZON-CL3-2026-01-DRS-03
- **Instrument**: IA (Innovation Action)
- **Duration**: 36 months
- **Requested EU Contribution**: ~EUR 4,000,000
- **Submission Deadline**: 2026-11-05

## Problem Statement

Search-and-rescue operations in hazardous conditions (structural collapse, wildfire, earthquake, industrial accident) push human responders to their cognitive and physical limits. Extended operations over 24-72 hours lead to fatigue, cognitive overload, and critical decision errors — yet there is no objective, real-time way to monitor or support the responder's cognitive state during operations.

Simultaneously, autonomous SAR systems (drones, UGVs) are reaching operational maturity (TRL 6-7) through projects like TRIFFID, HURRICANE, and PROACTIF. But these systems treat the human operator as a static command input — autonomy is binary (teleoperated or fully autonomous), with no adaptation to the operator's current capacity. The result: a growing gap between what technology can do and what human-robot teams actually achieve under stress.

C2 systems compound the problem by presenting all information equally regardless of the commander's capacity to process it, creating information overload during precisely the moments when clear decision-making is most critical.

## Proposed Solution — High-Level

CORTEX introduces the missing human-AI teaming layer for SAR: a closed-loop system where responder cognitive/physical state drives adaptive autonomy allocation, information prioritization, and team management decisions.

The system comprises: (1) a **Cognitive Twin** for each responder — PPE-embedded biosensors fused into a real-time Responder State Vector tracking cognitive load, stress, and fatigue; (2) an **Adaptive Autonomy Manager** that adjusts robot/drone autonomy levels based on operator state (advisory mode, human confirms); (3) an **Adaptive C2 Overlay** that integrates with existing C2/CAD systems to prioritize information and surface actionable recommendations based on commander cognitive state; (4) an **XR Training Module** for human-AI teaming skills; and (5) a **Mission Replay Tool** for post-mission cognitive after-action review.

CORTEX is platform-agnostic middleware — it works with whatever robots and C2 systems agencies already own.

## Objectives

1. **O1**: Develop and validate the Cognitive Twin — real-time multi-modal biosignal fusion achieving >80% cognitive state classification accuracy in operational SAR conditions (TRL 7-8 by M30)
2. **O2**: Design and validate the Adaptive Autonomy Manager — advisory biosignal-driven autonomy allocation demonstrating measurable team performance improvement vs. fixed autonomy (by M33)
3. **O3**: Deliver an adaptive C2 overlay compatible with existing systems, reducing decision latency for incident commanders during complex operations (by M30)
4. **O4**: Create a validated XR training curriculum for human-AI teaming in SAR with measurable learning outcomes (by M33)
5. **O5**: Deliver a post-mission cognitive replay tool for after-action review, synchronizing biosignal, telemetry, C2, and communication data (by M30)

## Expected Key Results

| Result | Type | TRL Start - End | Lead WP |
|--------|------|-----------------|---------|
| R1: Cognitive Twin Engine (inference software + PPE-compatible biosignal hardware) | Software + Hardware | TRL 5 - 7-8 | WP2 |
| R2: Adaptive Autonomy Manager (middleware with robot API) | Software | TRL 3-4 - 7 | WP3 |
| R3: Adaptive C2 Overlay (plugin for existing C2/CAD) | Software | TRL 5 - 7-8 | WP4 |
| R4: XR SAR Training Curriculum (environment + curriculum) | Software + Method | TRL 5 - 7 | WP5 |
| R5: Mission Replay Tool (after-action review system) | Software | TRL 4 - 7 | WP4 |
| R6: Ethical Governance Framework (DPIA, AI Act checklist, data policy) | Policy/Method | N/A | WP6 |
| R7: Field Validation Reports (TRL 7-8 evidence) | Report | N/A | WP7 |

## Work Package Overview (Preliminary)

| WP | Title | Lead (if known) | Key Partners | Months |
|----|-------|-----------------|--------------|--------|
| WP1 | Project Management & Coordination | AIT CTE (Coordinator) | All | M1-M36 |
| WP2 | Cognitive Twin: Biosignal Sensing & State Inference | AIT CTE | Biosignal HW Partner | M1-M30 |
| WP3 | Adaptive Autonomy Manager | AIT CTE + Robotics Partner | C2 Integrator | M6-M33 |
| WP4 | Adaptive C2 Overlay & Mission Replay | AIT CTE + C2 Integrator | All | M6-M33 |
| WP5 | XR Training for Human-AI Teaming | AIT CTE | End-User Partners | M6-M33 |
| WP6 | Ethics, Legal, Social Implications (ELSI) | ELSI Partner | AIT, End-Users | M1-M36 |
| WP7 | Field Validation & Demonstration | End-User Lead | All | M24-M36 |
| WP8 | Dissemination, Communication & Exploitation | TBD | All | M1-M36 |

## Target End-Users

- [x] Civil protection / disaster response agencies (fire services, USAR teams)
- [x] Other: Emergency Medical Services (EMS) / medical emergency coordination
- [x] Other: Mountain rescue, wildfire SAR teams
- [ ] Law Enforcement Agencies (where relevant to SAR)
- [ ] Border/Coast Guard authorities
- [ ] Critical infrastructure operators
- [ ] Policy makers (EU/national level) — indirect via framework

## Alignment with EU Policies

- [x] EU Preparedness Union Strategy (population preparedness, preparEU)
- [x] EU Civil Protection Mechanism (UCPM) / rescEU / ECPP capacity gaps
- [x] EU AI Act — designed for compliance (human-in-the-loop, transparency, high-risk system)
- [x] European Green Deal — climate-related disaster response
- [x] KAPP (Knowledge for Action in Prevention & Preparedness)
- [x] CER Directive (critical entity resilience)

## Cross-Cutting Dimensions

- **Gender Dimension**: Inclusive PPE sensor design for diverse body types; gender-balanced end-user panels; analysis of gender differences in cognitive load response
- **Open Science**: Open-source AAM middleware; FAIR biosignal datasets (anonymized); open training curriculum
- **DNSH (Do No Significant Harm)**: Low-power edge computing; no environmentally harmful materials in sensors
- **Ethics & Security Scrutiny**: Biosignal = health data (GDPR); AI Act high-risk system; works council / union engagement from M1; DPIA required; advisory-only autonomy (human always confirms)

## Key Design Decisions (from W0 End-User Review)

1. Adaptive autonomy is **advisory/confirmable** — never automatic override during live operations
2. C2 dashboard maintains **stable layout** — adapts content priority, not button positions
3. Biosensors must be **PPE-embedded** (not add-on) — partner with manufacturer
4. System integrates with **existing C2/CAD** via overlay/module — not a standalone replacement
5. All operations must work **offline-first** (edge computing, mesh radio) — no cloud dependency
6. Audio alerts via earpiece for field commanders — not visual-only dashboard
7. GDPR/works council/union process built into project timeline from M1
8. **Graceful degradation** — operations continue normally when tech fails

## Revision Log

| Date | Change | Author |
|------|--------|--------|
| 2026-03-06 | Initial concept — call selected, AIT positioning identified | Coordinator Hub |
| 2026-03-06 | Full W0 synthesis: SotA, architecture, ideation, end-user review. Concept refined. Storyline locked. | Coordinator Hub |
