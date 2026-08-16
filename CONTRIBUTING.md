# Contributing to Open Privacy

> **Open Privacy** · v1.0 · August 2026 · Maintainer: **Poorvith M P**

Thanks for wanting to improve Open Privacy. I built this library to be opinionated and decision-first: exactly **one primary tool** per category, **one alternative per concrete catch**, and a **local open-source path** when one exists.

Here is how to contribute without wasting your time.

---

## Category Page Rules

When editing or adding to any file under `categories/`:

1. **Keep the fixed section order**:
   - Header with metadata & official colored logo
   - Primary Recommendation Table
   - Why this is the one pick (5 points)
   - What it does not do (3 points)
   - Install Guide (numbered OS steps & copy-paste commands)
   - Catches Table (exactly one alternative per row)
   - Alternative Installs
   - Local Open-Source Path
   - Quick Decision Box
2. **Official Install Steps Only**: Copy commands directly from upstream documentation (e.g. official package repos, keyrings, or vendor guides). Do not invent custom install scripts.
3. **No Affiliate Links or Sponsorships**: Any PR adding referral links or paid placement will be closed immediately.
4. **Logos**: Use official colored SVG/PNG logos from upstream projects or simple-icons. Store them in `assets/logos/`. Never submit AI-generated logo artwork.
5. **No Threat-Model Essays**: Keep descriptions concise and practical. Explain what the tool does and where it falls short.

---

## How to Propose a Tool Change

If you believe a primary tool should be replaced (e.g. an upstream project was abandoned, bought out, or breached):

1. Open a GitHub Issue first and provide evidence (CVE, commit history, corporate announcement, or upstream license change).
2. If we agree on the replacement, open a PR that:
   - Updates the primary table and why/limits sections.
   - Updates install steps for Linux, Windows, macOS, Android, and iOS where applicable.
   - Rewrites the catch table to map to real catches of the *new* primary tool.
   - Updates [`INDEX.md`](INDEX.md), [`llms.txt`](llms.txt), and [`CHANGELOG.md`](CHANGELOG.md).

---

## Submitting Screenshots or Assets

When adding UI screenshots or assets:
- Store them under `categories/<id>/assets/`.
- Use descriptive filenames (e.g. `brave-shields-panel.png`).
- Keep file sizes under 500 KB (prefer WebP or compressed PNG).
- Never include personal emails, account numbers, or private credentials in screenshots.

---

## Code of Conduct & License

By contributing, you agree that your work will be licensed under the project's [MIT License](LICENSE) and that you will follow the [Code of Conduct](CODE_OF_CONDUCT.md).
