# Android App Store

> Open Privacy · v0.1 · July 2026 · Poorvith M P  
> Category ID: `20-app-store-android`  
> Replaces: Google Play Store as sole app source

---

## Primary recommendation

| Field | Value |
|---|---|
| **Name** | F-Droid |
| **Website** | https://f-droid.org |
| **Source / repo** | https://gitlab.com/fdroid |
| **Open source?** | **Yes** |
| **Local / self-host?** | **Yes** — client + repos; can add your own repo |
| **Target audience** | Android users preferring free/open-source apps |
| **Platforms** | Android |
| **Pricing** | Free |
| **Payment notes** | N/A |

### Why this is the one pick
1. Curated FOSS Android app repository.
2. Transparent build/metadata model.
3. Works well on de-Googled devices.
4. No Google account required.
5. Standard first stop for private Android apps.

### What it does not do
- Not every proprietary app is available.
- Updates can lag upstream releases for some apps.
- iOS has no F-Droid equivalent here.

---

## Install guide (primary)

### Download hubs
- https://f-droid.org
- Official APK: download F-Droid client from f-droid.org only

### Windows
1. Not applicable as an Android store client.
2. Use Android device/emulator for F-Droid.
3. Download the official APK on desktop only to transfer sideload if needed.

### macOS
1. Not applicable as a native client.
2. Transfer official F-Droid APK to Android if sideloading.
3. Prefer downloading F-Droid on-device via browser.

### Linux
1. Not the primary client platform.
2. Optional: tools for repo management are advanced; daily use is on Android.
3. Download official APK to sideload if required.

### Android
1. On your phone browser, open https://f-droid.org
2. Download the official F-Droid APK.
3. Allow install from browser/unknown sources for that one install.
4. Open F-Droid → update repositories → install apps.

### iOS
1. Not supported.
2. Use App Store with privacy-minded app choices instead.
3. See other categories for iOS apps.

### First-run checklist
1. Verify you installed F-Droid from f-droid.org.
2. Enable auto-updates inside F-Droid carefully.
3. Prefer apps with reproducible/open metadata.

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| Need apps only published on Play | Availability | **Aurora Store** (Play front-end) | Yes | Android | Don’t use anonymous Play scraping for highly sensitive accounts without care |
| Want direct GitHub APK updates | F-Droid lag | **Obtainium** | Yes | Android | Don’t enable untrusted sources casually |
| On GrapheneOS and need sandboxed Play | Compatibility | **Sandboxed Google Play (GrapheneOS)** | Partial | GrapheneOS | Don’t add full stock Play Services blindly |

### Alternative installs

#### Aurora Store
- https://auroraoss.com — install via F-Droid or official site instructions

#### Obtainium
- https://github.com/ImranR98/Obtainium — releases APK

#### GrapheneOS sandboxed Play
- Follow GrapheneOS docs for installing sandboxed Play services

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | F-Droid (+ own repos) |
| **Repo** | https://gitlab.com/fdroid |
| **What local means** | FOSS distribution without Google account |
| **Who it’s for** | Android privacy users |
| **Ops burden** | Low |
| **When primary still wins** | Primary is already local FOSS client |

### Local install
- Install F-Droid client from https://f-droid.org on Android

---

## Quick decision box

```text
Default FOSS app source              →  F-Droid
Need Play apps without Play Store UI →  Aurora Store
Track upstream APKs                  →  Obtainium
GrapheneOS Play compat               →  Sandboxed Play
```
