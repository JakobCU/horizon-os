# Consortium Scout Report -- GAP-01 Deep Search (Round 2)
# CORTEX (HORIZON-CL3-2026-01-DRS-03)

> **Scout**: Consortium Scout Agent
> **Date**: 2026-03-06
> **Round**: 2 (Deep Search)
> **Coordinator**: AIT Austrian Institute of Technology, Center for Technology Experience (Austria)
> **Scope**: 5-7 ADDITIONAL robotics/autonomous systems candidates beyond Round 1 (Robotnik, Fraunhofer FKIE, Eurecat)

---

## Search Methodology

This deep search systematically mined consortium partner lists from 9 EU-funded SAR/first-responder projects and cross-referenced with web verification of capabilities:

**CORDIS projects searched (full partner lists extracted):**
- CURSOR (H2020, 832790) -- 19 partners
- RESPOND-A (H2020, 883371) -- 34 partners
- RESPONDRONE (H2020, 833717) -- 20 partners
- INGENIOUS (H2020, 833435) -- 23 partners
- HURRICANE (Horizon Europe, 101168017) -- 16 partners
- PROACTIF (Horizon Europe, 101194239) -- 42 partners
- TeamAware (H2020, 101019808) -- 23 partners
- ASSISTANCE (H2020, 832576) -- 18 partners
- TRIFFID (Horizon Europe, 101168042) -- 14 partners

**Total unique organisations screened**: ~180+
**Filter criteria applied**: UGV/UAV platforms for SAR, ROS 2 compatible or open API, TRL 6+, EU project track record, NOT Greek institutions, geographic diversity (Nordic, Eastern EU, Benelux, Portugal prioritised)

---

## Candidate 1: INESC TEC -- Centre for Robotics and Autonomous Systems (Portugal)

| Field | Detail |
|-------|--------|
| **Full Name** | INESC TEC -- Instituto de Engenharia de Sistemas e Computadores, Tecnologia e Ciencia |
| **Country** | Portugal (Porto) |
| **Type** | RTO (non-profit research institute, ~750 researchers) |
| **Website** | https://www.inesctec.pt/en/centres/cras |

**Why they fit:**

- **Direct SAR robotics pedigree across multiple EU projects.** INESC TEC was a partner in RESPONDRONE (H2020, 833717), where they developed drone-supported wireless communication solutions for emergency response. They also participated in the FP7 ICARUS project (Integrated Components for Assisted Rescue and Unmanned Search Operations, EUR 17M, 24 partners), where they deployed the OTUS aerial robot in multi-domain SAR scenarios and won the euRathlon 2015 Grand Challenge with aerial reconnaissance, 3D mapping, and victim identification. They are a partner in HURRICANE (Horizon Europe, 101168017) for UGV-based crisis intelligence.
- **Dedicated robotics centre (CRAS).** The Centre for Robotics and Autonomous Systems focuses on TRL 5-8 prototypes and operational solutions. Their capabilities include autonomous navigation, SLAM, multi-robot coordination, computer vision, and AI -- across aerial, ground, and underwater domains.
- **UAV and UGV platforms.** CRAS operates both aerial robots (OTUS series) and ground/underwater platforms. They have published on cooperative UAV-UGV autonomous inspection systems, directly relevant to the CORTEX UAV-UGV cooperation concept.
- **Portugal = Widening country.** Portugal is a Horizon Europe widening country. Including INESC TEC strengthens the consortium's widening dimension, which is a scored criterion.
- **Strong publication and competition record.** euRathlon 2015 Grand Challenge winners. Active in REPMUS exercises (largest robotic exercise in the world, off Portuguese coast).

**EU project track record:**
- RESPONDRONE (H2020, 833717) -- drone fleet for disaster response
- HURRICANE (Horizon Europe, 101168017) -- UGV-based crisis intelligence
- ICARUS (FP7) -- unmanned SAR platforms (aerial, ground, marine)
- UNEXUP/UNEXMIN -- autonomous underground robots
- Multiple EDF (European Defence Fund) projects

