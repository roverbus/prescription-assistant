# Key Functionality of the AI-Assisted Approach

## Purpose

Define the core functionality for an AI-assisted prescribing access assistant that helps clinicians assess whether a medication is realistically executable, understand why access may fail, choose a more executable next step, and explain that choice clearly to the patient without removing clinician control.

## Product Stance

- `[P0]` The launch plan should assume a `90-day MVP`, so the first version must minimize dependency on deep EHR integration.
- `[P0]` `V1` should be a lightweight, clinician-in-the-loop access assistant focused on specialty ambulatory prescribing.
- `[P0]` The product should optimize for workflow fit, explainability, and actionability rather than deep automation.
- `[P0]` `V1` should include communication support so the clinician can explain barriers, alternatives, and likely next steps during the visit.
- `[P0]` The tool should support the prescribing moment, not replace coordinator workflow or ePA infrastructure.
- `[P1]` Deep EHR integration should be treated as a phase 2 capability after the core recommendation experience is proven.

## 1. How The System Should Access Prescription Intent

### Recommended approach by phase

- `[P0]` `V1 primary:` use `live recording + transcript detection` to identify medication discussion without waiting for EHR integration.
- `[P0]` `V1 companion surface:` use a `desktop browser extension` or desktop side panel to display recommendations alongside the clinician's normal workflow.
- `[P1]` `V1 optional:` use lightweight read-only EHR context if a customer can provide it quickly, but do not make it a dependency for launch.
- `[P1]` `Later phase:` add structured EHR integration for chart context, typed medication detection, and write-back.

### Channel options

- `Live recording and transcript`
  - `[P0]` Best launch option for a `90-day MVP` because it does not depend on enterprise EHR integration.
  - `[P0]` Can detect medication discussion before the clinician begins ordering.
  - `[P0]` Works best when paired with clinician confirmation before an assessment is shown as actionable.
  - `[P1]` Requires clear consent, privacy controls, and high-confidence intent detection.
- `Desktop browser extension`
  - `[P0]` Best launch surface for showing recommendations without asking clinicians to switch devices.
  - `[P0]` Can anchor the UI next to the browser-based EHR or prescribing workflow.
  - `[P1]` Can also detect typed medication names or copied prescription text in browser-based workflows where technically feasible.
- `EHR integration`
  - `[P1]` Best long-term source of patient context and typed medication intent.
  - `[P1]` Can eventually detect medication search, draft orders, plan updates, and medication changes.
  - `[P2]` Should later support write-back and deeper chart context.

### Recommendation

- `[P0]` Launch with `live recording/transcript detection + desktop browser extension`.
- `[P0]` Require clinician confirmation when the system believes a medication is being actively considered.
- `[P1]` Add limited structured inputs in the extension for insurer, diagnosis, pharmacy, or prior therapy when that context cannot be pulled automatically.
- `[P1]` Move to `EHR integration + write-back` only after the MVP proves value and trust.

## 2. When The Assessment Should Be Triggered

- `[P0]` Trigger when a medication is mentioned in conversation with high confidence that it is under active prescribing consideration.
- `[P0]` Trigger when the clinician confirms a detected medication from the transcript feed.
- `[P1]` Trigger when a medication is typed, searched, or selected in the EHR or browser workflow if that signal is available.
- `[P1]` Trigger when multiple candidate medications are being compared for the same treatment decision.
- `[P1]` Re-trigger when material context changes, such as payer, diagnosis, route, site of care, or preferred pharmacy.

### Trigger guardrails

- `[P0]` Do not trigger on every medication mention; require an intent-confidence threshold.
- `[P0]` Suppress duplicate assessments for the same medication in the same patient session unless context changes.
- `[P0]` Allow the clinician to manually request an assessment at any time.
- `[P0]` Allow the clinician to dismiss or snooze an assessment.
- `[P0]` Only surface a recommendation when there is enough information to provide a useful answer.
- `[P1]` If confidence is low, show a draft detection state such as `Medication mentioned - confirm to assess`.

## 3. What Supporting Data Is Needed And Where It Comes From

