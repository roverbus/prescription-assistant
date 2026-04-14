# Validation & Learning

## Core Hypotheses To Validate

1. Clinicians will engage with the product if it fits lightly into the prescribing moment and gives a useful answer in seconds.
2. Explainable access guidance can change behavior before downstream rework begins.
3. A narrow specialty launch can generate recommendations that are accurate enough to earn trust even without deep `EHR` integration.
4. Patient communication support materially increases perceived value because clinicians need help setting expectations in the room.
5. Buyers will view reduced rework, faster starts, and improved first-fill success as strong enough value to justify adoption.

## What I Would Test In The First 90 Days

### 1. Recommendation Quality

Run an initial `shadow mode` pilot in one or two high-friction specialties such as rheumatology, dermatology, or gastroenterology. The tool generates executability assessments and alternatives, but the team first compares those recommendations against real downstream outcomes, coordinator feedback, and retrospective chart review.

What I want to learn:

- Are the `High / Medium / Low` assessments directionally right often enough to be useful?
- Are the suggested alternatives actually executable, not just theoretically covered?
- Are the key friction drivers accurate and understandable?

### 2. Workflow Fit

Test the browser extension or side panel in live clinician workflows with minimal interruption.

What I want to learn:

- Do clinicians open and review the recommendation during real prescribing moments?
- Does the product help within seconds, or does it feel like another alert?
- Is transcript-based detection reliable enough, or do we need more manual confirmation in `V1`?

### 3. Behavior Change

Measure whether the product actually changes the prescribing conversation.

What I want to learn:

- How often does the clinician keep the original choice versus switch to an alternative?
- How often does the clinician use the patient-ready communication support?
- Does the tool reduce obvious low-executability decisions before they become downstream work?

### 4. Buyer Value

Even in early pilots, I would test whether the problem is painful enough for a buyer to fund rollout.

What I want to learn:

- Do service-line leaders, pharmacy leaders, or innovation buyers see measurable operational value?
- Are early signals strong enough to support a business case around  time to therapy,first-fill success, and rework reduction?
- Which buyer most clearly owns the budget and ROI story?

## Pilot Design

- Start with `1-2` specialty lines in a single health system or large specialty group.
- Focus on a narrow set of high-friction therapies where access failures are common and alternatives matter.
- Use `shadow mode` first, then move to a lightweight live pilot once recommendation quality looks credible.
- Pair quantitative instrumentation with qualitative case studys from clinicians, coordinators, and pilot sponsors.

## Metrics I Would Track

### Product Usage

- Percent of eligible encounters where the assistant is opened.
- Time from medication mention to surfaced assessment.
- Dismiss, snooze, and re-open rates.
- Repeat usage by the same clinician.

### Recommendation Quality

- Clinician agreement with top-line executability rating.
- Acceptance or meaningful consideration rate for alternatives.
- Share of assessments later judged directionally correct by downstream review.
- Share of recommendations where missing or stale inputs materially weakened usefulness.

### Outcome Signals

- Time to therapy initiation.
- First-fill success rate.
- Prescription abandonment rate.
- Avoidable re-prescribing or rerouting rate.
- Coordinator rework and access-related callback volume.

### Trust And Communication

- Clinician-rated trust in the rationale.
- Clinician-rated usefulness of patient talking points.
- Patient understanding of next steps, measured through lightweight follow-up surveys where feasible.

## Persevere / Pivot Criteria

I would `persevere` if the product shows three things at once: clinicians voluntarily reuse it, the explanations are viewed as credible, and early pilot signals suggest fewer downstream surprises for in-scope medications.

I would `pivot` if any of the following happens:

- Clinicians say the product is interesting but not worth opening in workflow.
- Recommendation quality is too inconsistent even in a narrow specialty wedge.
- Transcript detection is too noisy, making the entry point feel unreliable.
- Communication support is valued, but the recommendation engine is not yet trusted enough to drive decisions.

If results are mixed, I would narrow further rather than scale prematurely. That likely means one specialty, one therapy class, and one primary job to be done: help clinicians avoid obviously low-executability choices and explain the plan clearly to the patient.

## case study-Ready Framing

In the first 90 days, I would treat this as a trust-and-workflow validation effort, not a scale effort. I would start in shadow mode in one or two high-friction specialty settings, validate that the recommendations are directionally right, then test whether the product actually changes prescribing behavior and reduces downstream surprises. The key decision is whether we are becoming part of the prescribing decision or just generating interesting information around it.