**Risk flags:**
- **Overlap with Robotnik.** Both are in HURRICANE. If Robotnik is selected as the primary GAP-01 partner, having INESC TEC as well could create redundancy -- though INESC TEC brings complementary strengths in communications and the widening dimension.
- **Not an SME.** Large RTO (~750 researchers). Does not help SME count.
- **Underwater focus.** A significant portion of CRAS's work is maritime/underwater robotics. Need to ensure the SAR-focused aerial/ground team is assigned.
- **ROS 2 compatibility not explicitly confirmed.** CRAS uses ROS extensively (confirmed via ICARUS and publications), but explicit ROS 2 migration status was not verified. Given their scale and currency, ROS 2 capability is highly likely but should be confirmed.

**Rating: STRONG**

INESC TEC is the strongest new candidate identified in this round. They bring verified SAR project pedigree (RESPONDRONE, HURRICANE, ICARUS), TRL 5-8 robotics capability, the critical widening country dimension (Portugal), and deep expertise in UAV-UGV cooperation. Their HURRICANE participation alongside Robotnik means the two organisations already know each other, which de-risks collaboration.

---

## Candidate 2: Lukasiewicz -- PIAP (Poland)

| Field | Detail |
|-------|--------|
| **Full Name** | Siec Badawcza Lukasiewicz -- Przemyslowy Instytut Automatyki i Pomiarow PIAP |
| **Country** | Poland (Warsaw) |
| **Type** | RTO (part of Lukasiewicz Research Network, 3rd largest research network in Europe, 8,000+ employees network-wide) |
| **Website** | https://piap.lukasiewicz.gov.pl/en/ |

**Why they fit:**

- **Leading European UGV manufacturer.** PIAP is one of the biggest European producers of mobile robots for CBRN, EOD, surveillance, and rescue applications. Their robots are deployed in 28 countries worldwide.
- **Demonstrated SAR/rescue robot platforms at TRL 7-9.** PIAP IBIS is designed for EOD and reconnaissance, with capabilities for chemical reconnaissance and rescue support in hazardous environments. PIAP Patrol is a tracked robot for CBRN detection and reconnaissance. PIAP HUNTeR is the largest European remotely controlled robot. PIAP MULES is a logistics UGV for autonomous supply in hazardous zones.
- **EU project track record in security/SAR domain.** Partner in ASSISTANCE (H2020, 832576, SAR tools for first responders), TALOS (FP7, border protection with autonomous mobile robots, EUR 20M budget), and iMUGS2 (EDF, interoperable unmanned ground systems, 29 partners from 15 EU states). Also partner in PROACTIF (Horizon Europe, 101194239, unmanned vehicles for civil security).
- **Poland = Widening country (EU-13).** Poland qualifies under Horizon Europe's widening provisions, which is a scored evaluation criterion.
- **Dual-use capability.** Their platforms span military and civilian applications, with clear civilian rescue configurations available.

**EU project track record:**
- ASSISTANCE (H2020, 832576) -- SAR tools for first responders
- PROACTIF (Horizon Europe, 101194239) -- unmanned vehicles for civil security
- TALOS (FP7, 218081) -- autonomous border protection robots (EUR 20M)
- iMUGS2 (EDF) -- interoperable unmanned ground systems
- View Finder (FP7) -- rescue robot with SAR sensors

**Risk flags:**
- **ROS 2 compatibility not confirmed.** PIAP develops proprietary control systems for their UGVs. ROS/ROS 2 integration was not explicitly documented in searches. Their defence-oriented development may use proprietary stacks. This is the key technical risk and must be verified before outreach.
- **Defence orientation.** PIAP's primary market is military/security. For a CL3 civil security call, their civilian rescue configurations exist (IBIS for rescue, View Finder for SAR) but are less prominent than the defence product line.
- **Large institution.** As part of the Lukasiewicz Research Network, PIAP is a large entity. Overhead structures may be complex, though typically lower than Western European RTOs.
- **No confirmed UAV capability.** PIAP's strength is firmly in UGVs. UAV capability would need to come from another partner or a sub-contractor.

