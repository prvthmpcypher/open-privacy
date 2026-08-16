# Notes & Tasks

> Open Privacy · v0.2 · August 2026 · Poorvith M P  
> Category ID: `12-notes`  
> Replaces: Apple Notes, Google Keep, Notion / Evernote (unencrypted cloud databases)

---

## Primary recommendation

<img src="../../assets/logos/joplin.svg" width="36" height="36" alt="Joplin Logo">

| Field | Value |
|---|---|
| **Name** | Joplin |
| **Website** | https://joplinapp.org |
| **Source / repo** | https://github.com/laurent22/joplin |
| **Open source?** | **Yes** (AGPL 3.0) |
| **Local / self-host?** | **Yes** — local SQLite database + your choice of encrypted sync target |
| **Target audience** | Everyday users who want full control over their notes, checklists, and attachments |
| **Platforms** | Linux · Windows · macOS · Android · iOS · CLI |
| **Pricing** | 100% Free (optional paid Joplin Cloud) |
| **Payment notes** | N/A for self-hosted/local use |

### Why this is the one pick
1. 100% open-source applications and local-first architecture; notes work completely offline.
2. Supports end-to-end encryption across any sync target (Dropbox, OneDrive, WebDAV, Nextcloud, S3, or Joplin Cloud).
3. Markdown-based formatting with rich media attachments, checklists, and web clipping.
4. Active plugin ecosystem and comprehensive export options (raw Markdown + frontmatter, PDF, JEX).
5. Fast search across encrypted local SQLite databases.

### What it does not do
- Multi-user real-time collaborative editing is limited compared to Google Docs or Notion.
- Mobile UI is functional but lacks some visual flash of proprietary note apps.

---

## Install guide (primary)

### Desktop (Windows, macOS, Linux)
- **Windows:** `winget install Joplin.Joplin` or download installer from https://joplinapp.org/download/.
- **macOS:** `brew install --cask joplin` or download `.dmg` from https://joplinapp.org/download/.
- **Linux:** Run official update script:
```bash
wget -O - https://raw.githubusercontent.com/laurent22/joplin/dev/Joplin_install_and_update.sh | bash
```

### Mobile
- **Android:** https://play.google.com/store/apps/details?id=net.cozic.joplin (or F-Droid / GitHub APK)
- **iOS:** https://apps.apple.com/app/joplin/id1315579684

### First-run checklist
1. Open **Tools** → **Options** → **Synchronization**.
2. Select your sync target (Nextcloud WebDAV, Dropbox, or local directory).
3. Enable **Encryption** and set a strong master password.

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| Want zero sync setup with hosted 100% FOSS E2EE notes and modern UI | Joplin requires picking a sync target | **Notesnook** | Yes | All major | Don’t switch if you prefer keeping notes strictly in a local SQLite file |
| Want local plaintext `.md` files in folders without a database | Joplin stores notes in a local database | **Obsidian** (proprietary client) or **Logseq** (FOSS) | Partial / Yes | All major | Don’t switch if you want turnkey end-to-end encrypted mobile sync for free |
| Already deep in the Proton ecosystem | Prefer keeping email, drive, and notes under one vendor (Note: Standard Notes acquired by Proton in 2024) | **Standard Notes** | Yes | All major | Don’t switch if you want Joplin’s open plugin ecosystem |

### Alternative installs

#### Notesnook (100% FOSS E2EE Notes)
- Website: https://notesnook.com — register free account → download apps.

#### Obsidian & Logseq (Local Plaintext Vaults)
- Obsidian: https://obsidian.md/download
- Logseq: https://logseq.com

#### Standard Notes
- Website: https://standardnotes.com

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | Joplin (Local DB + WebDAV) / Logseq |
| **Repo** | https://github.com/laurent22/joplin |
| **What local means** | Notes remain in local files/databases on your physical storage |
| **Who it’s for** | Privacy power users and offline writers |
| **Ops burden** | Low |
| **When primary still wins** | Primary is already the open-source local standard |

---

## Quick decision box

```text
Default E2EE markdown notes          →  Joplin
Modern FOSS hosted E2EE suite        →  Notesnook
Local plaintext folder vault         →  Obsidian / Logseq
Proton-aligned notes                 →  Standard Notes
```
