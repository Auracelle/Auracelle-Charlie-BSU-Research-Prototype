# Research Notes

**Auracelle Charlie — BSU Doctoral Research Instrument**
PI: Evans, G-A. · Bath Spa University · Supervisor: Dr. John Curry

---

## Framework reference

**E-AGPO-HT** — Evans-Accelerated Governance Policy Optimisation — Hierarchical Theory

The framework operates across three strata with seven Broad Governance Capabilities (BGC):

| Code | Capability |
|------|-----------|
| STI | Strategic Threat Intelligence |
| SAD | Security Architecture Design |
| ESI | Exploratory Simulation Intelligence |
| NDM | Negotiation Dynamics Modelling |
| SRA | Strategic Rationality Assessment |
| IIC | Institutional Implementation Capacity |
| ASI | Adaptive Scalability Intelligence |

BGC scores are updated turn-by-turn from participant move data and aggregate into the g-GWC (General Governance Wargaming Capacity) index.

---

## Governance indicators

Eight indicators are derived from turn log data:

| Indicator | Derivation |
|-----------|-----------|
| Coalition Strength | Proportion of coalition-positive moves weighted by actor significance |
| Compliance Probability | Comply moves as proportion of proposal + comply total |
| Legitimacy Score | Verify + comply + high-confidence moves normalised over turns |
| Fragmentation Index | Defection and split moves weighted by round position (inverse: lower is better) |
| Decision Latency | Mean minutes per move across all turns |
| Escalation Index | Mean escalation signal over last 3 turns (0=stable, 1=conflict) |
| Public Trust (proxy) | 0.5·Legitimacy + 0.3·Compliance + 0.2·(1−Fragmentation) |
| Institutional Resilience | 0.4·Coalition + 0.3·Legitimacy + 0.3·(1−Fragmentation) |

---

## Research objectives mapping

| Objective | Instrument element |
|-----------|-------------------|
| Obj 3 — Demographic group effects | Composition group selector; turn log includes composition tag; deliverable CSV keyed by composition |
| Obj 4 — Governance indicators | Tab ③ live dashboard; AAR indicator summary; JSON export |
| Obj 5 — Resilience design principles | Tab ⑨ shock injection; resilience recovery curve; cascade count |
| Obj 6 — Foresight validity | Tab ④ historical case comparison; accuracy formula; three-way comparison in Tab ⑧ |

---

## Scenario domain packs

Six domains available. Each defines actor incentives, governance dilemmas, and use-case stress-tests:

- **AI Weapons Governance** — autonomous lethal systems, LOAC compliance, human oversight thresholds
- **Cyber Norms & Standards** — critical infrastructure, attribution disputes, private sector compliance
- **Nuclear-AI Nexus** — C2 governance, escalation ladder, NPT compatibility, strategic stability
- **Autonomous Systems** — meaningful human control, asymmetric actors, LOAC compliance
- **Data Sovereignty** — data localisation, training data provenance, export control evasion
- **Privacy Compliance** — algorithmic accountability, biometric governance, regulatory divergence

---

## Round arcs

Three structured deliverable frameworks for workshop design:

**Governance Negotiation Arc (6 rounds)**
Mirrors real multilateral diplomatic process:
1. Position Declaration — pre-negotiation prior capture
2. Policy Need Submission — surfacing negotiating space
3. Coalition Signal — formation moment; simultaneous reveal
4. Counter or Comply — no fence-sitting; every actor chooses
5. Shock Response — framework resilience under adversarial injection
6. Final Governance Outcome — primary outcome variable

**Crisis Response Arc (4 rounds)**
Compressed high-pressure arc for adversarial scenario workshops:
1. Threat Assessment · 2. Emergency Mechanism Proposal · 3. Coalition Commitment · 4. Crisis Resolution

**Standards Setting Arc (6 rounds)**
Technical governance arc:
1. Problem Framing · 2. Technical Requirements · 3. Draft Standard Proposal · 4. Objections & Amendments · 5. Compliance Commitment · 6. Final Adoption

---

## Qualitative coding scheme

Session outputs are structured for qualitative coding across three dimensions:

**Move-level coding**
- Action type (8 categories: propose, counter, coalition, defect, comply, escalate, verify, delay)
- BGC domain engaged
- Escalation signal (4 levels)
- Coalition effect (4 levels)

**Round-level coding**
- Deliverable text per actor per round
- Round arc stage (6 categories)
- Threshold events triggered

**Session-level coding**
- Equilibrium state (Non-Cooperative Lock-in / Escalation / Partial Nash / Cooperative Convergence)
- Foresight accuracy vs. historical case
- Composition group (6 categories)
- Stress-test use-case

---

## Export formats

**JSON export** (`charlie-{SESSION_ID}.json`)
Full structured session data including configuration, turn log, BGC scores, indicator values, thresholds crossed, and validation case metadata.

**CSV turn log** (`charlie-turns-{SESSION_ID}.csv`)
Turn-by-turn data keyed by actor, round, action type, BGC, rationale, latency, confidence, coalition effect, escalation signal, and composition group.

**Deliverable CSV** (`charlie-deliverables-{SESSION_ID}.csv`)
All round deliverables keyed by round, round name, deliverable type, actor, text, and composition group.

---

## Version notes

v0.4.0 adds round arc deliverable framework, document attachment, stress-test use-cases, agentic Policy Owner/Red Team, autonomous simulation (Tab ⑧), and improved alert styling. See CHANGELOG.md for full history.

---

## Cross-session archive (v0.5.0)

The Session Archive (Tab ⑪) persists all completed sessions to browser localStorage under the key `charlie_session_archive_v1`. Each archive record contains:

- Session metadata (ID, timestamp, scenario, composition, round arc, use-case)
- PSTOA score and all five dimension scores
- Final governance indicator values (8 indicators)
- BGC scores (7 capabilities)
- g-GWC final value
- Shocks fired, thresholds crossed, turns logged, deliverables submitted

### Export formats for Lab Notebook

**Archive CSV** (`charlie-archive-{DATE}.csv`)
28-column flat file. One row per session. Primary format for regression and significance testing in the Lab Notebook.

**Archive JSON** (`charlie-archive-{DATE}.json`)
Full structured archive with embedded Lab Notebook variable mapping. Primary format for Python ingestion.

### Optimization loop

1. Run stress-test → Generate AAR + PSTOA → session auto-saved to archive
2. Review PSTOA gap analysis and optimization signal
3. Amend policy design (scenario parameters, actor incentives, arc)
4. Re-run same scenario → compare PSTOA delta in Tab ⑪ trajectory chart
5. Export archive JSON to Lab Notebook for statistical analysis across iterations

### PSTOA scoring formula reference

- **D1 Policy Resilience (/25):** 25 − fragmentation_penalty − escalation_penalty + resilience_norm + shock_bonus
- **D2 Coalition Coherence (/20):** coalition_score − defection_penalty + coalition_move_bonus
- **D3 Compliance Signal (/20):** compliance_score + legitimacy_bonus + trust_bonus
- **D4 Foresight Accuracy (/20):** mean accuracy across 5 indicator comparisons vs. historical case × 20
- **D5 Process Efficiency (/15):** round_efficiency + turn_density + deliverable_bonus − latency_penalty