### Launch-feasible data for a 90-day MVP

- `[P0]` Medication name, formulation, and treatment context.
  - Source: transcript extraction plus clinician confirmation.
- `[P0]` Patient insurance plan or payer.
  - Source: manual entry, patient insurance card lookup, lightweight admin input, or optional read-only EHR context.
- `[P0]` Diagnosis and indication context.
  - Source: clinician quick-select, transcript clues, or optional EHR read access.
- `[P0]` Preferred pharmacy or site-of-care preference when relevant.
  - Source: clinician confirmation, staff entry, or saved patient profile.

### External access intelligence needed for recommendations

- `[P0]` Formulary and utilization management data such as preferred status, prior auth, step therapy, and quantity limits.
  - Source: payer/formulary vendors, PBM data, benefit intelligence partners, and specialty rules databases.
- `[P0]` Routing and channel constraints such as specialty pharmacy mandate, buy-and-bill logic, or site-of-care restrictions.
  - Source: payer policies, specialty pharmacy network rules, and curated workflow logic.
- `[P1]` Estimated out-of-pocket exposure and affordability signals.
  - Source: RTBT vendors, payer services, pharmacy benefit services, and affordability program data.
- `[P1]` Historical workflow friction such as common denial reasons, typical approval time, and common missing documentation.
  - Source: customer historical data, internal coordinator notes, or curated specialty knowledge.

### Data quality requirements

- `[P0]` Every recommendation should show source freshness.
- `[P0]` The system should clearly state when important inputs are missing, inferred, or stale.
- `[P0]` The system should remain explainable even when some sources are unavailable.
- `[P1]` The system should improve automatically as more structured customer data becomes available.

## 4. When And How The Assessment Should Be Presented

### Presentation timing

- `[P0]` Present the assessment during the prescribing conversation, ideally as soon as medication intent is confirmed.
- `[P0]` Keep the assessment available before the prescription is finalized so it can influence the choice.
- `[P1]` Avoid interruptive pop-ups unless access risk is high and likely to create immediate downstream failure.

### Recommended surfaces

- `[P0]` `Primary:` desktop browser plug-in or desktop side panel.
- `[P1]` `Secondary:` embedded EHR panel where integration later becomes available.
- `[P2]` `Mobile phone app:` only as a companion surface for saved recommendations or follow-up review, not the primary prescribing UI.

### Display requirements

- `[P0]` Show a top-line `High / Medium / Low` executability assessment.
- `[P0]` Show a one-sentence rationale next to the `H / M / L` label.
- `[P0]` If multiple medications are mentioned or evaluated, list them in chronological order of mention or selection.
- `[P0]` The default view should let a clinician understand the answer in a few seconds.
- `[P1]` Show a confidence or freshness indicator when the system is relying on incomplete information.

### Expanded detail view

- `[P0]` Clicking into an item should show detailed explanation of the main drivers.
- `[P0]` Drivers should include formulary status, prior auth burden, cost exposure if available, routing constraints, step edits, and missing information.
- `[P0]` If the medication is `Medium` or `Low`, show 2 to 3 recommended alternatives.
- `[P0]` Each alternative should include a short reason such as better coverage, lower expected out-of-pocket cost, lower PA burden, or easier routing.
- `[P0]` Include patient-ready talking points that help the clinician explain why the original option may be delayed, why an alternative may start faster, and what the patient should expect next.
- `[P0]` Communication guidance should be phrased in patient-friendly language rather than payer or utilization-management jargon.
- `[P1]` The assistant should optionally generate a suggested script such as a staged-plan explanation: start an accessible option now, then revisit the preferred therapy if needed.
- `[P1]` Show which inputs were manually confirmed by the clinician versus inferred by the system.

## 5. How The Decision Becomes Actionable