**Rating: GOOD**

PIAP brings unmatched UGV hardware maturity (TRL 7-9 platforms deployed in 28 countries), strong EU security project pedigree, and the valuable widening country dimension (Poland). The main uncertainty is ROS 2 compatibility -- if their platforms support ROS 2 or open APIs, they become a very strong candidate. If they use only proprietary control stacks, integration with CORTEX's ROS 2 architecture would require significant adaptation work. Recommended as a strong backup to Robotnik, especially if the consortium needs Eastern EU representation.

---

## Candidate 3: SINTEF AS (Norway)

| Field | Detail |
|-------|--------|
| **Full Name** | SINTEF AS |
| **Country** | Norway (Trondheim) |
| **Type** | RTO (independent non-profit, 2,200 employees, ~EUR 340M annual revenue) |
| **Website** | https://www.sintef.no/en/ |

**Why they fit:**

- **Partner in both CURSOR and INGENIOUS.** In CURSOR (H2020, 832790), SINTEF led WP3 (miniaturised SAR platforms), building and integrating the SMURF (Soft Miniaturised Underground Robotic Finder) prototypes -- developing hardware, interface definitions, control software, and simulator. In INGENIOUS (H2020, 833435), they contributed to the Next Generation Integrated Toolkit for first responders with autonomy and automation for SAR tasks.
- **Strategic robotics and autonomy research area.** SINTEF has designated robotics and autonomy as a strategic priority area, with capabilities in AUVs, UAVs, and AGVs. Their Robot Manipulator Lab in Trondheim tests perception and motion planning methods for increased autonomy.
- **Proven SAR robotics integration capability.** The CURSOR work specifically demonstrates SINTEF's ability to take a novel robot concept (SMURF), build physical prototypes, develop ROS-compatible control software, and deploy to field trials -- exactly the type of integration work needed in CORTEX WP3.
- **Nordic country.** Norway (associated country to Horizon Europe) adds Nordic representation, which is currently absent from the consortium.
- **Massive EU project portfolio.** One of Europe's largest independent research organisations with extensive Horizon 2020 and Horizon Europe participation.

**EU project track record:**
- CURSOR (H2020, 832790) -- WP3 lead, SAR miniaturised robots
- INGENIOUS (H2020, 833435) -- first responder integrated toolkit
- ARTIFEX -- robotic systems for autonomous task execution
- SAFESUB -- autonomous subsea intervention
- Multiple EDF and other security projects

**Risk flags:**
- **Associated country, not EU Member State.** Norway is associated to Horizon Europe and fully eligible, but some evaluators may prefer EU MS partners. Not a disqualifier.
- **Not an SME.** SINTEF is a large RTO (2,200 staff). Does not help SME count. High overhead likely.
- **Broad research portfolio.** SINTEF works across energy, ocean, digital, and many other sectors. The robotics/SAR team is a small fraction of the total organisation. Need to ensure the specific SAR robotics personnel from CURSOR/INGENIOUS are committed.
- **No own UGV/UAV product line.** SINTEF is a research integrator, not a platform manufacturer. They build prototypes and develop software but do not manufacture commercial robots. For CORTEX, they would need to work with Robotnik's or another manufacturer's platforms.

**Rating: GOOD**

SINTEF brings proven SAR robotics integration skills (CURSOR WP3 lead, INGENIOUS partner), deep control software and simulation expertise, and Nordic geographic diversity. They are best positioned as a complementary integration/software partner rather than a platform provider -- ideal if Robotnik provides the hardware and SINTEF provides autonomy software and integration. The CURSOR + INGENIOUS double pedigree is a strong signal.

---

## Candidate 4: Avular Innovations BV (Netherlands)

| Field | Detail |
|-------|--------|
| **Full Name** | Avular Innovations BV |
| **Country** | Netherlands (Eindhoven) |
| **Type** | SME (spin-off from Eindhoven University of Technology, founded 2014) |
| **Website** | https://www.avular.com |

