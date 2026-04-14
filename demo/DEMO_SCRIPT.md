# Prescription Assistant — case study Demo Script
### Print this. Keep it face-down. Glance only if you need it.

---

## ⏱ TOTAL TIME: ~4–5 minutes

---

## 1. OPENING PITCH (30 sec — before touching the screen)

> *"I built a working prototype of a product I'm calling Prescription Assistant —
> a real-time clinical decision support tool that sits inside the physician's
> EHR workflow. The core problem it solves: clinicians spend years training
> to know which drug is best clinically, but they have almost no visibility
> into whether that drug will actually be accessible to their patient.
> Prior authorization, step therapy, formulary tiers — all of that is
> invisible at the point of prescription. Prescription Assistant makes it visible,
> in real time, as the clinical conversation is happening.*
>
> *Let me show you a demo."*

---

## 2. SET THE SCENE (15 sec)

**[Point to the left panel — EHR]**

> *"This is the simulated EHR. Sarah Chen is a 38-year-old with obesity —
> BMI 34.2 — pre-diabetes, and hypertension that's well controlled.
> She's here for a follow-up on weight management. She's been trying
> diet and exercise for six months. It's not working."*

**[Point to the center panel — Demo Conversation]**

> *"This center panel shows the conversation as it unfolds.
> And this right panel is Prescription Assistant — what the doctor sees."*

---

## 3. START THE DEMO

**[Click "Scripted" if not already selected → Click "Start Demo"]**

---

## 4. WALK THROUGH THE CONVERSATION

### 🔵 Dr. Martinez opens the visit
*[On screen: "So tell me how things have been going with the diet and exercise plan…"]*

