# Medication Access Mismatch - Scientific Literature Researcher Report

## Bottom line
The broader medication access mismatch is real, material, and not well solved by current workflow tools. The strongest evidence is for two failure modes: `prior authorization` and `out-of-pocket cost`, both of which are associated with delayed starts, abandonment, discontinuation, and substantial patient/provider burden. Evidence for `formulary restrictions`, `step therapy`, and `pharmacy routing/network constraints` is directionally consistent but more fragmented and class-specific. Evidence for `patient confusion and communication failure` is strong on lived experience and burden, but less often tied to hard utilization endpoints.

Current interventions help pieces of the problem, not the whole path from prescribing intent to successful start. `ePA` improves transaction speed but has weak evidence on actual starts or adherence. `RTBT/RTPB` can lower patient cost in the subset of prescriptions where a clear cheaper alternative exists, but real-world uptake and behavior change are modest, and timing is often poor. `Integrated specialty pharmacy coordination` has some of the most practical evidence for reducing time to treatment, especially in specialty drugs. `Affordability support` works best when it actually lowers patient cost exposure; evidence is weaker and more vendor-linked when framed as branded patient support programs.

## Evidence by failure mode
**Prior authorization**
- Strongest peer-reviewed causal-style evidence: a 2023 `Journal of Clinical Oncology` study using Medicare Part D claims from `2010-2020` found that adding a new PA requirement to established oral anticancer drugs was associated with `7.1x` higher odds of discontinuation within 120 days and `9.7` additional days to next fill (`n=2,495` exposed patients vs `22,641` controls; quasi-experimental claims analysis). URL: `https://pubmed.ncbi.nlm.nih.gov/38086013/`
- Another strong policy example: a 2020 `JAMA Network Open` analysis of Medicare beneficiaries found that Medicare Part D PA restrictions on `buprenorphine-naloxone` were associated with lower prescribing, and removing those restrictions was associated with improved prescribing and lower downstream inpatient and ED use (`n≈949,206`; policy/claims analysis). URL: `https://jamanetwork.com/journals/jamanetworkopen/fullarticle/2764598`
- Provider burden evidence is very consistent, though survey-based rather than causal: the `AMA 2024` PA physician survey found `39` PAs per physician per week, `13` staff/physician hours per week, `93%` reporting delayed care, and `82%` reporting treatment abandonment risk. URL: `https://www.ama-assn.org/system/files/prior-authorization-survey.pdf`

**Cost-sharing / out-of-pocket burden**
- This is one of the most robust evidence areas. A `2025 JMCP` study using Symphony Health data found that each additional `$100` in patient OOP cost increased abandonment risk by `21%` for `nonvalvular atrial fibrillation` and `17%` for `venous thromboembolism` among first DOAC claims (`n=753,755 NVAF` and `308,429 VTE`; claims analysis). URL: `https://www.jmcp.org/doi/10.18553/jmcp.2025.31.4.366`
- A seminal but still highly relevant `2017 Journal of Clinical Oncology` study of new oral anticancer prescriptions found abandonment rose from `10.0%` at OOP `≤$10` to `49.4%` at OOP `>$2,000`, with delayed initiation also rising sharply (`n=38,111`; claims analysis). This is older than preferred, but still one of the clearest dose-response studies. URL: `https://ascopubs.org/doi/full/10.1200/JCO.2017.74.5091`
- A `2022` systematic review of cost-sharing and adherence literature reported that about `90%` of included studies found higher cost-sharing worsened adherence, persistence, or discontinuation. URL: `https://www.jmcp.org/doi/10.18553/jmcp.2022.21270`

**Formulary restrictions**
- Direct evidence exists, though it is less abundant than for PA or OOP burden. A `2024` study of Medicare patients with atrial fibrillation found delayed OAC initiation in `30.0%` of patients; PA was associated with delay (`OR 1.69`) and `Tier 4` formulary placement was also associated with delay (`OR 1.26`) (`n=446,441`; claims analysis). URL: `https://www.sciencedirect.com/science/article/pii/S2666602224000120`
- Descriptive Medicare Part D studies show that formulary coverage and restriction patterns vary substantially even within clinically similar drug classes. For `SGLT2i` and `GLP-1 RA`, a `2020` Medicare Part D review across `3,992` plans showed uneven coverage, frequent PA/step edits, and high OOP exposure despite strong clinical evidence for these therapies. URL: `https://pmc.ncbi.nlm.nih.gov/articles/PMC7563069/`
- Overall implication: formulary mismatch is a real barrier, but much of the literature measures it indirectly through delayed initiation or restricted coverage rather than direct abandonment.