**Why they fit:**

- **ROS 2 native platform manufacturer.** Avular's Origin One UGV platform natively supports ROS 2, with full C++ SDK access, NVIDIA Jetson integration, and simulation environments. This is the most directly ROS 2-aligned platform identified outside of Robotnik.
- **Partner in PROACTIF (Horizon Europe, 101194239).** Avular is in the 42-partner PROACTIF consortium for unmanned vehicles in civil security and surveillance. PROACTIF explicitly develops UGV platforms for "emergency sites, wildfires, search and rescue" -- directly demonstrating SAR relevance.
- **Both UGV and UAV platforms.** Avular manufactures both the Origin One (ground robot) and Vertex One (drone) platforms, offering modular autonomy across domains. Both designed for outdoor operation with LiDAR, GNSS, and obstacle avoidance.
- **European production.** Avular explicitly positions EU-manufactured robots as an alternative to US/Chinese platforms, emphasising supply chain security -- aligned with Horizon Europe's strategic autonomy goals.
- **SME status.** As a spin-off SME, Avular contributes to the consortium's SME count.
- **Benelux representation.** Netherlands adds Benelux geographic diversity.

**EU project track record:**
- PROACTIF (Horizon Europe, 101194239) -- unmanned vehicles for civil security (42 partners, 13 countries)
- ITEA projects (confirmed via ITEA4 portal)
- Partnerships with ProRail for autonomous rail inspection

**Risk flags:**
- **Young company.** Founded 2014, spin-off from TU Eindhoven. May have limited financial capacity for a EUR 500k commitment. Revenue and headcount need verification.
- **Platforms are research/inspection-grade, not yet SAR-hardened.** The Origin One is designed for inspection and research. Ruggedisation for SAR hazardous conditions (rubble, debris, extreme temperatures, dust) has not been demonstrated. This is a project engineering task but adds risk.
- **Limited SAR field experience.** PROACTIF is their main security project, and it started recently (2025). They do not have the deep SAR deployment history of Robotnik or PIAP.
- **PROACTIF overlap.** If PROACTIF is running concurrently with CORTEX, Avular may face capacity constraints.
- **TRL of SAR configuration.** Base platform is TRL 7-8 (commercial product), but SAR-specific configuration would be TRL 4-5. Significant development work needed within CORTEX.

**Rating: CONDITIONAL**

Avular is an interesting SME candidate with native ROS 2 support, dual UGV/UAV capability, and Benelux geographic diversity. The PROACTIF pedigree demonstrates entry into the security domain. However, their platforms are not yet SAR-proven, the company is young, and financial capacity for EUR 500k needs verification. Best suited as a secondary robotics partner contributing platform hardware if Robotnik handles the SAR integration, or as a backup if Robotnik declines.

---

## Candidate 5: Totalforsvarets Forskningsinstitut -- FOI (Sweden)

| Field | Detail |
|-------|--------|
| **Full Name** | Totalforsvarets Forskningsinstitut (Swedish Defence Research Agency) |
| **Country** | Sweden (Stockholm / Linkoping) |
| **Type** | Government agency / RTO |
| **Website** | https://www.foi.se/en/ |

**Why they fit:**

- **Partner in INGENIOUS (H2020, 833435).** FOI contributed to the INGENIOUS first responder toolkit project (EUR 576k budget share), working on SAR technologies alongside SINTEF, DLR, and other leading European robotics groups.
- **Autonomous systems expertise.** FOI conducts research on autonomous drones (including drone swarms), SAR radar technology (3D SAR for small drone-based monitoring), and autonomous ground systems. Their defence research mandate covers dual-use autonomous systems for both military and civil security.
- **Dual-use SAR radar technology.** FOI has developed and tested radar sensors for drones, including SAR technology combined with group antennas for monitoring smaller areas -- potentially valuable for SAR victim detection through debris.
- **Nordic country.** Sweden adds Nordic representation to the consortium, which is currently absent.
- **Swedish partner in first responder exercises.** FOI's civil defence research mission includes collaboration with Swedish first responder organisations (Sodertorns Brandforsvarsförbund, which was also in INGENIOUS and ASSISTANCE).

