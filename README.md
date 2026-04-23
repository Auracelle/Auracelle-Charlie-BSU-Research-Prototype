# Auracelle Charlie — BSU Doctoral Research Instrument

**PI:** Grace-Alice Evans · Bath Spa University · Auracelle AI Governance Labs
**Supervisor:** Dr. John Curry, Bath Spa University
**Framework:** E-AGPO-HT v3.1 (Evans-Accelerated Governance Policy Optimisation — Hierarchical Theory)
**Affiliation:** Non-Resident Senior Fellow, UC Berkeley Center for Long-Term Cybersecurity (CLTC)

---

## What this is

Auracelle Charlie is a browser-based governance wargaming simulation instrument built for doctoral research into AI governance policy outcomes. It operationalises the E-AGPO-HT framework as a structured multi-actor negotiation environment with full cross-session tracking and optimization analysis.

Single-file HTML — no build step, no server, no external dependencies beyond Google Fonts and the optional Anthropic API.

---

## Capability overview

| Tab | Function |
|-----|----------|
| ① Session Design | Composition group, scenario domain, round arc, stress-test use-case |
| ② Facilitator Mode | Turn logging, round deliverable capture, Policy Owner always-on panel |
| ③ Governance Indicators | Real-time E-AGPO-HT indicator dashboard (8 indicators, 7 BGC scores) |
| ④ Foresight Validation | Simulated vs. historical case comparison + live archive summary |
| ⑤ After-Action Review | AAR + PSTOA scoring, qualitative coding prompts, exports |
| ⑥ SIPRI Data | Military expenditure context mapped to BGC parameters |
| ⑦ MARL Engine | Q-learning, Stackelberg dynamics, EGT, Nash detection |
| ⑧ Autonomous Sim | Goal-directed autonomous session — three-way Human/AI/Historical comparison |
| ⑨ Red Team & Shocks | Shock library, MITRE ATT&CK compound chains (APT41, Sandworm, APT29, XENOTIME) |
| ⑩ Agentic AI | LLM-backed Policy Owner + Agentic Red Team via Anthropic API |
| ⑪ Session Archive | Cross-session tracking, optimization trajectory, cross-group comparison, Lab Notebook exports |

---

## Quick start

### Option A — open locally
1. Download or clone this repository.
2. Open `index.html` in Chrome, Edge, or Firefox.

### Option B — serve locally
```bash
python -m http.server 8080
```
Open `http://localhost:8080`.

### Option C — GitHub Pages
Enable Pages in repository settings → main branch root. Auto-deploys on push via `.github/workflows/deploy.yml`.

---

## Cross-session tracking (Tab ⑪)

Every session saved via Generate AAR + PSTOA is automatically archived in browser localStorage. Tab ⑪ provides:

- **Session Archive table** — all sessions with PSTOA scores, dimension breakdown, and verdict
- **Optimization Trajectory** — PSTOA score progression with delta indicators across iterations
- **Cross-Composition Comparison** — same scenario, different participant groups (primary Objective 3 data)
- **Indicator Trajectories** — all 8 governance indicators tracked across sessions
- **Export Archive CSV/JSON** — structured exports for the Auracelle Charlie Lab Notebook

### Lab Notebook variable mapping
| Role | Variable |
|------|---------|
| Primary dependent variable | `pstoa_total_score` |
| Primary independent variable (Obj 3) | `composition` |
| Covariates | `scenario`, `round_arc`, `use_case`, `shocks_total`, `rounds_completed` |
| Indicator variables | `ind_coalition`, `ind_compliance`, `ind_legitimacy`, `ind_fragmentation`, `ind_escalation`, `ind_resilience` |

---

## Policy Stress-Test Outcome Assessment (PSTOA)

Generated automatically in Tab ⑤. Composite 0–100 score across five dimensions:

| Dimension | Weight | Measures |
|-----------|--------|---------|
| Policy Resilience | /25 | Shock absorption, fragmentation control, escalation management |
| Coalition Coherence | /20 | Coalition formation, defection resistance, alliance stability |
| Compliance Signal | /20 | Compliance probability, legitimacy, public trust |
| Foresight Accuracy | /20 | Simulated vs. historical governance trajectory |
| Process Efficiency | /15 | Session completeness, turn density, deliverable capture |

**Verdict tiers:** Holds (80+) · Conditional (60–79) · Fragile (40–59) · Failure (<40)

---

## Round arcs

| Arc | Rounds | Deliverable sequence |
|-----|--------|---------------------|
| Governance Negotiation | 6 | Position → Policy Need → Coalition → Counter/Comply → Shock Response → Final Outcome |
| Crisis Response | 4 | Threat Assessment → Emergency Proposal → Coalition Commitment → Resolution |
| Standards Setting | 6 | Problem Framing → Requirements → Draft → Objections → Compliance → Adoption |

---

## Agentic AI (Tab ⑩)

Requires Anthropic API key — entered once per browser session in Tab ⑩, stored in session memory only.

- **Policy Owner** — always-on, fires automatically each round, enriched with active round arc deliverables and stress-test use-case
- **Agentic Red Team** — APT-profile reasoning (APT41 / Sandworm / APT29 / XENOTIME), narrative escalation, governance indicator feedback

Model: `claude-sonnet-4-20250514`

---

## MITRE ATT&CK

Compound shock chains in Tab ⑨ mapped to ATT&CK Enterprise + ICS matrices:
- APT41 — T1195.002 Supply Chain Compromise
- Sandworm — T1583.006/T1586.002 Influence Operation
- APT29 — T1078/T1552.001 Credential Exfiltration
- XENOTIME — T0816/T0826/T0880 ICS Coercion

Citation: MITRE ATT&CK® v14 — [attack.mitre.org](https://attack.mitre.org)

---

## Files

```
index.html                    Main application (v0.5.0, single-file)
README.md
CITATION.cff                  Academic citation metadata
CHANGELOG.md                  Version history
CONTRIBUTING.md
CODE_OF_CONDUCT.md
SECURITY.md
LICENSE                       MIT + E-AGPO-HT IP notice
.gitignore
docs/
  ETHICS.md
  RESEARCH-NOTES.md
  FACILITATOR-GUIDE.md
.github/
  ISSUE_TEMPLATE/
  workflows/deploy.yml         GitHub Pages auto-deploy
```

---

## Citation

> Evans, G-A. (2026). *Auracelle Charlie: A Governance Wargaming Research Instrument* (v0.5.0). Bath Spa University / Auracelle AI Governance Labs.

See `CITATION.cff` for full metadata.

---

## License

MIT License. See [LICENSE](LICENSE).
E-AGPO-HT framework methodology is proprietary IP — see LICENSE NOTICE.

## Contact

**Grace-Alice Evans**
LinkedIn: [grace-alice-evans-5a9632a3](https://www.linkedin.com/in/grace-alice-evans-5a9632a3)
Platform: [Auracelle AI Governance Labs](https://auracelle.github.io/Auracelle-AI-Governance-Labs-Platform-Comms-Public)
