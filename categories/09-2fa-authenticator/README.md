# 2FA Authenticator

> Open Privacy · v0.1 · July 2026 · Poorvith M P  
> Category ID: `09-2fa-authenticator`  
> Replaces: SMS 2FA; closed authenticator apps that trap exports

---

## Primary recommendation

| Field | Value |
|---|---|
| **Name** | Ente Auth |
| **Website** | https://ente.io/auth |
| **Source / repo** | https://github.com/ente-io/ente |
| **Open source?** | **Yes** |
| **Local / self-host?** | **Partial** — open apps; cloud optional for sync |
| **Target audience** | Users who need cross-platform TOTP with export freedom |
| **Platforms** | Android · iOS · desktop/web options per Ente docs |
| **Pricing** | Free authenticator product (see ente.io for any sync tiers) |
| **Payment notes** | N/A for local use; cloud features per Ente |

### Why this is the one pick
1. Open-source authenticator with modern UX.
2. Cross-platform story stronger than Android-only apps.
3. Export-friendly design vs lock-in authenticators.
4. Actively maintained.
5. Better default than SMS 2FA.

### What it does not do
- 2FA apps are not a password manager.
- You must back up recovery codes for each account.
- Cloud sync is optional—understand the tradeoff.

---

## Install guide (primary)

### Download hubs
- https://ente.io/auth
- Mobile stores linked from that page; desktop/web per Ente Auth docs

### Windows
1. Open https://ente.io/auth and download the desktop/web client options listed.
2. Install/open Ente Auth.
3. Add TOTP secrets by scanning QR codes from account security pages.

### macOS
1. Download macOS/iOS companion options from https://ente.io/auth
2. Install and add accounts via QR/manual entry.

### Linux
1. Use the Linux build or web/desktop option published on https://ente.io/auth
2. Install via the provided package/AppImage as listed.
3. Import/export only through official export features.

### Android
1. Install Ente Auth from the Play Store / F-Droid link provided on ente.io/auth.
2. Grant camera permission only when scanning QR codes.
3. Enable app lock (device biometrics/PIN).

### iOS
1. Install Ente Auth from the App Store link on ente.io/auth.
2. Add TOTP accounts.
3. Enable iOS app lock features available in the app.

### First-run checklist
1. Export/backup codes using official export.
2. Store recovery codes offline for critical accounts.
3. Prefer TOTP/hardware keys over SMS 2FA wherever possible.

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| Android-only user who wants fully offline FOSS vault | Prefer local-only Android UX | **Aegis** | Yes | Android | Don’t pick Aegis if you need first-class iOS |
| Want hardware-backed 2FA instead of software TOTP | Software TOTP can be phished in some flows | **YubiKey (WebAuthn/FIDO2)** | Hardware + open standards | USB/NFC + major OS | Don’t buy keys if sites you use lack WebAuthn |
| Already standardized on Proton stack | Fewer apps preference | **Proton Authenticator** | Yes/Partial per Proton | Mobile | Don’t migrate codes casually without export |

### Alternative installs

#### Aegis
- https://getaegis.app/ — Android (Play Store / F-Droid)
- **iOS / desktop:** not the primary Aegis platform

#### YubiKey (WebAuthn/FIDO2)
- Buy from Yubico; set up via https://www.yubico.com/support/download/
- Register keys in each account’s security settings

#### Proton Authenticator
- https://proton.me/authenticator — install official mobile apps

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | Aegis (Android offline) or KeePassXC TOTP |
| **Repo** | https://github.com/beemdevelopment/Aegis |
| **What local means** | TOTP secrets stored only on device/local DB |
| **Who it’s for** | Users who refuse cloud sync for 2FA |
| **Ops burden** | Low |
| **When primary still wins** | You need easy multi-device encrypted sync UX |

### Local install
- **Android:** Aegis from getaegis.app
- **Desktop TOTP:** KeePassXC TOTP feature with local `.kdbx`

---

## Quick decision box

```text
Default authenticator                →  Ente Auth
Android offline FOSS                 →  Aegis
Hardware keys                        →  YubiKey
Proton ecosystem                     →  Proton Authenticator
```
