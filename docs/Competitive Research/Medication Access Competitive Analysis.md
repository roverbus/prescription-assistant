# Medication Access Competitive Analysis

Date: 2026-03-09

## Scope

This analysis evaluates the competitive landscape for a proposed product positioned as a point-of-prescribing Prescription Assistant for specialty ambulatory care. The concept helps clinicians assess whether a medication is realistically startable for a given patient, recommends executable alternatives when access risk is high, and supports clearer patient expectation-setting during the prescribing conversation.

Primary inputs:

- `PreScripts/Problem Statement/Product Strategy.md`
- `PreScripts/Problem Statement/Problem Statement.md`

Assumptions:

- Focus is U.S. outpatient specialty prescribing.
- Initial customers are large specialty ambulatory care organizations, specialty service lines within IDNs, and large independent specialty groups.
- Initial specialties of interest are rheumatology, dermatology, gastroenterology, neurology, and endocrinology/obesity medicine.

## Synthesized Summary

### Bottom line

The market is crowded in real-time benefit, prior authorization, and specialty initiation workflows, but there is still a meaningful gap at the exact moment this concept targets: helping a clinician decide whether a therapy is actually executable for a specific patient before the prescription creates downstream rework.

### Key takeaways

- The strongest direct product analog is `Arrive Health (RxRevu)`, because it already sits in the prescribing workflow and is expanding from RTBT-style guidance into AI-assisted medication access.
- The biggest ecosystem threat is `Surescripts`, because it owns a large share of the underlying benefit and prior auth infrastructure and could expand upward into more workflow intelligence.
- `CoverMyMeds` remains strategically important because it is still a default brand for medication access and is broadening into specialty onboarding and support workflows.
- `Epic` is less a pure functional competitor than a platform constraint. If native Epic workflows plus partners feel good enough, displacement becomes hard even if the incumbent experience is incomplete.
- Most incumbents optimize transaction execution after a therapy is chosen. The proposed product instead optimizes therapy selection quality before downstream work begins.
- Existing tools often surface isolated signals such as cost, coverage, or PA requirements, but they do not consistently synthesize those signals into an explainable, executable recommendation for the clinician in the room.
- Patient communication remains under-served. There is little evidence of a strong prescriber-time workflow that helps explain likely barriers, timing, next steps, and alternatives in plain language before the visit ends.
- Ambient AI note takers are an important adjacent threat because they are increasingly owning the in-visit workflow, clinician attention, and structured clinical context that could later power prescribing and medication-access actions.
- The best initial wedge appears to be high-friction specialty prescribing, especially inflammatory and biologic-heavy categories such as rheumatology, dermatology, and gastroenterology.
- The winning positioning is not "better ePA." It is "prescribing-moment executable therapy guidance" that reduces avoidable re-prescribing, accelerates time to therapy, and improves patient expectation setting.

## Competitive Landscape

### Direct competitors

These are the closest competitors to the prescribing-moment access decision.


| Competitor               | What it does                                                                                   | Why it matters                                                  |
| ------------------------ | ---------------------------------------------------------------------------------------------- | --------------------------------------------------------------- |
| `Arrive Health (RxRevu)` | In-EHR prescription benefit and medication access guidance                                     | Closest product shape to a prescriber-facing Prescription Assistant     |
| `Surescripts`            | RTBT, ePA automation, benefit intelligence, patient-facing price transparency                  | Strongest infrastructure-layer competitor with network reach    |
| `DrFirst`                | EHR-integrated price transparency, alternatives, and PA visibility                             | Strong affordability and formulary-aware prescribing competitor |
| `CoverMyMeds`            | Broad medication access platform spanning ePA, affordability, and specialty workflow expansion | Incumbent access brand with broad market mindshare              |
| `Epic`                   | Native prescribing surface with RTBT and partner integrations                                  | Key workflow owner and implementation gatekeeper                |


### Adjacent and indirect competitors

These companies solve important parts of the same problem, but usually later in the workflow.


