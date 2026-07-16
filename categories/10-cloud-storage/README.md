# Cloud Storage

> Open Privacy · v0.1 · July 2026 · Poorvith M P  
> Category ID: `10-cloud-storage`  
> Replaces: Google Drive / Dropbox defaults

---

## Primary recommendation

| Field | Value |
|---|---|
| **Name** | Proton Drive |
| **Website** | https://proton.me/drive |
| **Source / repo** | https://proton.me/drive |
| **Open source?** | **Partial** — Proton clients often open; service hosted |
| **Local / self-host?** | **No** as primary SaaS |
| **Target audience** | Users wanting encrypted cloud files without running servers |
| **Platforms** | Web · Windows · macOS · Linux · Android · iOS |
| **Pricing** | Free tier + paid |
| **Payment notes** | Card via Proton |

### Why this is the one pick
1. Encrypted cloud storage with official multi-platform apps.
2. Fits users already considering Proton Mail.
3. Lower ops than Nextcloud.
4. Practical sharing features for everyday files.
5. Clear alternative to Google Drive.

### What it does not do
- Free storage is limited.
- Not a full NAS replacement.
- Metadata/account identity still exist at the provider.

---

## Install guide (primary)

### Download hubs
- https://proton.me/drive
- Apps: https://proton.me/drive/download (or apps hub on proton.me)

### Windows
1. Create/login Proton account.
2. Download Proton Drive Windows app from Proton’s download page.
3. Install, sign in, choose sync folders.

### macOS
1. Download macOS app from Proton Drive download page.
2. Install to Applications; sign in; grant folder permissions.

### Linux
1. Use web app at Proton Drive and/or Linux client if listed on download page.
2. For package installs, follow the exact artifact Proton publishes for Linux.

### Android
1. Install Proton Drive from store links on proton.me.
2. Sign in; enable only needed permissions.

### iOS
1. Install Proton Drive from App Store link on proton.me.
2. Sign in; enable Files app integration if offered.

### First-run checklist
1. Enable account 2FA.
2. Don’t sync your entire home folder on day one—start selective.
3. For highly sensitive archives, consider client-side containers (Cryptomator) too.

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| Need full self-hosted cloud with web UI | Proton Drive is SaaS | **Nextcloud** | Yes | Self-host + apps | Don’t self-host if you cannot maintain updates/backups |
| Want zero cloud account—device-to-device only | Cloud provider still in the middle | **Syncthing** | Yes | Desktop · Android (iOS limited) | Don’t use Syncthing if you need web sharing links for non-tech people |
| Want encrypted layer on any cloud including Google Drive | Keep existing storage but encrypt content | **Cryptomator** | Yes | Desktop · mobile | Don’t add Cryptomator if you can leave big-tech storage entirely |

### Alternative installs

#### Nextcloud
- Server: https://docs.nextcloud.com/server/latest/admin_manual/installation/
- Clients: https://nextcloud.com/install/#install-clients

#### Syncthing
- https://syncthing.net/downloads/ for Windows/macOS/Linux/Android

#### Cryptomator
- https://cryptomator.org/downloads/

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | Nextcloud or Syncthing |
| **Repo** | https://github.com/nextcloud/server · https://github.com/syncthing/syncthing |
| **What local means** | Self-hosted cloud or P2P sync without a storage vendor |
| **Who it’s for** | Homelab users |
| **Ops burden** | Medium–High (Nextcloud) / Medium (Syncthing) |
| **When primary still wins** | You want zero server maintenance |

### Local install
- **Nextcloud:** official server install docs + desktop/mobile clients
- **Syncthing:** syncthing.net/downloads on each device; share folders

---

## Quick decision box

```text
Default encrypted cloud              →  Proton Drive
Self-host cloud                      →  Nextcloud
P2P no cloud vendor                  →  Syncthing
Encrypt any cloud                    →  Cryptomator
```