**EU project track record:**
- INGENIOUS (H2020, 833435) -- first responder integrated toolkit (EUR 576k)
- Multiple EDF projects (5 projects worth ~EUR 68M total via VTT/FOI consortium)
- Swedish national defence research programmes

**Risk flags:**
- **Government agency, not SME.** FOI is a Swedish government agency. Does not contribute to SME count and may have complex approval processes for consortium participation.
- **Defence-primary orientation.** FOI's primary mandate is Swedish defence research. While they have dual-use and civil security capabilities, their organisational culture and processes are defence-oriented.
- **No own robotic platforms for SAR.** FOI is a research agency, not a platform manufacturer. They develop and test technologies but do not produce UGVs or UAVs. Would need to work with a platform provider.
- **Associated country (non-EU MS).** Sweden is an EU Member State, so this is not an issue. (Note: Sweden is indeed an EU MS.)
- **Capacity uncertainty.** As a government agency, FOI's ability to commit to a Horizon Europe project depends on internal priorities and Swedish government approval.

**Rating: CONDITIONAL**

FOI brings genuine SAR technology expertise (INGENIOUS partner), Nordic geographic diversity, and dual-use autonomous systems research capability. However, they are a government agency without their own robotic platforms, making them more suitable as a technology/algorithm contributor than a platform provider. Best considered if the consortium specifically needs Nordic representation and SAR sensor technology (e.g., drone-mounted radar for victim detection), rather than as the primary robotics platform partner.

---

## Candidate 6: VTT Technical Research Centre of Finland (Finland)

| Field | Detail |
|-------|--------|
| **Full Name** | Teknologian tutkimuskeskus VTT Oy |
| **Country** | Finland (Espoo) |
| **Type** | RTO (state-owned, ~2,000 employees) |
| **Website** | https://www.vttresearch.com |

**Why they fit:**

- **Partner in PROACTIF (Horizon Europe, 101194239).** VTT is in the 42-partner PROACTIF consortium developing unmanned vehicles for civil security. PROACTIF specifically develops UGV and UAV platforms for emergency response, SAR, and infrastructure protection.
- **Autonomous drone systems expertise.** VTT leads the MISEL project (H2020, EUR 4.96M) developing multispectral intelligent vision systems for drones and robots. They develop machine vision for autonomous drones and robots inspired by human vision systems, with applications in surveillance and inspection.
- **Finnish RAAS ecosystem.** VTT is a founding member of RAAS (Rethinking Autonomy and Safety), Finland's new innovation ecosystem for autonomous systems and drones, aiming to be one of the world's leading development environments.
- **Defence and security portfolio.** VTT is involved in 5 European Defence Fund projects worth ~EUR 68M total, demonstrating capability in security-relevant autonomous systems.
- **Nordic/EU MS representation.** Finland adds Nordic EU Member State representation.

**EU project track record:**
- PROACTIF (Horizon Europe, 101194239) -- unmanned vehicles for civil security
- MISEL (H2020) -- multispectral vision for autonomous drones/robots (coordinator)
- AutoSOS -- autonomous multi-robot SAR assistance platform
- 5 European Defence Fund projects (~EUR 68M total)

**Risk flags:**
- **Not an SME.** Large state-owned RTO (~2,000 staff). High overhead structures.
- **Broad research organisation.** VTT works across energy, manufacturing, health, and digital domains. The autonomous systems team is a fraction of the whole. Need to ensure specific SAR/robotics personnel are committed.
- **No own UGV/UAV platforms.** VTT is a research organisation, not a platform manufacturer. They develop sensors, AI, and vision systems but do not manufacture robots.
- **Limited demonstrated SAR field deployment.** VTT's drone and autonomous systems work is primarily in inspection, monitoring, and agricultural domains. Direct SAR field deployment evidence is limited to the AutoSOS project.
- **Finnish overhead.** VTT's cost structures are typically high for Horizon Europe projects.

