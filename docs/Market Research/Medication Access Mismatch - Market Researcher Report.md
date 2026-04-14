# Medication Access Mismatch - Market Researcher Report

## Market definition

The relevant market is **U.S. provider-side outpatient medication access workflow**: software and services that help a provider organization turn a prescribing decision into an actual therapy start.

It is broader than prior auth automation. The core workflow spans:

- patient-specific coverage and formulary intelligence
- prior authorization risk detection and submission support
- next-best-action recommendations such as covered alternatives, different pharmacies, or affordability programs
- staff work queues and orchestration across clinic, pharmacy, and patient-access teams
- patient-facing status and expectation management through first fill

This market sits between prescribing and dispensing. It overlaps with `RTBT/RTPB`, `ePA`, specialty pharmacy operations, and affordability tools, but is not identical to any one of them. The clearest category label is **medication access workflow software** or **medication access orchestration**.

What it includes:

- pre-prescription access intelligence
- point-of-prescribing recommendations
- post-prescription exception handling
- medication access team workflow
- first-fill conversion support

What it excludes:

- pure payer utilization management systems
- pharmacy dispensing systems by themselves
- manufacturer-only patient support hubs
- general medical prior auth APIs not focused on medications

## Market drivers

- **Administrative burden is already large and visible.** AMA's 2024 survey found practices complete `39` prior authorizations per physician per week and physicians plus staff spend `13 hours/week` on the process. `89%` said PA contributes to burnout.
- **Access delays have real clinical and business consequences.** In the same AMA survey, `93%` said PA delays necessary care and `82%` said it can lead to treatment abandonment.
- **Prescription-to-start failure is not a niche problem.** IQVIA reports `27%` of written prescriptions go unfilled across payers, driven by payer rejection and patient abandonment. That is broader than PA alone and supports the "mismatch" framing.
- **High-cost outpatient therapies are growing.** Specialty drugs represent a disproportionate share of pharmacy spend, which increases the value of getting routing, benefit checks, alternatives, and assistance right on the first attempt.
- **Digital rails now exist, but they do not solve the workflow.** Surescripts reported `2.6B` e-prescriptions filled in 2024 and `889,907` prescribers using Real-Time Prescription Benefit. The infrastructure is real; the orchestration layer is still incomplete.
- **Ambulatory EHR penetration is high enough for deployment.** About `88%` of office-based physicians use an EHR, so this is no longer blocked by basic digitization.
- **Regulatory pressure favors interoperability, but drug workflows remain under-served.** CMS prior-authorization interoperability rules focus mostly on medical services, not prescription drugs, leaving a product gap in outpatient medication access.

## Submarket map


| Submarket                    | What it does                                                                               | Typical buyer                                                  | Representative players                                                                       | Why it is insufficient alone                                                                 |
| ---------------------------- | ------------------------------------------------------------------------------------------ | -------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| `RTBT / RTPB`                | Shows patient-specific benefit and out-of-pocket info, sometimes PA flags and alternatives | EHR/IT, pharmacy, ambulatory ops                               | Surescripts, DrFirst, RxRevu, EHR-integrated tools                                           | Often appears too late in workflow; can be informative but not orchestrative                 |
| `ePA`                        | Digitizes PA initiation, questions, submission, and determination                          | Provider IT, ambulatory ops, pharmacy                          | CoverMyMeds, Surescripts CompletEPA, DrFirst, EHR modules                                    | Reactive after drug choice; does not solve affordability, routing, or patient follow-through |
| `Medication access workflow` | Coordinates staff tasks, recommendations, tracking, and first-fill conversion              | Health systems, specialty groups, med-access leaders           | Emerging/fragmented; overlaps with RxRevu, CoverMyMeds provider tools, homegrown work queues | Category is immature and not cleanly standardized                                            |
| `Specialty pharmacy support` | Benefits investigation, triage, limited-distribution routing, therapy onboarding           | Health systems with specialty pharmacy, large specialty groups | AssistRx, Shields, in-house specialty pharmacy teams                                         | Strong for specialty starts, weaker for broader ambulatory prescribing                       |
| `Affordability navigation`   | Finds copay, foundation, PAP, bridge, or free-drug support                                 | Financial navigation, pharmacy, social work                    | TailorMed, manufacturer assistance workflows, patient assistance vendors                     | Solves only one failure mode: affordability                                                  |
| `Adjacent admin automation`  | General prior auth APIs, RCM bots, intake automation                                       | CIO, rev-cycle, ops                                            | Availity, Waystar, payer portals, generic AI/RPA                                             | Usually not medication-specific and lacks prescribing context                                |


