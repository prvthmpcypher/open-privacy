# Mobile OS Privacy Path

> Open Privacy · v0.2 · August 2026 · Poorvith M P  
> Category ID: `19-os-mobile`  
> Replaces: Stock Android (Google Play Services tracking, advertising ID, continuous background location), iOS defaults

---

## Primary recommendation

<img src="../../assets/logos/grapheneos.svg" width="36" height="36" alt="GrapheneOS Logo">

| Field | Value |
|---|---|
| **Name** | GrapheneOS |
| **Website** | https://grapheneos.org |
| **Source / repo** | https://github.com/GrapheneOS |
| **Open source?** | **Yes** (MIT / GPL / AOSP) |
| **Local / self-host?** | **Yes** — runs entirely on your mobile device hardware |
| **Target audience** | Mobile users who want the gold standard in smartphone security, sandboxing, and de-Googling |
| **Platforms** | Google Pixel smartphones (Pixel 6, 6a, 7, 7a, 8, 8a, 9, 9 Pro, Fold) |
| **Pricing** | 100% Free (Open Source non-profit) |
| **Payment notes** | N/A |

### Why this is the one pick
1. Hardened Android Open Source Project (AOSP) with a memory-safe allocator (`hardened_malloc`), kernel hardening, and zero OEM bloatware.
2. Sandboxed Google Play Services: runs Google Play Services as standard unprivileged apps with zero special OS-level capabilities.
3. Granular privacy toggles: Network and Sensor permissions per app; Storage Scopes (allow apps access only to selected folders without full media access).
4. WebUSB browser installer makes flashing as simple as clicking a button in Brave or Chromium.
5. Preserves verified boot and full hardware-backed keystore encryption.

### What it does not do
- Runs officially only on Google Pixel hardware (due to requirements for custom key verified boot, robust secure elements, and rapid kernel patch availability).
- Certain banking apps that enforce strict hardware attestation (`MEETS_STRONG_INTEGRITY`) may refuse to run.

---

## Install guide (primary)

### Prerequisites
- A supported Google Pixel device.
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
1. Open **Apps** (GrapheneOS app manager) to install Sandboxed Google Play Services only if proprietary apps require push notifications.
2. Install **F-Droid** or **Obtainium** for open-source apps (see `20-app-store-android`).
3. Set up **Storage Scopes** for messaging apps rather than granting broad media permissions.

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| Do not own a supported Pixel device (using Fairphone, Motorola, or SHIFTphone) | GrapheneOS hardware support is Pixel-exclusive | <img src="../../assets/logos/grapheneos.svg" width="16" height="16" alt="CalyxOS"> **CalyxOS** | Yes | Fairphone · select Motorola · SHIFTphone 8 · Pixels | Don’t choose CalyxOS on a Pixel where GrapheneOS provides strictly superior security |
| Must remain on an iPhone for personal/work ecosystem | Hardware constraints prevent moving to Android | <img src="../../assets/logos/apple.svg" width="16" height="16" alt="Apple iOS"> **iOS + Lockdown Mode + Privacy Hardening** | No | iPhone (iOS) | Don’t expect true de-Googling/de-Apple on a closed iOS operating system |
| Older legacy Android device unsupported by GrapheneOS or CalyxOS | Older hardware lacks modern hardware security chips | <img src="../../assets/logos/android.svg" width="16" height="16" alt="LineageOS"> **LineageOS for microG** | Yes | Broad device catalog | Don’t use legacy LineageOS on devices without security patch maintenance unless unavoidable |

### Alternative installs

#### CalyxOS
- Website & supported devices: https://calyxos.org/install/

#### LineageOS for microG
- Website: https://lineage.microg.org

---

## Real-world gotcha: The Banking & Play Integrity reality

Sandboxed Google Play on GrapheneOS passes `MEETS_BASIC_INTEGRITY` and `MEETS_DEVICE_INTEGRITY`. 90% of banking, ride-sharing, and transit apps run without issue.

However, a small subset of strict financial apps (particularly apps enforcing `MEETS_STRONG_INTEGRITY` or aggressive root-detection scanners) will refuse to run on custom OS builds regardless of how secure the sandbox is.

**What to do before wiping your daily driver:**
1. Check user reports on the [GrapheneOS Banking Apps directory](https://privsec.dev/posts/android/banking-applications-compatibility-with-grapheneos/).
2. For stubborn apps, use their mobile web browser portal or keep a secondary cheap stock device for authentication.

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