| Competitor            | What it does                                                                         | Why it matters                                                                    |
| --------------------- | ------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------- |
| `TailorMed`           | Financial navigation, benefit verification, and assistance matching                  | Strong on affordability execution after therapy is chosen                         |
| `AssistRx`            | Specialty therapy initiation, enrollment, benefit verification, and patient support  | Strong specialty depth but more post-prescribing                                  |
| `Latent Health`       | AI-enabled PA, appeals, and specialty access operations                              | Emerging AI threat if it moves upstream                                           |
| `RxLightning`         | Specialty onboarding and enrollment workflow digitization                            | Relevant especially as part of CoverMyMeds                                        |
| `Abridge`             | Ambient clinical documentation expanding into real-time order generation inside Epic | Natural upstream entrant because it can turn conversation into structured actions |
| `Nabla`               | Ambient clinical documentation with broad EHR footprint and specialty templates      | Relevant because it can expand from note capture into visit workflow actions      |
| `Ambience Healthcare` | Ambient AI for documentation, coding, and broader clinical workflow support          | Important platform-style entrant with strong health-system traction               |


### Substitute approaches

Common substitutes include:

- Internal medication access coordinators and centralized PA teams
- Health-system specialty pharmacy teams that catch issues after prescribing
- Manual use of EHR alerts, payer portals, faxes, manufacturer forms, and pharmacy callbacks
- Bundled use of RTBT plus ePA plus affordability tools without a unified recommendation layer

## Detailed Competitor Assessment

### `Arrive Health`

**What it does**

Arrive Health provides in-workflow prescription benefit and medication access guidance inside the EHR. Public announcements indicate expansion into generative-AI-supported medication access and faster ePA preparation.

**Strengths**

- Closest current analog to the proposed concept
- Already embedded in provider workflow
- Strong story around payer-specific access context and faster medication access decisions
- Demonstrated traction with health systems

**Weaknesses versus the proposed concept**

- Public messaging still leans more toward affordability and PA acceleration than specialty-specific executable therapy guidance
- Less evidence of robust specialty routing or channel logic
- Limited visible differentiation in clinician-patient communication support

**Strategic implication**

This is the clearest direct competitor and should be treated as the primary benchmark.

### `Surescripts`

**What it does**

Surescripts provides RTBT, prior authorization automation, and broad benefit intelligence infrastructure used by EHRs, PBMs, payers, and providers.

**Strengths**

- Deep network reach and payer/PBM connectivity
- Strong raw data position around coverage, alternatives, and PA requirements
- Can influence both clinician workflow and patient transparency

**Weaknesses versus the proposed concept**

- More infrastructure-first than decision-support-first
- Limited public evidence of a specialty-specific "startability" Assistant
- Strong on data exchange, weaker on synthesized, explainable recommendations

**Strategic implication**

Surescripts is the biggest long-term platform threat even if it is not the most direct product substitute today.

### `DrFirst`

**What it does**

DrFirst provides EHR-integrated price transparency and medication benefit visibility, including expected out-of-pocket costs, coverage alternatives, and PA flags.

**Strengths**

- Clear affordability value proposition
- Strong fit for formulary-aware prescribing
- Easy to understand and implement in existing workflows

**Weaknesses versus the proposed concept**

- Appears narrower in scope than the proposed concept
- Less visible specialty access depth
- Less evidence of channel, routing, or affordability pathway orchestration

**Strategic implication**

DrFirst is an important comparison point, especially in broader ambulatory prescribing and obesity-related use cases, but is not as threatening as Arrive Health or Surescripts for the initial wedge.

### `CoverMyMeds`

**What it does**

CoverMyMeds has historically been known for ePA and broader medication access workflows. It has expanded into affordability, patient support, and specialty onboarding capabilities.

**Strengths**

- Strong medication-access brand recognition
- Large installed base and buyer familiarity
- Breadth across prior authorization and specialty-adjacent workflows

**Weaknesses versus the proposed concept**

