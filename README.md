# Auracelle Charlie — BSU Research Instrument (Prototype)

This repository contains a **single-file interactive HTML prototype** of the *Auracelle Charlie* doctoral research instrument.

## What this is
Auracelle Charlie is a governance-focused wargaming interface for recording structured turns (rounds/injects/actor moves), generating **After-Action Reviews (AARs)**, and exporting structured session data (JSON/CSV) for research analysis.

## Quick start
### Option A — open locally (simplest)
1. Download this repository.
2. Open `index.html` in a modern browser (Chrome/Edge/Firefox).

### Option B — serve locally (recommended for consistent behavior)
Some browsers restrict local file APIs when opening HTML directly. If anything behaves oddly, serve the folder:

```bash
python -m http.server 8080
```

Then open:
- `http://localhost:8080`

## Files
- `index.html` — the prototype application (no build step)
- `.github/` — issue/PR templates + GitHub Pages workflow
- `docs/` — lightweight documentation (ethics, research notes)
- `CITATION.cff` — citation metadata for academic reuse

## Research / ethics notes
- This prototype is intended for **research and educational demonstration**.
- Do not use it to make operational, legal, or policy decisions without appropriate governance and review.

## License
See [LICENSE](LICENSE).

## Contact
PI: **Grace-Alice Evans**