**Step therapy**
- Evidence is real but thinner and more class-specific. A `2019 PharmacoEconomics - Open` study using IBM MarketScan data found that among RA/PsA patients initiating biologics, plan-level access restrictions including step therapy were associated with lower odds of treatment effectiveness, largely mediated by worse adherence (`n=5,706` across `25` plans; claims-based comparative analysis). URL: `https://link.springer.com/article/10.1007/s41669-019-0152-1`
- More recent evidence tends to be survey or policy oriented rather than rigorous natural experiments. For example, recent dermatology access surveys report frequent denials/delays involving step therapy, but these are weaker than the PA and OOP evidence.
- Net: step therapy likely contributes meaningfully to mismatch, but the independent outpatient evidence base is only moderate.

**Pharmacy routing / network constraints / limited distribution**
- In specialty drugs, routing matters. A `2024` retrospective Mayo Clinic study found median time to first fill for `palbociclib` was `6 days` via a health-system specialty pharmacy vs `12 days` via external specialty pharmacies (`n=88`; single-center retrospective analysis). URL: `https://pmc.ncbi.nlm.nih.gov/articles/PMC10982575/`
- Qualitative provider evidence is also consistent: a `2022 PLOS One` study of `14` providers in specialty clinics found that limited distribution networks and external pharmacy coordination created substantial workflow burden, communication friction, and risk of missed doses or care delays. URL: `https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0273040`
- This area is important for provider-facing product design because the failure often occurs after prescribing, outside the physician's direct line of sight.

**Patient confusion / communication failure**
- The best direct evidence is from oncology. A `2023 JAMA Network Open` cross-sectional survey of cancer patients (`n=178`, with qualitative responses from `89`) found `69%` reported PA-related delays, `22%` did not receive recommended care due to delays or denials, `67%` had to get personally involved, `20%` spent `11+` hours on the issue, and `72%` described the experience as bad or horrible. Qualitative themes included `blinded navigation`, `interference with care`, and a `broken system`. URL: `https://jamanetwork.com/journals/jamanetworkopen/fullarticle/2810824`
- Broader consumer evidence from `KFF 2023` found `16%` of insured adults had PA problems in the past year, with higher rates among Medicaid enrollees, high utilizers, and patients with diabetes or mental health needs (`n=3,605`; nationally representative survey). URL: `https://www.kff.org/affordable-care-act/consumer-problems-with-prior-authorization-evidence-from-kff-survey/`
- This is one of the clearest signals that even when a therapy eventually starts, the process itself can damage trust, create anxiety, and force patients into self-navigation.

## Intervention evidence
**Electronic prior authorization (`ePA`)**
- Best independent patient-outcome evidence is mixed to negative. A `2021` study of staggered `ePA` implementation in a large health system matched `38,851` ePA prescriptions to controls from `74,546` eligible prescriptions and found no improvement in 30-day fill; reported fill rates were `64.2%` vs `68.8%` in matched comparisons (`aRR 0.92`; quasi-experimental implementation analysis). URL: `https://pubmed.ncbi.nlm.nih.gov/34279657/`
- Some transaction-level studies report materially faster determinations with ePA than manual workflows, but much of that literature is operational and often vendor-linked.
- Takeaway: `ePA` helps with admin mechanics, but there is weak evidence that it reliably fixes medication initiation.

**RTBT / RTPB**
- Strongest positive evidence: a `2022 JAMA Internal Medicine` cluster RCT in an academic health system found that among `867,757` outpatient prescriptions, only `36,419` (`4.2%`) were eligible for a recommendation, but in those eligible prescriptions RTPB lowered patient OOP costs by `11.2%` overall and `38.9%` in high-cost drug classes. URL: `https://jamanetwork.com/journals/jamainternalmedicine/article-abstract/2796059`
- Real-world implementation evidence is more sobering. A recent multicenter retrospective study across three academic systems found alternatives were displayed in `45.0%` of prescribing encounters but clinicians selected an alternative in only `7.1%` of those encounters; many accepted changes were pharmacy changes rather than therapeutic substitutions (`6.5 million` encounters). URL: `https://pmc.ncbi.nlm.nih.gov/articles/PMC11419340/`
- A `2022` qualitative study of `15` physicians found RTBTs often deliver the right information at the wrong time, after the clinician has already discussed therapy with the patient. URL: `https://pubmed.ncbi.nlm.nih.gov/36122592/`
- A more recent interrupted time-series study found no adherence benefit and possible worsening in one health-system implementation (`n=54,328` orders), reinforcing that implementation quality matters. URL: `https://repositories.lib.utexas.edu/items/a4e1d20a-f79f-4d5d-8a50-114094e264ad`

