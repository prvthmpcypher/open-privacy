# Android App Store

> Open Privacy · v0.2 · August 2026 · Poorvith M P  
> Category ID: `20-app-store-android`  
> Replaces: Google Play Store (mandatory Google account, telemetry, tracking IDs)

---

## Primary recommendation

<img src="../../assets/logos/fdroid.svg" width="36" height="36" alt="F-Droid Logo">

| Field | Value |
|---|---|
| **Name** | F-Droid |
| **Website** | https://f-droid.org |
| **Source / repo** | https://gitlab.com/fdroid |
| **Open source?** | **Yes** (GPL 3.0) |
| **Local / self-host?** | **Yes** — client and repository can be self-hosted |
| **Target audience** | Android users seeking free, open-source applications built directly from source |
| **Platforms** | Android |
| **Pricing** | 100% Free |
| **Payment notes** | N/A |

### Why this is the one pick
1. Verified catalogue of Free and Open Source Software (FOSS) built directly from verified source repositories.
2. Anti-Feature warnings: clearly flags if an app contains tracking, ads, non-free network services, or upstream telemetry.
3. Zero account required to browse, download, and update applications.
4. Supports adding third-party custom repositories (e.g. Guardian Project, Bitwarden, SimpleX).
5. Standard first stop for all privacy-oriented and de-Googled Android devices.

### What it does not do
- Does not host proprietary commercial apps (WhatsApp, banking apps, Uber).
- App update releases can lag upstream developer GitHub tags due to F-Droid server build queues.

---

## Install guide (primary)

### Installation
1. On your Android device, navigate to https://f-droid.org.
2. Download and install `F-Droid.apk`.
3. Open F-Droid and allow it to initialize and update its repository index.

### First-run checklist
1. In F-Droid settings, configure automatic background update checks over Wi-Fi.
2. Enable third-party repositories for your preferred apps if needed.

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| Need proprietary apps only published on Google Play (banking, transit) | F-Droid only carries open-source software | **Aurora Store** (Google Play Front-end) | Yes | Android | Don’t use Aurora Store with your personal Google account (use anonymous session) |
| Want instant APK updates directly from developer GitHub / GitLab releases | F-Droid build servers can take days to compile new releases | **Obtainium** | Yes | Android | Don’t switch if you prefer centralized curation over managing individual release feeds |
| Want modern signed APK updates with cryptographic developer signatures | F-Droid signs packages with its own server build key | **Accrescent** | Yes | Android | Don’t switch if your required apps are only indexed on standard F-Droid |

### Alternative installs

#### Aurora Store (Anonymous Google Play Client)
- Download: https://auroraoss.com or via F-Droid.

#### Obtainium (Direct Release Updater)
- GitHub: https://github.com/ImranR98/Obtainium/releases

#### Accrescent (Modern Secure Android App Store)
- Website: https://accrescent.app

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | F-Droid / Custom F-Droid Server / Obtainium |
| **Repo** | https://gitlab.com/fdroid/fdroidserver |
| **What local means** | Client connects directly to decentralized repository mirrors or Git tags |
| **Who it’s for** | Android privacy users |
| **Ops burden** | Low |
| **When primary still wins** | Primary provides the most established repository catalog |

---

## Quick decision box

```text
Default FOSS Android app catalogue  →  F-Droid
Anonymous Play Store app downloads   →  Aurora Store
Instant GitHub/GitLab direct updates →  Obtainium
Next-gen signed APK store            →  Accrescent
```