**Rating: CONDITIONAL**

VTT brings autonomous vision systems expertise, PROACTIF security project pedigree, and Finnish/Nordic geographic diversity. However, they are a large RTO without own platforms, and their SAR-specific field experience is limited compared to INESC TEC, Robotnik, or PIAP. Best considered if the consortium needs specific AI vision/perception capabilities for the autonomy stack, or if Nordic EU MS representation is strategically important and FOI is not available.

---

## Candidate 7: Alpha Unmanned Systems SL (Spain)

| Field | Detail |
|-------|--------|
| **Full Name** | Alpha Unmanned Systems SL |
| **Country** | Spain (Madrid) |
| **Type** | SME (founded 2014) |
| **Website** | https://alphaunmannedsystems.com |

**Why they fit:**

- **Partner in RESPONDRONE (H2020, 833717).** Alpha Unmanned was a partner in the RESPONDRONE project (drone fleet for disaster response, 20 partners, EUR 8M), providing UAV platforms for first responder drone operations.
- **Helicopter UAV platform.** The Alpha 900 (A900) is a fully autonomous single-rotor helicopter UAV capable of 4-hour flight endurance and 3-4 kg payload capacity. Designed for SAR, mapping, inspection, surveillance, and reconnaissance missions.
- **SAR-specific configuration.** EO/IR camera combined with sensors makes the A900 a tool for mountain rescue and intelligence missions. The rotary-wing design enables VTOL operations in confined areas where fixed-wing drones cannot operate -- relevant for SAR in collapsed structures/rubble environments.
- **International deployment track record.** Products sold to US DoD, Indonesian Coast Guard, Hellenic Navy, and clients in 12+ countries, demonstrating TRL 8-9 maturity.
- **SME status.** Contributes to consortium SME count.
- **Recent Airbus partnership.** 2025 MoU with Airbus Helicopters Espana for crewed-uncrewed teaming (MUM-T) demonstrates industry credibility and advanced autonomous capability.

**EU project track record:**
- RESPONDRONE (H2020, 833717) -- drone fleet for first responders

**Risk flags:**
- **UAV only, no UGV.** Alpha Unmanned only makes helicopter drones. Cannot fill the UGV component of GAP-01. Would need to be paired with a UGV partner.
- **Third Spanish candidate.** With Robotnik already recommended as primary GAP-01 fill, adding another Spanish partner creates geographic concentration. However, they are in Madrid (vs. Robotnik in Valencia) and different domains (UAV vs. UGV).
- **ROS 2 compatibility unconfirmed.** Searches did not reveal ROS/ROS 2 integration for the A900 platform. Military/defence UAVs often use proprietary autopilots (e.g., Pixhawk variants). This is a key technical question.
- **Defence-primary market.** Most sales are to military/naval customers. Civil SAR is a secondary market.
- **Single EU project.** Only one confirmed EU research project (RESPONDRONE). Limited Horizon Europe consortium experience compared to other candidates.

**Rating: CONDITIONAL**

Alpha Unmanned brings a mature, SAR-capable rotary-wing UAV platform with RESPONDRONE pedigree and international deployment credibility. However, they are UAV-only (no UGV), ROS 2 compatibility is uncertain, and geographic overlap with Robotnik (both Spanish) is a concern. Best considered as a supplementary UAV-specific partner if the consortium needs dedicated rotary-wing drone capability beyond what Robotnik can provide, or as a backup UAV partner if Robotnik focuses primarily on UGVs.

---

## Summary Ranking -- Round 2 Candidates

