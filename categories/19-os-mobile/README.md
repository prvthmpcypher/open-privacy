# Mobile OS Privacy Path

> Open Privacy · v0.2 · August 2026 · Poorvith M P  
> Category ID: `19-os-mobile`  
> Replaces: Stock Android (Google Play Services tracking, ad ID, location history), iOS defaults

---

## Primary recommendation

<img src="../../assets/logos/grapheneos.svg" width="36" height="36" alt="GrapheneOS Logo">

| Field | Value |
|---|---|
| **Name** | GrapheneOS |
| **Website** | https://grapheneos.org |
| **Source / repo** | https://github.com/GrapheneOS |
| **Open source?** | **Yes** (MIT / GPL / AOSP) |
| **Local / self-host?** | **Yes** — runs entirely on your mobile device |
| **Target audience** | Mobile phone users who want the gold standard in smartphone security, sandboxing, and de-Googling |
| **Platforms** | Google Pixel smartphones (Pixel 6, 7, 8, 9 and newer generations) |
| **Pricing** | 100% Free (Open Source non-profit) |
| **Payment notes** | N/A |

### Why this is the one pick
1. Hardened Android Open Source Project (AOSP) with a memory-safe allocator (`hardened_malloc`), kernel hardening, and exploit mitigations.
2. Sandboxed Google Play Services: runs Google Play Services as a standard unprivileged app with zero special OS permissions.
3. Granular privacy toggles: Network and Sensor permissions per app; Storage Scopes (allow apps access to specific folders without full storage access).
4. WebUSB browser-based installer makes flashing as simple as clicking a button in Brave/Chromium.
5. Preserves verified boot and complete hardware-backed keystore encryption.

### What it does not do
- Runs officially only on Google Pixel hardware (due to requirements for strong security chips, verified boot with custom keys, and prompt kernel security updates).
- Some banking apps that enforce strict Google Play Integrity (Strong Integrity) may restrict certain features.

---

## Install guide (primary)

### Prerequisites
- A supported Google Pixel device (Pixel 6/6a/7/7a/8/8a/9/9 Pro/Fold).
- A computer running Linux, macOS, or Windows.
- A WebUSB-compatible browser (Brave, Chrome, Edge).

### Web Installer Steps
1. On your Pixel: Enable **Developer Options** → Enable **OEM Unlocking**.
2. Connect your Pixel to your PC via USB cable.
3. Navigate to https://grapheneos.org/install/web.
4. Click **Unlock bootloader** and confirm on your phone screen.
5. Click **Download release** → Click **Flash release**.
6. Click **Lock bootloader** to restore verified boot hardware security.
7. Reboot your phone into GrapheneOS.

### First-run checklist
1. Open **Apps** (GrapheneOS app manager) to install Sandboxed Google Play Services only if specific proprietary apps require push notifications.
2. Install **F-Droid** or **Obtainium** for open-source apps (see `20-app-store-android`).
3. Set up **Storage Scopes** for messaging apps rather than granting broad media permissions.

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| Do not own a supported Pixel device (using Fairphone, Motorola, or SHIFTphone) | GrapheneOS hardware support is Pixel-exclusive | **CalyxOS** | Yes | Fairphone · select Motorola · SHIFTphone 8 · Pixels | Don’t choose CalyxOS on a Pixel where GrapheneOS provides strictly superior security |
| Must remain on an iPhone for personal/work ecosystem | Hardware constraints prevent moving to Android | **iOS + Lockdown Mode + Privacy Hardening** | No | iPhone (iOS) | Don’t expect true de-Googling/de-Apple on a closed iOS operating system |
| Older legacy Android device unsupported by GrapheneOS or CalyxOS | Older hardware lacks modern hardware security chips | **LineageOS for microG** | Yes | Broad device catalog | Don’t use legacy LineageOS on devices without security patch maintenance unless unavoidable |

### Alternative installs

#### CalyxOS
- Website & supported devices: https://calyxos.org/install/

#### LineageOS for microG
- Website: https://lineage.microg.org

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | GrapheneOS / CalyxOS |
| **Repo** | https://github.com/GrapheneOS/platform_manifest |
| **What local means** | Complete open-source operating system running on physical device hardware |
| **Who it’s for** | Anyone wanting a private smartphone |
| **Ops burden** | Low (automatic OTA system updates) |
| **When primary still wins** | GrapheneOS delivers industry-leading mobile sandbox and hardware hardening |

---

## Quick decision box

```text
Default mobile privacy OS (Pixel)   →  GrapheneOS
Non-Pixel modern hardware (Fairphone)→  CalyxOS
Legacy device de-Googling            →  LineageOS for microG
iOS device hardening                 →  iOS Lockdown Mode
```
