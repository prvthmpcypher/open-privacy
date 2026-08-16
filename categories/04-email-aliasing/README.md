# Email Aliasing

> Open Privacy · v0.2 · August 2026 · Poorvith M P  
> Category ID: `04-email-aliasing`  
> Replaces: Giving your real primary email to every newsletter, website, and app

---

## Primary recommendation

<img src="../../assets/logos/simplelogin.svg" width="36" height="36" alt="SimpleLogin Logo">

| Field | Value |
|---|---|
| **Name** | SimpleLogin |
| **Website** | https://simplelogin.io |
| **Source / repo** | https://github.com/simple-login/app |
| **Open source?** | **Yes** (AGPL 3.0) |
| **Local / self-host?** | **Yes** — self-hostable via Docker Compose |
| **Target audience** | Users who want to protect their real email address from spam, data breaches, and cross-site tracking |
| **Platforms** | Web · Browser Extensions · Android · iOS |
| **Pricing** | Free tier (10 aliases); Premium included with Proton Unlimited |
| **Payment notes** | Card, PayPal, Crypto |

### Why this is the one pick
1. Open-source backend and client extensions.
2. Supports PGP encryption of forwarded emails so relay servers cannot read forwarded payloads.
3. Deep integration into Proton ecosystem (Proton Pass alias generator).
4. Enables reverse-aliasing: you can reply to forwarded emails without exposing your real address.
5. Self-hostable with standard Docker Compose recipes.

### What it does not do
- Does not replace your primary inbox; it acts as a forwarding proxy shield in front of it.
- Free tier is limited to 10 active aliases without custom domain support.

---

## Install guide (primary)

### Setup & Extensions
1. Register at https://simplelogin.io (or connect via your Proton account).
2. Install the browser extension:
   - **Firefox Add-on:** https://addons.mozilla.org/en-US/firefox/addon/simplelogin/
   - **Chrome / Brave Extension:** https://chromewebstore.google.com/detail/simplelogin/dphilobhebphkdjbpfohgikllaljmgbn
3. Click the extension icon on any signup form to generate a unique forwarding alias.

### Mobile Apps
- **Android:** https://play.google.com/store/apps/details?id=io.simplelogin.android (or F-Droid / GitHub APK)
- **iOS:** https://apps.apple.com/app/simplelogin-protect-email/id1494051017

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| Want an independent non-Proton FOSS aliasing service | Prefer independent hosting outside the Proton umbrella | **addy.io** (formerly AnonAddy) | Yes | Web · Extension · Self-Host | Don’t switch if you already use Proton Unlimited |
| Already using Proton Pass and want integrated aliases | No need for a separate SimpleLogin web login | **Proton Pass built-in aliases** | Yes | All major | Don’t switch if you need complex regex routing or advanced alias sharing rules |
| Cannot trust third-party relay servers | Forwarding metadata passes through external infrastructure | **Self-hosted SimpleLogin** | Yes | Linux VPS | Don’t self-host unless you manage your own mail domain and SPF/DKIM records |

### Alternative installs

#### addy.io
- Website: https://addy.io — create account → install browser extension.

#### Self-Hosted SimpleLogin
- Follow official Docker guide: https://github.com/simple-login/app#self-hosting

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | SimpleLogin (Self-Hosted) |
| **Repo** | https://github.com/simple-login/app |
| **What local means** | Aliasing and forwarding service hosted on your own server |
| **Who it’s for** | Users with their own domain and VPS infrastructure |
| **Ops burden** | Medium |
| **When primary still wins** | You want zero maintenance and instant alias creation |

---

## Quick decision box

```text
Default email aliasing               →  SimpleLogin
Independent FOSS alternative         →  addy.io
Built into password manager          →  Proton Pass
Self-hosted aliasing                 →  SimpleLogin Docker
```