| Rank | Candidate | Country | Type | Rating | Key Advantage | Key Risk |
|------|-----------|---------|------|--------|---------------|----------|
| 1 | **INESC TEC (CRAS)** | Portugal | RTO | **STRONG** | RESPONDRONE + HURRICANE + ICARUS pedigree; widening country; TRL 5-8 | Not SME; ROS 2 to confirm |
| 2 | **Lukasiewicz -- PIAP** | Poland | RTO | **GOOD** | Leading European UGV manufacturer; TRL 7-9 platforms in 28 countries; widening country | ROS 2 unconfirmed; defence-primary; no UAV |
| 3 | **SINTEF AS** | Norway | RTO | **GOOD** | CURSOR WP3 lead + INGENIOUS; SAR integration proven; Nordic | Not SME; no own platforms; integrator not manufacturer |
| 4 | **Avular Innovations** | Netherlands | SME | **CONDITIONAL** | ROS 2 native; dual UGV+UAV; Benelux; PROACTIF | Young company; no SAR field experience; capacity risk |
| 5 | **FOI** | Sweden | Gov. agency | **CONDITIONAL** | INGENIOUS partner; SAR radar; Nordic EU MS | Govt agency; no platforms; defence-primary |
| 6 | **VTT** | Finland | RTO | **CONDITIONAL** | PROACTIF; autonomous vision; Nordic EU MS | No platforms; limited SAR deployment; high overhead |
| 7 | **Alpha Unmanned** | Spain | SME | **CONDITIONAL** | RESPONDRONE; mature helicopter UAV; TRL 8-9 | UAV only; ROS 2 unclear; Spain overlap; single EU project |

---

## Recommended Combinations for CORTEX Consortium

### Option A: Maximum SAR Pedigree + Widening (Recommended)
**Primary**: Robotnik (Spain, SME) -- UGV platforms, ROS 2, SAR integration lead
**Secondary**: INESC TEC (Portugal, RTO) -- UAV systems, communications, widening country
**Rationale**: Both are already HURRICANE partners (know each other), complementary strengths (Robotnik = UGV hardware, INESC TEC = aerial/comms), Portugal adds widening dimension. Total robotics budget: ~EUR 500k Robotnik + ~EUR 300k INESC TEC.

### Option B: Dual Widening + UGV Depth
**Primary**: Robotnik (Spain, SME) -- UGV platforms, ROS 2
**Secondary**: Lukasiewicz-PIAP (Poland, RTO) -- additional UGV platforms, CBRN capability, widening country
**Rationale**: Two widening countries (if PLUX also joins for biosensors). PIAP adds CBRN-hardened UGV capability that Robotnik's research platforms lack. Risk: ROS 2 compatibility of PIAP platforms must be verified.

### Option C: Platform + Integration Split
**Primary**: Robotnik (Spain, SME) -- UGV/UAV hardware platforms
**Secondary**: SINTEF (Norway, RTO) -- autonomy software, simulation, SAR integration
**Rationale**: Clean division between hardware (Robotnik) and integration/software (SINTEF). SINTEF's CURSOR experience in building SAR robot prototypes and control software complements Robotnik's commercial platforms. Nordic diversity.

### Option D: SME-Heavy + Benelux
**Primary**: Robotnik (Spain, SME) -- UGV platforms, SAR integration
**Secondary**: Avular (Netherlands, SME) -- modular ROS 2 UGV, UAV platforms, Benelux
**Rationale**: Two SMEs for strong SME count. Avular's ROS 2 native stack simplifies integration. Risk: Avular lacks SAR field experience.

---

## Cross-Reference: Partners Appearing in Multiple Searched Projects

| Organisation | Projects Found In | Countries |
|-------------|-------------------|-----------|
| SINTEF AS | CURSOR, INGENIOUS | Norway |
| INESC TEC | RESPONDRONE, HURRICANE | Portugal |
| Lukasiewicz-PIAP | ASSISTANCE, PROACTIF | Poland |
| Sodertorns Brandforsvarsförbund | INGENIOUS, ASSISTANCE | Sweden |
| Trilateral Research | CURSOR, INGENIOUS | Ireland |
| Thales SIX GTS France | RESPONDRONE, TeamAware | France |
| DLR (Deutsches Zentrum fur Luft- und Raumfahrt) | RESPONDRONE, INGENIOUS | Germany |
| SDIS Haute-Corse (fire service) | RESPONDRONE, HURRICANE | France |
| Elliniki Omada Diasosis (Greek rescue) | CURSOR, INGENIOUS | Greece (excluded) |