- Center of gravity still appears downstream of the prescribing choice
- More focused on clearing the originally selected therapy than improving the initial therapy decision
- Less clearly positioned around in-room executable alternatives and patient expectation-setting

**Strategic implication**

CoverMyMeds is a broad market incumbent that may become more threatening if it unifies its access and specialty capabilities into a tighter prescriber-facing workflow.

### `Epic`

**What it does**

Epic owns the core prescribing workflow for many health systems and supports native and partner-enabled real-time benefit and prior authorization integrations.

**Strengths**

- Owns the clinician workflow surface
- Has major implementation and distribution leverage
- Can make partner functionality feel native

**Weaknesses versus the proposed concept**

- Epic is more a platform than a specialized access intelligence layer
- Native features may be adequate but not deeply differentiated
- Specialty access synthesis appears to rely on partners rather than native Epic-only logic

**Strategic implication**

Epic is the most important gatekeeper. Any market entry strategy should assume an Epic-first integration path and a complementary positioning.

### `TailorMed`

**What it does**

TailorMed focuses on affordability and financial navigation, including benefit verification, assistance matching, enrollment, and patient support workflows.

**Strengths**

- Strong patient affordability execution
- Good fit for health systems and specialty pharmacies
- Clear value around financial support operations

**Weaknesses versus the proposed concept**

- Generally enters after a therapy has already been selected
- Does not appear to own the clinician's prescribing decision moment
- More finance-centric than prescribing-centric

**Strategic implication**

TailorMed looks more like a downstream partner or expansion adjacency than a core direct competitor.

### `AssistRx`

**What it does**

AssistRx supports specialty therapy initiation and related workflows, including enrollment, benefit verification, PA, copay support, and patient status visibility.

**Strengths**

- Deep specialty workflow expertise
- Strong support for complex therapy initiation
- Relevant in high-friction specialty categories

**Weaknesses versus the proposed concept**

- Primarily focused after the medication choice is made
- Better aligned to coordinator or hub workflows than prescriber-first decision support
- Less clearly differentiated around alternative selection before the prescription is finalized

**Strategic implication**

AssistRx is a credible adjacent competitor in specialty-heavy lines, but more for downstream execution than initial therapy selection.

### `Latent Health`

**What it does**

Latent Health is an AI-native entrant focused on specialty PA, appeals, and access operations.

**Strengths**

- AI-first operating model
- Specialty credibility
- Strong narrative around administrative efficiency

**Weaknesses versus the proposed concept**

- Not clearly prescriber-facing today
- Focus appears operational rather than point-of-prescribing
- Limited evidence of clinician alternative recommendation workflows

**Strategic implication**

This is an emerging threat to watch because AI-native operations vendors could move upstream quickly.

### `Abridge`

**What it does**

Abridge started as an ambient clinical documentation platform, but has already expanded into generating outpatient medication orders and other order types inside Epic based on the clinician-patient conversation.

**Strengths**

- Owns the in-visit workflow and clinician attention
- Deep Epic partnership and embedded workflow presence
- Strong trust narrative through linked evidence and source-grounded outputs
- Broad specialty coverage and fast enterprise adoption

**Weaknesses versus the proposed concept**

- Current expansion appears broader around documentation and order generation, not specifically around medication-access intelligence
- Turning conversation into an order is not the same as determining whether that order is executable from coverage, routing, and affordability perspectives
- Less visible evidence today of specialty-specific alternative recommendation logic or access-risk explanation

**Strategic implication**

Abridge is one of the most important adjacent threats because it could naturally extend from "draft the order" to "recommend the best executable order." If it adds payer and access logic, it could become a serious competitor quickly.

### `Nabla`

**What it does**

Nabla is an ambient AI assistant focused on clinical documentation across multiple EHRs and specialties, with growing enterprise adoption in ambulatory and inpatient settings.

**Strengths**

- Broad EHR footprint
- Strong provider value proposition around documentation burden reduction
- Specialty-specific templates and configurable workflows

**Weaknesses versus the proposed concept**

