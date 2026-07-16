# Password Manager

> Open Privacy · v0.1 · July 2026 · Poorvith M P  
> Category ID: `08-password-manager`  
> Replaces: Browser-only password saving; reused passwords

---

## Primary recommendation

| Field | Value |
|---|---|
| **Name** | Bitwarden |
| **Website** | https://bitwarden.com |
| **Source / repo** | https://github.com/bitwarden |
| **Open source?** | **Yes** — clients open source; hosted cloud optional |
| **Local / self-host?** | **Yes** via Vaultwarden/official server |
| **Target audience** | Everyone who needs cross-device passwords and passkeys |
| **Platforms** | Windows · macOS · Linux · Android · iOS · Web · extensions |
| **Pricing** | Free tier + paid |
| **Payment notes** | Card on hosted |

### Why this is the one pick
1. Open-source clients with polished multi-platform apps.
2. Easy sync for everyday users.
3. Browser extensions and modern passkey support.
4. Self-host path available later.
5. Strong default across privacy communities.

### What it does not do
- Hosted vault means trusting the provider (mitigate with strong master password + 2FA).
- Losing the master password can mean losing the vault.

---

## Install guide (primary)

### Download hubs
- https://bitwarden.com/download/

### Windows
1. Create an account at https://bitwarden.com
2. Download Windows app from https://bitwarden.com/download/
3. Install browser extension from the same page.
4. Use a strong master password; enable 2FA.

### macOS
1. Download macOS app + browser extension from https://bitwarden.com/download/
2. Sign in; allow autofill permissions if prompted.

### Linux
1. Download package options from https://bitwarden.com/download/
2. Install app + browser extension.
3. Sign in and test autofill.

### Android
1. Install Bitwarden from the store link on the download page.
2. Enable Autofill service → Bitwarden in Android settings.

### iOS
1. Install Bitwarden from the App Store.
2. Settings → Passwords → AutoFill Passwords → enable Bitwarden.

### First-run checklist
1. Create a long unique master password; keep an offline backup of it.
2. Enable 2FA on Bitwarden.
3. Change reused passwords starting with email and banking.

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| Want offline-only encrypted DB file | Bitwarden default is account sync | **KeePassXC** | Yes | Desktop (+ mobile companions) | Don’t pick offline-only if you need seamless phone sync without DIY |
| Want self-host API compatible with Bitwarden clients | Prefer not to use bitwarden.com cloud | **Vaultwarden** | Yes | Linux server + official clients | Don’t self-host without backups |
| Prefer Proton ecosystem passwords | Single-vendor preference | **Proton Pass** | Partial | All major | Don’t migrate without an export plan |

### Alternative installs

#### KeePassXC
- https://keepassxc.org/download/ for Linux/Windows/macOS
- Mobile: KeePassDX (Android) / KeePassium or Strongbox (iOS) — evaluate each

#### Vaultwarden
- https://github.com/dani-garcia/vaultwarden — Docker on Linux; point Bitwarden clients to your URL

#### Proton Pass
- https://proton.me/pass/download — install official apps per OS

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | KeePassXC or Vaultwarden |
| **Repo** | https://github.com/keepassxreboot/keepassxc · https://github.com/dani-garcia/vaultwarden |
| **What local means** | Local DB file or self-hosted Bitwarden-compatible server |
| **Who it’s for** | Users who refuse third-party vault hosting |
| **Ops burden** | Low (KeePassXC) / Medium (Vaultwarden) |
| **When primary still wins** | You want easiest multi-device sync |

### Local install
- **KeePassXC:** keepassxc.org/download
- **Vaultwarden:** Docker compose per project wiki

---

## Quick decision box

```text
Default password manager             →  Bitwarden
Offline DB file                      →  KeePassXC
Self-host Bitwarden clients          →  Vaultwarden
Proton ecosystem                     →  Proton Pass
```
