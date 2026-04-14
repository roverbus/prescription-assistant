# Azure AI Setup for Clinician Demo

**Endpoint is already pre-configured** in `clinician-companion.html`.

## Run the demo (important)

Opening the HTML file directly (`file://`) can make it static — buttons won't work. **Run a local server instead:**

```bash
cd Mockup && python3 -m http.server 8765
```

Then open in your browser: **http://localhost:8765/clinician-companion.html**

## Steps

1. Open `clinician-companion.html` in **Chrome**.
2. Click the **gear icon** (⚙️) in the Prescription Assistant panel header.
3. The **Endpoint** is pre-filled (`grok-4-1-fast-reasoning` deployment). Paste your **API key** into the API Key field.
4. Click **Save** — your key is stored in your browser only (never in the file).
5. Close the settings panel.

## Live mode

- Switch to **Live (You = Patient, AI = Clinician)** mode.
- Click **Start Live** — allow microphone when prompted.
- You speak as Sarah (patient); the AI plays Dr. Martinez (clinician).
- The AI clinician will greet you first and mention **semaglutide** to trigger the evaluation.
