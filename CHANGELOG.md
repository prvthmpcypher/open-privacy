# Changelog

## v1.0.0 — August 2026

- **Official v1.0 Release**: Complete production-ready curated privacy guide covering 25 categories.
- **Real Brand-Colored Logos & OS Badges**: Added 60+ verified vector SVG logos for primary tools, alternatives, and all major operating systems (Linux, Windows, macOS, Android, iOS).
- **AI-SEO & Agent Infrastructure**: Added standardized [`llms.txt`](llms.txt) (llmstxt.org specification) and [`INDEX.md`](INDEX.md) machine-readable tool registry for autonomous agents and LLM search engines.
- **Real-World Edge Cases & Gotchas**: Added deep reality checks covering Chrome Manifest V3, GrapheneOS Play Integrity banking attestation, self-hosted mail deliverability traps, Proton Bridge desktop requirements, and Mullvad port forwarding deprecation.
- **Upstream Documentation Upgrades**:
  - `01-browser`: Updated Brave install commands for Fedora 41+ (`dnf5`) and modern Debian/Ubuntu keyrings.
  - `03-email`: Added Proton official desktop app for Linux/Win/Mac; documented Stalwart Rust mail server.
  - `05-messenger`: Added **SimpleX Chat** (zero user IDs, metadata-free onion routing) as an explicit catch alternative.
  - `08-password-manager`: Added Passkeys guidance and modern Vaultwarden Docker configs.
  - `09-2fa-authenticator`: Added **2FAS** (cross-platform offline/cloud backup) alongside Aegis Authenticator.
  - `11-file-sharing`: Documented OnionShare, Send (`timvisee`), and Magic Wormhole CLI.
  - `12-notes`: Documented Standard Notes' acquisition by Proton and added **Notesnook** (100% FOSS E2EE notes).
  - `17-analytics-selfhost`: Updated Umami Docker Compose with PostgreSQL 16 Alpine.
  - `19-os-mobile`: Verified GrapheneOS WebUSB installer and updated CalyxOS device list (cleaned DivestOS).
  - `20-app-store-android`: Added **Accrescent** and **Obtainium** to the Android app installation paths.
  - `21-browser-extensions`: Clarified Manifest V3 impact: uBlock Origin Lite for Chromium vs full uBO on Firefox/Brave.
  - `24-translation`: Updated Firefox Translations to reflect native built-in browser translation in modern Firefox.
- **Security & Governance**: Added root [`SECURITY.md`](SECURITY.md) vulnerability policy and updated [`CONTRIBUTING.md`](CONTRIBUTING.md) and [`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md).

## v0.1 — July 2026

- Initial public release of **Open Privacy** by Poorvith M P.
- 25 categories with one primary tool each.
- Catch alternatives and local open-source paths.
- Install guides for Linux, Windows, macOS, Android, and iOS where applicable.
- MIT License.
