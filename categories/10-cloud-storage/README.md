# Cloud Storage

> Open Privacy · v0.2 · August 2026 · Poorvith M P  
> Category ID: `10-cloud-storage`  
> Replaces: Google Drive (content scanning, unencrypted at rest from Google), Dropbox / OneDrive

---

## Primary recommendation

<img src="../../assets/logos/protondrive.svg" width="36" height="36" alt="Proton Drive Logo">

| Field | Value |
|---|---|
| **Name** | Proton Drive |
| **Website** | https://proton.me/drive |
| **Source / repo** | https://github.com/ProtonMail |
| **Open source?** | **Yes** (Client apps and cryptographic libraries) |
| **Local / self-host?** | **No** as a hosted cloud; Nextcloud / Syncthing for self-host |
| **Target audience** | Everyday users who want automatic end-to-end encrypted file sync and sharing |
| **Platforms** | Windows · macOS · Android · iOS · Web |
| **Pricing** | Free tier (up to 5 GB with tasks); paid tiers for 200 GB+ |
| **Payment notes** | Card, PayPal, Bitcoin |

### Why this is the one pick
1. End-to-end encryption by default; Proton cannot read your stored files, filenames, or folder structures.
2. Official desktop sync clients for Windows and macOS with on-demand file hydration.
3. Secure, password-protected file sharing links with expiration dates.
4. Integrated document editor with zero-access encryption (Proton Docs).
5. Protected under Swiss privacy laws.

### What it does not do
- Free storage (5 GB) is modest compared to ad-subsidized Big Tech cloud offerings.
- Linux sync client is community-driven or CLI/web-based.
- Does not offer advanced server-side indexing or search on file contents (since files are encrypted client-side).

---

## Install guide (primary)

### Web & Desktop
1. Create an account at https://proton.me/drive.
2. Download desktop sync apps:
   - **Windows:** https://proton.me/drive/download (or `winget install Proton.ProtonDrive`)
   - **macOS:** https://proton.me/drive/download (or Mac App Store)

### Mobile
- **Android:** https://play.google.com/store/apps/details?id=me.proton.android.drive
- **iOS:** https://apps.apple.com/app/proton-drive-cloud-storage/id1509667826

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| Need a complete self-hosted private cloud on your server | Proton Drive is a managed commercial service | **Nextcloud** | Yes | Linux / Docker | Don’t self-host unless you can manage disk storage, backups, and updates |
| Want continuous folder sync between your devices with zero cloud | Do not want third-party servers storing any data | **Syncthing** | Yes | All major | Don’t switch if you need public web link sharing for friends |
| Want to encrypt files on your existing Google Drive or OneDrive | Already paying for cheap cloud storage | **Cryptomator** | Yes | All major | Don’t switch if you want a clean unified web interface |

### Alternative installs

#### Nextcloud (Self-Hosted Cloud)
- Official Docker installation: https://github.com/nextcloud/docker

#### Syncthing (P2P Device Sync)
- Download clients: https://syncthing.net/downloads/

#### Cryptomator (Client-Side Vault Encryption)
- Download app: https://cryptomator.org/downloads/

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | Nextcloud / Syncthing |
| **Repo** | https://github.com/syncthing/syncthing |
| **What local means** | File synchronization occurs directly between your devices or private server |
| **Who it’s for** | Homelab operators and privacy-first sync workflows |
| **Ops burden** | Low (Syncthing) / High (Nextcloud) |
| **When primary still wins** | You want simple cloud access from any browser without managing hardware |

---

## Quick decision box

```text
Default E2EE cloud storage           →  Proton Drive
Self-hosted full cloud suite         →  Nextcloud
P2P device-to-device zero-cloud sync →  Syncthing
Client-side encryption on any cloud  →  Cryptomator
```
