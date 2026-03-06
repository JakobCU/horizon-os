# Consortium Scout Report -- GAP-01, GAP-02, GAP-03
# CORTEX (HORIZON-CL3-2026-01-DRS-03)

> **Scout**: Consortium Scout Agent
> **Date**: 2026-03-06
> **Round**: 1
> **Coordinator**: AIT Austrian Institute of Technology, Center for Technology Experience (Austria)

---

## GAP-01: Robotics / Autonomous Systems Partner

**Need**: UGV + UAV platforms with autonomy API (ROS 2 compatible), SAR field experience
**Budget**: ~EUR 500,000 | **Role**: WP3 co-lead (Adaptive Autonomy Manager), BB5 (robot platforms)
**Preference**: NOT Greek. German, Italian, Spanish, Nordic, or Eastern EU preferred.

---

### Candidate 1.1: Robotnik Automation SLL (Spain)

| Field | Detail |
|-------|--------|
| **Full Name** | Robotnik Automation SLL |
| **Country** | Spain (Valencia / Paterna) |
| **Type** | SME (~70-80 employees, ~EUR 5.8M revenue) |
| **Website** | https://robotnik.eu |

**Why they fit:**

- **Direct SAR project experience across multiple EU programmes.** Robotnik is a partner in HURRICANE (Horizon Europe, 101168017) -- a 15-partner project on UGV-based resilient real-time intelligence for crisis and emergency, involving UAV-UGV cooperation, 5G comms, and laser-based charging. They also participated in FASTER (H2020, 833507) as WP5 leader for autonomous platforms (RB-CAR and SUMMIT-XL robots for first responder use), RESPOND-A (H2020, next-gen equipment for first responders), and the INTREPID project.
- **ROS 2 native.** Robotnik is one of the most prominent European ROS integrators. They offer ROS 2 migration services and all their platforms (SUMMIT-XL, RB-CAR, RB-VOGUI) ship with ROS 2 APIs. Their publication "Professional Service Robotics Applications with ROS" (Springer, 2017) is a reference in the field.
- **Dual UGV + UAV capability.** In FASTER they deployed both ground robots (SUMMIT-XL for exploration, RB-CAR for transport) and coordinated with drone partners. In HURRICANE they work on UAV-UGV cooperation pathways.
- **TRL 6+ platforms.** Their SUMMIT-XL and RB-VOGUI product lines are commercial products (TRL 8-9 as base platforms) that are customised for research at TRL 6-7 in SAR configurations.
- **SME status confirmed.** Classified as "Innovative SME" by the EC. Appropriate budget absorption for EUR 500k.

**Risk flags:**
- Robotnik is already in HURRICANE (running through ~2027). Need to confirm they have capacity for a parallel project starting late 2027. Given their size (~70-80 staff) and the fact that HURRICANE would be winding down, this is manageable.
- They are Spanish -- good for geographic diversity with AIT (Austria), but Spain is heavily represented in CL3 consortia, so evaluators may see this as "usual suspects." Mitigated by their genuine technical excellence.
- As an SME, they may push for higher overhead rates.

**Recommendation: STRONG_FIT**

Robotnik is the single strongest candidate across all searches. They have the exact platform portfolio (UGV + UAV coordination), the exact software stack (ROS 2), and the exact EU project pedigree (FASTER, RESPOND-A, HURRICANE) that this gap demands. Their SME status also helps the consortium's SME count.

---

### Candidate 1.2: Fraunhofer FKIE -- Cognitive Mobile Systems Department (Germany)

| Field | Detail |
|-------|--------|
| **Full Name** | Fraunhofer-Institut fuer Kommunikation, Informationsverarbeitung und Ergonomie (Fraunhofer FKIE) |
| **Country** | Germany (Wachtberg / Bonn) |
| **Type** | RTO (part of Fraunhofer-Gesellschaft) |
| **Website** | https://www.fkie.fraunhofer.de |

**Why they fit:**

