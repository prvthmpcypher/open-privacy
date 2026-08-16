# Password Manager

> Open Privacy · v0.2 · August 2026 · Poorvith M P  
> Category ID: `08-password-manager`  
> Replaces: Reusing passwords across sites, browser password stores, plaintext notes

---

## Primary recommendation

<img src="../../assets/logos/bitwarden.svg" width="36" height="36" alt="Bitwarden Logo">

| Field | Value |
|---|---|
| **Name** | Bitwarden |
| **Website** | https://bitwarden.com |
| **Source / repo** | https://github.com/bitwarden |
| **Open source?** | **Yes** (GPL 3.0 Clients / AGPL 3.0 Server) |
| **Local / self-host?** | **Yes** — official server or lightweight Vaultwarden |
| **Target audience** | Everyone who needs secure, synced passwords across devices |
| **Platforms** | Windows · macOS · Linux · Android · iOS · Browser Extensions · CLI |
| **Pricing** | Free tier (unlimited passwords & devices); Premium $10/year for TOTP/passkeys |
| **Payment notes** | Card, PayPal, Bitcoin |

### Why this is the one pick
1. 100% open-source client applications and audited zero-knowledge encryption (AES-256 / XChaCha20-Poly1305).
2. Unlimited passwords synced across unlimited devices on the free tier.
3. Cross-platform support covering desktop, mobile, all major browser extensions, and a powerful CLI.
4. Passkey storage and hardware security key support (FIDO2/WebAuthn).
5. Easy migration path to self-hosted Vaultwarden with zero client changes.

### What it does not do
- Free tier does not include integrated TOTP authenticator generation (upgrade to Premium or use `09-2fa-authenticator`).
- Cloud sync relies on Bitwarden infrastructure unless you self-host Vaultwarden.

---

## Install guide (primary)

### Account Setup & Desktop
1. Create a free account at https://bitwarden.com.
2. Choose a strong, memorable Master Password (never lose this).
3. Download apps from https://bitwarden.com/download/:
   - **Windows:** `winget install Bitwarden.Bitwarden` or direct installer.
   - **macOS:** `brew install --cask bitwarden` or Mac App Store.
   - **Linux:** `flatpak install com.bitwarden.desktop` or `.deb` / `.rpm` / AppImage.

### Browser Extensions
- Install official extension from Firefox Add-ons, Chrome Web Store, or Safari.
- Enable auto-fill on page load in extension settings.

### Mobile
- **Android:** https://play.google.com/store/apps/details?id=com.x8bit.bitwarden (or F-Droid / GitHub APK)
- **iOS:** https://apps.apple.com/app/bitwarden-password-manager/id1137397744

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| Want 100% offline encrypted file storage without any cloud | Prefer keeping your vault exclusively in a `.kdbx` file | **KeePassXC** | Yes | Desktop · Mobile (via KeePassDX) | Don’t switch if you need effortless automatic sync across devices |
| Want self-hosted backend compatible with Bitwarden apps | Official Bitwarden server is heavy (MSSQL) | **Vaultwarden** | Yes | Linux / Docker | Don’t self-host unless you manage your own automated encrypted backups |
| Already deep in the Proton ecosystem | Prefer keeping email, drive, and passwords in one account | **Proton Pass** | Yes | All major | Don’t switch if you need enterprise organization sharing |

### Alternative installs

#### KeePassXC
- Website: https://keepassxc.org/download/

#### Vaultwarden (Lightweight Rust Backend)
- Docker Compose:
```yaml
version: '3'
services:
  vaultwarden:
    image: vaultwarden/server:latest
    container_name: vaultwarden
    restart: always
    environment:
      - WEBSOCKET_ENABLED=true
    volumes:
      - ./vw-data:/data
    ports:
      - 8080:80
```

#### Proton Pass
- Website: https://proton.me/pass/download

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | KeePassXC / Vaultwarden |
| **Repo** | https://github.com/keepassxreboot/keepassxc |
| **What local means** | Vault file resides on your local disk or self-hosted Docker server |
| **Who it’s for** | Offline purists and self-hosters |
| **Ops burden** | Low (KeePassXC) / Medium (Vaultwarden) |
| **When primary still wins** | You want seamless, zero-maintenance cross-device auto-fill |

---

## Quick decision box

```text
Default cloud password manager       →  Bitwarden
Offline encrypted .kdbx file         →  KeePassXC
Self-hosted lightweight backend      →  Vaultwarden
Proton-integrated vault              →  Proton Pass
```