## TAM/SAM methodology

I use a **seat-based provider-software model** as the primary sizing method because public event-level pricing is sparse and many incumbents bundle features. I use an **event-based cross-check** only to test plausibility.

### Primary model

`TAM = relevant outpatient prescribers x annual software value per prescriber`

### Public denominator assumptions


| Assumption            | Public data point                                                                                  | Modeling choice                             | Confidence |
| --------------------- | -------------------------------------------------------------------------------------------------- | ------------------------------------------- | ---------- |
| Physicians            | `851,282` direct patient care physicians in 2023 (AAMC)                                            | Use `65%-75%` as outpatient-relevant        | Medium     |
| Nurse practitioners   | `320,400` employed NPs in 2024 (BLS)                                                               | Use `70%-80%` as outpatient-relevant        | Medium     |
| Physician assistants  | `189,907` board-certified PAs in 2024 (NCCPA)                                                      | Use `60%-70%` as outpatient-relevant        | Medium     |
| Annual contract value | No clean public list pricing; value inferred from labor savings and enterprise workflow importance | Use `$1,500-$3,000` per prescriber per year | Medium-low |


### Resulting relevant prescriber base

- Low case: `851,282 x 65% + 320,400 x 70% + 189,907 x 60% = 891,557`
- Mid case: `851,282 x 70% + 320,400 x 75% + 189,907 x 65% = 959,636`
- High case: `851,282 x 75% + 320,400 x 80% + 189,907 x 70% = 1,027,717`

### Event-based cross-check

This is not the primary model, but it supports the order of magnitude:

- Surescripts reports `2.6B` e-prescriptions filled in 2024.
- IQVIA reports `27%` of written prescriptions go unfilled.
- If only `5%-10%` of ambulatory prescriptions represent access-intensive moments worth intervention, and software captures `$4-$8` of value per high-friction event, the implied annual market is roughly `~$0.5B-$2.1B`.

That is directionally consistent with the seat-based result and suggests the seat-based model is not wildly inflated.

## Estimated TAM

Using the primary seat-based model:

- Low case: `891,557 x $1,500 = $1.34B`
- Mid case: `959,636 x $2,000 = $1.92B`
- High case: `1,027,717 x $3,000 = $3.08B`

**Estimated U.S. TAM: `$1.3B-$3.1B` annually**

**Most credible planning number: `~$1.9B-$2.1B`**

**Confidence: `medium-low`**

- Good confidence that the problem is large and persistent.
- Lower confidence on pricing because many comparison products are bundled, subsidized, or service-heavy.

## Estimated SAM

For initial go-to-market, the realistic SAM is not all outpatient prescribers. It is the subset inside organized providers that have both high medication-access friction and the operational capacity to buy an integrated workflow product.

### Serviceable segment definition

Include:

- large health systems and IDNs with specialty-heavy ambulatory care
- large multispecialty groups with centralized medication access teams
- specialty groups with high-cost branded and specialty prescribing
- organizations with owned or affiliated specialty pharmacy

Exclude, initially:

- solo and very small independent practices
- inpatient-heavy organizations
- organizations relying entirely on external pharmacy/hub services with little internal workflow ownership

### SAM assumptions