- **German Rescue Robotics Center (DRZ) co-founder.** Fraunhofer FKIE is a founding partner of the DRZ, Germany's national competence center for rescue robotics. Their primary task is design and development of heavy tracked outdoor robotic platforms (D3 demonstrator class) and cross-platform modularization concepts.
- **ROS expertise confirmed.** FKIE has developed software to exchange information between the IOP domain and ROS, and publishes open-source ROS packages on GitHub (github.com/fkie). They have demonstrated autonomous teams of heterogeneous UGVs and UAVs using ROS and BML interfaces.
- **European Robotics Hackathon (EnRicH) 2025.** FKIE co-organized and participated in EnRicH 2025, testing ground robots and drones under realistic SAR conditions -- combined driving/flying scenarios across Search & Rescue, CBRN, and mapping.
- **Strong publication record** in multi-robot systems, SLAM, autonomous exploration, and human-robot teaming for SAR.
- **German RTO.** Excellent geographic complement to AIT (Austria) and would bring gravitas to the consortium as a large, established defence/security research institute.

**Risk flags:**
- **Not an SME.** As part of Fraunhofer-Gesellschaft, they are a large RTO. This does not help the consortium's SME target. However, the partner matrix already has SME slots for GAP-02 and GAP-03.
- **Budget absorption.** Fraunhofer institutes typically have high overhead (sometimes >100% flat rate). EUR 500k may not buy as many PMs as with an SME. Need to negotiate scope carefully.
- **Defence orientation.** Some of FKIE's work is dual-use/defence. For a purely civil security call (CL3-DRS), ensure the team proposed has clear civil SAR credentials (DRZ work qualifies).
- **Potential competing interest.** Fraunhofer institutes participate in many CL3 proposals. Need to verify they are not already committed to a competing consortium for DRS-03.

**Recommendation: GOOD_FIT**

Excellent technical match with deep SAR robotics credentials and the DRZ pedigree. The main drawback vs. Robotnik is that FKIE is not an SME and has higher overhead. Best positioned as a backup if Robotnik declines, or as an additional partner if budget allows expanding the consortium.

---

### Candidate 1.3: Eurecat -- Centre Tecnologic de Catalunya (Spain)

| Field | Detail |
|-------|--------|
| **Full Name** | Eurecat, Centre Tecnologic de Catalunya |
| **Country** | Spain (Barcelona / Sabadell) |
| **Type** | RTO (largest technology center in Catalonia, 450+ professionals) |
| **Website** | https://eurecat.org |

**Why they fit:**

- **ICARUS project pedigree.** Eurecat participated in the ICARUS project (Assisted Rescue and Unmanned Search Operations), contributing multirotor systems optimized for SAR operations. The project involved up to 10 aerial, ground, and marine vehicles with victim detection sensors.
- **Autonomous systems group.** Eurecat's robotics team works on aircraft design, localization, SLAM, trajectory planning, control strategies, and abstraction layers for autonomous and semi-autonomous navigation in unstructured indoor/outdoor environments -- directly applicable to SAR.
- **Aero-Train project.** Currently participating in the EUR 4.1M Aero-Train project (14 partners, 7 countries) for aerial robotics applied to infrastructure inspection, demonstrating current EU project activity.
- **RTO with broad capabilities.** As Catalonia's major technology center, they bring not just robotics but also sensor integration, AI, and data processing capabilities that could span WP3 and beyond.

**Risk flags:**
- **Two Spanish candidates** (Robotnik and Eurecat). Having both would over-represent Spain. Choose one.
- **Less focused on UGV.** Eurecat's SAR robotics expertise leans more toward aerial platforms (drones). UGV capabilities are present but less prominently showcased than at Robotnik.
- **RTO, not SME.** Same issue as Fraunhofer FKIE -- does not contribute to the SME count.
- **ICARUS project is older** (FP7 era). More recent SAR-specific project evidence is thinner compared to Robotnik's FASTER/HURRICANE.

