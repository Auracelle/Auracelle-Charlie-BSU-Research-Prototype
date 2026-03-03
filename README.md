# Auracelle Charlie — BSU Research Instrument (v3 HTML Prototype)

This repository packages the **single-file interactive HTML prototype** for *Auracelle Charlie* (Bath Spa University doctoral research instrument).

## Quick start
### Option A — open locally
Open `index.html` in a modern browser.

### Option B — serve locally (recommended)
Some browsers restrict local file APIs when opening HTML directly. Serve the folder:

```bash
python -m http.server 8080
```

Then open:
- `http://localhost:8080`

## GitHub Pages
This repo includes a GitHub Actions workflow to deploy to GitHub Pages on push to `main`.
After enabling Pages in repo settings (Build and deployment → GitHub Actions), the site will publish automatically.

## Repository contents
- `index.html` — the prototype (no build step)
- `.github/` — issue/PR templates + Pages deploy workflow
- `docs/` — ethics + facilitator notes
- `CITATION.cff` — citation metadata for academic reuse

## Responsible use
This is a **research/training prototype** for tabletop-style governance stress-testing.
Outputs are not forecasts and should not be used as operational decisions without appropriate oversight.

## License
See [LICENSE](LICENSE).

## Contact
PI: **Grace-Alice Evans**
