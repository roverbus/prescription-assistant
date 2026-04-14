# Medication Access Mismatch - Research Analyst Report

## Bottom line
The broader problem statement is **supported in substance, mildly overstated in implied prevalence, and incomplete in its current framing**.

What is well supported:
- In U.S. outpatient care, there is a recurring gap between the drug a clinician intends and the drug a patient can actually start.
- That gap is caused by more than prior authorization alone: cost exposure, formulary design, step therapy, pharmacy routing, specialty distribution, quantity limits, coupon/copay assistance mechanics, and poor patient communication all contribute.
- Existing tools such as `ePA` and `RTBT/RTPB` help on narrow slices of the workflow but do **not** reliably ensure that the prescribed therapy is executable, affordable, and understandable.

What is overstated:
- The statement risks implying this is true for most outpatient prescriptions. Public evidence is strongest for **specialty, high-cost, chronic, and complex therapies**, plus patients with heavier service use, not for every routine script.
- The best-supported claim is not "providers have no visibility," but "visibility is fragmented, late, plan-specific, and often not actionable enough."

What is incomplete:
- The problem is not only "coverage requirements." It is a broader **medication access orchestration** problem spanning clinical appropriateness, payer rules, pharmacy channel constraints, affordability, and patient follow-through.
- Patient communication and navigation are not side effects; they are a core failure mode.

## Component failure modes
| Failure mode | What breaks | Evidence signal | More provider pain or patient pain? |
|---|---|---|---|
| Prior authorization | Approval needed after prescribing, requiring documentation, back-and-forth, appeals, peer-to-peer review | Very strong | Both; especially provider ops pain |
| Step therapy | Payer requires trial/failure of another drug before intended therapy | Strong, but more disease-specific in public evidence | Both; more provider rework plus patient delay |
| Formulary exclusions | Intended drug not covered or pushed off formulary; nonmedical switching | Strong | High patient pain, high provider re-prescribing pain |
| Deductible / coinsurance / OOP exposure | Drug is covered but unaffordable at point of fill | Very strong | Highest patient pain |
| Pharmacy network / routing | Rx sent to wrong pharmacy or non-network pharmacy; rerouting needed | Moderate to strong | More provider/staff coordination pain |
| Quantity limits | Claim rejects due to allowed amount/days supply; partial fills or resubmission needed | Real but under-documented as a standalone mode | Moderate provider and patient pain |
| Specialty pharmacy / limited distribution routing | Drug must go through a specific specialty pharmacy or limited network | Strong in specialty meds | Very high provider pain and meaningful patient delay |
| Coupons / copay assistance / accumulators / maximizers | Financial assistance exists but is opaque, administratively complex, or does not count toward deductible/OOP max | Strong | More patient affordability pain; also staff burden |
| Patient communication failures | Patient does not understand delay, next step, expected cost, alternate options, or who owns follow-up | Very strong | High patient pain; amplifies every other failure mode |

**Where provider pain is greatest**
- `PA`
- `Specialty pharmacy / limited distribution routing`
- `Formulary exclusion + step therapy` rework
- `Coupon/copay assistance` administration in specialty settings

**Where patient pain is greatest**
- `Deductible / coinsurance / OOP exposure`
- `Formulary exclusions / nonmedical switching`
- `PA-related delay or denial`
- `Communication failures`