- `[P0]` The clinician should be able to `accept`, `reject`, `dismiss`, or `save for later`.
- `[P0]` The clinician should remain the final decision-maker before any prescription is changed or signed.
- `[P0]` The clinician should be able to use the assistant's communication support to explain the recommended option or alternative before the patient leaves the room.
- `[P0]` If direct EHR integration is not available, the recommendation should be saved in the app with reasoning, timestamp, and patient context preserved.
- `[P0]` Saved recommendations should include the communication summary used in the visit so the clinician does not lose the patient-facing explanation.
- `[P0]` Saved recommendations should be easy to reopen so clinicians do not lose the logic behind the decision.
- `[P0]` The system should maintain an audit trail of what was recommended, what data supported it, and what the clinician chose.
- `[P1]` If integrated with the EHR later, accepted recommendations should sync back as a draft or clinician-reviewed update.
- `[P1]` If a recommendation is rejected, the clinician should be able to optionally capture a quick reason for future model and workflow learning.

### Collecting the clinician’s final decision (recommendation quality and improvement)

- `[P0]` The system must collect the clinician’s final decision for each recommendation: accept, reject, dismiss, or save for later.
- `[P0]` Feedback can be collected in two ways: (1) **explicitly in our UI** (e.g. clinician taps accept, reject, dismiss, or save for later), or (2) **via live recording / transcription** (inferring from what the clinician said or did in the visit, with appropriate consent and confidence thresholds).
- `[P0]` This enables measurement of recommendation quality (e.g. acceptance or meaningful-consideration rate) and shows whether clinicians actually act on our guidance.
- `[P0]` Stored decisions should be linked to the recommendation, rationale, and context so we can analyze which recommendations are accepted vs rejected and why.
- `[P1]` When the clinician rejects or dismisses, optionally capture a short reason (e.g. “preferred original,” “patient choice,” “data outdated”) to improve the model and prompts over time.
- `[P1]` Use this feedback loop to tune executability logic, alternative ranking, and talking points.

## 6. Additional Functional Requirements

- `[P0]` Results should load fast enough to be useful during the visit.
- `[P0]` The system should handle multiple candidate therapies in one encounter.
- `[P0]` The experience should be recommendation-oriented, not another dense alert or data dump.
- `[P0]` The experience should support the patient conversation, not just the prescribing decision, by helping the clinician set realistic expectations in the room.
- `[P0]` Compliance, consent, auditability, and source transparency should be built in from the start.
- `[P0]` The system should work within a narrow specialty and drug launch scope first, then expand over time.
- `[P1]` The system should degrade gracefully when some data sources are unavailable.
- `[P1]` The product should log acceptance, rejection, dismiss, and downstream outcome signals for continuous improvement.
- `[P1]` The system should support staff handoff or coordinator follow-up in a later release.

## Non-Requirements And Guardrails

- `[P0]` The system should not autonomously choose, switch, or discontinue medications.
- `[P0]` The system should not auto-submit prior authorizations, appeals, enrollment forms, or routing actions in `V1`.
- `[P0]` The system should not present black-box outputs without access-specific rationale.
- `[P0]` The system should not guarantee final payer approval, final coverage, or final patient cost.
- `[P0]` The system should not become a general ambient scribe or note-taking product in `V1`.
- `[P0]` The system should not force clinicians to leave their normal prescribing workflow for core actions.
- `[P0]` The system should not interrupt the clinician for every medication mention or search.
- `[P1]` The system should not replace the medication access coordinator workflow in the first release.

## Suggested V1 Summary

- `[P0]` Detect prescription intent primarily through `live recording and transcript detection`, with clinician confirmation.
- `[P0]` Use a `desktop browser extension` or desktop side panel as the main presentation surface.
- `[P0]` Trigger assessment when a medication is mentioned and confirmed during the visit.
- `[P0]` Use payer, formulary, routing, and available cost data to generate an explainable `High / Medium / Low` executability signal.
- `[P0]` Present multiple medications in chronological order with one-sentence rationale, drill-down details, and patient-facing communication support.
- `[P0]` Let clinicians accept or reject recommendations while preserving human control.
- `[P0]` Save accepted or reviewed recommendations in the app with full reasoning and the patient-facing explanation when EHR integration is not yet available.
- `[P1]` Add read-only EHR context and later write-back once the MVP proves value.