**Recommendation: CONDITIONAL**

Solid technical profile, but weaker SAR-specific pedigree than Robotnik, and having two Spanish partners for GAP-01 creates redundancy. Best considered if Robotnik and Fraunhofer FKIE both decline, or if the consortium specifically needs stronger aerial/drone expertise separate from UGV.

---

## GAP-02: C2 System Integrator

**Need**: SME or mid-cap with existing operational C2 platform deployed with European fire/rescue services
**Budget**: ~EUR 400,000 | **Role**: WP4 co-lead (Adaptive C2 Overlay)
**Ideal**: EDXL support, API-accessible platform, EU project experience

---

### Candidate 2.1: IES Solutions / Webgenesys S.p.A. (Italy)

| Field | Detail |
|-------|--------|
| **Full Name** | IES Solutions S.r.l. (merged into Webgenesys S.p.A. as of October 2023) |
| **Country** | Italy (Catania, Sicily) |
| **Type** | SME (now part of Webgenesys mid-cap group) |
| **Website** | https://ies.solutions |

**Why they fit:**

- **JIXEL platform -- the exact product needed.** JIXEL is a web-based joint control room suite enabling fire brigades, ambulances, police, and civil protection to exchange information during day-to-day operations and catastrophic events. It is the first Web 2.0 Joint Control Room for interoperability between emergency services.
- **EDXL-compliant -- confirmed.** JIXEL is explicitly EDXL-CAP compliant and EDXL-DE enabled, implementing a Service Oriented Architecture. This directly satisfies the EDXL requirement in the gap specification.
- **Operational deployment with European civil protection.** JIXEL is deployed as a cloud service with Regione Sicilia (Italy) and extended to West Attica and Evros regions (Greece) for end-to-end management of emergency operations, from risk nowcasting to response coordination.
- **Strong EU project track record.** IES Solutions participated in RESILOC (H2020, Resilient Europe and Societies by Innovating Local Communities) as technical coordinator, and the FP7 EmerGent project. The JIXEL platform was enriched with resilience evaluation features through RESILOC.
- **Italian national standard adoption.** The XML data format developed through IES's project experience was adopted by the Italian Ministry of Interiors as the national standard for data exchange between control rooms (Decree 17 June 2008, based on CAP protocol).
- **API-accessible.** JIXEL is built on a SOA (Service Oriented Architecture) with RESTful web services, making it API-accessible by design.
- **Southern Italy / Widening dimension.** Sicily-based, which could contribute to the Horizon Europe widening objective (Italy is not a widening country, but southern Italy is often underrepresented).

**Risk flags:**
- **Corporate structure change.** IES Solutions merged into Webgenesys S.p.A. in October 2023. Need to verify: (a) whether Webgenesys still qualifies as an SME or is now a mid-cap, (b) whether the JIXEL team and key personnel are intact, and (c) the legal entity name for the Grant Agreement.
- **Regional focus.** Current deployments are primarily in Italy (Sicily) and Greece. Broader European deployment evidence is limited, though the technology is inherently scalable.
- **Niche company size.** May have limited bandwidth for a EUR 400k commitment alongside commercial operations. Need to verify staffing capacity.

**Recommendation: STRONG_FIT**

IES Solutions / Webgenesys is the strongest C2 candidate identified. JIXEL is purpose-built for exactly the interoperability scenario CORTEX needs, with confirmed EDXL compliance, operational deployment with fire/rescue services, and a meaningful EU project track record. The corporate restructuring needs due diligence but is not a deal-breaker.

---

### Candidate 2.2: CS GROUP / DIGINEXT -- Crimson Platform (France)

| Field | Detail |
|-------|--------|
| **Full Name** | CS GROUP (DIGINEXT brand) |
| **Country** | France (Toulouse) |
| **Type** | Mid-cap / Large Enterprise (international group, civilian + military) |
| **Website** | https://www.crimson.eu |

**Why they fit:**