- Serviceable prescribers: `320k-450k`
- Initial pricing: `$1,500-$2,500` per prescriber per year`

### SAM outputs

- Low case: `320,000 x $1,500 = $480M`
- Mid case: `380,000 x $2,000 = $760M`
- High case: `450,000 x $2,500 = $1.13B`

**Estimated U.S. SAM: `$0.5B-$1.1B` annually**

**Most credible planning number: `~$750M`**

**Confidence: `medium`**

- Segment boundaries are clearer than TAM boundaries.
- Enterprise readiness and specialty mix make this a more defendable first market.

## Best buyer segments

The best initial buyers are not generic primary-care practices. They are organizations where medication-access failures are frequent, expensive, and operationally visible.

### 1. Large health systems with specialty-heavy ambulatory clinics

Best fit:

- dermatology
- rheumatology
- gastroenterology
- neurology
- endocrinology and obesity medicine
- pulmonology/allergy
- oral oncology programs

Why this segment wins first:

- high PA and formulary complexity
- expensive drugs and higher abandonment risk
- existing med-access staff to route work to
- strong ROI from avoided rework, faster starts, and specialty pharmacy capture

Likely economic buyers:

- ambulatory operations
- chief pharmacy officer / specialty pharmacy leadership
- service-line leadership
- CMIO/CIO as workflow gatekeepers

### 2. Large multispecialty groups with centralized refill and authorization teams

Why attractive:

- one buyer can standardize workflows across many prescribers
- labor savings are measurable
- enough branded prescribing volume to justify integration
- usually more agile than large hospital systems

### 3. IDNs with owned or affiliated specialty pharmacy

Why especially valuable:

- they can measure downstream conversion, leakage, and time-to-therapy
- routing intelligence directly affects internal capture
- access workflow and pharmacy economics are tightly linked

### Highest-value use cases

- **Specialty therapy initiation.** Biologics, oral oncology, migraine, inflammatory disease, and MS starts where PA, routing, and affordability all matter.
- **Covered alternative recommendation during the encounter.** Swap from a likely-to-fail order to a clinically acceptable covered option before the patient leaves.
- **PA packet automation with next-best action.** Prefill documentation, collect missing evidence, and route only the exceptions that need humans.
- **Pharmacy routing optimization.** Identify when retail, specialty, mail, or health-system pharmacy is the executable path.
- **Affordability navigation for deductible shock or copay cliffs.** Match patients to copay cards, PAPs, bridge programs, or cash options.
- **First-fill rescue workflow.** Detect abandoned or rejected scripts and trigger staff follow-up before therapy is lost.

## Competitive landscape

The market is fragmented because no single incumbent fully owns the provider-side medication access workflow.

### 1. Infrastructure and transaction rails

Examples:

- Surescripts
- CoverMyMeds
- DrFirst

Strengths:

- payer and pharmacy connectivity
- embedded transaction standards
- high scale and EHR integrations

Weakness:

- they mostly power transactions, not end-to-end provider team orchestration
- many workflows remain reactive after the prescription is chosen

### 2. Embedded EHR tools

Examples:

- Epic-integrated RTBT/ePA capabilities
- Oracle Health/Cerner capabilities
- athenahealth, Veradigm, eClinicalWorks modules

Strengths:

- native workflow placement
- distribution through existing provider systems
- lower change-management burden

Weakness:

- feature depth is often thinner than the operational problem
- innovation pace is slower
- many organizations still need external workflow, analytics, or staff tools around the EHR

### 3. Medication-access and prescribing intelligence vendors

Examples:

- RxRevu
- CoverMyMeds provider offerings
- overlapping point solutions around prescribing intelligence

Strengths:

- closer to the "Prescription Assistant" vision
- better fit for point-of-prescribing recommendations

Weakness:

- category still fragmented
- hard to win without deep EHR embedding and payer/pharmacy connectivity

### 4. Specialty pharmacy and patient-access service vendors

Examples:

- AssistRx
- Shields Health Solutions
- manufacturer hub services
- in-house med-access teams

Strengths:

- strong operational capability in high-friction therapies
- deep knowledge of benefits investigation and onboarding

Weakness:

- often service-heavy and concentrated in specialty meds
- can solve downstream exceptions without improving the upstream prescribing decision

### 5. Affordability navigation vendors

Examples:

- TailorMed
- internal financial navigation teams
- manufacturer assistance workflows

Strengths:

- strong on financial assistance discovery and enrollment
- clear ROI in oncology and specialty care

Weakness:

- affordability is only one piece of the mismatch problem
- does not by itself solve coverage rules, routing, or prescribing alternatives

### 6. Manual labor as the largest incumbent substitute

The biggest real-world competitor is still:

- nurses and MAs working payer portals
- pharmacy techs handling reroutes and callbacks
- specialty pharmacy liaisons
- patient calls and message threads
- fax, phone, and appeals

That matters strategically: the wedge is not "replace software X." It is **replace rework and fragmented labor with an action layer**.

## Risks and assumptions

- **Category overlap risk.** Budget may sit in ambulatory IT, pharmacy, specialty pharmacy, rev-cycle, or service lines rather than a clean standalone market.
- **Pricing opacity.** Many comparable tools are bundled into EHRs, network services, or service contracts, so the price range is inferred rather than directly observed.
- **Denominator uncertainty.** The model assumes outpatient relevance by role; actual contractable users may be fewer if a vendor sells to staff teams rather than all prescribers.
- **Vendor-reported outcomes bias.** Surescripts, CoverMyMeds, and others publish helpful scale data, but some performance claims are vendor-sponsored.
- **Workflow dependency risk.** If recommendations appear at the wrong time, the product becomes another alert rather than a useful intervention.
- **EHR platform risk.** Embedded EHR functionality could commoditize some features, forcing differentiation toward orchestration, analytics, and specialty workflows.
- **Proof burden.** Buyers will want evidence on time-to-therapy, first-fill conversion, staff productivity, and specialty pharmacy capture, not just faster PA turnaround.
- **Regulatory scope mismatch.** CMS interoperability rules improve adjacent workflows but still largely exclude prescription-drug PA, so regulatory tailwinds are indirect rather than complete.

## Source list

- [AAMC 2024 Key Findings and Definitions](https://www.aamc.org/data-reports/data/2024-key-findings-and-definitions)
- [BLS: Nurse Anesthetists, Nurse Midwives, and Nurse Practitioners](https://www.bls.gov/ooh/healthcare/nurse-anesthetists-nurse-midwives-and-nurse-practitioners.htm)
- [AANP: Data Sources and Methods for Counting Nurse Practitioners](https://storage.aanp.org/www/documents/research/NP_Count_Methods_Snapshot_2025.pdf)
- [NCCPA 2024 Statistical Profile of Board Certified PAs](https://www.nccpa.net/2024-statistical-profile-of-board-certified-pas-report/)
- [ASTP/HealthIT: Office-based Physician Electronic Health Record Adoption](https://www.healthit.gov/data/quickstats/office-based-physician-electronic-health-record-adoption)
- [AMA 2024 Prior Authorization Physician Survey](https://fixpriorauth.org/2024-ama-prior-authorization-physician-survey)
- [IQVIA: The Use of Medicines in the U.S. 2024](https://www.iqvia.com/insights/the-iqvia-institute/reports-and-publications/reports/the-use-of-medicines-in-the-us-2024)
- [IQVIA: Understanding the Use of Medicines in the U.S. 2025](https://www.iqvia.com/insights/the-iqvia-institute/reports-and-publications/reports/understanding-the-use-of-medicines-in-the-us-2025)
- [Surescripts 2024 Annual Impact Report Highlights](https://surescripts.com/insights/surescripts-2024-annual-impact-report)
- [KFF: Final Prior Authorization Rules Look to Streamline the Process, but Issues Remain](https://www.kff.org/private-insurance/issue-brief/final-prior-authorization-rules-look-to-streamline-the-process-but-issues-remain/)
- [KFF Health Tracking Poll: Prior Authorizations Rank as Public's Biggest Burden](https://www.kff.org/public-opinion/kff-health-tracking-poll-prior-authorizations-rank-as-publics-biggest-burden-when-getting-health-care/)
- [Effects of Real-time Prescription Benefit Recommendations on Patient Out-of-Pocket Costs](https://pmc.ncbi.nlm.nih.gov/articles/PMC9468947/)
- [Physician Perspectives on Implementation of Real-Time Benefit Tools](https://pmc.ncbi.nlm.nih.gov/articles/PMC9646401/)
- [Prior Authorization and Association With Delayed or Discontinued Prescription Fills](https://pmc.ncbi.nlm.nih.gov/articles/PMC10927330/)
- [The Patient Experience of Prior Authorization for Cancer Care](https://jamanetwork.com/journals/jamanetworkopen/fullarticle/2810824)
- [CoverMyMeds Provider Solutions](https://marketingbuilder.covermymeds.com/solutions/provider/)
- [Surescripts and Epic Improve Prescribing Accuracy and Efficiency with EHR-Integrated Electronic Prior Authorization](https://surescripts.com/press-releases/surescripts-and-epic-improve-prescribing-accuracy-and-efficiency-ehr-integrated-electronic-prior-authorization)
- [TailorMed Platform](https://tailormed.co/platform/)
- [AssistRx for Healthcare Providers](https://www.assistrx.com/partners/healthcare-providers/)
- [Shields Health Solutions](https://shieldshealthsolutions.com/)