**Formulary decision support**
- Direct modern evidence for standalone formulary decision support is relatively weak. Most current evidence is embedded inside RTBT/RTPB studies or older e-prescribing studies showing modest shifts toward preferred-tier drugs.
- Practical conclusion: formulary decision support is necessary infrastructure, but the evidence base suggests that `information alone` does little unless delivered early, actionably, and with patient-specific alternatives.

**Specialty pharmacy coordination**
- Evidence is moderate and operationally persuasive. Integrated specialty pharmacy models consistently show shorter time to first dispense than external routing in specialty therapeutics, with the clearest measured effect in oncology (`6` vs `12` days to first palbociclib fill at Mayo). URL: `https://pmc.ncbi.nlm.nih.gov/articles/PMC10982575/`
- Qualitative studies show these teams also absorb coordination work that otherwise lands on clinic staff and patients. URL: `https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0273040`
- This is one of the more promising intervention areas for a provider product because the value is workflow orchestration, not just an alert.

**Affordability support**
- Strongest evidence is not "support program" branding, but actual reduction of patient cost exposure. A study of zero-dollar copay expansion found improved adherence by `2.1 percentage points` and lower medical spending among commercially insured members (`n=6,463` intervention, `1,821` controls). URL: `https://www.ajmc.com/view/association-of-co-pay-elimination-with-medication-adherence-and-total-cost`
- A systematic review of financial medication assistance found generally positive effects on adherence and persistence, but with heterogeneous study designs and limited long-term clinical outcome evidence. URL: `https://pmc.ncbi.nlm.nih.gov/articles/PMC10084847/`
- Manufacturer-linked patient support evidence can be large and directionally favorable, but it is often observational and vendor-sponsored. Example: a `2019` adalimumab support program study reported markedly lower abandonment among participants, but should be interpreted cautiously. URL: `https://pmc.ncbi.nlm.nih.gov/articles/PMC6750846/`

## Strength of evidence
**Strong**
- `Prior authorization` causing treatment delay and discontinuation in affected drug classes.
- `Out-of-pocket burden` driving abandonment, non-initiation, and worse adherence.
- `Patient burden` and confusion as a lived-experience problem, especially in high-stakes specialty care.

**Moderate**
- `Formulary restrictions` and higher-tier placement delaying initiation.
- `Step therapy` worsening access and likely reducing effectiveness via adherence.
- `Specialty pharmacy coordination` improving time to treatment in specialty contexts.
- `RTBT/RTPB` lowering OOP cost when a clear actionable alternative exists.

**Weak or mixed**
- `ePA` improving actual medication starts, adherence, or downstream outcomes.
- `Standalone formulary decision support` as a behavior-changing intervention.
- Broad claims that current point-of-prescribing tools solve the mismatch.

**Mostly vendor-commissioned or operational**
- Many `ePA` time-savings studies.
- Some `patient support` or manufacturer hub studies.
- Vendor summaries of `RTBT` benefit without strong comparative outcomes.

## Implications for product design
- The product should solve the `full access path`, not just PA submission. The evidence supports a workflow that checks `PA risk`, `tier/formulary status`, `step edits`, `network pharmacy constraints`, and `expected OOP` before the prescription leaves the visit.
- Timing matters. RTBT literature strongly suggests the tool must intervene `before` the clinician commits to a therapy discussion, not after the order is already built.
- Actionability matters more than visibility. The product should not just say "PA likely" or "high cost"; it should suggest the `next best executable option`: covered alternative, lower-cost pharmacy, required documentation, specialty routing, or affordability pathway.
- Patient communication is not optional. A useful provider product should auto-generate plain-language explanations of what is happening, expected delays, and what the patient should do next.
- Routing and coordination are core features, not back-office extras. The evidence around specialty pharmacy and LDNs suggests value comes from closing loops across prescriber, staff, payer, pharmacy, and patient.
- Avoid alert fatigue. Only interrupt when the tool can materially change access, cost, or delay risk.
- Measure success with `therapy start` metrics, not just clicks: time to first fill, successful initiation, abandonment, rerouting success, PA turnaround, and patient-reported understanding.