- Public evidence is still concentrated on documentation rather than prescribing or medication-access logic
- Less visible traction in order-generation and medication workflow than Abridge
- Does not appear to own payer, formulary, specialty routing, or affordability reasoning

**Strategic implication**

Nabla is less of an immediate threat than Abridge, but it fits the same pattern: ambient tools can become workflow platforms once they own the clinician conversation.

### `Ambience Healthcare`

**What it does**

Ambience Healthcare positions itself as an AI platform for clinical documentation, revenue integrity, and broader clinical workflows across outpatient, emergency, and inpatient settings.

**Strengths**

- Strong enterprise health-system traction
- Broad specialty coverage
- Expanding beyond pure note generation into workflow and chart-aware intelligence
- Strong value story tied to operational and financial outcomes

**Weaknesses versus the proposed concept**

- Public positioning is still more centered on documentation, coding, and general workflow than specialty prescribing access
- Limited visible proof of medication-access-specific reasoning at the point of prescribing
- Does not appear to have a differentiated position in specialty routing or executable therapy alternatives

**Strategic implication**

Ambience matters because it shows how ambient vendors may evolve into general clinical workflow platforms. Even without deep medication-access capabilities today, it could become a bundling threat in enterprise deals.

## Comparison Against the Proposed Product


| Dimension                     | Current market state                                                                                       | Gap the proposed product can address                                                                                       |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| Timing in workflow            | Good progress on cost and PA visibility during prescribing, but richer specialty logic often appears later | Decide whether a therapy is realistically startable before the order creates downstream work                               |
| Explainability                | Many tools show separate data points and alerts                                                            | Synthesize access risk into a clear explanation clinicians can trust                                                       |
| Alternative recommendations   | Usually cost- or formulary-driven                                                                          | Recommend the most executable next-best therapy path                                                                       |
| Specialty depth               | Strong later in specialty initiation and support workflows                                                 | Bring specialty access intelligence earlier into therapy selection                                                         |
| Patient communication support | Fragmented and often downstream                                                                            | Help clinicians explain likely barriers and next steps in the visit                                                        |
| Implementation fit            | Incumbents benefit from existing EHR presence                                                              | Win by being lightweight, complementary, and ROI-visible without replacing existing systems                                |
| Visit workflow ownership      | Ambient AI vendors increasingly own note creation and order drafting inside the visit                      | Bring differentiated medication-access intelligence into that same moment before ambient vendors extend into this category |


## Most Important Market Gap

The clearest white space is an explainable specialty prescribing Assistant that combines:

- patient-specific access risk
- main driver of failure risk
- executable next-best alternatives
- pharmacy channel and specialty routing guidance
- affordability pathway guidance
- patient-ready talking points

This gap exists because current categories are split:

- RTBT tools are good at visibility into price and coverage
- ePA tools are good at processing authorization workflows
- specialty initiation tools are good at downstream execution
- EHRs are good at hosting workflow but are not the differentiated logic layer

No player clearly owns the full question: "Should this clinician choose this therapy for this patient right now, and if not, what is the most executable alternative?"

## Competitive Threats

### Highest-priority threats

1. `Arrive Health`
2. `Surescripts`
3. `CoverMyMeds`
4. `Epic`
5. `Abridge`

### Why they matter

- `Arrive Health` is the closest functional substitute.
- `Surescripts` has the strongest infrastructure and data moat.
- `CoverMyMeds` has the strongest medication-access brand recognition.
- `Epic` can compress differentiation by making access intelligence feel native or sufficiently bundled.
- `Abridge` is the most credible ambient AI entrant because it already converts visit conversation into draft medication orders inside Epic.

## How We Can Win

### Core answer

We win by owning a narrower but more defensible product truth than the incumbents:

**Not just whether a drug can be ordered, but whether it is realistically startable and what the best executable next step is for this patient.**

### Why this wedge can win

