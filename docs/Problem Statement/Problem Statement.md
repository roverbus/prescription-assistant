# Mission

Empower clinicians to make better prescription decisions that is not only clinically appropriate, but also realistically executable and have better conversations with patients.

# Problem Statement

In U.S. outpatient care, there is a frequent mismatch between a physician’s prescribing decision and a patient’s real medical access to start the intended medication. After prescription intent is surfaced in the clinic visit, providers often lack timely, patient-specific visibility into coverage requirements, prior authorization risk, formulary restrictions, pharmacy routing constraints, and out-of-pocket cost. 
The lack of the timely information, coming with poor patient communication and unclear ownership of next steps, results in patients experiencing delays, unexpected expense, therapy abandonment, and confusion, while clinicians and staff absorbing significant administrative burden through rework, manual coordination, and follow-up. Existing tools such as Electronic prior authorization (ePA) and Real-time benefit tools (RTBT) address parts of the workflow, but they do not reliably ensure that the selected medication is executable, affordable, and understandable in the moment of care.

# PainPoints

"Pain Point","Who Feels It Most","Supporting Evidence","Why It Matters"
"Treatment delays before therapy starts","Patients, clinicians","AMA 2024: 93% of physicians said PA delays necessary care. Oral anticancer study: new PA added 9.7 days to next fill.","Delays reduce clinical effectiveness and create anxiety at the exact moment treatment is supposed to begin."
"Administrative burden and workflow drag","Clinicians, clinic staff","AMA 2024: 39 PAs per physician per week and 13 hours/week spent by physicians and staff. 40% reported staff dedicated exclusively to PA.","This creates costly rework, pulls staff away from patient care, and contributes to burnout."
"Existing tools provide alerts too late, and do not provide actionable alternative suggestions.","Clinicians, provider orgs","AMA: only 23% of physicians said their EHR offers ePA for medications. RTBT trial: only 4.2% of prescriptions had an eligible recommendation; later study shows only 11% of the warnings are accepted.","Today’s solutions are fragmented, incomplete, or poorly timed, leaving the core access problem unresolved."
"Poor patient transparency and confusion","Patients, providers","
KFF 2025: 51% of insured adults said they needed prior authorization in the past two years. Among those, 47% said it was somewhat or very difficult to navigate.
PAN Foundation 2026 poll: 28% did not appeal their insurer’s decision. Of those, 12% said they did not appeal because they didn’t know they could.","Lack of clarity forces patients to self-navigate a complex system and increases stress and dropout risk."
"Treatment abandonment or discontinuation","Patients, providers","AMA 2024: 82% of physicians said PA can lead to treatment abandonment. Oral anticancer study: 7.1x higher odds of discontinuation when PA was newly imposed.","If patients never start or stop therapy, the clinical decision fails despite being medically appropriate."

# Personas

> Below is a simplified version of Persona; for full persona, refer to `Medication Access Personas.md` doc

Customer Persona
Users:

Persona	Who	Priority	Primary job to be done	Top pains	Desired outcomes	Likely objections
Prescribing Clinician	Physician, Nurse Practitioner, Physician Assistant	P0	Choose and start the right therapy without creating downstream access failure, patient confusion, or excessive rework.	Limited visibility into prior auth, step therapy, formulary restrictions, expected patient out-of-pocket cost, and specialty pharmacy routing at the moment of prescribing; learns about access problems too late; receives callbacks and re-prescribing work; has little confidence that the patient understands next steps.	Know before signing the order whether the medication is likely to be coverable, affordable, and routable; see the next best executable alternative when the original therapy is likely to fail; reduce follow-up messages and therapy restarts; preserve patient trust through clearer expectation setting.	"I already have EHR alerts and benefit tools."; "Do not add clicks or interrupt my visit."; "If the recommendations are wrong, they will waste my time."
Medication Access Coordinator	Insurance Liaison, Prior Authorization Specialist, Medication Access Specialist, Referral / Benefits Investigation Staff, Specialty Medication Coordinator	P1	Turn a prescribed therapy into an approved, affordable, correctly routed, and started medication.	Work is fragmented across payer portals, EHR inboxes, faxes, pharmacies, assistance programs, and patient phone calls; must manually triage many different barrier types; ownership is often unclear when a case gets stuck; repeated patient outreach is needed because expectations were not set clearly upstream.	A single queue with case status, likely barrier type, next best action, and handoff tracking; fewer dropped or duplicated cases; faster time from prescription to therapy start; less manual searching for payer rules, routing rules, and affordability options.	"We already use ePA and our own work queues."; "If this misses edge cases, we still need to do the work manually."; "I do not want another dashboard that duplicates my workflow."

Buying and Implementation Stakeholders
Below are core stakeholders impacting the implementation decision. In a bigger clinic or hospital, they should be considered as P0 stakeholders.

Persona	Role	What they care about	Why they matter
Healthcare Provider leadership	Economic buyer or senior sponsor.	Faster therapy starts; reduced staff burden and rework; better patient experience in specialty-heavy clinics; measurable ROI beyond simple prior authorization turnaround.	They approve budget and need confidence this is a workflow platform, not just another narrow point solution.
IT/Integration Lead	Technical gatekeeper.	Implementation risk, data flow, integration scope, security, and support burden.	A workflow product must fit into the EHR and existing operational systems.
Compliance Officer	Approval and governance stakeholder.	Privacy, auditability, permitted data use, and workflow safety.	Important for approval, but not a daily end user.

Impacted Personas
Not core users for the product, but they are impacted by the prescription decision, or provides key inputs into the decision making

Impacted persona	Role in the workflow	How they are impacted	Desired outcomes
Patient	End recipient of the prescribed therapy	Feels the downstream consequences when a prescription is delayed, denied, too expensive, or routed incorrectly	Fast therapy start, predictable cost, clear explanation of barriers, easy next steps, confidence that someone owns the process
Pharmacy	Dispenses medication and often surfaces the first real execution barrier	Gets pulled into rerouting, rejection handling, specialty distribution issues, affordability questions, and repeated patient follow-up	Correct routing on first send, cleaner handoff from clinic, fewer rejected fills, faster first-fill conversion, less manual coordination
Pharmacy Benefit Manager	Operationalizes formulary design, pharmacy network rules, and benefit logic across plans	Influences alternatives shown, preferred channels, patient OOP exposure, and rejection patterns at point of prescribing and fill	More accurate benefit intelligence, fewer unnecessary rejects, better routing, lower avoidable manual intervention

