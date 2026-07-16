# Photo Storage

> Open Privacy · v0.1 · July 2026 · Poorvith M P  
> Category ID: `16-photo-storage`  
> Replaces: Google Photos defaults

---

## Primary recommendation

| Field | Value |
|---|---|
| **Name** | ente Photos |
| **Website** | https://ente.io |
| **Source / repo** | https://github.com/ente-io/ente |
| **Open source?** | **Yes** |
| **Local / self-host?** | **Yes** — self-host possible; hosted available |
| **Target audience** | Users wanting end-to-end encrypted photo backup |
| **Platforms** | Windows · macOS · Linux · Android · iOS · Web |
| **Pricing** | Free trial/paid plans on hosted; self-host costs are your infra |
| **Payment notes** | Card on hosted ente |

### Why this is the one pick
1. E2EE photo backup with open-source clients.
2. Multi-platform apps including mobile auto-backup flows.
3. Stronger privacy model than Google Photos scanning defaults.
4. Self-host path exists for advanced users.
5. Practical everyday replacement for photo libraries.

### What it does not do
- Free unlimited cloud like some big-tech promos.
- Self-hosting is operational work.
- Sharing UX differs from Google Photos social features.

---

## Install guide (primary)

### Download hubs
- https://ente.io
- Apps: links from ente.io for desktop/mobile

### Windows
1. Create an ente account at https://ente.io (or prepare self-host endpoint).
2. Download Windows app from ente.io.
3. Install, sign in, select folders to back up.

### macOS
1. Download macOS app from ente.io.
2. Install to Applications; grant Photos/Files permissions as needed.
3. Enable backup for chosen libraries.

### Linux
1. Download Linux build from ente.io / GitHub releases as published.
2. Install/run the client.
3. Configure backup targets.

### Android
1. Install ente Photos from store links on ente.io.
2. Sign in → enable auto-backup for Camera/DCIM.
3. Restrict battery optimizations if backups pause.

### iOS
1. Install from App Store link on ente.io.
2. Allow Photos access.
3. Enable backup; test a few uploads on Wi‑Fi.

### First-run checklist
1. Save recovery key offline.
2. Enable 2FA on the account.
3. Confirm a known photo appears on a second device before trusting migration.

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| Want fully self-hosted Google-Photos-like server | Prefer your NAS/VPS only | **Immich** | Yes | Self-host + apps | Don’t self-host without storage/backup plan |
| Want encrypt-any-folder rather than photo app | Different workflow | **Cryptomator + any sync** | Yes | Desktop · mobile | Don’t add complexity if ente already fits |
| Already on Proton stack | Fewer vendors | **Proton Drive** (photos as files) | Partial | All major | Don’t expect full photo timeline features |

### Alternative installs

#### Immich
- https://immich.app/docs/install/requirements — Docker on Linux server; mobile apps from Immich docs

#### Cryptomator + any sync
- https://cryptomator.org/downloads/

#### Proton Drive
- https://proton.me/drive/download

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | Immich |
| **Repo** | https://github.com/immich-app/immich |
| **What local means** | Photo library server on your hardware |
| **Who it’s for** | Homelab users with disk capacity |
| **Ops burden** | Medium–High |
| **When primary still wins** | You want zero server maintenance |

### Local install
- Follow https://immich.app docs for Docker Compose on Linux
- Install official mobile/desktop clients pointed at your server

---

## Quick decision box

```text
Default E2EE photos                  →  ente Photos
Self-host photo server               →  Immich
Encrypt folders on any cloud         →  Cryptomator
Proton-only files                    →  Proton Drive
```
