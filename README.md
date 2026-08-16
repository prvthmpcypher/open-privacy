# Open Privacy — Curated Decision-First Privacy Tools

> Curated digital privacy library by **Poorvith M P**.  
> Version: **v0.2** · Last updated: **August 2026** · License: **MIT**

[![Version](https://img.shields.io/badge/version-v0.2-059669.svg)](CHANGELOG.md)
[![License: MIT](https://img.shields.io/badge/License-MIT-059669.svg)](LICENSE)
[![Security Policy](https://img.shields.io/badge/security-policy-0f172a.svg)](SECURITY.md)
[![Categories](https://img.shields.io/badge/categories-25%20covered-059669.svg)](#categories)
[![Machine Readable](https://img.shields.io/badge/llms.txt-standard-10b981.svg)](llms.txt)

---

## What is Open Privacy?

Open Privacy is a decision-first digital privacy guide. Instead of dumping hundreds of tools into an unorganized catalog, I picked exactly one proven primary tool for each category, one specific alternative for every concrete catch, and a self-hosted open-source path when one exists.

Every recommendation is verified against upstream official documentation and tested for practical usability. No corporate sponsorships, no affiliate links, and no fake hype.

---

## Quick Decision Matrix

```text
Default Daily Browser        →  Brave Browser (Alt: Firefox, Tor)
Private Web Search           →  Brave Search (Alt: SearXNG, Startpage)
Encrypted Email              →  Proton Mail (Alt: Tuta Mail, Stalwart)
Email Aliasing / Masking     →  SimpleLogin (Alt: addy.io, Proton Pass)
Encrypted Messenger          →  Signal (Alt: SimpleX Chat, Session)
No-Logs VPN                  →  Mullvad VPN (Alt: Proton VPN Free, WireGuard)
Private DNS Resolver         →  Quad9 (Alt: NextDNS, Pi-hole, Unbound)
Password Management          →  Bitwarden (Alt: KeePassXC, Vaultwarden)
2FA Authenticator            →  Ente Auth (Alt: 2FAS, Aegis Authenticator)
Encrypted Cloud Storage      →  Proton Drive (Alt: Nextcloud, Syncthing)
Tor / P2P File Sharing       →  OnionShare (Alt: Send, Magic Wormhole)
Private Notes & Tasks        →  Joplin (Alt: Notesnook, Obsidian)
Encrypted Calendar & PIM     →  Proton Calendar (Alt: Nextcloud Calendar)
Offline Maps & Navigation    →  Organic Maps (Alt: OsmAnd)
FOSS Office Suite            →  LibreOffice (Alt: CryptPad, OnlyOffice)
Encrypted Photo Backup       →  Ente Photos (Alt: Immich)
Cookieless Web Analytics     →  Umami (Alt: Plausible, GoatCounter)
Hardened Desktop OS          →  Fedora Workstation (Alt: Qubes OS, Mint)
Hardened Mobile OS           →  GrapheneOS (Alt: CalyxOS, LineageOS)
FOSS Android App Store       →  F-Droid (Alt: Aurora Store, Obtainium)
Tracker & Ad Blocker         →  uBlock Origin (Alt: uBlock Origin Lite)
On-Device Local AI           →  Ollama (Alt: Open WebUI, LM Studio)
Private Video Calls          →  Jitsi Meet (Alt: Signal Calls, Element Call)
On-Device Translation        →  Firefox Translations (Alt: LibreTranslate)
Privacy Payments & Cards     →  Cash & Monero (Alt: Privacy.com)
```

---

## Categories

| ID | Category | Icon | Primary Tool | Top Catch Alternative | Local / Self-Host Path |
|---|---|:---:|---|---|---|
| [`01-browser`](categories/01-browser/README.md) | Web Browser | <img src="assets/logos/brave.svg" width="18" height="18" alt="Brave"> | **Brave Browser** | <img src="assets/logos/tor.svg" width="14" height="14" alt="Tor"> [Tor Browser](categories/01-browser/README.md#tor-browser) (Anonymity) | Firefox (FOSS) |
| [`02-search`](categories/02-search/README.md) | Search Engine | <img src="assets/logos/brave-search.svg" width="18" height="18" alt="Brave Search"> | **Brave Search** | <img src="assets/logos/brave-search.svg" width="14" height="14" alt="SearXNG"> [SearXNG](categories/02-search/README.md#searxng) (Self-Host) | SearXNG |
| [`03-email`](categories/03-email/README.md) | Email Provider | <img src="assets/logos/protonmail.svg" width="18" height="18" alt="Proton Mail"> | **Proton Mail** | <img src="assets/logos/tuta.svg" width="14" height="14" alt="Tuta"> [Tuta Mail](categories/03-email/README.md#tuta) (Post-Quantum) | Stalwart / Mailcow |
| [`04-email-aliasing`](categories/04-email-aliasing/README.md) | Email Aliasing | <img src="assets/logos/simplelogin.svg" width="18" height="18" alt="SimpleLogin"> | **SimpleLogin** | <img src="assets/logos/simplelogin.svg" width="14" height="14" alt="addy.io"> [addy.io](categories/04-email-aliasing/README.md#addyio) (Independent) | SimpleLogin Docker |
| [`05-messenger`](categories/05-messenger/README.md) | Instant Messaging | <img src="assets/logos/signal.svg" width="18" height="18" alt="Signal"> | **Signal** | <img src="assets/logos/simplex.svg" width="14" height="14" alt="SimpleX"> [SimpleX Chat](categories/05-messenger/README.md#simplex-chat) (No User IDs) | Matrix / Element |
| [`06-vpn`](categories/06-vpn/README.md) | VPN | <img src="assets/logos/mullvad.svg" width="18" height="18" alt="Mullvad"> | **Mullvad VPN** | <img src="assets/logos/protonvpn.svg" width="14" height="14" alt="Proton VPN"> [Proton VPN](categories/06-vpn/README.md#proton-vpn-free) (Free Tier) | WireGuard VPS |
| [`07-dns`](categories/07-dns/README.md) | DNS Resolver | <img src="assets/logos/quad9.svg" width="18" height="18" alt="Quad9"> | **Quad9** | <img src="assets/logos/quad9.svg" width="14" height="14" alt="NextDNS"> [NextDNS](categories/07-dns/README.md#nextdns) (Custom Lists) | Unbound / Pi-hole |
| [`08-password-manager`](categories/08-password-manager/README.md) | Password Manager | <img src="assets/logos/bitwarden.svg" width="18" height="18" alt="Bitwarden"> | **Bitwarden** | <img src="assets/logos/keepassxc.svg" width="14" height="14" alt="KeePassXC"> [KeePassXC](categories/08-password-manager/README.md#keepassxc) (Offline Vault) | Vaultwarden |
| [`09-2fa-authenticator`](categories/09-2fa-authenticator/README.md) | 2FA Authenticator | <img src="assets/logos/ente.svg" width="18" height="18" alt="Ente"> | **Ente Auth** | <img src="assets/logos/ente.svg" width="14" height="14" alt="2FAS"> [2FAS](categories/09-2fa-authenticator/README.md#2fas) (Cross-Platform FOSS) | Aegis (Android) |
| [`10-cloud-storage`](categories/10-cloud-storage/README.md) | Cloud Storage | <img src="assets/logos/protondrive.svg" width="18" height="18" alt="Proton Drive"> | **Proton Drive** | <img src="assets/logos/nextcloud.svg" width="14" height="14" alt="Nextcloud"> [Nextcloud](categories/10-cloud-storage/README.md#nextcloud) (Self-Host) | Syncthing |
| [`11-file-sharing`](categories/11-file-sharing/README.md) | File Sharing | <img src="assets/logos/onionshare.svg" width="18" height="18" alt="OnionShare"> | **OnionShare** | <img src="assets/logos/onionshare.svg" width="14" height="14" alt="Send"> [Send](categories/11-file-sharing/README.md#send-timviseesend) (HTTPS Link) | OnionShare / Send |
| [`12-notes`](categories/12-notes/README.md) | Notes & Tasks | <img src="assets/logos/joplin.svg" width="18" height="18" alt="Joplin"> | **Joplin** | <img src="assets/logos/notesnook.png" width="14" height="14" alt="Notesnook"> [Notesnook](categories/12-notes/README.md#notesnook) (E2EE Markdown) | Joplin (Local DB) |
| [`13-calendar-contacts`](categories/13-calendar-contacts/README.md) | Calendar & Contacts | <img src="assets/logos/protoncalendar.svg" width="18" height="18" alt="Proton Calendar"> | **Proton Calendar** | <img src="assets/logos/nextcloud.svg" width="14" height="14" alt="Nextcloud"> [Nextcloud](categories/13-calendar-contacts/README.md#nextcloud-calendarcontacts) (CalDAV) | Nextcloud CalDAV |
| [`14-maps`](categories/14-maps/README.md) | Maps & Navigation | <img src="assets/logos/organicmaps.svg" width="18" height="18" alt="Organic Maps"> | **Organic Maps** | <img src="assets/logos/organicmaps.svg" width="14" height="14" alt="OsmAnd"> [OsmAnd](categories/14-maps/README.md#osmand) (Topography/Trails) | Offline OSM Packs |
| [`15-office-docs`](categories/15-office-docs/README.md) | Office / Docs | <img src="assets/logos/libreoffice.svg" width="18" height="18" alt="LibreOffice"> | **LibreOffice** | <img src="assets/logos/libreoffice.svg" width="14" height="14" alt="CryptPad"> [CryptPad](categories/15-office-docs/README.md#cryptpad) (E2EE Collab) | LibreOffice |
| [`16-photo-storage`](categories/16-photo-storage/README.md) | Photo Storage | <img src="assets/logos/ente.svg" width="18" height="18" alt="Ente Photos"> | **Ente Photos** | <img src="assets/logos/immich.svg" width="14" height="14" alt="Immich"> [Immich](categories/16-photo-storage/README.md#immich) (Self-Host) | Immich |
| [`17-analytics-selfhost`](categories/17-analytics-selfhost/README.md) | Web Analytics | <img src="assets/logos/umami.svg" width="18" height="18" alt="Umami"> | **Umami** | <img src="assets/logos/umami.svg" width="14" height="14" alt="GoatCounter"> [GoatCounter](categories/17-analytics-selfhost/README.md#goatcounter) (Micro) | Umami |
| [`18-os-desktop`](categories/18-os-desktop/README.md) | Desktop OS | <img src="assets/logos/fedora.svg" width="18" height="18" alt="Fedora"> | **Fedora Workstation** | <img src="assets/logos/fedora.svg" width="14" height="14" alt="Qubes OS"> [Qubes OS](categories/18-os-desktop/README.md#qubes-os) (Compartments) | Fedora / Mint |
| [`19-os-mobile`](categories/19-os-mobile/README.md) | Mobile OS | <img src="assets/logos/grapheneos.svg" width="18" height="18" alt="GrapheneOS"> | **GrapheneOS** | <img src="assets/logos/grapheneos.svg" width="14" height="14" alt="CalyxOS"> [CalyxOS](categories/19-os-mobile/README.md#calyxos) (Non-Pixel) | GrapheneOS |
| [`20-app-store-android`](categories/20-app-store-android/README.md) | Android App Store | <img src="assets/logos/fdroid.svg" width="18" height="18" alt="F-Droid"> | **F-Droid** | <img src="assets/logos/fdroid.svg" width="14" height="14" alt="Aurora Store"> [Aurora Store](categories/20-app-store-android/README.md#aurora-store) (Play Mirror) | F-Droid Repos |
| [`21-browser-extensions`](categories/21-browser-extensions/README.md) | Browser Extensions | <img src="assets/logos/ublockorigin.svg" width="18" height="18" alt="uBlock Origin"> | **uBlock Origin** | <img src="assets/logos/ublockorigin.svg" width="14" height="14" alt="uBO Lite"> [uBO Lite](categories/21-browser-extensions/README.md#ublock-origin-lite) (Chromium MV3) | uBlock Origin |
| [`22-ai-local`](categories/22-ai-local/README.md) | Local AI Chat | <img src="assets/logos/ollama.svg" width="18" height="18" alt="Ollama"> | **Ollama** | <img src="assets/logos/ollama.svg" width="14" height="14" alt="Open WebUI"> [Open WebUI](categories/22-ai-local/README.md#open-webui) (Web Interface) | Ollama + WebUI |
| [`23-video-calls`](categories/23-video-calls/README.md) | Video / Audio Calls | <img src="assets/logos/jitsi.svg" width="18" height="18" alt="Jitsi Meet"> | **Jitsi Meet** | <img src="assets/logos/signal.svg" width="14" height="14" alt="Signal Calls"> [Signal Calls](categories/23-video-calls/README.md#signal-calls) (Small Groups) | Jitsi Docker |
| [`24-translation`](categories/24-translation/README.md) | Translation | <img src="assets/logos/firefox.svg" width="18" height="18" alt="Firefox"> | **Firefox Translations** | <img src="assets/logos/firefox.svg" width="14" height="14" alt="LibreTranslate"> [LibreTranslate](categories/24-translation/README.md#libretranslate) (API/Web) | Local Neural Models |
| [`25-payments-privacy`](categories/25-payments-privacy/README.md) | Privacy Payments | <img src="assets/logos/monero.svg" width="18" height="18" alt="Monero"> | **Cash & Minimizing Cards** | <img src="assets/logos/monero.svg" width="14" height="14" alt="Monero"> [Monero](categories/25-payments-privacy/README.md#monero-cake-wallet) (Unlinkable) | Cash / Monero GUI |

---

## Real-World Edge Cases & Gotchas

Before switching your entire stack, read these practical reality checks:

1. **The Chrome Manifest V3 Trap**: Google is phasing out Manifest V2 in Chrome and Edge. Full uBlock Origin will stop working on Chrome. If you want wide-spectrum ad/tracker blocking, switch to **Firefox** or **Brave**. On Chrome, you are restricted to **uBlock Origin Lite**.
2. **Banking Apps & Play Integrity**: GrapheneOS runs Sandboxed Google Play Services, passing basic device integrity checks. But a small number of strict banking apps require hardware key attestation (`MEETS_STRONG_INTEGRITY`) and will fail. Check app compatibility or keep a secondary device before wiping your phone.
3. **Self-Hosted Email Deliverability**: Setting up a mail server on a VPS is easy; getting Gmail and Outlook to accept your outbound emails is hard. Cloud VPS IP ranges are heavily blacklisted. For personal email, use hosted zero-access providers like **Proton Mail** or **Tuta Mail**.
4. **Desktop Proton Mail on Free Plans**: Proton encrypts data client-side, meaning standard IMAP in Thunderbird requires a paid Proton Bridge subscription. On free plans, use Proton's official desktop apps for Linux, Windows, and macOS instead.
5. **Mullvad Port Forwarding**: Mullvad removed port forwarding in 2023. If you need open inbound ports for torrent seeding or home server hosting, use **IVPN** or deploy your own **WireGuard** VPS.
6. **OnionShare Speeds**: Routing large multi-gigabyte files through Tor relays is slow and iOS lacks native OnionShare support. For big files or iPhone recipients, use **Send (timvisee)** or **Magic Wormhole**.

---

## How to Use This Repository

1. **Pick the category** you want to fix today.
2. **Install the primary tool** following its step-by-step OS guide.
3. If a specific limitation blocks you (unsupported hardware, payment constraints, or offline needs), **use the single catch alternative** listed in that category's table.
4. If you run a homelab and want zero cloud dependencies, **use the local open-source path**.

---

## Machine-Readable Manifests & AI Agents

If you are an autonomous agent, LLM-based researcher, or automated script:
- Read [`llms.txt`](llms.txt) for standard high-level index mapping.
- Read [`INDEX.md`](INDEX.md) for full structured YAML and tabular metadata across all 25 categories.

---

## Frequently Asked Questions

### Why only one primary recommendation per category?
Most privacy directories dump dozens of tools without telling you which one to actually use. That leads to decision paralysis. I picked one clear default that balances strong privacy defaults, active maintenance, and multi-platform convenience.

### What if the primary tool doesn't work for my setup?
Every category README includes a **Catches Table**. For every real drawback (such as lack of iOS support, closed-source dependencies, or subscription pricing), I documented exactly one vetted alternative that resolves that specific catch.

### Are these tools completely free?
Whenever possible, I chose free and open-source software (FOSS). For categories where reliable infrastructure requires ongoing server costs (like commercial VPNs or hosted encrypted email), I recommend audited, no-logs paid services alongside free tiers and self-hosted options.

### How are install steps verified?
Install commands are taken directly from upstream package repositories (Debian/Ubuntu keyrings, Fedora DNF5 repos, Homebrew casks, and official Git releases). No invented install scripts.

---

## Governance & Security

- **Contributing**: Read [CONTRIBUTING.md](CONTRIBUTING.md) before opening a pull request.
- **Code of Conduct**: See [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) for community standards.
- **Security Policy**: Read [SECURITY.md](SECURITY.md) to report vulnerabilities or compromised tools.
- **Methodology**: Read [METHODOLOGY.md](METHODOLOGY.md) to understand curation criteria.
- **References**: Maintainer upstream verification index is in [sources/REFERENCES.md](sources/REFERENCES.md).

---

## Author & License

Curated and maintained by **Poorvith M P**.  
Licensed under the [MIT License](LICENSE).
