# Auracelle Charlie — Facilitator Guide

**Version 0.4.0 · Evans, G-A. · Bath Spa University**

---

## Before the session

### 1. Select your configuration (Tab ①)

**Participant Composition Group** — this is your primary independent variable (Objective 3). Select the group that matches your participants:
- Cross-Sector (MX) — baseline
- All-Military (ML)
- All-Female (AF) / All-Male (AM) — gender study compositions
- Civil Society (CS)
- Technical/Industry (TI)

**Scenario Domain** — choose the governance domain your workshop is exploring. Actors and their incentive structures will reflect the domain.

**Workshop Use-Case / Stress-Test Objective** — select the specific policy question you are stress-testing, or write a custom objective. This frames the entire session and appears in the Facilitator Mode header and Policy Owner challenges.

**Round Arc** — select a structured deliverable framework:
- *Governance Negotiation Arc* (6 rounds) — recommended for most workshops
- *Crisis Response Arc* (4 rounds) — for high-pressure or crisis scenario workshops
- *Standards Setting Arc* (6 rounds) — for technical standards negotiation workshops
- *Free-form* — no structured deliverables; use Time Pressure setting for round count

When a Round Arc is selected, Time Pressure syncs automatically.

**Validation Case** — select the historical governance case you are comparing against (for Objective 6 foresight validity).

### 2. Agentic AI (Tab ⑩, optional)

If using the Policy Owner and Agentic Red Team features, enter your Anthropic API key before initialising the session. The Policy Owner will fire automatically at session start and after each round advance — no additional action required.

---

## Running the session (Tab ②)

### Policy Owner panel
The teal panel at the top of Facilitator Mode shows the current round's governance challenge. This is visible to you (and optionally to participants on a shared screen). It updates automatically each round.

### Round Deliverable Zone
When a Round Arc is active, the blue deliverable zone opens automatically after session initialisation and after each round advance. For each round:
1. Read the round prompt to participants
2. Give participants time to formulate their deliverable
3. Select each actor in turn and enter their submission (text, attached document, or both)
4. Zero submissions are acceptable — click **Continue to Governance Indicators** to proceed
5. All submissions are logged in the Deliverable Log below

### Logging participant moves (turn log)
Use the turn entry form to record each participant move:
- **Actor** — who is making the move
- **BGC Engaged** — which governance capability domain this move primarily engages
- **Governance Move Type** — the strategic type (propose, counter, coalition, defect, comply, escalate, verify, delay)
- **Governance Action Taken** — the specific action from the dropdown
- **Rationale Captured** — verbatim or paraphrased reasoning from the participant
- **Decision Latency** — minutes taken to decide
- **Escalation Signal** — your assessment of whether this move escalates tension

### Advancing rounds
Click **→ Advance Round** when all participants have moved. The Policy Owner will automatically issue a challenge for the new round.

### Injecting shocks (Tab ⑨)
Switch to Tab ⑨ at any point to inject a shock event. Single shocks take effect immediately. Compound ATT&CK chains unfold over 3 staged impacts with 1.8 seconds between stages. Return to Tab ② to continue logging participant responses.

---

## Role structure for workshops

For structured workshops, consider assigning the following roles:

| Role | Function |
|------|----------|
| **Policy Owner** | Neutral governance authority — issues challenges, monitors indicators. Ideally played by the AI agent (Tab ⑩) or by the facilitator. |
| **Red Team (2–3 people)** | Adversarial actors — pursue fragmentation, defection, and escalation. Designated in Tab ⑨. |
| **Neutral Observer/Scribe** | Documents decision rationale, does not participate. Ideally the researcher. |
| **Remaining participants** | Play assigned actor roles in good faith. |

---

## After the session

1. **Tab ③** — Review final governance indicators and BGC scores
2. **Tab ④** — Check foresight validity against the selected historical case
3. **Tab ⑤** — Generate After-Action Review. Use the qualitative coding prompts for post-session analysis. Export JSON (full session data) and CSV (turn log) for research records.
4. **Deliverable Log** — Export deliverables CSV from the Deliverable Log in Tab ②

---

## Data recording notes

- Session ID is auto-generated — record it against your IRB/ethics reference for traceability
- Do not enter participant names in free-text fields — use actor role identifiers
- If using Tab ⑩ agentic features, note that turn rationale excerpts are transmitted to Anthropic's API — see `docs/ETHICS.md`

---

## Troubleshooting

**Session doesn't initialise when I click the button**
Ensure you have selected a Participant Composition Group (a tile must be highlighted in teal) and a Scenario Domain before clicking Initialise Session.

**Round deliverable zone doesn't appear**
Confirm a Round Arc is selected (not "No structured arc"). If using free-form, the deliverable zone does not appear by design.

**Policy Owner shows "check API key" message**
Enter and save your Anthropic API key in Tab ⑩ before initialising the session, or after — the agent will activate immediately once the key is saved with a valid session running.

**Final round (R6) doesn't appear**
This was a known bug fixed in v0.4.0. Ensure you are using the current version.

---

## Cross-session tracking (Tab ⑪)

### How sessions are saved

Every time you click **Generate AAR + PSTOA** in Tab ⑤, the session is automatically saved to the browser's localStorage archive. No manual action is required. Sessions persist across browser restarts on the same machine.

### Viewing the archive

Navigate to **Tab ⑪ Session Archive** to see all saved sessions. The archive table shows:
- Session ID, scenario, composition group, round arc
- PSTOA total score with colour-coded verdict
- Resilience, coalition, and foresight dimension scores
- Date

### Optimization workflow between sessions

1. Complete a session and generate AAR + PSTOA
2. Review the **Optimization Signal** in Tab ⑤ — this tells you specifically what to change in the next iteration
3. Go to Tab ⑪ and check the **Optimization Trajectory** chart — is the PSTOA score improving?
4. Check **Cross-Composition Comparison** — if you've run the same scenario with different groups, which group produced better governance outcomes?
5. Use the **Indicator Trajectories** panel to identify which specific governance indicators are improving or deteriorating across iterations

### Exporting for the Lab Notebook

Use **Export Archive JSON** in Tab ⑪ to produce the structured dataset for the Auracelle Charlie Lab Notebook. This file contains all sessions with PSTOA scores, indicator trajectories, and embedded variable mapping — ready for regression, correlation, and significance testing.

### Archive management

- Archives are stored in the browser only — they do not sync across devices
- Use **Export Archive JSON** regularly to back up your dataset
- The **Clear Archive** button permanently removes all stored sessions — export first
- If you use multiple browsers or devices, maintain a single export JSON as your canonical dataset and re-import it to the Lab Notebook
