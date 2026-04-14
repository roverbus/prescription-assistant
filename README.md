# Prescription Assistant — Product Management Case Study

Welcome to the Prescription Assistant case study! This repository houses the product strategy, go-to-market plan, and an interactive prototype for an AI-powered clinical decision support tool focused on medication access management.

## 💊 The Problem Space

Medication access is broken. When a clinician prescribes a complex or expensive therapy (like GLP-1s), it often triggers a maze of prior authorizations, step therapy requirements, and affordability barriers. 

This results in:
- High abandonment rates (patients giving up on their meds)
- Massive operational friction (clinic coordinators spending hours on phone calls)
- Burnout and eroded trust between clinician, patient, and system

## 🚀 The Solution: Prescription Assistant 

The **Prescription Assistant** is a proposed clinical support tool designed to inject access-feasibility intelligence directly into the prescribing workflow *before* the script is sent.

### The 90-Day MVP Approach

For the initial launch, the strategy deliberately prioritizes:

- **Explainability over automation**: We aren't fully automating Prior Auths yet. We are making the *barriers visible* so the clinician can adjust care plans in the room.
- **Workflow adjacency over deep EHR integration**: We rely heavily on a lightweight entry point to prove value immediately, reducing health system implementation risk.
- **Executable prescribing**: The wedge isn't predicting prior auth outcomes; it's about giving clinicians an executable, realistic path to get patients on therapy.

## 🛠 My Meta-Approach: Building This With AI

I approached this case study with an unconventional methodology: acting as the primary Product Manager while directing a team of specialized AI "subagents."

**Rapid Research & Prototyping:**
I leaned heavily on AI to rapidly research the domain, synthesize the regulatory environment, and draft the initial structure for my competitive analysis. I also collaborated with an AI coding agent to quickly spin up the interactive browser prototype you'll find in the `demo/` folder—allowing me to show, rather than tell, the value proposition.

**Navigating Disagreements & Product Decisions:**
Working with AI in a PM capacity requires pushing back. During our work, the AI naturally gravitated toward the most technically complex solutions—like building a standalone Prior Authorization prediction engine or demanding deep, autonomous EHR integration from day one.

I fundamentally disagreed with these paths for an MVP. Deep automation introduces massive clinician trust and regulatory risks. Instead, I forced the scope back to reality: focusing the product sharply on **workflow adjacency**, **explainability**, and delivering an immediate "yes/no/why" signal in the exam room. The AI generated the raw materials, but the strategic bounds, tradeoffs, and the MVP wedge were entirely human-directed.

## 🗂 Repository Structure

This repository is organized to follow standard Product Management artifacts:

- **`demo/`**: An interactive, single-page web app prototype simulating the clinician experience with the Prescription Assistant. Contains its own README for local setup.
- **`docs/01_Problem_Statement/`**: Personas, the core problem definition, and initial hypotheses.
- **`docs/02_Market_and_Competitive_Research/`**: In-depth analysis of the medication access mismatch, literature review, and competitive teardowns.
- **`docs/03_Approach_and_MVP_Scope/`**: The Core Solution Guiding Principles and the First Shippable Version (90-Day Scope).
- **`docs/04_GTM_and_Risks/`**: Launch and validation strategies, regulatory analysis, and an honest reflection on the biggest product risks.

*(Note: These docs were adapted and refactored from their original working directory).*

## 📚 Tools & References

To build this case study, I leveraged several excellent industry resources and agentic frameworks:

- **Product Strategy Frameworks & Methods**: The strategy artifacts and methodologies found in the `docs/Tools/Product Strategy Tools/` directory (e.g., Rumelt's Strategy Kernel, Gibson Biddle's DHM model, Devil's Advocate Method, SWOT) were adapted from [CC for PMs](https://ccforpms.com).
- **AI Subagents**: The AI subagent architecture and specialized routines used during the rapid research and prototyping phases were drawn from the [awesome-claude-code-subagents](https://github.com/VoltAgent/awesome-claude-code-subagents) repository.

---
Feel free to dive into the `docs/` and run the demo to see it in action!
