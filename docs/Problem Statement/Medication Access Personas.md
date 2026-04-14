# Medication Access Personas

## Purpose
This document reframes the target personas for the medication access mismatch opportunity described in `PreScripts/Market Research/Medication Access Mismatch Research Report.md`.

For product opportunity prioritization in this document:
- `Prescribing Clinician` is the `P0` persona.
- `Medication Access Coordinator` is the `P1` persona.
- `Buying and Implementation Stakeholders`, when they exist in an organization, should be treated as `P0` because they materially influence implementation, rollout, and adoption.

The core correction is:
- `Provider Org` is not a persona. It is a customer segment or account type.
- `Executives`, `Compliance`, and `IT` are not core day-to-day product personas. They are buying, approval, or implementation stakeholders.
- The operational user is broader than `insurance liaison`. The stronger persona is `medication access staff`, because the workflow spans prior authorization, formulary restrictions, affordability, routing, and patient follow-up.

## Recommended Persona Taxonomy
Use four layers:

1. `Core Product Personas`
2. `Buying and Implementation Stakeholders`
3. `Secondary or Adjacent Personas`
4. `Target Customer Segments`

This taxonomy better matches the research finding that the problem is a `medication access orchestration` problem rather than just a prior authorization workflow.

## Core Product Personas

### Persona Table
| Persona | Who | Primary job to be done | Top pains | Desired outcomes | Likely objections | MVP priority |
| --- | --- | --- | --- | --- | --- | --- |
| `Prescribing Clinician` | `Physician`, `Nurse Practitioner`, `Physician Assistant` | Choose and start the right therapy without creating downstream access failure, patient confusion, or excessive rework. | Limited visibility into prior auth, step therapy, formulary restrictions, expected patient out-of-pocket cost, and specialty pharmacy routing at the moment of prescribing; learns about access problems too late; receives callbacks and re-prescribing work; has little confidence that the patient understands next steps. | Know before signing the order whether the medication is likely to be coverable, affordable, and routable; see the next best executable alternative when the original therapy is likely to fail; reduce follow-up messages and therapy restarts; preserve patient trust through clearer expectation setting. | "I already have EHR alerts and benefit tools."; "Do not add clicks or interrupt my visit."; "If the recommendations are wrong, they will waste my time." | `P0` |
| `Medication Access Coordinator` | `Insurance Liaison`, `Prior Authorization Specialist`, `Medication Access Specialist`, `Referral / Benefits Investigation Staff`, `Specialty Medication Coordinator` | Turn a prescribed therapy into an approved, affordable, correctly routed, and started medication. | Work is fragmented across payer portals, EHR inboxes, faxes, pharmacies, assistance programs, and patient phone calls; must manually triage many different barrier types; ownership is often unclear when a case gets stuck; repeated patient outreach is needed because expectations were not set clearly upstream. | A single queue with case status, likely barrier type, next best action, and handoff tracking; fewer dropped or duplicated cases; faster time from prescription to therapy start; less manual searching for payer rules, routing rules, and affordability options. | "We already use ePA and our own work queues."; "If this misses edge cases, we still need to do the work manually."; "I do not want another dashboard that duplicates my workflow." | `P1` |

### 3. Specialty Pharmacy Liaison or Affiliated Pharmacy Coordinator
**Who**
- `Specialty Pharmacy Liaison`
- `Integrated Health-System Pharmacy Staff`
- `Clinic-Embedded Pharmacy Coordinator`

**Primary job to be done**
- Make sure specialty or high-friction prescriptions reach the right channel and convert to a successful first fill.

**Top pains**
- Prescriptions are often routed to the wrong pharmacy or blocked by limited distribution rules.
- Upstream clinic context is incomplete by the time the case reaches pharmacy.
- Handoffs between clinic, pharmacy, payer, and patient are inconsistent.
- Staff spends time chasing status instead of resolving the blocker.

**Desired outcomes**
- Correct routing the first time.
- Clean handoff from clinician or access staff with required documentation and context.
- Better visibility into what is blocking the start.
- Faster first fill and less leakage.

**Likely objections**
- "This may be too clinic-centric and not solve pharmacy handoffs."
- "Integration with pharmacy workflow matters more than another alert."

