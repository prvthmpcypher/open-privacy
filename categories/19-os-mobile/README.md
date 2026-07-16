# Mobile OS Privacy Path

> Open Privacy · v0.1 · July 2026 · Poorvith M P  
> Category ID: `19-os-mobile`  
> Replaces: Stock Android / iOS defaults without hardening

---

## Primary recommendation

| Field | Value |
|---|---|
| **Name** | GrapheneOS |
| **Website** | https://grapheneos.org |
| **Source / repo** | https://github.com/GrapheneOS |
| **Open source?** | **Yes** |
| **Local / self-host?** | **Yes** — OS on your phone |
| **Target audience** | Users with supported Pixel hardware who want a hardened Android path |
| **Platforms** | Supported Google Pixel devices (see official device list) |
| **Pricing** | Free software; hardware cost is yours |
| **Payment notes** | Buy phones from trusted retailers |

### Why this is the one pick
1. Strong security/privacy-focused Android hard fork.
2. Clear official install documentation.
3. Sandboxed Google Play compatibility options without full stock Android trust model.
4. Actively maintained releases.
5. Best-in-class mobile privacy path for supported devices.

### What it does not do
- Not available for all phone brands.
- Banking apps can still break depending on attestation/Play integrity.
- Not an iPhone replacement path.

---

## Install guide (primary)

### Download hubs
- https://grapheneos.org/install/
- Web installer: follow current official method on grapheneos.org

### Windows
1. Use the official GrapheneOS web install guide from a Chromium-based browser as documented.
2. Install required USB drivers only from links GrapheneOS documents.
3. Unlock bootloader → install → relock as instructed on grapheneos.org/install/

### macOS
1. Follow the same official web install flow GrapheneOS publishes.
2. Use a supported browser and cable.
3. Do not use third-party “one click root” tools.

### Linux
1. Official install works well from Linux desktops.
2. Follow https://grapheneos.org/install/ step-by-step (CLI or web installer as currently recommended).
3. Verify factory images/signatures per docs.

### Android
1. You are installing onto Android hardware (Pixel).
2. Backup data first; unlock bootloader wipes the device.
3. After boot, set strong lock screen and avoid unnecessary Google account login.

### iOS
1. GrapheneOS is not for iPhone.
2. iOS users should use stock iOS hardening + privacy apps from this library.
3. See catch alternative for staying on iOS.

### First-run checklist
1. Set strong PIN/passphrase.
2. Prefer Auditor / hardened network defaults GrapheneOS documents.
3. Install apps via careful sources (see `20-app-store-android`).

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| No supported Pixel device | Hardware requirement | **CalyxOS** — also supports Fairphone, select Motorola models, and SHIFTphone 8 | Yes | Android (Pixel · Fairphone · select Motorola · SHIFTphone 8) | Don’t flash unofficial builds for unsupported devices |
| Must stay on iPhone | Ecosystem/hardware | **iOS + Lockdown Mode (when needed) + privacy apps** | No | iOS | Still use Signal/Bitwarden/etc from this library |
| Need easier de-Google without Graphene learning curve | Complexity | **LineageOS for microG** — broader device support, lighter learning curve, weaker hardening than GrapheneOS | Yes | Specific devices | Don’t sacrifice security updates for convenience |

### Alternative installs

#### CalyxOS
- https://calyxos.org/install/ — pick your device model, then use the Web Installer where offered (Pixel and Motorola); other supported devices use the device flasher tool (Windows/Linux)

#### iOS stay path
- Settings hardening; Lockdown Mode for high risk; minimize App Tracking

#### LineageOS for microG
- https://lineage.microg.org — only for officially supported devices

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | GrapheneOS |
| **Repo** | https://github.com/GrapheneOS |
| **What local means** | OS image on your phone |
| **Who it’s for** | Pixel owners serious about mobile privacy |
| **Ops burden** | Medium (install once; update regularly) |
| **When primary still wins** | Primary is already local FOSS OS |

### Local install
- Only https://grapheneos.org/install/

---

## Quick decision box

```text
Supported Pixel                      →  GrapheneOS
iPhone user                          →  Harden iOS + private apps
Pixel/Fairphone/Motorola/SHIFTphone 8 outside GrapheneOS support → CalyxOS
Other officially supported device, want lighter setup → LineageOS for microG
```
