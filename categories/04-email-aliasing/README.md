# Email Aliasing

> Open Privacy · v0.1 · July 2026 · Poorvith M P  
> Category ID: `04-email-aliasing`  
> Replaces: Using one real inbox address on every website

---

## Primary recommendation

| Field | Value |
|---|---|
| **Name** | SimpleLogin |
| **Website** | https://simplelogin.io |
| **Source / repo** | https://github.com/simple-login/app |
| **Open source?** | **Yes** (AGPL) — self-hostable; hosted service available |
| **Local / self-host?** | **Yes** |
| **Target audience** | Anyone reducing spam, breaches, and cross-site email correlation |
| **Platforms** | Web · browser extensions · mobile apps · self-host |
| **Pricing** | Free tier + paid |
| **Payment notes** | Card on hosted service |

### Why this is the one pick
1. Purpose-built aliasing with open-source server.
2. Unique addresses per site are easy.
3. Browser extensions speed signups.
4. Can self-host later without changing the model.
5. Strong identity-hygiene tool alongside a private mailbox.

### What it does not do
- Still forwards to a real mailbox you must secure.
- Hosted free tiers have limits.
- Aliases do not encrypt the destination provider.

---

## Install guide (primary)

### Download hubs
- https://simplelogin.io
- Docs: https://simplelogin.io/docs/

### Windows
1. Create a SimpleLogin account at https://simplelogin.io
2. Connect forwarding to your real mailbox (Proton Mail recommended).
3. Install the browser extension from SimpleLogin’s extension links.
4. Create an alias and test receive/reply.

### macOS
1. Same account setup as Windows.
2. Install browser extension for your browser.
3. Optional: install mobile apps for on-the-go aliases.

### Linux
1. Use web app + Firefox/Chromium extension.
2. For self-host, follow https://github.com/simple-login/app on a Linux VPS.

### Android
1. Install SimpleLogin Android app via links on https://simplelogin.io
2. Sign in → create alias → use share sheet on signups.

### iOS
1. Install SimpleLogin iOS app from App Store (link from simplelogin.io).
2. Enable share/autofill permissions if prompted.
3. Generate a new alias before each signup.

### First-run checklist
1. Stop using your root address on new sites.
2. Enable 2FA on SimpleLogin and the destination mailbox.
3. Name aliases by site for easy disable-later.

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| Already deep in Proton ecosystem | Prefer fewer vendors | **Proton Pass hide-my-email** | Partial | Proton apps | Don’t fragment if SimpleLogin already works |
| Want alternative hosted FOSS aliasing vendor | Preference/pricing | **addy.io** | Yes | Web · self-host | Don’t migrate without exporting alias map |
| Cannot rely on third-party SaaS | Hosted alias provider is another party | **Self-hosted SimpleLogin** | Yes | Linux server | Don’t self-host without backups |

### Alternative installs

#### Proton Pass hide-my-email
- https://proton.me/pass — create hide-my-email aliases in Proton Pass apps/web

#### addy.io
- Hosted: https://addy.io
- Self-host via project docs/GitHub

#### Self-hosted SimpleLogin
- https://github.com/simple-login/app — Docker/self-host README
- Configure DNS as required

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | Self-hosted SimpleLogin |
| **Repo** | https://github.com/simple-login/app |
| **What local means** | You run the aliasing service |
| **Who it’s for** | Users with a domain and VPS |
| **Ops burden** | Medium–High |
| **When primary still wins** | Hosted SimpleLogin is fine |

### Local install
- **Linux:** SimpleLogin self-hosting README/Docker
- **Clients:** same web/extensions against your domain

---

## Quick decision box

```text
Default aliasing                     →  SimpleLogin
Proton-only stack                    →  Proton hide-my-email
Alt hosted FOSS                      →  addy.io
Full control                         →  Self-hosted SimpleLogin
```