- `Arrive Health` is strong in access visibility, but the public story still centers on coverage insight and PA acceleration.
- `Surescripts` is strong in infrastructure and transactions, but not clearly in clinician-facing synthesis.
- `Ambient AI` vendors are strong in visit capture and workflow presence, but they do not yet appear to own medication-access reasoning.
- The proposed product can sit exactly where these categories overlap but none fully solve the problem: the moment a clinician needs a confident, explainable recommendation.

### What must be true to win

1. Be better than alerts.
  The product cannot simply warn that a medication may be hard to access. It must recommend the most executable next-best path.
2. Be better than RTBT.
  The output must go beyond price and covered alternatives to include likely documentation burden, specialty routing constraints, and affordability pathways.
3. Be better than note takers.
  Ambient AI may help create orders, but this product must decide whether the order is wise from an access-execution perspective.
4. Be better than coordinator tools.
  The product must prevent avoidable downstream work, not just help clean it up faster.

### Product choices that improve odds of winning

- Start with specialty categories where routing, PA, affordability, and alternative choice all matter at once.
- Make the access score explicitly explainable so clinicians can trust it in the visit.
- Show recommended alternatives in clinician-friendly language such as "most likely to start this week" rather than payer-centric jargon.
- Add patient-ready talking points so the product improves both execution and conversation quality.
- Use existing downstream infrastructure rather than trying to replace it.

## Recommended Wedge and Positioning

### Recommended wedge

Position the product as:

**The prescribing-moment executable therapy guidance layer for specialty biologics and other high-friction branded therapies.**

### Best initial segments

Best initial specialties:

- Rheumatology
- Dermatology
- Gastroenterology

Why these first:

- High specialty-medication complexity
- Frequent prior auth and step-therapy friction
- Real choice among alternatives
- Significant financial and routing complexity
- Strong opportunity to reduce downstream rework and time-to-therapy delays

### Positioning statement

Before the clinician signs the order, the product should answer:

- Is this therapy likely to be startable?
- Why might access fail?
- What is the most executable alternative?
- What should the patient be told right now?

### What makes the positioning defensible

- It is earlier than coordinator tools.
- It is broader than ePA.
- It is more actionable than RTBT alerts alone.
- It is more patient-communication-aware than infrastructure tools.

## How To Beat `Arrive Health`

`Arrive Health` is the competitor to beat because it is the closest current product shape. The best strategy is not to out-market it as another medication access tool, but to be obviously better on the dimensions where its public positioning is still thinner.

### Where `Arrive Health` appears strongest

- In-EHR workflow fit
- Existing customer traction
- Benefit and PA visibility
- Framing around faster medication access

### Where to differentiate

1. Go deeper into specialty execution logic.
  Focus on specialty pharmacy routing, channel constraints, affordability pathways, and documentation burden in ways that are especially valuable in rheumatology, dermatology, and gastroenterology.
2. Make alternatives more executable, not just covered.
  Recommend next-best therapy paths that optimize for speed-to-start and likelihood of successful initiation, not only formulary status.
3. Make the reasoning more transparent.
  Show the top 2 to 4 drivers of access risk in plain language. Clinicians should understand why the system is recommending a switch.
4. Own patient expectation setting.
  Turn the recommendation into language the clinician can use immediately with the patient. This is a weakly defended area in the current landscape.
5. Measure outcomes `Arrive` is less likely to own.
  Win on first-fill success, avoidable reroutes avoided, abandonment reduction, and patient understanding, not only PA turnaround.

### Practical go-to-market strategy against `Arrive`

- Sell into specialty service lines where generic RTBT-style guidance is not enough.
- Position as complementary to existing RTBT and ePA tools rather than as a replacement.
- Land with one or two high-friction therapy classes and prove operational ROI fast.
- Integrate into Epic in a lightweight way so workflow disruption is minimal.
- Build proprietary specialty rules, routing logic, and learned recommendation quality faster than `Arrive` can generalize.

## Monitoring Signals for the Next 12 Months

