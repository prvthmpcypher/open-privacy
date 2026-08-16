# Email Provider

> Open Privacy · v0.2 · August 2026 · Poorvith M P  
> Category ID: `03-email`  
> Replaces: Gmail (ad profiling), Outlook / Yahoo

---

## Primary recommendation

<img src="../../assets/logos/protonmail.svg" width="36" height="36" alt="Proton Mail Logo">

| Field | Value |
|---|---|
| **Name** | Proton Mail |
| **Website** | https://proton.me/mail |
| **Source / repo** | https://github.com/ProtonMail |
| **Open source?** | **Yes** (Client apps and cryptography libraries are open source) |
| **Local / self-host?** | **No** as a hosted service; Stalwart / Mailcow for local self-host |
| **Target audience** | Everyday users who want zero-access encrypted email without running a mail server |
| **Platforms** | Web · <img src="../../assets/logos/windows.svg" width="14" height="14" alt="Windows"> Windows · <img src="../../assets/logos/macos.svg" width="14" height="14" alt="macOS"> macOS · <img src="../../assets/logos/linux.svg" width="14" height="14" alt="Linux"> Linux · <img src="../../assets/logos/android.svg" width="14" height="14" alt="Android"> Android · <img src="../../assets/logos/ios.svg" width="14" height="14" alt="iOS"> iOS |
| **Pricing** | Free tier (1 GB storage); paid tiers for custom domains and expanded storage |
| **Payment notes** | Card, PayPal, Bitcoin, Cash |

### Why this is the one pick
1. Zero-access encryption protects your inbox at rest; Proton cannot read your stored emails.
2. End-to-end encryption between Proton users and PGP interoperability with external contacts.
3. Official standalone desktop apps for Windows, macOS, and Linux alongside full mobile apps.
4. Based in Switzerland under Swiss privacy laws outside US/EU 14-Eyes surveillance agreements.
5. Ecosystem integration with Proton Calendar, Drive, and SimpleLogin aliasing.

### What it does not do
- Standard IMAP/SMTP requires Proton Bridge (paid plan) because client-side cryptography handles decryption. **Gotcha**: If you are on the free tier, use the official Proton desktop app instead of trying to configure Thunderbird.
- Free tier has storage limits (1 GB) and a single email address.
- Email headers (subject lines, recipient addresses, timestamps) are not end-to-end encrypted under standard SMTP protocols.

---

## Install guide (primary)

### Web & Desktop
1. Create an account at https://proton.me/mail.
2. Download official desktop apps from https://proton.me/mail/download:
   - **Windows:** Download `.exe` installer.
   - **macOS:** Download `.dmg` installer.
   - **Linux:** Download `.deb` or `.rpm` packages from Proton.

### <img src="../../assets/logos/android.svg" width="18" height="18" alt="Android"> Android
1. Install from Google Play: https://play.google.com/store/apps/details?id=ch.protonmail.android
2. Or download official APK directly from Proton's website or F-Droid APK repos.

### <img src="../../assets/logos/ios.svg" width="18" height="18" alt="iOS"> iOS
1. Install from the App Store: https://apps.apple.com/app/proton-mail-encrypted-email/id979659489

### First-run checklist
1. Save your account recovery phrase / keys in a secure password manager (see `08-password-manager`).
2. Enable 2-Factor Authentication (2FA) immediately (see `09-2fa-authenticator`).
3. Set up email aliasing for daily registrations (see `04-email-aliasing`).

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| Want post-quantum encryption and non-Swiss jurisdiction | Prefer German jurisdiction and Tuta's post-quantum protocol (TutaCrypt) | <img src="../../assets/logos/tuta.svg" width="16" height="16" alt="Tuta"> **Tuta Mail** | Yes | All major | Don’t switch if you depend on PGP or standard desktop IMAP clients |
| Need full self-hosted email on your own domain | Hosted providers still hold encrypted blobs | <img src="../../assets/logos/protonmail.svg" width="16" height="16" alt="Stalwart"> **Stalwart** or Mailcow | Yes | Linux VPS | Don’t self-host mail unless you can maintain DNS, PTR, DKIM, and deliverability |
| Need standard IMAP on a free account | Proton Bridge requires a paid Proton tier | <img src="../../assets/logos/tuta.svg" width="16" height="16" alt="Tuta"> **Tuta Mail** or self-hosted | Yes | All major | Don’t leave Proton if web/desktop client workflow is sufficient |

### Alternative installs

#### Tuta Mail
- https://tuta.com — create account → download desktop/mobile apps.

#### Stalwart (Self-Hosted Mail)
- https://stalw.art — modern all-in-one mail server written in Rust (JMAP, IMAP, SMTP).

#### Mailcow
- https://mailcow.github.io/mailcow-dockerized-docs/ — Dockerized email suite for Linux servers.

---

## Real-world gotcha: The self-hosted deliverability trap

If you decide to self-host with Stalwart or Mailcow, understand the catch: **outbound email deliverability is heavily gatekept**. 

Major providers (Gmail, Microsoft Outlook, Yahoo) frequently discard or spam-folder emails coming from cloud VPS IP ranges (DigitalOcean, Hetzner, Linode) even when your SPF, DKIM, DMARC, and reverse DNS (PTR) records are completely valid. Unless you are willing to warm up an IP address, monitor blacklists, and handle postmaster rejections, stick to hosted zero-access providers like Proton or Tuta for personal correspondence.

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | Stalwart Mail Server / Mailcow |
| **Repo** | https://github.com/stalwartlabs/mail-server |
| **What local means** | Self-hosted mail server on a VPS you own |
| **Who it’s for** | Sysadmins and homelab enthusiasts |
| **Ops burden** | High (IP reputation, SPF/DKIM/DMARC, backup maintenance) |
| **When primary still wins** | You want zero deliverability headaches and guaranteed inbox reliability |

---

## Quick decision box

```text
Default encrypted email             →  Proton Mail
Post-quantum encrypted mail          →  Tuta Mail
Self-hosted modern Rust mail server  →  Stalwart
Dockerized full email suite          →  Mailcow
```
