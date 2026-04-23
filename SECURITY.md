# Security Policy

## Supported versions

Auracelle Charlie is an academic research prototype. Security support is best-effort and focused on the current release.

| Version | Supported |
|---------|-----------|
| 0.4.x (current) | ✓ Active |
| < 0.4.0 | ✗ No longer maintained |

## Scope

As a single-file client-side HTML application, the primary security considerations are:

- **API key handling** — the Anthropic API key (Tab ⑩) is stored only in browser session memory and never persisted to disk, sent to any server other than `api.anthropic.com`, or logged. Users should treat their API key as a secret and not share sessions or screenshots that expose it.
- **File attachments** — uploaded documents (Tab ② deliverable attachments) are read locally via FileReader API and stored in browser session memory only. Files are not transmitted anywhere.
- **localStorage** — completed session metadata is stored in browser localStorage. This is local to the user's machine. Do not record sensitive participant data (names, organisations, identifying information) in free-text fields if using shared or institutional machines.
- **No server, no database** — this application has no backend. All data stays in the browser session unless explicitly exported by the user.

## Reporting a vulnerability

If you discover a security issue, please **do not open a public GitHub issue**.

Contact the PI privately:

**Grace-Alice Evans**
Auracelle AI Governance Labs
LinkedIn: https://www.linkedin.com/in/grace-alice-evans-5a9632a3

Include in your report:
- A clear description of the issue
- Steps to reproduce
- Potential impact assessment
- Your suggested fix (if any)

You will receive acknowledgement within 5 working days. Thank you for helping keep the project safe.

## Responsible disclosure

We ask that you give us reasonable time to address a reported vulnerability before public disclosure. We commit to working with you in good faith and will credit responsible disclosures appropriately.