- **Crimson platform -- mature, deployed C2/C4ISR system.** Crimson is a multi-domain, data-centric C2 system leveraging digital twins, simulation, extended reality, and AI for situational awareness, information sharing, coordination, and decision support. Conceived in 2005 as an EU co-funded R&D project.
- **Massive fire service deployment.** Over 75 French Fire and Rescue Department Services have adopted Crimson Tactic for emergency operations (wildfires, flooding, earthquakes, COVID). Crimson Tactic was designed for firefighters' Advanced Command Posts and municipal Emergency Action Plans.
- **Multi-country deployment.** Deployed in Austria, Italy, Greece, Spain, and Turkey through the iProcureSecurity PCP project (H2020). This demonstrates cross-border interoperability.
- **Extensive EU project portfolio.** Crimson is described as "the reference research platform in Europe" for crisis management. Used day-to-day by police forces, fire services, rescue organizations, and medical teams across multiple EU projects. Also assessed in the DIREKTION network.
- **Austrian deployment.** Already deployed in Austria, which creates a natural connection to the AIT-led consortium.

**Risk flags:**
- **NOT an SME.** CS GROUP is an international group with ~2,300 employees (acquired by Sopra Steria in 2022). This is a large enterprise, which does not satisfy the "SME or mid-cap" preference in the gap description. The consortium's SME balance would need to be met elsewhere.
- **French origin.** France is heavily represented in CL3 consortia. Not a problem per se, but does not add geographic novelty.
- **Cost structure.** As a large enterprise, day rates and overhead will be significantly higher than an SME. EUR 400k may buy limited person-months.
- **Sopra Steria acquisition.** CS GROUP was acquired by Sopra Steria (a major IT services firm) in 2022. This further distances the entity from SME status and may introduce corporate bureaucracy into consortium decision-making.
- **Dual civilian-military orientation.** Some Crimson capabilities are military C4ISR. Need to ensure the civil protection configuration is proposed, not the military one.

**Recommendation: CONDITIONAL**

Crimson is technically the most mature and widely deployed C2 platform identified, but CS GROUP's large enterprise status is a significant misfit for the consortium's SME needs. Best considered if: (a) the consortium secures enough SMEs elsewhere, or (b) a DIGINEXT sub-unit can be ring-fenced as a contributing entity with more manageable overhead. Also a strong option if IES Solutions / Webgenesys has capacity issues.

---

### Candidate 2.3: Frequentis AG / Regola S.r.l. (Austria / Italy)

| Field | Detail |
|-------|--------|
| **Full Name** | Frequentis AG (with Regola S.r.l. as subsidiary since 2022) |
| **Country** | Austria (Vienna) / Italy (Turin) |
| **Type** | Mid-cap (~2,000 employees, publicly traded on Vienna Stock Exchange) |
| **Website** | https://www.frequentis.com / https://en.regola.it |

**Why they fit:**

- **ASGARD and ICCS platforms.** Frequentis provides ASGARD (voice communication system for fire/rescue control rooms) and ICCS (Integrated Command and Control System), combining voice, video, and data with support for NENA i3 (NG911), EENA LTD (NG112), TCCA, and ETSI standards.
- **Regola subsidiary -- fire-specific software.** Regola (Turin, acquired 2022) develops Unique Fire, a tactical software for fire brigade and private fire service operations, and Unique EMS for medical emergency control rooms. Regola has been in the emergency management market since 1995.
- **Operational deployment.** Frequentis/Regola solutions are deployed with fire/rescue and EMS organizations across Europe, including South Tyrol (Italy/Austria border region), Norway, and multiple other countries.
- **Austrian company.** Same country as coordinator AIT, which simplifies coordination logistics but reduces geographic diversity.
- **Control Room Solution.** The combined Regola tactical software + Frequentis LifeX platform creates an integrated control room solution specifically for public safety.