## Evidence gaps
- There is still limited independent evidence that current provider tools improve `actual therapy initiation` or `patient outcomes` at scale.
- Most rigorous studies are concentrated in `oncology`, `addiction treatment`, and `specialty medications`; evidence is thinner for common primary-care prescribing.
- `Step therapy` and `pharmacy routing/network constraints` are clearly important, but the literature is less standardized and less causal than the PA/OOP literature.
- There is not much modern evidence on how to combine `coverage`, `cost`, `routing`, and `patient messaging` into one provider workflow.
- Cash-pay, coupon, and alternative-pharmacy pathways are common in practice but under-studied in peer-reviewed outpatient access literature.
- Equity implications are likely important, but many studies do not deeply stratify by race, income, health literacy, or digital access.

## Source list
- `AMA 2024 Prior Authorization Physician Survey`  
  `https://www.ama-assn.org/system/files/prior-authorization-survey.pdf`
- `Prior Authorization and Association With Delayed or Discontinued Prescription Fills`  
  `https://pubmed.ncbi.nlm.nih.gov/38086013/`
- `Association of Formulary Prior Authorization Policies With Buprenorphine-Naloxone Prescriptions and Hospital and Emergency Department Use Among Medicare Beneficiaries`  
  `https://jamanetwork.com/journals/jamanetworkopen/fullarticle/2764598`
- `Out-of-pocket costs for direct oral anticoagulants and prescription abandonment among patients with nonvalvular atrial fibrillation or venous thromboembolism`  
  `https://www.jmcp.org/doi/10.18553/jmcp.2025.31.4.366`
- `Association of Patient Out-of-Pocket Costs With Prescription Abandonment and Delay in Fills of Novel Oral Anticancer Agents`  
  `https://ascopubs.org/doi/full/10.1200/JCO.2017.74.5091`
- `Cost-sharing and adherence, clinical outcomes, health care utilization, and costs: A systematic literature review`  
  `https://www.jmcp.org/doi/10.18553/jmcp.2022.21270`
- `Delayed treatment initiation of oral anticoagulants among Medicare patients with atrial fibrillation`  
  `https://www.sciencedirect.com/science/article/pii/S2666602224000120`
- `Coverage, Formulary Restrictions, and Out-of-Pocket Costs for Sodium-Glucose Cotransporter 2 Inhibitors and Glucagon-Like Peptide 1 Receptor Agonists in the Medicare Part D Program`  
  `https://pmc.ncbi.nlm.nih.gov/articles/PMC7563069/`
- `Impact of Plan-Level Access Restrictions on Effectiveness of Biologics Among Patients with Rheumatoid or Psoriatic Arthritis`  
  `https://link.springer.com/article/10.1007/s41669-019-0152-1`
- `The Patient Experience of Prior Authorization for Cancer Care`  
  `https://jamanetwork.com/journals/jamanetworkopen/fullarticle/2810824`
- `Consumer Problems with Prior Authorization: Evidence from KFF Survey`  
  `https://www.kff.org/affordable-care-act/consumer-problems-with-prior-authorization-evidence-from-kff-survey/`
- `Impact of implementing electronic prior authorization on medication filling in an electronic health record system in a large healthcare system`  
  `https://pubmed.ncbi.nlm.nih.gov/34279657/`
- `Effects of Real-time Prescription Benefit Recommendations on Patient Out-of-Pocket Costs: A Cluster Randomized Clinical Trial`  
  `https://jamanetwork.com/journals/jamainternalmedicine/article-abstract/2796059`
- `Physician Perspectives on Implementation of Real-Time Benefit Tools: A Qualitative Study`  
  `https://pubmed.ncbi.nlm.nih.gov/36122592/`
- `Price transparency at the point of prescribing with real-time prescription benefits`  
  `https://pmc.ncbi.nlm.nih.gov/articles/PMC11419340/`
- `Comparison of time to treatment initiation of specialty medications between an integrated health system specialty pharmacy and external specialty pharmacies`  
  `https://pmc.ncbi.nlm.nih.gov/articles/PMC10982575/`
- `Exploring healthcare providers' experiences with specialty medication and limited distribution networks`  
  `https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0273040`
- `Association of Co-pay Elimination With Medication Adherence and Total Cost`  
  `https://www.ajmc.com/view/association-of-co-pay-elimination-with-medication-adherence-and-total-cost`
- `Impact of financial medication assistance on medication adherence: a systematic review`  
  `https://pmc.ncbi.nlm.nih.gov/articles/PMC10084847/`
- `Participation in an innovative patient support program reduces prescription abandonment for adalimumab-treated patients in a commercial population`  
  `https://pmc.ncbi.nlm.nih.gov/articles/PMC6750846/`
