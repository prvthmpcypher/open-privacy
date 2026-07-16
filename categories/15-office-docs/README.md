# Office / Docs

> Open Privacy · v0.1 · July 2026 · Poorvith M P  
> Category ID: `15-office-docs`  
> Replaces: Google Docs / Microsoft 365 cloud defaults

---

## Primary recommendation

| Field | Value |
|---|---|
| **Name** | LibreOffice |
| **Website** | https://www.libreoffice.org |
| **Source / repo** | https://www.libreoffice.org/about-us/source-code/ |
| **Open source?** | **Yes** (MPL) |
| **Local / self-host?** | **Yes** — fully local desktop suite |
| **Target audience** | Users who want offline office docs without cloud lock-in |
| **Platforms** | Windows · macOS · Linux |
| **Pricing** | Free |
| **Payment notes** | N/A |

### Why this is the one pick
1. Mature full office suite, fully open source.
2. Works offline by default.
3. Broad file compatibility for daily documents.
4. No account required.
5. Standard privacy-preserving replacement for cloud suites.

### What it does not do
- Real-time multiplayer collab is weaker than Google Docs.
- Mobile editing is not the main strength.
- Complex corporate macros may differ from Microsoft Office.

---

## Install guide (primary)

### Download hubs
- https://www.libreoffice.org/download/download-libreoffice/

### Windows
1. Download Windows installer from the LibreOffice download page.
2. Run installer → next through defaults (or customize components).
3. Open Writer/Calc/Impress and set as default for ODF if desired.

### macOS
1. Download macOS DMG from LibreOffice download page.
2. Drag LibreOffice to Applications.
3. First launch may require Gatekeeper approval.

### Linux
1. Prefer distro packages: e.g. `sudo apt install libreoffice` or use official packages from libreoffice.org.
2. Launch from app menu.
3. Install language packs if needed.

### Android
1. LibreOffice is desktop-first; for mobile viewing use Collabora Office / compatible apps if needed.
2. Prefer editing on desktop for complex docs.
3. Avoid random “LibreOffice” mobile clones.

### iOS
1. No full official LibreOffice iOS suite as primary workflow.
2. Use desktop LibreOffice + private cloud sync for files.
3. For mobile collab catch path, use CryptPad in browser.

### First-run checklist
1. Default to ODF formats for archival.
2. Export PDF when sharing outward.
3. Disable auto-fetch of untrusted remote resources in documents when possible.

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| Need browser-based collaborative editing | LibreOffice is desktop-local | **CryptPad** | Yes | Web · self-host | Don’t use if offline desktop suite is enough |
| Need Microsoft-format fidelity in enterprises | Complex DOCX/XLSX edge cases | **OnlyOffice** | Yes (community) | Desktop · self-host · web | Don’t switch if ODF workflow works |
| Need mobile-first notes/docs lightly | Suite is heavy | **Joplin** (see notes category) | Yes | All major | Don’t replace full office suite with notes app for formal documents |

### Alternative installs

#### CryptPad
- Hosted or self-host: https://cryptpad.org
- Self-host docs on CryptPad project site/GitHub

#### OnlyOffice
- https://www.onlyoffice.com/download-desktop.aspx
- Docs server self-host options on onlyoffice.com

#### Joplin
- https://joplinapp.org/download/

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | LibreOffice (already local) |
| **Repo** | https://www.libreoffice.org/about-us/source-code/ |
| **What local means** | Documents stay on your machine unless you sync them |
| **Who it’s for** | Everyone who can run a desktop OS |
| **Ops burden** | Low |
| **When primary still wins** | Primary is already local FOSS |

### Local install
- Use libreoffice.org download page for Windows/macOS/Linux

---

## Quick decision box

```text
Default offline office suite         →  LibreOffice
Private browser collab               →  CryptPad
MS-format + self-host collab         →  OnlyOffice
```