**MVP priority**
- `P1`

## Buying and Implementation Stakeholders

These stakeholders should be treated as `P0` whenever they exist in a target organization, because they directly influence implementation approval, rollout, and long-term adoption.

### Stakeholder Table
| Persona | Role | What they care about | Why they matter | Priority |
| --- | --- | --- | --- |
| `Ambulatory or Service Line Executive` | Economic buyer or senior sponsor. | Faster therapy starts; reduced staff burden and rework; better patient experience in specialty-heavy clinics; measurable ROI beyond simple prior authorization turnaround. | They approve budget and need confidence this is a workflow platform, not just another narrow point solution. | `P0` |
| `IT / EHR / Integration Lead` | Technical gatekeeper. | Implementation risk, data flow, integration scope, security, and support burden. | A workflow product must fit into the EHR and existing operational systems. | `P0` |
| `Compliance / Privacy Stakeholder` | Approval and governance stakeholder. | Privacy, auditability, permitted data use, and workflow safety. | Important for approval, but not a daily end user. | `P0` |

### 2. Pharmacy or Specialty Pharmacy Leadership
**Role**
- Buyer or strong influencer, especially in systems with owned or affiliated specialty pharmacy.

**What they care about**
- Better routing, reduced leakage, faster starts, and clearer clinic-to-pharmacy coordination.

**Why they matter**
- They often feel the downstream impact of broken prescribing-to-start workflows and can quantify business value.

### 3. Clinic or Access Operations Manager
**Role**
- Operational champion.

**What they care about**
- Standardized workflows, queue management, staff productivity, and fewer dropped handoffs.

**Why they matter**
- They are often the internal owner of rollout success.

## Secondary or Adjacent Personas

### Patient
**Why included**
- The patient is the end beneficiary and should influence workflow design, especially around plain-language explanations and next-step clarity.

**Why not core for MVP**
- The research supports starting with a provider-side workflow product rather than a direct-to-patient app.

### General Clinic Staff
**Why included**
- Medical assistants, front desk staff, and refill teams may touch parts of the process.

**Why not core for MVP**
- This category is too broad. It is better to design first for the more specific and higher-friction `medication access coordinator` persona.

## Target Customer Segments
These are not personas, but they should guide product focus and go-to-market.

### Best-fit segments
- `Large health systems with specialty-heavy ambulatory care`
- `Large multispecialty groups with centralized medication access teams`
- `IDNs with owned or affiliated specialty pharmacy`

### Best initial beachhead
`Large health systems with specialty-heavy ambulatory clinics and owned or affiliated specialty pharmacy`

**Why this is the best starting segment**
- The mismatch is most painful where medications are expensive, specialty-heavy, and operationally complex.
- These organizations already feel the burden of prior auth, formulary restrictions, affordability issues, and pharmacy routing breakdowns.
- They are more likely to have dedicated staff who can operationalize a shared workflow.
- They can measure outcomes that matter, such as time to therapy start, first-fill success, abandonment reduction, and leakage.

## What to Correct From the Original Persona List

### Keep, but refine
- `Clinicians (Physicians, PA, NP)` -> keep as `Prescribing Clinician`
- `Clinic Staff (Insurance Liaison)` -> expand to `Medication Access Coordinator`

### Move to stakeholder category
- `Onboarding Staff (Executives, Compliance, IT)` -> move to `Buying and Implementation Stakeholders`

### Reclassify
- `Provider Org (Clinics, Hospitals)` -> reclassify as `Target Customer Segment`, not persona

## Recommended MVP Focus
If you need only two core personas for the first product narrative, use:

1. `Prescribing Clinician`
2. `Medication Access Coordinator`

With your prioritization rule, treat them as:
- `Prescribing Clinician` = core `P0` product persona
- `Medication Access Coordinator` = core `P1` product persona
- `Buying and Implementation Stakeholders` = `P0` implementation personas when present in the account

If you need a third persona because specialty routing is central to the wedge, add:

3. `Specialty Pharmacy Liaison`

This structure aligns best with the research: the daily workflow problem sits between prescriber intent, operational resolution, and successful therapy start.
