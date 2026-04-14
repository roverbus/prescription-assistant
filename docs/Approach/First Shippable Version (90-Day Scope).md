# First Shippable Version (90-Day Scope)

## Goal

Validate the product idea: that clinicians will trust and use a prescribing-moment Prescription Assistant that gives a fast, explainable, actionable answer—by shipping a lightweight version in a narrow wedge and measuring workflow fit, trust, and early outcome impact.

## Non-goal (first 90 days)

Proving we can build a full access platform, scale across specialties, or automate downstream workflows; the 90 days are for learning whether the product idea is right, not for feature completeness or broad rollout.

## What Is In Scope

- `Live recording + transcript detection` to identify when an in-scope medication is being actively considered.
- `Clinician confirmation` before showing an assessment as actionable.
- `Desktop browser extension` or desktop side panel as the primary workflow surface.
- A top-line `High / Medium / Low` executability assessment for the medication under consideration, grounded in visible drivers and source freshness.
- A one-sentence rationale that explains the main drivers of access friction, such as formulary status, prior auth burden, routing constraints, or likely affordability issues.
- Collection or integration of access intelligence data (formulary, PA burden, routing, affordability) to support grounded assessments and alternative recommendations.
- `2-3` recommended alternatives when the original option looks harder to start.
- Patient-ready talking points so the clinician can explain likely barriers, faster paths, and next steps during the visit.
- Lightweight structured inputs for missing context, such as payer, diagnosis, pharmacy, or site-of-care preference.
- Saved recommendations with timestamp, reasoning, and audit trail so the logic is not lost after the visit.
- **Collecting the clinician’s final decision** (accept, reject, dismiss, or save for later—and optional reason when rejected) so we can measure recommendation quality (e.g. acceptance rate), learn from feedback, and improve the model and prompts over time; feedback can be collected explicitly in our UI or inferred via live recording / transcription (with consent and confidence thresholds).
- Initial launch in a narrow set of high-friction specialty workflows rather than a broad multi-specialty release.

## What Is Explicitly Out Of Scope

- Deep `EHR` integration, write-back, or custom ordering workflow changes.
- Autonomous medication switching, therapy selection, or prescription changes.
- Auto-submission of prior auths, appeals, enrollment forms, or routing actions.
- Full coordinator workflow replacement or exception-management workbench.
- Broad ambient scribing or note-taking use cases beyond medication-intent detection.
- A patient app, standalone follow-up workflow, or broad care-management layer.
- Multi-specialty expansion before the product proves trust and workflow fit in a narrow wedge.
- Black-box recommendations with no visible rationale or source freshness.

## Why This Is The Right 90-Day Cut

This is the right first cut because it maximizes learning while minimizing implementation risk. The hardest question is not whether we can build a fully integrated access platform in 90 days. It is whether clinicians will trust and use an access-feasibility assistant at the point of prescribing if it gives a fast, explainable, and actionable answer.

Launching with transcript detection plus a browser-side workflow avoids the biggest source of schedule risk, which is deep enterprise `EHR` integration. It also keeps the product focused on the highest-leverage moment: before the prescription becomes downstream rework. If we can help the clinician avoid choosing a therapy that is unlikely to get to first fill, we create value upstream rather than trying to clean up failure later.

This scope is also intentionally narrow enough to earn trust. `High / Medium / Low`, rationale, alternatives, and patient talking points are easy to understand in a few seconds. That is a much stronger 90-day wedge than trying to automate prior auth, replace coordinators, or orchestrate every downstream workflow from day one.

## Investment Needed (Time and Materials)

- **Engineering:** Transcript pipeline (live recording → medication-intent detection), desktop browser extension or side-panel UI, backend for executability logic and saved recommendations with audit trail. No EHR integration in v1.
- **AI API resource:** APIs for transcription, medication-intent detection, and any LLM-backed rationale or talking-point generation (e.g. speech-to-text, intent/NER, summarization).
- **Machine learning / AI engineering:** Tune AI prompts to generate the H/M/L executability risk and rationale; prompt engineering for grounded, explainable outputs and patient-ready talking points.
- **Industry experts (consultants):** Clinicians and operations staff (e.g. medication access coordinators, specialty pharmacy liaisons) as consultants to validate workflow, talking points, alternative logic, and specialty rules.
- **Access intelligence data / integration:** Collection or integration of data to ground assessments and alternatives.
  - **Formulary and utilization management** (preferred status, PA requirements, step therapy, quantity limits): payer/formulary vendors, PBM data, benefit intelligence partners, specialty rules databases.
  - **Routing and channel** (specialty pharmacy mandate, buy-and-bill, site-of-care): payer policies, specialty pharmacy network rules, curated workflow logic.
  - **Affordability** (optional for 90-day): RTBT vendors, payer services, pharmacy benefit services, affordability program data.
  - **Prior authorization stats** (approval rates, denial reasons, turnaround): public or aggregated PA data where available (e.g. Washington state public PA data), payer reports, or curated specialty benchmarks.
- **Design and UX:** Extension/side-panel flows for confirm → H/M/L + rationale → drill-down (drivers, alternatives, talking points); “understand in a few seconds” and clinician confirmation.
- **Compliance and consent:** Consent and privacy controls for live recording/transcript; clear disclosure; auditability and source freshness / “missing or inferred” indicators in the UI.
- **Clinical and specialty scope:** Narrow drug and specialty set (e.g. one or two therapy classes in rheumatology, dermatology, or gastroenterology) so rules and UX are tractable; clinical input for talking points and alternative logic.
- **Pilot and validation:** One or two pilot sites (e.g. specialty ambulatory groups) for workflow fit, trust, and early outcome signals (time to therapy, first-fill success, abandonment, avoidable re-prescribing).
- **Time:** ~90 days end-to-end; success = clinicians use it, trust it, and early outcome impact is visible enough to justify phase 2 (EHR, write-back, broader specialties).

## Success Metrics

- Time to therapy start for targeted medications.
- First-fill success rate.
- Prescription abandonment rate.
- Reduction in avoidable re-prescribing, rerouting, or access-related callbacks.
- Clinician usage rate in eligible encounters.
- Recommendation acceptance or meaningful-consideration rate.
- Clinician trust in recommendation quality and explanation clarity.
- Clinician-rated usefulness of patient communication support.

## case study-Ready Framing

My first shippable version would not try to be a full access platform. In 90 days, I would ship a narrow prescribing-moment Assistant for specialty ambulatory care: detect medication intent, show an explainable executability signal, suggest a few lower-friction alternatives, and help the clinician explain the plan to the patient before they leave the room. I would explicitly avoid deep `EHR` dependency and downstream automation so the team can prove workflow fit, trust, and outcome impact before taking on heavier integration.