**Risk flags:**
- **NOT an SME.** Frequentis is a publicly traded mid-cap company (~EUR 400M revenue). Well above SME thresholds.
- **Same country as coordinator.** Both AIT and Frequentis are Austrian. This reduces geographic diversity and may raise evaluator concerns about national concentration. The Regola (Italy) subsidiary partially mitigates this.
- **Commercial product focus.** Frequentis may be reluctant to open APIs or adapt their commercial platform for a research project. Their R&D budget allocation model may differ from typical EU project participants.
- **Overhead and bureaucracy.** As a publicly traded company, Frequentis has corporate governance requirements that can slow consortium decision-making.
- **EDXL support unclear.** Frequentis supports NENA, EENA, TCCA, and ETSI standards, but explicit EDXL-CAP/DE support was not confirmed in searches. This needs verification.

**Recommendation: CONDITIONAL**

Frequentis/Regola has the right product portfolio but is a poor organizational fit: too large, too expensive, same country as coordinator, and unclear EDXL support. Consider only if IES Solutions and CS GROUP both fall through, and if the Regola subsidiary (Italy) can be the contracting entity to improve geographic diversity.

---

## GAP-03: Biosignal Hardware / Wearable Manufacturer

**Need**: Ruggedised biosignal sensors (ECG, EDA, temperature, SpO2) for PPE integration
**Budget**: ~EUR 350,000 | **Role**: WP2 co-develop (BB1 hardware)
**Ideal**: SME, can produce small series (20-50 units), EU project experience preferred

---

### Candidate 3.1: Smartex S.r.l. (Italy)

| Field | Detail |
|-------|--------|
| **Full Name** | Smartex S.r.l. |
| **Country** | Italy (Pisa) |
| **Type** | SME |
| **Website** | https://www.smartex.it |

**Why they fit:**

- **SIXTHSENSE project -- direct first responder wearable experience.** Smartex was an SME partner in SIXTHSENSE (H2020, 883315), the EU project most directly relevant to GAP-03. They coordinated WP9 (System Integration), responsible for gathering results from all other WPs and producing Alpha, Beta, and Gamma system prototypes -- exactly the integration and small-series production capability needed.
- **E-textile biosignal expertise since 1999.** Smartex's core activity is implementing bio-sensing apparel (T-shirts, bands, vests) that monitor ECG, heart rate, respiration, activity indices, posture, gesture, and temperature. Sensors, electronics, and interconnections are woven directly into fabric -- exactly the textile-integrated sensor approach needed for PPE integration.
- **Wearable Wellness System (WWS).** Their WWS product includes hardware for acquisition, processing, storage, and transmission of textile sensor data, plus a complete software kit for data management and device configuration. This is a mature product line (TRL 7+).
- **Prior EU project heritage.** Smartex's technology traces back to EU-funded projects Wealthy and My Heart, demonstrating a 20+ year trajectory of EU-funded wearable biosignal research.
- **Small series production capability.** As an e-textile manufacturer, Smartex has the facilities to produce 20-50 units of custom sensor garments -- directly matching the requirement.
- **Italian SME.** Adds Italy to the consortium's country mix and contributes to the SME count.

**Risk flags:**
- **Niche company size.** Smartex is a small Italian SME. Need to verify current headcount and financial stability to absorb EUR 350k over the project duration.
- **ECG and respiratory focus.** Their core strengths are ECG, heart rate, and respiration. SpO2 and EDA capabilities were less prominently featured. May need a supplementary sensor module (e.g., PPG-based SpO2 clip) from another source.
- **Ruggedization for SAR.** Smartex's products are designed for comfort/wellness monitoring. Ruggedization to IP67+ and operating temperature range (-10C to +80C) for SAR PPE may require additional engineering, which should be budgeted within the project.
- **SIXTHSENSE project ended October 2023.** Need to confirm that key personnel (especially the WP9 integration lead) are still available.

**Recommendation: STRONG_FIT**

