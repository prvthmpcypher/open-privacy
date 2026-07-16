# Contributing to Open Privacy

Maintainer: **Poorvith M P** · **v0.1** · July 2026

## What this repo is

Each category under `categories/` recommends **one primary tool**, **one alternative per catch** of that primary, and a **local open-source path** when applicable.

## Category page rules

- Keep the fixed section order (see any existing category `README.md`).
- Do **not** add contributor callouts on category pages.
- Do **not** add threat-model sections in v0.1.
- Do **not** add per-OS “Source:” citation lines under install steps.
- Install steps must match the tool’s **official** install documentation.
- Keep catch tables to **one alternative per catch row**.

## Updating install steps

1. Open the vendor’s official download/install page.
2. Replace steps only when upstream changed.
3. Prefer copy-pasteable commands and numbered UI steps.
4. If a platform is unsupported, write `Not supported` and one short reason.

## Images (screenshots)

When adding images later:

1. Store under `categories/<id>/assets/` (create the folder if needed).
2. Use descriptive names: `windows-installer.png`, `android-play-listing.png`.
3. Prefer PNG or WebP; keep each file under ~500 KB when possible.
4. Add Markdown as: `![Short description](assets/filename.png)`.
5. Do not include personal data, email addresses, or account IDs in screenshots.
6. Do not add decorative screenshots that do not help installation.
7. Alt text must describe the UI action (e.g. “Windows UAC prompt for Brave setup”).

## Proposing a primary change

Open a PR that:

1. Updates the primary table and why/limits sections.
2. Rewrites install steps for all five OSes (Linux, Windows, macOS, Android, iOS) as applicable.
3. Rebuilds the catch table so alternatives still map to real catches of the **new** primary.
4. Updates local FOSS path if needed.
5. Adds a CHANGELOG entry under Unreleased or the next version.

## License

By contributing, you agree your contributions are licensed under the MIT License (Copyright Poorvith M P).
