# Prescription Assistant — Clinician Companion Demo

A single-page interactive demo simulating an AI-powered clinical decision support tool for medication access management.

---

## ▶️ How to Start the Website

> **Important:** Always serve via `localhost`, NOT by opening the file directly in the browser (`file://`).
> Chrome does not persist microphone permissions for `file://` URLs and will re-prompt every time.

### Step 1 — Start the local server

Open a terminal, navigate to the `demo` directory and run:

```bash
cd demo
python3 -m http.server 8765
```
### Step 2 — Open in Chrome

Navigate to:

```
http://localhost:8765/clinician-companion.html
```

> The server runs on port **8765**. Leave the terminal open while using the site. To stop the server, press `Ctrl+C`.

---

## 🗂 File Structure

```
demo/
├── clinician-companion.html   # The entire demo (self-contained single-page app)
├── AZURE_SETUP.md             # Azure AI Foundry endpoint setup instructions
└── README.md                  # This file
```

---

## 🎮 Demo Modes

The demo has two modes, toggled via the buttons in the top-right header:

### Scripted Mode
A fully pre-scripted conversation that runs automatically. Good for presenting to an audience. Click **Start Demo** to begin — no microphone needed.

**Scripted flow:**
1. Dr. Martinez opens the visit
2. Patient mentions diet/exercise frustration
3. Doctor mentions **semaglutide** → Prescription Assistant assessment panel appears
4. Patient asks about trying it sooner → Doctor checks insurance
5. Patient mentions **tirzepatide/Mounjaro** → Second medication notification appears
6. Demo shows the full access intelligence workflow

### Live Mode (You = Patient, AI = Clinician)
You speak as the patient; Azure AI responds as Dr. Martinez in real time. The Prescription Assistant panel activates automatically when a medication is mentioned.

**Live mode conversation arc:**
1. **Before medication detected:** Dr. Martinez responds with pure clinical enthusiasm — recommends Wegovy, no mention of insurance barriers (she hasn't checked yet)
2. **Medication detected** (doctor mentions Wegovy/semaglutide): Assessment panel appears; a bridging line auto-injects — *"Let me just pull up your insurance coverage real quick…"*
3. **Before Accept:** If patient mentions tirzepatide/Mounjaro, doctor responds warmly — *"Great option, let me check your chart…"* — still no barriers revealed
4. **After clicking Accept:** Doctor explains the access findings (PA required, step therapy) and pivots naturally to phentermine as the near-term path

---

## 🔑 Azure AI Configuration

To run Live Mode, you must provide your own Azure AI Foundry endpoint and API key.

When you open the demo for the first time, it will automatically prompt you to enter these credentials via the **Settings (⚙️) menu**.

- The credentials are saved securely in your browser's **localStorage**.
- You can change them at any time by clicking the gear icon in the top right.

See `AZURE_SETUP.md` for instructions on provisioning a new Azure endpoint.

---

## 🎙 Microphone (Live Mode Only)

- Live mode requires microphone access for speech recognition (Web Speech API)
- **Always use `localhost:8765`** — Chrome persists mic permission for localhost permanently after one Allow click
- On `file://` URLs, Chrome re-prompts every session (cannot be fixed in code)
- If mic is denied, the demo automatically falls back to Scripted mode

---

## 🐛 Known Behaviors & Notes

| Behavior | Notes |
|---|---|
| Doctor speaks one box at a time | Clinician bubbles are queued — they type sequentially, never simultaneously |
| Medication detection | Triggers on both patient speech AND doctor's response text — handles garbled speech recognition |
| Three-phase doctor persona | Phase 1: enthusiastic, Phase 2: checking, Phase 3: explains access (only after Accept) |
| "Clinician" prefix stripped | AI occasionally prepends its own speaker label — this is auto-removed from all replies |

---

## 🔧 Troubleshooting

**Port already in use:**
```bash
lsof -i :8765          # find the process
kill -9 <PID>          # kill it
python3 -m http.server 8765  # restart
```

**Mic keeps prompting:**
Make sure you're on `http://localhost:8765/` not `file:///`. Open Chrome site settings and set microphone to "Allow" for `localhost`.

**Azure AI not responding:**
Check the API key hasn't expired. Use the ⚙️ settings gear → "Test Connection" to verify.