Smartex is the most directly relevant candidate for GAP-03. Their SIXTHSENSE pedigree (system integration lead for a first responder wearable health monitoring project), e-textile manufacturing capability, and 20+ year track record in biosignal garments make them a natural fit. The ruggedization gap is a known engineering challenge that the CORTEX project itself would address.

---

### Candidate 3.2: Senetics Healthcare Group GmbH & Co. KG (Germany)

| Field | Detail |
|-------|--------|
| **Full Name** | Senetics Healthcare Group GmbH & Co. KG |
| **Country** | Germany (Ansbach, Bavaria) |
| **Type** | SME |
| **Website** | https://www.senetics-healthcare.com |

**Why they fit:**

- **SIXTHSENSE project partner.** Senetics was an SME partner in SIXTHSENSE (H2020, 883315) and coordinated WP5 (development and validation of data fusion algorithms). They contributed directly to the sensor data fusion pipeline that combined multiple biosignal streams into actionable health status indicators.
- **Medical device development expertise.** Senetics is a specialized R&D and consulting company in medical technology, pharmacy, and biotechnology. They have developed telemedicine monitoring devices with industry partners and are currently developing a wearable hydration sensing device using sensor data fusion.
- **Sensor data fusion algorithms.** Their specific strength is not the hardware itself but the data fusion layer that combines multi-modal biosignal inputs -- ECG, EDA, temperature, SpO2 -- into meaningful physiological state assessments. This complements AIT's Cognitive Twin concept in WP2.
- **German SME in Bavaria.** Adds Germany to the country mix and contributes to the SME count. Bavaria has strong medical technology infrastructure.
- **Regulatory knowledge.** As a medical device consultancy, Senetics understands CE marking, MDR compliance, and the regulatory pathway for wearable health monitoring devices -- valuable for exploitation planning.

**Risk flags:**
- **Not a hardware manufacturer.** Senetics's strength is R&D, consulting, and algorithms -- not hardware manufacturing. They may not be able to produce the 20-50 ruggedised sensor units required. Would need to be paired with a hardware partner (e.g., Smartex for the garment, Senetics for the fusion algorithms).
- **Small company.** Need to verify current headcount and whether they can commit sufficient PMs for EUR 350k.
- **Overlap with AIT.** Both AIT and Senetics work on biosignal data processing/fusion. Role delineation would need to be clear: Senetics on hardware-level sensor fusion, AIT on higher-level Cognitive Twin modeling.

**Recommendation: GOOD_FIT**

Senetics brings valuable sensor data fusion and medical device expertise from SIXTHSENSE, but they are an R&D/consulting firm, not a hardware manufacturer. Best positioned as a complement to Smartex (Smartex builds the sensor garment, Senetics contributes fusion algorithms) rather than a standalone GAP-03 fill. If budget allows splitting GAP-03 between two partners, the Smartex + Senetics combination would be very strong.

---

### Candidate 3.3: PLUX -- Wireless Biosignals S.A. (Portugal)

| Field | Detail |
|-------|--------|
| **Full Name** | PLUX -- Wireless Biosignals S.A. |
| **Country** | Portugal (Lisbon) |
| **Type** | SME |
| **Website** | https://www.pluxbiosignals.com |

**Why they fit:**

- **Full biosignal sensor portfolio.** PLUX manufactures dedicated sensors for ECG, EDA, respiration, SpO2, EMG, EEG, temperature, and accelerometry -- covering all four biosignal modalities required (ECG, EDA, temperature, SpO2). Their biosignalsplux platform is a mature, modular, wireless acquisition system used in thousands of research labs worldwide.
- **First responder SAR application demonstrated.** Published academic research demonstrating PLUX biosignal technology for real-time biological sensor monitoring of first responders during SAR missions, measuring ECG, EDA, respiration, and EEG for stress, anxiety, and fatigue detection.
- **Hardware manufacturer with small-series capability.** Unlike Senetics, PLUX is a genuine hardware manufacturer. They produce sensor units, hubs, and complete kits. Producing 20-50 custom units is within their operational model.
- **Modular, API-accessible platform.** The biosignalsplux system supports Bluetooth and WiFi streaming with documented APIs (Python, MATLAB, C++, Unity), making integration with WP2's Cognitive Twin and WP4's C2 overlay straightforward.
- **Portugal -- Widening country.** Portugal is classified as a Horizon Europe widening country. Including PLUX would satisfy the consortium's widening dimension, which is a scored criterion in Horizon Europe evaluations.
- **EU project experience.** PLUX participates in the SUSTRONICS Project (sustainable electronics) and has a broad collaborative research network, though specific CL3/DRS project experience was not confirmed.