*Multi-project appearances indicate organisations with sustained commitment to SAR/first-responder EU research.*

---

## Next Steps

1. **Priority outreach**: INESC TEC (CRAS centre) -- verify ROS 2 status, confirm interest, check HURRICANE timeline overlap
2. **Secondary outreach**: Lukasiewicz-PIAP -- verify ROS 2 / open API compatibility of UGV platforms, confirm civilian SAR team availability
3. **Explore SINTEF**: If consortium needs integration/software partner separate from platform provider
4. **Verify Avular**: Financial capacity for EUR 500k, SAR ruggedisation roadmap
5. **Update partner_matrix.md**: Add INESC TEC and PIAP as CANDIDATE entries for GAP-01

---

## Sources

- [CORDIS - CURSOR Project 832790](https://cordis.europa.eu/project/id/832790)
- [CORDIS - RESPOND-A Project 883371](https://cordis.europa.eu/project/id/883371)
- [CORDIS - RESPONDRONE Project 833717](https://cordis.europa.eu/project/id/833717)
- [CORDIS - INGENIOUS Project 833435](https://cordis.europa.eu/project/id/833435)
- [CORDIS - HURRICANE Project 101168017](https://cordis.europa.eu/project/id/101168017)
- [CORDIS - PROACTIF Project 101194239](https://cordis.europa.eu/project/id/101194239)
- [CORDIS - TeamAware Project 101019808](https://cordis.europa.eu/project/id/101019808)
- [CORDIS - ASSISTANCE Project 832576](https://cordis.europa.eu/project/id/832576)
- [CORDIS - TRIFFID Project 101168042](https://cordis.europa.eu/project/id/101168042)
- [INESC TEC - Robotics and Autonomous Systems (CRAS)](https://www.inesctec.pt/en/centres/cras)
- [INESC TEC - RESPONDRONE Project Page](https://www.inesctec.pt/en/projects/respondrone)
- [INESC TEC - ICARUS Project Page](https://www.inesctec.pt/en/projects/icarus-cras)
- [Lukasiewicz-PIAP Official Website](https://piap.lukasiewicz.gov.pl/en/)
- [Lukasiewicz-PIAP Mobile Robots](https://piap.lukasiewicz.gov.pl/en/products/mobile-robots-for-special-applications/)
- [Lukasiewicz-PIAP in iMUGS2](https://lukasiewicz.gov.pl/en/lukasiewicz-piap-plays-a-key-role-in-the-new-european-imugs2-project-developing-interoperable-unmanned-ground-systems/)
- [SINTEF - INGENIOUS Project](https://www.sintef.no/en/projects/2019/ingenious/)
- [SINTEF - CURSOR Consortium Page](https://www.cursor-project.eu/the-team/consortium/sintef/)
- [SINTEF - Robotics and Autonomy](https://www.sintef.no/en/sintef-research-areas/robotics-and-autonomy/)
- [Avular Official Website](https://www.avular.com/)
- [Avular - Robots (ROS 2)](https://www.avular.com/robots)
- [Avular at ERF 2024](https://www.rockingrobots.com/dutch-innovation-at-erf-2024-avular-and-im-systems/)
- [FOI - Swedish Defence Research Agency](https://www.foi.se/en/foi.html)
- [VTT - Innovative Air Mobility](https://www.vttresearch.com/en/ourservices/innovative-air-mobility)
- [VTT - Defence and Security](https://www.vttresearch.com/en/industries/defence-and-security)
- [Alpha Unmanned Systems](https://alphaunmannedsystems.com/)
- [Alpha Unmanned - Wikipedia](https://en.wikipedia.org/wiki/Alpha_Unmanned_Systems)
- [ResponDrone Partners](https://respondroneproject.com/partners/)
- [HURRICANE Project Partners](https://www.hurricane-project.eu/partners)
- [PROACTIF Project Website](https://proactif-project.eu/)
