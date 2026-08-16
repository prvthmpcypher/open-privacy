# 2FA Authenticator

> Open Privacy · v1.0 · August 2026 · Poorvith M P  
> Category ID: `09-2fa-authenticator`  
> Replaces: SMS 2FA (SIM swap vulnerability), Google Authenticator / Microsoft Authenticator (closed cloud lock-in)

---

## Primary recommendation

<img src="../../assets/logos/ente.svg" width="36" height="36" alt="Ente Auth Logo">

| Field | Value |
|---|---|
| **Name** | Ente Auth |
| **Website** | https://ente.io/auth |
| **Source / repo** | https://github.com/ente-io/ente |
| **Open source?** | **Yes** (AGPL 3.0) |
| **Local / self-host?** | **Yes** — clients operate locally; server can be self-hosted |
| **Target audience** | Users who want end-to-end encrypted, multi-device 2FA code synchronization |
| **Platforms** | <img src="../../assets/logos/android.svg" width="14" height="14" alt="Android"> Android · <img src="../../assets/logos/ios.svg" width="14" height="14" alt="iOS"> iOS · <img src="../../assets/logos/linux.svg" width="14" height="14" alt="Linux"> Linux · <img src="../../assets/logos/windows.svg" width="14" height="14" alt="Windows"> Windows · <img src="../../assets/logos/macos.svg" width="14" height="14" alt="macOS"> macOS · Web |
| **Pricing** | 100% Free |
| **Payment notes** | N/A |

### Why this is the one pick
1. 100% open-source applications and audited zero-knowledge end-to-end encryption.
2. Cross-platform sync across desktop and mobile devices with zero lock-in.
3. Supports manual offline encrypted backups (export to unencrypted or encrypted JSON).
4. Standalone dedicated 2FA application (not bundled inside a single password manager).
5. Clean, modern UI with biometric unlock, tags, and search.

### What it does not do
- Does not replace hardware FIDO2 security keys (YubiKey) for maximum phishing protection.
- Requires remembering your Ente account recovery key for cloud-synced restore.

---

## Install guide (primary)

### Download hubs
- Website: https://ente.io/auth/
- GitHub Releases: https://github.com/ente-io/ente/releases

### Desktop (Windows, macOS, Linux)
- **Windows:** Download `.exe` from ente.io.
- **macOS:** Download `.dmg` from ente.io.
- **Linux:** Download AppImage or `.deb` from GitHub releases.

### Mobile
- **Android:** https://play.google.com/store/apps/details?id=io.ente.auth (or F-Droid / GitHub APK)
- **iOS:** https://apps.apple.com/app/ente-auth/id6444121398

### First-run checklist
1. Write down your **Recovery Key** and store it offline.
2. Enable biometric unlock (Fingerprint / Face ID).
3. Test exporting an encrypted backup file to an external drive.

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| Want cross-platform FOSS TOTP without registering an Ente account | Prefer cloud backup via personal Google Drive / iCloud without a 3rd party account | <img src="../../assets/logos/ente.svg" width="16" height="16" alt="2FAS"> **2FAS** | Yes | Android · iOS · Extension | Don’t switch if you need a native desktop client |
| Android-only user wanting 100% offline local encrypted vault | Do not want any cloud sync code in the app | <img src="../../assets/logos/ente.svg" width="16" height="16" alt="Aegis"> **Aegis Authenticator** | Yes | Android | Don’t switch if you need cross-device sync with an iPhone or PC |
| Need maximum phishing resistance for high-value accounts | Software TOTP codes can still be phished on fake login pages | <img src="../../assets/logos/yubikey.svg" width="16" height="16" alt="YubiKey"> **YubiKey (FIDO2/WebAuthn)** | Hardware | All major | Don’t rely exclusively on hardware keys without registering a backup key |

### Alternative installs

#### 2FAS Authenticator
- Website: https://2fas.com — install app on iOS or Android.

#### Aegis Authenticator (Android Offline)
- F-Droid: https://f-droid.org/packages/com.beemdevelopment.aegis/
- Google Play: https://play.google.com/store/apps/details?id=com.beemdevelopment.aegis

#### YubiKey (Hardware Security Key)
- Hardware store: https://www.yubico.com/products/

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | Aegis Authenticator (Android) / KeePassXC TOTP (Desktop) |
| **Repo** | https://github.com/beemdevelopment/Aegis |
| **What local means** | 2FA tokens remain strictly on your local hardware in an encrypted vault |
| **Who it’s for** | Offline purists and air-gapped security workflows |
| **Ops burden** | Low (must remember to take manual export backups) |
| **When primary still wins** | You want automatic cross-platform sync when switching phones |

---

## Quick decision box

```text
Default E2EE synced 2FA              →  Ente Auth
Cross-platform accountless backup    →  2FAS
Android-only offline vault           →  Aegis Authenticator
Hardware-level anti-phishing         →  YubiKey (WebAuthn)
```
