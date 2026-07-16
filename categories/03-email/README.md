# Email Provider

> Open Privacy · v0.1 · July 2026 · Poorvith M P  
> Category ID: `03-email`  
> Replaces: Gmail, Outlook.com defaults

---

## Primary recommendation

| Field | Value |
|---|---|
| **Name** | Proton Mail |
| **Website** | https://proton.me/mail |
| **Source / repo** | https://github.com/ProtonMail |
| **Open source?** | **Partial** — clients largely open; hosted service |
| **Local / self-host?** | **No** as primary SaaS |
| **Target audience** | Everyday users wanting encrypted-friendly mail without running servers |
| **Platforms** | Web · Windows · macOS · Linux · Android · iOS |
| **Pricing** | Free tier + paid plans |
| **Payment notes** | Card; check proton.me for regional options |

### Why this is the one pick
1. Mature encrypted-mail product with apps on all major platforms.
2. Usable free tier for testing a full switch.
3. Clear multi-product ecosystem (calendar/drive/pass) if you expand later.
4. Lower ops burden than self-hosted mail.
5. Strong everyday alternative to Gmail.

### What it does not do
- Email metadata realities still apply.
- Free tier has limits.
- Not the same as running your own mailserver.

---

## Install guide (primary)

### Download hubs
- Web: https://proton.me/mail
- Apps: https://proton.me/mail/download

### Windows
1. Create an account at https://proton.me/mail
2. Download **Proton Mail** desktop app from https://proton.me/mail/download (or use web).
3. Install and sign in.
4. Optional: Proton Bridge for Outlook/Thunderbird (plan limits may apply).

### macOS
1. Create account at https://proton.me/mail
2. Download macOS app from https://proton.me/mail/download
3. Open the download and move the app to Applications.
4. Sign in.

### Linux
1. Create account at https://proton.me/mail
2. Download Linux package from https://proton.me/mail/download
3. Install via your package tool, or use https://mail.proton.me in a browser.

### Android
1. Install **Proton Mail** from the store link on https://proton.me/mail/download
2. Sign in or create account.
3. Adjust battery optimizations if background sync fails.

### iOS
1. Install **Proton Mail** from the App Store (link via download page).
2. Sign in → allow notifications if desired.

### First-run checklist
1. Enable 2FA on the Proton account.
2. Set recovery methods you control.
3. Migrate important account recovery emails gradually.
4. Import old mail only if you accept storage/privacy tradeoffs.

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| Prefer a different encrypted mail vendor | Vendor preference / feature fit | **Tuta** | Partial (clients open) | Web · apps | Don’t switch mid-migration without a contacts/alias plan |
| Need full self-hosted mail you control | Proton is hosted SaaS | **Stalwart or Mailcow** | Yes | Linux server | Don’t self-host if you cannot handle DNS, spam, and updates |
| Need classic IMAP on a tight budget | Bridge/IMAP features may require paid tiers | **Self-host mail** | Yes | Linux server | Don’t pick solely on IMAP if web/app UX is enough |

### Alternative installs

#### Tuta
- https://tuta.com — create account
- Apps: download section on tuta.com for Windows/macOS/Linux/Android/iOS

#### Stalwart or Mailcow
- Stalwart: https://stalw.art/docs/install/
- Mailcow: https://docs.mailcow.email/getstarted/install/
- Configure DNS (SPF/DKIM/DMARC) then use any mail client

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | Mailcow or Stalwart (self-hosted mail) |
| **Repo** | https://github.com/mailcow/mailcow-dockerized · https://github.com/stalwartlabs/mail-server |
| **What local means** | You run SMTP/IMAP on your infrastructure |
| **Who it’s for** | Admins comfortable with DNS and mail ops |
| **Ops burden** | High |
| **When primary still wins** | You want reliable mail without server ops |

### Local install
- **Linux server:** follow Mailcow or Stalwart official install docs
- **Clients on all OSes:** standard IMAP/SMTP or webmail after DNS works

---

## Quick decision box

```text
Default private mail                 →  Proton Mail
Alternative hosted encrypted mail    →  Tuta
Full control self-host               →  Mailcow / Stalwart
```
