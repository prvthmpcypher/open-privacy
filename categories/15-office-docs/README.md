# Office / Docs

> Open Privacy · v0.2 · August 2026 · Poorvith M P  
> Category ID: `15-office-docs`  
> Replaces: Google Docs & Microsoft 365 cloud telemetry

---

## Primary recommendation

<img src="../../assets/logos/libreoffice.svg" width="36" height="36" alt="LibreOffice Logo">

| Field | Value |
|---|---|
| **Name** | LibreOffice |
| **Website** | https://www.libreoffice.org |
| **Source / repo** | https://www.libreoffice.org/about-us/source-code/ |
| **Open source?** | **Yes** (MPL 2.0) |
| **Local / self-host?** | **Yes** — runs 100% offline on your computer |
| **Target audience** | Everyday users who want full-featured word processing, spreadsheets, and presentations without cloud telemetry |
| **Platforms** | Linux · Windows · macOS |
| **Pricing** | 100% Free |
| **Payment notes** | N/A |

### Why this is the one pick
1. Full-featured, mature desktop office suite (Writer, Calc, Impress, Draw, Math).
2. Works 100% offline with zero cloud phone-home or AI data harvesting.
3. Native OpenDocument Format (ODF: `.odt`, `.ods`, `.odp`) standards along with Microsoft Office (`.docx`, `.xlsx`, `.pptx`) compatibility.
4. No account creation, subscription fees, or license keys required.
5. Backed by The Document Foundation non-profit.

### What it does not do
- Does not offer native real-time multi-user browser collaboration (use CryptPad for that).
- Mobile editing experience is minimal compared to desktop.
- Complex enterprise VBA macros may require adjustments.

---

## Install guide (primary)

### Windows & macOS
- **Windows:** `winget install TheDocumentFoundation.LibreOffice` (or download MSI from https://www.libreoffice.org/download/download-libreoffice/).
- **macOS:** `brew install --cask libreoffice` (or download DMG from https://www.libreoffice.org/download/download-libreoffice/).

### Linux
- **Debian / Ubuntu / Mint:** `sudo apt install libreoffice`
- **Fedora / RHEL:** `sudo dnf install libreoffice`
- **Arch Linux:** `sudo pacman -S libreoffice-fresh`
- **Flatpak:** `flatpak install flathub org.libreoffice.LibreOffice`

### First-run checklist
1. Open Writer → Tools → Options → LibreOffice → Security → Check **Remove personal info on saving**.
2. Set default document format to ODF or standard DOCX/XLSX depending on your collaborators.

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| Need real-time browser collaboration with zero-knowledge encryption | LibreOffice is an offline desktop program | **CryptPad** | Yes | Web · Docker | Don’t switch if you need complex desktop desktop publishing tools |
| Require pixel-perfect Microsoft Office layout compatibility | Extreme DOCX/XLSX formatting quirks | **OnlyOffice** | Yes (Community) | Desktop · Web · Self-Host | Don’t switch if standard ODF workflows work for your team |
| Just need quick notes and checklists rather than formal office files | Full office suite is heavy for quick thoughts | **Joplin** (see `12-notes`) | Yes | All major | Don’t replace office suites when formal documents are required |

### Alternative installs

#### CryptPad (E2EE Collaborative Suite)
- Website: https://cryptpad.org
- Self-host via Docker: https://github.com/cryptpad/cryptpad

#### OnlyOffice Desktop Editors
- Website: https://www.onlyoffice.com/download-desktop.aspx

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | LibreOffice (Native Desktop Suite) |
| **Repo** | https://github.com/LibreOffice/core |
| **What local means** | Files remain strictly on your local disk unless you explicitly share them |
| **Who it’s for** | Everyone writing documents, managing spreadsheets, or creating slide decks |
| **Ops burden** | Low |
| **When primary still wins** | Primary is already the open-source local standard |

---

## Quick decision box

```text
Default offline office suite         →  LibreOffice
E2EE real-time browser collaboration →  CryptPad
High Microsoft Office compatibility  →  OnlyOffice
Lightweight notes and markdown       →  Joplin
```
