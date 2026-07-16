# Notes & Tasks

> Open Privacy · v0.1 · July 2026 · Poorvith M P  
> Category ID: `12-notes`  
> Replaces: Google Keep / Evernote defaults

---

## Primary recommendation

| Field | Value |
|---|---|
| **Name** | Joplin |
| **Website** | https://joplinapp.org |
| **Source / repo** | https://github.com/laurent22/joplin |
| **Open source?** | **Yes** |
| **Local / self-host?** | **Yes** — local notes; sync via your own target |
| **Target audience** | Users who want FOSS notes with optional E2EE sync |
| **Platforms** | Windows · macOS · Linux · Android · iOS |
| **Pricing** | Free (optional Joplin Cloud) |
| **Payment notes** | N/A for local use |

### Why this is the one pick
1. Fully open-source multi-platform notes app.
2. Markdown-friendly and exportable.
3. End-to-end encryption available for sync.
4. Can sync without vendor lock-in (WebDAV, filesystem, etc.).
5. Strong local FOSS default.

### What it does not do
- UX is less “consumer flashy” than some proprietary apps.
- You must choose and secure a sync backend.
- Real-time collab is not Google Docs.

---

## Install guide (primary)

### Download hubs
- https://joplinapp.org/download/

### Windows
1. Download Windows installer from https://joplinapp.org/download/
2. Install and open Joplin.
3. Create a notebook; configure sync under Options → Synchronisation.

### macOS
1. Download macOS build from the download page.
2. Move to Applications and open.
3. Configure sync/encryption as needed.

### Linux
1. Download AppImage/deb/rpm from https://joplinapp.org/download/ or use distro packages if current.
2. Launch Joplin.
3. Set sync target (e.g. Nextcloud WebDAV).

### Android
1. Install Joplin from the store link on joplinapp.org/download.
2. Sign into the same sync target with E2EE password if used.

### iOS
1. Install Joplin from App Store link on the download page.
2. Configure synchronisation to match desktop.

### First-run checklist
1. Enable encryption if using remote sync.
2. Save the encryption password offline.
3. Test create → sync → appear on second device before relying on it.

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| Want hosted E2EE notes with less sync setup | Joplin sync DIY friction | **Standard Notes** | Partial/Yes clients | All major | Don’t switch if you need deep Markdown plugin ecosystem |
| Want pure local plain files only | App database model | **Obsidian** (local vault; proprietary app) or **Logseq** | Varies | Desktop · mobile | Prefer Joplin if you need open sync E2EE defaults |
| Want full self-host web notes suite | Different architecture | **AppFlowy / Affine / Trilium** (pick **AppFlowy** here) | Yes | Desktop · self-host options | Don’t expand scope if simple notes suffice |

### Alternative installs

#### Standard Notes
- https://standardnotes.com — apps for all major platforms

#### Logseq (local FOSS-leaning knowledge base)
- https://logseq.com/downloads

#### AppFlowy
- https://appflowy.com/download

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | Joplin (local) + optional Nextcloud WebDAV |
| **Repo** | https://github.com/laurent22/joplin |
| **What local means** | Notes on device; sync backend you control |
| **Who it’s for** | FOSS-first users |
| **Ops burden** | Low–Medium |
| **When primary still wins** | Primary already is local FOSS |

### Local install
- Install Joplin clients from joplinapp.org/download
- Sync via filesystem/WebDAV/Nextcloud you operate

---

## Quick decision box

```text
Default FOSS notes                   →  Joplin
Hosted E2EE simpler UX               →  Standard Notes
Local graph/outliner                 →  Logseq
```
