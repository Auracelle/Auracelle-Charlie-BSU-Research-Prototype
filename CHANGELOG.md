# Changelog

All notable changes to Auracelle Charlie are documented here.
Format follows [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).

---

## [0.5.0] — 2026-04-14

### Added
- **Tab ⑪ Session Archive** — cross-session tracking engine persisting to browser localStorage:
  - Full session archive table with PSTOA score, resilience, coalition, foresight dimensions, verdict, and date per session
  - Filter by scenario and composition group
  - Optimization Trajectory chart — PSTOA score progression across sessions with delta indicators (▲/▼) showing improvement between iterations
  - Cross-Composition Comparison — same scenario, different participant groups; primary Objective 3 data surface
  - Governance Indicator Trajectories — coalition, compliance, legitimacy, fragmentation, escalation, resilience across all sessions
  - Export Archive CSV — structured flat file ready for Lab Notebook ingestion (28 columns including all PSTOA dimensions and governance indicators)
  - Export Archive JSON — full structured archive with Lab Notebook variable mapping embedded (`primary_dv`, `primary_iv`, `covariates`, `indicator_variables`)
  - Sessions auto-save on Generate AAR + PSTOA — no manual action required
- **Policy Stress-Test Outcome Assessment (PSTOA)** — composite 0–100 score in Tab ⑤:
  - Five weighted dimensions: Policy Resilience (/25), Coalition Coherence (/20), Compliance Signal (/20), Foresight Accuracy (/20), Process Efficiency (/15)
  - Four-tier verdict: Holds · Conditional · Fragile · Failure
  - Gap analysis with governance design implications per failed dimension
  - Optimization signal — concrete next-iteration instruction
  - Design recommendations — actionable list including Lab Notebook export prompt
  - Export PSTOA JSON — `charlie-pstoa-{SESSION_ID}.json`
  - PSTOA score embedded in session JSON export
- Tab ④ cross-session comparison table updated to show live archive (5 most recent sessions)
- View Archive button added to Tab ⑤ AAR card header

### Changed
- Tab ⑤ Generate button relabelled "Generate AAR + PSTOA"
- `loadCompletedSessions` stub replaced with full archive load and render
- Nav expanded from 10 to 11 tabs

---

## [0.4.0] — 2026-04-13

### Added
- **Round Arc / Deliverable Framework** — three structured workshop arcs:
  - Governance Negotiation Arc (6 rounds)
  - Crisis Response Arc (4 rounds)
  - Standards Setting Arc (6 rounds)
- Document/artifact attachment in round deliverable submissions
- Workshop Use-Case / Stress-Test Objective — scenario-linked pre-built use-cases + free-text field
- Tab ⑧ Autonomous Simulation — goal-directed autonomous session, three-way foresight comparison
- Tab ⑩ Agentic AI — LLM-backed Policy Owner + Agentic Red Team via Anthropic API

### Changed
- Alert banners significantly more pronounced (info/warn/crit colour differentiation)
- GWC display panel changed to warm charcoal gradient (#2a2520 → #1c1814)
- Round advance logic fixed: final round now reachable
- Arc/time pressure conflict resolved; time pressure disabled when arc active

### Fixed
- `initSession` infinite loop from JS function wrapper/hoisting conflict
- Duplicate `advanceRound` definition removed

---

## [0.3.0] — 2026-03-15

### Added
- Tab ⑨ Red Team & Shocks — shock library, MITRE ATT&CK compound chains (APT41, Sandworm, APT29, XENOTIME/ICS)
- Tab ⑦ MARL Engine — Q-learning, Stackelberg, EGT, Nash detection
- Policy Owner always-on panel in Facilitator Mode

---

## [0.2.0] — 2026-03-02

### Added
- Foresight Validation tab with historical case comparison
- After-Action Review generation, JSON/CSV export
- SIPRI data feed, EDS, SEM reliability metrics
- Six demographic composition groups

---

## [0.1.0] — 2026-02-15

### Added
- Initial single-file HTML prototype
- Session configuration, facilitator turn logging
- Governance indicators, g-GWC index, threshold alerting