- Whether `Arrive Health` expands from PA acceleration into broader specialty access recommendations
- Whether `Surescripts` combines benefit intelligence, PA automation, and patient messaging into a fuller workflow product
- Whether `CoverMyMeds` integrates specialty onboarding more tightly into prescriber workflow
- Whether Epic raises the default floor for RTBT and medication access capabilities
- Whether AI-native operations vendors move upstream from coordinator workflows into clinician-facing guidance
- Whether ambient AI note takers, especially `Abridge`, expand from note generation and order drafting into medication-access recommendations
- Whether health systems increasingly prioritize integrated specialty pharmacy routing economics in prescribing decisions
- Whether obesity and GLP-1 market volatility changes the importance of payer policy intelligence in the prescriber workflow

## Sources

1. [Surescripts Real-Time Prescription Benefit](https://surescripts.com/what-we-do/real-time-prescription-benefit)
2. [Surescripts Prior Authorization Automation](https://surescripts.com/what-we-do/touchless-prior-authorization)
3. [Surescripts specialty and patient access pages](https://surescripts.com/specialty-patient-enrollment)
4. [Arrive Health launch announcement for AI-powered medication access](https://arrivehealth.com/press/arrive-health-in-partnership-with-aws-and-a-leading-integrated-delivery-network-launches-innovative-generative-ai-powered-solution-to-accelerate-medication-access/)
5. [UCHealth on Arrive Health medication access workflow](https://www.uchealth.org/today/arrive-health-takes-the-pain-and-time-out-of-prescription-prior-authorizations/)
6. [DrFirst price transparency](https://drfirst.com/price-transparency)
7. [McKesson / CoverMyMeds overview](https://www.mckesson.com/business-solutions/our-businesses/covermymeds/)
8. [McKesson story on specialty medication workflows](https://www.mckesson.com/stories-insights/digitally-transforming-specialty-medication-workflows/)
9. [Epic Open: real-time prescription benefit interfaces](https://open.epic.com/Interface/Other)
10. [TailorMed platform](https://tailormed.co/platform/)
11. [AssistRx iAssist](https://www.assistrx.com/specialty-pharmaceutical-solutions/iassist/)
12. [medRxiv: RTPB across three academic health systems](https://www.medrxiv.org/content/10.1101/2024.12.27.24318670v1)
13. [Implementation study for real-time prescription benefit](https://pmc.ncbi.nlm.nih.gov/articles/PMC10880821/)
14. [HealthIT quick stats: hospital adoption of RTBT](https://www.healthit.gov/data/quickstats/hospital-adoption-real-time-benefit-tools/)
15. [Latent Health](https://latenthealth.com/)
16. [AMA prior authorization survey press release](https://www.ama-assn.org/press-center/ama-press-releases/ama-survey-indicates-prior-authorization-wreaks-havoc-patient-care)
17. [KFF poll on prior authorization burden](https://www.kff.org/patient-consumer-protections/poll-finding/kff-health-tracking-poll-public-finds-prior-authorization-process-difficult-to-manage/)
18. [AHA summary of HHS HTI-4 rule](https://www.aha.org/news/headline/2025-09-02-hhs-announces-access-real-time-drug-pricing-changes-prior-authorization)
19. [Study on integrated vs external specialty pharmacy time to treatment](https://pmc.ncbi.nlm.nih.gov/articles/PMC10982575/)
20. [RxLightning homepage](https://rxlightning.com/)
21. [Abridge orders in real-time at the point of care](https://www.abridge.com/blog/orders-real-time-clinical-documentation)
22. [Abridge Inside for inpatient and outpatient orders](https://www.abridge.com/press-release/abridge-inside-for-inpatient-and-outpatient-orders)
23. [Nabla enterprise deployment with specialty templates and workflow expansion signals](https://www.nabla.com/press-release/neighborhood-healthcare-integrates-nablas-ambient-ai-to-support-clinicians-and-improve-patient-experience)
24. [Ambience Healthcare 2026 KLAS/CHIME Trailblazer announcement](https://www.businesswire.com/news/home/20260223783619/en/Ambience-Healthcare-Recognized-as-2026-KLASCHIME-Trailblazer-Award-Winner)

