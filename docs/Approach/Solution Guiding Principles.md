# Solution Guiding Principles

## How AI should help

- Surface an explainable accessibility assessment at the moment of prescribing.
- Synthesize fragmented signals such as PA risk, formulary friction, out-of-pocket cost, and routing constraints.
- Recommend executable alternatives, not just covered alternatives.
- Prioritize options that improve likelihood to start therapy and speed to start.
- Generate concise, patient-ready talking points for barrier and next-step discussions.
- Reduce downstream rework by helping clinicians make a more executable initial choice.
- Fit lightly into existing EHR and access workflows rather than replacing them.
- Make reasoning visible by showing key drivers, source basis, and freshness.

## What should remain explicitly human

- Final therapy choice and prescribing judgment must stay with the clinician.
- Tradeoffs between clinical preference, access friction, and patient context should be decided by humans.
- Any prescription change, routing action, or PA-related submission should be user-initiated and reviewable.
- Patient counseling should remain clinician-led, with AI as support rather than spokesperson.
- Organizations should define guardrails for approved alternatives and escalation paths.

## Where AI should not be used

- Do not let AI autonomously choose or switch medications.
- Do not use black-box recommendations with no clear rationale.
- Do not auto-submit prior auths, appeals, routing, or enrollment actions from AI output alone.
- Do not position AI as determining clinical superiority; keep it focused on access feasibility.
- Do not rely on autonomous patient-facing AI for medication-access guidance in high-stakes cases.
- Do not use AI where bias, missing data, or stale payer logic cannot be surfaced and checked.

## Overall Product Guardrails

- Be better than alerts: pair risk signals with actionable next steps.
- Be better than RTBT alone: combine coverage, cost, routing, and documentation burden.
- Be better than note takers: focus on whether an order is realistically startable.
- Measure success with time to therapy, first-fill success, abandonment reduction, and rework reduction.