**Risk flags:**
- **No confirmed CL3/DRS EU project track record.** PLUX's EU project experience appears to be in health/research domains, not specifically in civil security or first responder contexts. The SAR application was an academic publication, not a funded EU project.
- **Research-grade vs. ruggedised.** PLUX sensors are designed for laboratory and clinical research environments. They are not inherently ruggedised for SAR conditions (IP67, extreme temperatures, PPE integration). Significant engineering would be needed to adapt their sensors for under-turnout-gear deployment.
- **No textile integration.** PLUX sensors are discrete clip-on/strap-on units, not woven into fabric. This is a different approach from the textile-integrated sensors in the gap description. Could be complementary (PLUX for SpO2/temperature modules, textile partner for ECG/EDA).

**Recommendation: CONDITIONAL**

PLUX has the broadest sensor portfolio and genuine hardware manufacturing capability, plus the valuable widening country dimension (Portugal). However, the lack of CL3 project experience and the ruggedization gap are significant. Best considered if: (a) the consortium specifically needs a widening country partner, (b) PLUX is paired with a textile integration partner, or (c) the project scope can accommodate a significant sensor ruggedization work package.

---

## Summary Ranking

| Gap | Rank | Candidate | Country | Type | Recommendation | Key Advantage |
|-----|------|-----------|---------|------|----------------|---------------|
| GAP-01 | 1 | **Robotnik Automation** | Spain | SME | STRONG_FIT | ROS 2 native, FASTER + HURRICANE pedigree, UGV+UAV |
| GAP-01 | 2 | Fraunhofer FKIE (CMS) | Germany | RTO | GOOD_FIT | DRZ co-founder, deep SAR robotics, but high overhead |
| GAP-01 | 3 | Eurecat | Spain | RTO | CONDITIONAL | ICARUS SAR drones, but weaker UGV + older references |
| GAP-02 | 1 | **IES Solutions / Webgenesys** | Italy | SME* | STRONG_FIT | JIXEL platform, EDXL-CAP/DE, deployed with fire services |
| GAP-02 | 2 | CS GROUP / DIGINEXT (Crimson) | France | Large | CONDITIONAL | Crimson in 75+ FR fire depts, but not SME |
| GAP-02 | 3 | Frequentis / Regola | Austria/Italy | Mid-cap | CONDITIONAL | Strong product, but same country as coordinator, not SME |
| GAP-03 | 1 | **Smartex** | Italy | SME | STRONG_FIT | SIXTHSENSE WP9 lead, e-textile biosensors since 1999 |
| GAP-03 | 2 | Senetics Healthcare Group | Germany | SME | GOOD_FIT | SIXTHSENSE data fusion, but R&D not manufacturing |
| GAP-03 | 3 | PLUX Wireless Biosignals | Portugal | SME | CONDITIONAL | Full sensor portfolio + widening country, but no CL3 pedigree |

## Recommended Primary Consortium Composition

If first-choice candidates accept:

| # | Partner | Country | Type | Gap Filled |
|---|---------|---------|------|------------|
| 1 | AIT CTE | Austria | RTO | Coordinator (existing) |
| 2 | Robotnik Automation | Spain | SME | GAP-01: Robotics/Autonomy |
| 3 | IES Solutions / Webgenesys | Italy | SME* | GAP-02: C2 System |
| 4 | Smartex | Italy | SME | GAP-03: Biosignal Hardware |