## Evidence and statistics
- **PA burden on practices remains large.** AMA's 2024 survey found physicians and staff complete **39 PA requests per physician per week**, spend about **13 hours/week** on PA, and **40%** of physicians report staff who work exclusively on PA. **93%** said PA delays necessary care, **82%** said it can lead to treatment abandonment, and **29%** reported a serious adverse event in a patient's care.  
  Source: [AMA 2024 survey summary](https://ama-assn.org/press-center/ama-press-releases/ama-survey-indicates-prior-authorization-wreaks-havoc-patient-care)

- **The patient burden is real and visible.** KFF found **16%** of insured adults had prior authorization problems in the last year; among those with PA-related insurance problems, **34%** said they were unable to receive recommended care, **32%** had significant delays, **26%** said health declined, and **37%** paid more out of pocket.  
  Source: [KFF consumer problems with PA](https://www.kff.org/affordable-care-act/consumer-problems-with-prior-authorization-evidence-from-kff-survey/)

- **PA is experienced as a major consumer burden.** In KFF polling, about **69%** of insured adults describe prior authorization as a burden, and **34%** call it the single biggest burden in navigating care. In 2025 polling, **51%** of insured adults said they had needed prior authorization in the prior two years; among them, **48%** reported delays and **43%** reported denials.  
  Sources: [KFF burden poll](https://www.kff.org/patient-consumer-protections/kff-health-tracking-poll-public-finds-prior-authorization-process-difficult-to-manage/), [KFF issue brief](https://www.kff.org/private-insurance/issue-brief/final-prior-authorization-rules-look-to-streamline-the-process-but-issues-remain/)

- **The strongest causal evidence shows PA changes access, not just sentiment.** A 2024 study of oral anticancer drugs found newly imposed PA requirements were associated with **7.1x higher odds of discontinuation** and roughly **9.7 additional days** to next fill.  
  Source: [JCO / PMC study](https://pmc.ncbi.nlm.nih.gov/articles/PMC10927330/)

- **Coverage restrictions extend beyond PA.** In a large U.S. study of SGLT2 inhibitor coverage across **4,135 health plans** covering **297.8 million lives**, Medicare plans were far more permissive than commercial or other plans; only **61%** of commercial/employer-covered lives had access to at least one SGLT2 inhibitor without PA or step therapy, while Medicaid plans often required PA, including **48%** of covered lives for empagliflozin. Step therapy in commercial coverage affected roughly **40%** of covered lives for dapagliflozin.  
  Source: [JAMA Health Forum / PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC8796944/)

- **Affordability is a separate failure mode from coverage.** KFF found **24%** of people taking prescriptions say it is difficult to afford them, and **29%** of adults report not taking medicines as prescribed at some point in the past year because of cost, including **19%** who did not fill a prescription.  
  Source: [KFF prescription affordability poll](https://www.kff.org/health-costs/poll-nearly-1-in-4-americans-taking-prescription-drugs-say-its-difficult-to-afford-medicines-including-larger-shares-with-low-incomes/)

- **Insurance often "covers" drugs but still leaves patients exposed.** KFF reported **23%** of insured adults said insurance did not cover a prescribed drug or required a very high copay; among those in fair or poor health this rose to **35%**.  
  Source: [KFF copay adjustment brief](https://www.kff.org/health-costs/copay-adjustment-programs-what-are-they-and-what-do-they-mean-for-consumers/)

- **Coupons/copay assistance reduce cash burden but add process burden and can fail to solve total affordability.** In one oral oncology study, initial mean patient copay was **$1,226**, falling to **$125** after copay assistance, but **54%** of prescriptions required financial assistance and those cases needed more calls and longer time to drug receipt.  
  Source: [Provider and patient burdens of obtaining oral anticancer medications](https://pmc.ncbi.nlm.nih.gov/articles/PMC7596764/)

- **Specialty pharmacy routing is a real execution bottleneck.** In the same oral oncology study, median time from prescription to patient receipt was **12 days**, and **73%** of prescriptions required at least 2 staff phone calls while **40%** required at least 5.  
  Source: [PMC study](https://pmc.ncbi.nlm.nih.gov/articles/PMC7596764/)

- **Limited distribution and external specialty routing create clinic burden.** A qualitative study found communication failures with insurers, manufacturers, and outside pharmacies, plus substantial time and workflow disruption. A national survey cited in that work found **68%+** of health-system specialty pharmacies could not dispense more than half of prescriptions written by their own providers because of restricted networks and limited distribution drugs.  
  Source: [PLOS One / PMC limited distribution study](https://pmc.ncbi.nlm.nih.gov/articles/PMC9377589/)

- **Routing affects speed, not just convenience.** Integrated health-system specialty pharmacies have reported materially faster initiation than external specialty pharmacies, for example **6 vs 12 days** for palbociclib in one health-system comparison.  
  Source: [Comparison study overview](https://pmc.ncbi.nlm.nih.gov/articles/PMC10982575/)

- **Patient communication failures are not trivial.** In a cancer-care PA study, **69%** reported PA-related delays, **22%** did not receive recommended care because of delay or denial, **67%** had to personally get involved, **20%** spent 11+ hours on it, and **89%** trusted their insurer less afterward.  
  Source: [JAMA Network Open / PMC](https://jamanetwork.com/journals/jamanetworkopen/fullarticle/2810824)

## Where current tools fail
Current workflows and tools **partially solve** the mismatch, but they do not close it.

- **`ePA` helps process PA, not medication access as a whole.** It can speed some request-to-decision workflows, but it does not solve affordability, routing, patient communication, step therapy alternatives, or specialty distribution. A large-health-system study found ePA implementation did **not** improve medication filling; filled-within-30-days rates were **64.2%** for ePA prescriptions vs **68.8%** for controls, with issues including insurance fragmentation and misfires.  
  Source: [ePA implementation study](https://pmc.ncbi.nlm.nih.gov/articles/PMC8449617/)

- **CMS/KFF reforms still miss prescription drugs and employer plans.** KFF notes the CMS final PA rule improves electronic exchange and transparency for some medical items/services, but it **does not apply to prescription drug prior authorization** and excludes most employer-sponsored plans.  
  Source: [KFF issue brief](https://www.kff.org/private-insurance/issue-brief/final-prior-authorization-rules-look-to-streamline-the-process-but-issues-remain/)

- **`RTBT/RTPB` is useful but too narrow and too late.** The randomized trial showed an **11.2%** OOP reduction overall and **38.9%** reduction for high-cost drug classes, but only **4.2%** of prescriptions had an eligible recommendation.  
  Source: [JAMA Internal Medicine trial / PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC9468947/)

- **Even where RTBT exists, it is not consistently actionable.** Qualitative physician research described it as the "right information at the wrong time," often appearing after the drug choice discussion, creating rework instead of helping initial selection.  
  Sources: [Qualitative study / PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC9646401/), [summary](https://www.benmedica.com/articles/physician-perspectives-of-real-time-benefit-tools)

- **Adoption does not equal resolution.** Federal data indicate hospital RTBT capability is rising, with **56.2%** of non-federal acute care hospitals integrated for all or almost all payers in 2023 and another **15.8%** integrated for a limited set of payers. But provider use is still voluntary, payer coverage is uneven, and the tools remain point solutions.  
  Source: [ASTP/HealthIT quick stats](https://beta.healthit.gov/data/quickstats/hospital-adoption-real-time-benefit-tools/)

- **The dominant real-world competitor is still labor.** Medication access teams, prior-auth staff, pharmacy rerouting, patient-assistance specialists, and repeated patient follow-up remain the practical operating system for getting therapy started.

## Implications for product strategy
1. Build for the broader problem: **medication access orchestration**, not just prior authorization automation.
2. Focus initial wedge on **specialty-heavy, high-cost, chronic outpatient prescribing**, where mismatch is most painful and measurable.
3. Surface the full execution path at prescription time: likely PA, step edit, formulary status, expected OOP, preferred pharmacy channel, specialty routing, and likely assistance options.
4. Recommend the **next best executable option**, not just an alert. Providers need covered alternatives, pharmacy/channel alternatives, and documentation guidance.
5. Treat affordability as first-class product logic. "Covered" is not enough if deductible, coinsurance, or accumulator/maximizer design still makes the fill unrealistic.
6. Include a **work-queue layer for staff**, because many failures are resolved by coordinated human follow-up, not by the prescriber alone.
7. Make patient communication part of the product. Generate a plain-language explanation of what is happening, what the patient should expect, and what alternatives exist.
8. Optimize for **timing and interruption design**. The winning workflow intervenes before therapy choice is "committed," not after order entry.
9. Use specialty pharmacy and network intelligence as a differentiator. Routing and limited-distribution constraints are under-served but create large provider pain.
10. Measure success on **time-to-therapy-start, first-fill success, abandonment reduction, reroutes avoided, and staff time saved**, not just PA turnaround.

## Open questions and risks
- The evidence is strongest in specialty and high-cost therapies; the exact prevalence of mismatch in routine primary-care prescribing is less clear.
- Public data on **quantity limits**, pharmacy rerouting frequency, and patient-specific coupon discovery rates are thinner than PA and affordability data.
- Some tool-performance evidence is vendor-linked or operational rather than patient-outcome based.
- Payer variation is extreme; a product may need to be plan- and market-specific before it becomes reliably accurate.
- EHR workflow dependency is high. If the intervention is out-of-workflow or late, adoption will lag.
- Some recommendations could be perceived as "steering to cheaper care" unless clinical appropriateness is explicit and defensible.
- Copay assistance is legally and operationally messy across commercial vs public coverage; product claims here need careful compliance review.

## Source list
- AMA 2024 PA survey press release: [https://ama-assn.org/press-center/ama-press-releases/ama-survey-indicates-prior-authorization-wreaks-havoc-patient-care](https://ama-assn.org/press-center/ama-press-releases/ama-survey-indicates-prior-authorization-wreaks-havoc-patient-care)
- KFF consumer PA problems: [https://www.kff.org/affordable-care-act/consumer-problems-with-prior-authorization-evidence-from-kff-survey/](https://www.kff.org/affordable-care-act/consumer-problems-with-prior-authorization-evidence-from-kff-survey/)
- KFF PA rule/limits brief: [https://www.kff.org/private-insurance/issue-brief/final-prior-authorization-rules-look-to-streamline-the-process-but-issues-remain/](https://www.kff.org/private-insurance/issue-brief/final-prior-authorization-rules-look-to-streamline-the-process-but-issues-remain/)
- KFF PA burden poll: [https://www.kff.org/patient-consumer-protections/kff-health-tracking-poll-public-finds-prior-authorization-process-difficult-to-manage/](https://www.kff.org/patient-consumer-protections/kff-health-tracking-poll-public-finds-prior-authorization-process-difficult-to-manage/)
- KFF Rx affordability poll: [https://www.kff.org/health-costs/poll-nearly-1-in-4-americans-taking-prescription-drugs-say-its-difficult-to-afford-medicines-including-larger-shares-with-low-incomes/](https://www.kff.org/health-costs/poll-nearly-1-in-4-americans-taking-prescription-drugs-say-its-difficult-to-afford-medicines-including-larger-shares-with-low-incomes/)
- KFF copay adjustment programs: [https://www.kff.org/health-costs/copay-adjustment-programs-what-are-they-and-what-do-they-mean-for-consumers/](https://www.kff.org/health-costs/copay-adjustment-programs-what-are-they-and-what-do-they-mean-for-consumers/)
- Oral anticancer PA delay/discontinuation: [https://pmc.ncbi.nlm.nih.gov/articles/PMC10927330/](https://pmc.ncbi.nlm.nih.gov/articles/PMC10927330/)
- Oral anticancer burdens study: [https://pmc.ncbi.nlm.nih.gov/articles/PMC7596764/](https://pmc.ncbi.nlm.nih.gov/articles/PMC7596764/)
- SGLT2 coverage/restrictions study: [https://pmc.ncbi.nlm.nih.gov/articles/PMC8796944/](https://pmc.ncbi.nlm.nih.gov/articles/PMC8796944/)
- Cancer patient experience of PA: [https://jamanetwork.com/journals/jamanetworkopen/fullarticle/2810824](https://jamanetwork.com/journals/jamanetworkopen/fullarticle/2810824)
- ePA implementation study: [https://pmc.ncbi.nlm.nih.gov/articles/PMC8449617/](https://pmc.ncbi.nlm.nih.gov/articles/PMC8449617/)
- RTBT randomized trial: [https://pmc.ncbi.nlm.nih.gov/articles/PMC9468947/](https://pmc.ncbi.nlm.nih.gov/articles/PMC9468947/)
- RTBT qualitative study: [https://pmc.ncbi.nlm.nih.gov/articles/PMC9646401/](https://pmc.ncbi.nlm.nih.gov/articles/PMC9646401/)
- RTBT timing summary: [https://www.benmedica.com/articles/physician-perspectives-of-real-time-benefit-tools](https://www.benmedica.com/articles/physician-perspectives-of-real-time-benefit-tools)
- Health IT RTBT adoption stats: [https://beta.healthit.gov/data/quickstats/hospital-adoption-real-time-benefit-tools/](https://beta.healthit.gov/data/quickstats/hospital-adoption-real-time-benefit-tools/)
- Limited distribution/provider burden: [https://pmc.ncbi.nlm.nih.gov/articles/PMC9377589/](https://pmc.ncbi.nlm.nih.gov/articles/PMC9377589/)
- Integrated vs external specialty pharmacy timing: [https://pmc.ncbi.nlm.nih.gov/articles/PMC10982575/](https://pmc.ncbi.nlm.nih.gov/articles/PMC10982575/)