> *(Let it play. Don't narrate yet.)*

---

### 🔴 Sarah expresses frustration
*[On screen: "Honestly, I've been trying for months, but nothing is really working…"]*

> *(Still silent. Let the scene breathe.)*

---

### 🔵 Doctor mentions Wegovy / semaglutide ← **KEY MOMENT #1**
*[On screen: "Let's talk about some medication options. Have you heard of semaglutide?"]*
*[Prescription Assistant panel ACTIVATES — "MEDIUM" risk badge appears]*

**[Point to the right panel as it populates]**

> *"Watch what happens the moment the doctor says 'semaglutide' —
> Prescription Assistant detects the medication and instantly surface the
> patient's coverage landscape. No clicking, no tab-switching, no
> waiting. It just appears.*
>
> *Wegovy is covered under Aetna PPO — but there's a catch.
> Prior authorization required. Step therapy mandate — Sarah has to
> try a preferred agent for 90 days first. And that PA process
> takes 5 to 10 days with only 62% approval.*
>
> *The doctor didn't know any of this when she recommended Wegovy.
> Now she does."*

---

### 🔴 Sarah says she wants to start soon
*[On screen: "Yes, I've seen ads. I'd like to start something soon — I don't want to wait."]*

> *(Let it play.)*

---

### 🔵 Doctor checks insurance ← **KEY MOMENT #2**
*[On screen: "I hear you. Let me take a quick look at what your insurance covers for this…"]*

> *"The doctor pauses to consult the tool. This is the pivot moment —
> the clinical decision is about to change because of real-time access data."*

---

### 📋 Recommended Alternative appears
*[On screen: Phentermine (Generic) — HIGH confidence, No PA needed, ~$10–$30/mo]*

**[Point to the green "Accept" button]**

> *"Prescription Assistant doesn't just surface the barrier — it recommends
> a path forward. Phentermine is Tier 1, no prior auth, $10 copay,
> starts immediately. And crucially — it satisfies the step therapy
> requirement, which means documenting this three-month trial is also
> building the case for semaglutide approval later.*
>
> *One click. The doctor accepts the recommendation."*

**[Click "Accept"]**

---

### 🔵 Doctor pivots to explain the plan ← **KEY MOMENT #3**
*[On screen: scripted dialogue explaining the phentermine path, the timeline, the plan]*

> *"The doctor explains this to Sarah in plain language.
> No jargon, no 'I'll have to check with your insurance.'
> She already has the answer. She's confident. She has a plan."*

---

### 🔴 Sarah mentions Mounjaro / tirzepatide ← **BONUS MOMENT**
*[On screen: "My friend is taking tirzepatide — Mounjaro? Could we look into that?"]*
*[Second medication notification appears]*

**[Point to the "New Medication Detected" notification]**

> *"Sarah mentions a second medication. Prescription Assistant catches it
> automatically. The doctor can tap that notification and see a
> parallel assessment for tirzepatide — without losing context
> on the current conversation.*
>
> *This is what real-time means. Not a report you pull after the visit.
> The intelligence is there when the decision is being made."*

---

## 5. CLOSE THE DEMO (30 sec)

**[Let the BG conversation scroll — show the natural follow-up dialogue]**

> *"What you're watching in the background is the rest of the visit —
> the doctor and patient discussing side effects, dosing, the follow-up plan.
> The access problem has been solved. The clinical conversation can continue.*
>
> *The insight this prototype is designed to test: if you give doctors
> access intelligence at the moment of prescription — not in a portal,
> not in a prior auth workflow, not in a fax — you reduce delays,
> reduce denials, and give patients a faster path to the right drug.*
>
> *That's Prescription Assistant."*

---

## 6. KEY TALKING POINTS (use if asked follow-up questions)

### "Why does this matter?"
> Prior authorization causes ~25% of prescription abandonments. The average PA takes 5–10 business days. For a GLP-1 like Wegovy, approval rates hover around 60%. The delay is the problem — and it starts at the point of prescribing.

### "Why build this into the EHR workflow?"
> Because that's where the decision is made. Post-visit PA portals are firefighting. If the doctor knows at the point of prescribing that there's a step therapy requirement, they can proactively start phentermine and document it — making the eventual GLP-1 approval nearly inevitable instead of contested.

### "What's the AI doing?"
> In Live mode, Azure AI (GPT-4 class model) is playing the role of the clinician in real time, adapting its recommendations based on the patient's words and the formulary data Prescription Assistant surfaces. In Scripted mode, the dialogue is pre-written to show the cleanest narrative arc.

### "How does it get formulary data?"
> This prototype uses a modeled formulary based on publicly available Aetna 2025–2026 commercial PPO preferred drug list structures. In production, this would connect to real-time PBM APIs (CVS Caremark, Express Scripts, etc.) or an aggregated formulary data layer.

### "Who's the customer?"
> Primary: health systems and large physician groups who bear the friction cost of PA delays. Secondary: PBMs or payers who want to reduce PA volume by solving the problem upstream. Tertiary: pharma (access intelligence for their own brands).

### "What would you build next?"
> (1) Connect to live PBM formulary APIs for real data. (2) Add PA auto-initiation — one click from the assessment panel to pre-fill and submit the PA form. (3) Track outcomes: what % of Prescription Assistant-assisted prescriptions get filled vs. abandoned.

---

## 7. QUICK REFERENCE — WHAT'S ON SCREEN

| Panel | What it shows |
|---|---|
| **Left** | EHR — patient chart, conditions, meds |
| **Center** | Demo Conversation — doctor & patient dialogue |
| **Right (top)** | Prescription Assistant assessment — coverage, PA, alt drug |
| **Right (bottom)** | Live Transcript / conversation intelligence |

---

## ⚡ IF SOMETHING GOES WRONG

| Problem | Fix |
|---|---|
| Demo froze | Click **Reset** → **Start Demo** again |
| Nothing happening | Make sure you clicked **Start Demo** (not just the mode toggle) |
| Wrong mode showing | Click **Scripted** toggle at the top right |
| Site not loading | Go to `http://localhost:8765/clinician-companion.html` |
| Server not running | Run `python3 -m http.server 8765` from inside the demo folder |

---

*Good luck. You built this. You know it cold.*
