# Contributing to Auracelle Charlie

Thank you for your interest in contributing to this research instrument.

## Before you contribute

Auracelle Charlie is an active doctoral research instrument under the supervision of Dr. John Curry at Bath Spa University. The E-AGPO-HT framework, BGC taxonomy, scoring logic, and indicator formulations are proprietary intellectual property of Grace-Alice Evans / Auracelle AI Governance Labs. Contributions that modify the mathematical framework, indicator weights, or scoring architecture require prior approval from the PI.

## What you can contribute

- Bug fixes and browser compatibility improvements
- UI/UX improvements that do not alter research mechanics
- Documentation, scenario pack content, and research notes (in `docs/`)
- New scenario domain packs (submit as a proposal via issue first)
- Accessibility improvements
- Performance optimisations

## How to contribute

1. **Open an issue first** — describe what you want to change and why before writing code. This avoids wasted effort if the change conflicts with research design constraints.
2. **Fork the repository** and create a feature branch from `main`.
3. Keep changes focused. One logical change per pull request.
4. If you modify any simulation mechanics, include:
   - Clear rationale for the change
   - Any implications for measurement validity or research reproducibility
   - An example session demonstrating the change works as expected
5. Open a Pull Request against `main` with a clear description.

## Style guidelines

- **No build step** — this repository is intentionally a single-file HTML application. Do not introduce npm, bundlers, or compiled dependencies.
- **Vanilla JS** — prefer small, readable vanilla JavaScript additions. Do not introduce frameworks.
- **IP protection** — do not expose E-AGPO-HT formula weights, BGC/NOF taxonomy specifics, or stratum labels in public-facing code or documentation.
- **Test in Chrome and Firefox** before submitting.

## Research integrity

If a proposed change would affect the validity, reproducibility, or comparability of session data across the doctoral study, it will not be accepted without formal review. The instrument is a live research tool — changes to scoring logic mid-study would compromise data integrity.

## Contact

PI: Grace-Alice Evans
Supervisor: Dr. John Curry, Bath Spa University
