# Photo Storage

> Open Privacy · v1.0 · August 2026 · Poorvith M P  
> Category ID: `16-photo-storage`  
> Replaces: Google Photos (facial recognition scanning, metadata profiling, ad training)

---

## Primary recommendation

<img src="../../assets/logos/ente.svg" width="36" height="36" alt="Ente Photos Logo">

| Field | Value |
|---|---|
| **Name** | Ente Photos |
| **Website** | https://ente.io/photos |
| **Source / repo** | https://github.com/ente-io/ente |
| **Open source?** | **Yes** (AGPL 3.0) |
| **Local / self-host?** | **Yes** — clients operate locally; server can be self-hosted |
| **Target audience** | Everyday users who want automatic, end-to-end encrypted photo and video backup |
| **Platforms** | <img src="../../assets/logos/android.svg" width="14" height="14" alt="Android"> Android · <img src="../../assets/logos/ios.svg" width="14" height="14" alt="iOS"> iOS · <img src="../../assets/logos/linux.svg" width="14" height="14" alt="Linux"> Linux · <img src="../../assets/logos/windows.svg" width="14" height="14" alt="Windows"> Windows · <img src="../../assets/logos/macos.svg" width="14" height="14" alt="macOS"> macOS · Web |
| **Pricing** | Free trial (1 GB / 5 GB); paid plans from $3/month for 50 GB+ |
| **Payment notes** | Card, PayPal, Crypto |

### Why this is the one pick
1. Audited zero-knowledge end-to-end encryption; your photos and EXIF metadata cannot be scanned by anyone but you.
2. 100% open-source desktop, web, and mobile client applications.
3. Mobile apps feature automatic camera background backup, album sharing, and on-device machine learning (facial clustering and search done client-side).
4. Includes family sharing plans where storage is shared without compromising individual encryption.
5. Automated 3-location cloud replication architecture.

### What it does not do
- Free storage is limited (paid plan needed for large galleries).
- Full self-hosting of the Ente server stack requires configuring S3-compatible storage and microservices.

---

## Install guide (primary)

### Mobile & Desktop
- **Android:** https://play.google.com/store/apps/details?id=io.ente.photos (or F-Droid / GitHub APK)
- **iOS:** https://apps.apple.com/app/ente-photos-encrypted-backup/id1542041765
- **Desktop (Windows, macOS, Linux):** https://ente.io/download/

### First-run checklist
1. Write down your **Recovery Key** and store it offline.
2. Grant camera roll permissions and enable background backup over Wi-Fi.
3. Turn on on-device face recognition in app settings if desired.

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| Want a 100% self-hosted Google Photos replacement on your home server | Ente Photos is primarily a paid hosted service | <img src="../../assets/logos/immich.svg" width="16" height="16" alt="Immich"> **Immich** | Yes (AGPL 3.0) | Linux / Docker · Mobile | Don’t self-host without a multi-disk backup and RAID/NAS strategy |
| Want to encrypt photo folders on existing standard cloud storage | Prefer encrypting raw files rather than a photo-specific app | <img src="../../assets/logos/cryptomator.svg" width="16" height="16" alt="Cryptomator"> **Cryptomator** | Yes | All major | Don’t switch if you want a dedicated photo gallery UI with timeline and search |
| Already using Proton Unlimited for storage | Do not want a separate subscription | **Proton Drive** (Photos tab) | Yes | All major | Don’t expect advanced face clustering or smart photo search |

### Alternative installs

#### Immich (Self-Hosted Photo Server)
- Official Docker Compose setup: https://immich.app/docs/install/docker-compose
```yaml
version: "3.8"
services:
  immich-server:
    image: ghcr.io/immich-app/immich-server:release
    volumes:
      - /path/to/photos:/usr/src/app/upload
    env_file:
      - .env
    ports:
      - 2283:2283
    restart: always
```

#### Cryptomator
- Download: https://cryptomator.org/downloads/

#### Proton Drive Photos
- Mobile app: https://proton.me/drive/download

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | Immich |
| **Repo** | https://github.com/immich-app/immich |
| **What local means** | Self-hosted photo management server running on your homelab or NAS |
| **Who it’s for** | Homelab operators with large local storage arrays |
| **Ops burden** | High (machine learning models, PostgreSQL, disk redundancy) |
| **When primary still wins** | You want turnkey multi-location cloud backup with zero maintenance |

---

## Quick decision box

```text
Default E2EE photo backup            →  Ente Photos
Self-hosted Google Photos clone      →  Immich
Encrypt photo folders anywhere       →  Cryptomator
Proton-integrated photo storage      →  Proton Drive
```