**Consortium balance with these additions:**
- Countries: 3 (Austria, Spain, Italy) -- meets minimum 3 MS requirement
- SMEs: 2-3 (Robotnik, Smartex, possibly IES/Webgenesys) -- meets >= 2 SME target
- Geographic spread: Central Europe + Southern Europe -- good
- Two Italian partners (IES + Smartex) -- acceptable, they are in different cities (Catania vs Pisa) and completely different domains

**Note:** GAP-04 through GAP-06 (end-users, medical authorities, ELSI) remain open and should add 2-3 more countries (Nordic, Eastern EU recommended) to strengthen geographic diversity.

## Next Steps

1. **Verify corporate status** of IES Solutions / Webgenesys (SME vs. mid-cap after merger)
2. **Draft outreach emails** for Robotnik, IES/Webgenesys, and Smartex (priority tier)
3. **Prepare backup outreach** for Fraunhofer FKIE and Senetics Healthcare (second tier)
4. **Check PLUX** for widening country benefit if consortium balance requires it
5. **Update partner_matrix.md** with candidate assignments and status changes

---

*Sources used in this research:*
- [CORDIS - CURSOR Project 832790](https://cordis.europa.eu/project/id/832790)
- [CORDIS - HURRICANE Project 101168017](https://cordis.europa.eu/project/id/101168017)
- [Robotnik HURRICANE page](https://robotnik.eu/projects/hurricane-project/)
- [Robotnik FASTER page](https://robotnik.eu/projects/faster-en/)
- [Robotnik RESPOND-A page](https://robotnik.eu/projects/respond-a-en/)
- [Robotnik Wikipedia](https://en.wikipedia.org/wiki/Robotnik_Automation)
- [Robotnik ROS 2 migration](https://robotnik.eu/ros-2-migration/)
- [Fraunhofer FKIE - DRZ](https://www.fkie.fraunhofer.de/en/departments/cms/drz.html)
- [Fraunhofer FKIE - CMS Department](https://www.fkie.fraunhofer.de/en/departments/cms.html)
- [Fraunhofer FKIE - EnRicH 2025](https://www.fkie.fraunhofer.de/en/press-releases/summary-european-robotics-hackathon-2025.html)
- [Eurecat - ICARUS](https://eurecat.org/en/portfolio-items/icarus/)
- [IES Solutions - JIXEL](https://ies.solutions/en/products/products-security/control-room/products-jixel/)
- [IES Solutions - RESILOC](https://ies.solutions/en/projects/eu-project-security/resiloc/)
- [IES Solutions - Our Story](https://ies.solutions/en/company/about-us/our-story/)
- [Crimson - R&D](https://www.crimson.eu/en/use-cases/r-d)
- [Crimson - Civil Security](https://www.crimson.eu/en/use-cases/civil-security)
- [Crimson - Deployed in Austria, Italy, Greece, Spain, Turkey](https://crimson.eu/en/news?catid=34%3Anews&id=110)
- [Frequentis Public Safety](https://www.frequentis.com/en/public-safety)
- [Regola - Unique Fire](https://en.regola.it/uniquefire/)
- [SIXTHSENSE Project](https://sixthsenseproject.eu/)
- [SIXTHSENSE - Smartex](https://sixthsenseproject.eu/smartex/)
- [SIXTHSENSE - Senetics](https://sixthsenseproject.eu/senetics-healthcare-group/)
- [SIXTHSENSE - BiFlow](https://sixthsenseproject.eu/biflow-systems-gmbh/)
- [Smartex Products](https://www.smartex.it/products)
- [CORDIS - SIXTHSENSE 883315](https://cordis.europa.eu/project/id/883315)
- [PLUX Biosignals](https://www.pluxbiosignals.com/)
- [CORDIS - FASTER 833507](https://cordis.europa.eu/project/id/833507)
- [ResponDrone Project](https://respondroneproject.com/)
