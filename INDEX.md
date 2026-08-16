# Open Privacy — Machine-Readable Tool Index

> **Open Privacy** · v1.0 · August 2026 · Poorvith M P  
> Curated directory of 25 digital privacy categories. Designed for humans, developers, and AI agents evaluating privacy tooling.

---

## 25 Categories Quick Index

| ID | Category | Primary Tool | License | Platforms | Local / Self-Host | Primary Website |
|---|---|---|---|---|---|---|
| `01-browser` | Web Browser | Brave Browser | MPL 2.0 (core) | Linux, Windows, macOS, Android, iOS | Firefox (FOSS client) | https://brave.com |
| `02-search` | Search Engine | Brave Search | Proprietary Index | Web (any browser) | SearXNG (Docker FOSS) | https://search.brave.com |
| `03-email` | Email Provider | Proton Mail | Open Source Apps | Web, Desktop (Linux/Win/Mac), Mobile | Stalwart / Mailcow | https://proton.me/mail |
| `04-email-aliasing` | Email Aliasing | SimpleLogin | AGPL 3.0 | Web, Extension, Mobile | SimpleLogin (Self-Host) | https://simplelogin.io |
| `05-messenger` | Instant Messaging | Signal | GPL 3.0 / AGPL | Linux, Windows, macOS, Android, iOS | Matrix (Synapse/Conduit) | https://signal.org |
| `06-vpn` | VPN | Mullvad VPN | GPL 3.0 (Apps) | Linux, Windows, macOS, Android, iOS | WireGuard (Self-Host) | https://mullvad.net |
| `07-dns` | DNS Resolver | Quad9 | Public Service | Router, OS Settings, Android Private DNS | Unbound / Pi-hole | https://quad9.net |
| `08-password-manager` | Password Manager | Bitwarden | GPL 3.0 (Clients) | Linux, Windows, macOS, Android, iOS, CLI | Vaultwarden / KeePassXC | https://bitwarden.com |
| `09-2fa-authenticator` | 2FA Authenticator | Ente Auth | AGPL 3.0 | Linux, Windows, macOS, Android, iOS, Web | Aegis (Android) / KeePassXC | https://ente.io/auth |
| `10-cloud-storage` | Cloud Storage | Proton Drive | Open Source Apps | Windows, macOS, Android, iOS, Web | Nextcloud / Syncthing | https://proton.me/drive |
| `11-file-sharing` | File Sharing | OnionShare | GPL 3.0 | Linux, Windows, macOS, CLI | OnionShare / Send | https://onionshare.org |
| `12-notes` | Notes & Tasks | Joplin | AGPL 3.0 | Linux, Windows, macOS, Android, iOS, CLI | Joplin (Local DB) | https://joplinapp.org |
| `13-calendar-contacts` | Calendar & Contacts | Proton Calendar | Open Source Apps | Web, Android, iOS | Nextcloud CalDAV/CardDAV | https://proton.me/calendar |
| `14-maps` | Maps & Navigation | Organic Maps | Apache 2.0 | Android, iOS | Organic Maps / OsmAnd | https://organicmaps.app |
| `15-office-docs` | Office / Docs | LibreOffice | MPL 2.0 | Linux, Windows, macOS | LibreOffice (Native) | https://www.libreoffice.org |
| `16-photo-storage` | Photo Storage | Ente Photos | AGPL 3.0 | Linux, Windows, macOS, Android, iOS, Web | Immich (Self-Host) | https://ente.io/photos |
| `17-analytics-selfhost` | Web Analytics | Umami | MIT | Linux (Docker / Node) | Umami (Self-Host) | https://umami.is |
| `18-os-desktop` | Desktop OS | Fedora Workstation | GPL / Free Software | x86_64, aarch64 | Fedora / Qubes OS | https://fedoraproject.org/workstation |
| `19-os-mobile` | Mobile OS | GrapheneOS | MIT / GPL / AOSP | Google Pixel (6, 7, 8, 9+) | GrapheneOS | https://grapheneos.org |
| `20-app-store-android` | Android App Store | F-Droid | GPL 3.0 | Android | F-Droid + custom repos | https://f-droid.org |
| `21-browser-extensions` | Browser Extensions | uBlock Origin | GPL 3.0 | Firefox, Chromium (uBO Lite) | uBlock Origin | https://ublockorigin.com |
| `22-ai-local` | Local AI Chat | Ollama | MIT | Linux, Windows, macOS | Ollama + Open WebUI | https://ollama.com |
| `23-video-calls` | Video & Audio Calls | Jitsi Meet | Apache 2.0 | Web, Android, iOS, Self-Host | Self-Hosted Jitsi | https://meet.jit.si |
| `24-translation` | On-Device Translation | Firefox Translations | MPL 2.0 | Firefox Desktop / Mobile (Built-in) | Firefox / LibreTranslate | https://support.mozilla.org |
| `25-payments-privacy` | Privacy Payments | Cash & Monero | Open Source (Monero) | Global / Multi-platform | Monero / Cash Ledger | https://getmonero.org |

---

## Ecosystem Decision Mappings (Catches & Key Alternatives)

```yaml
01-browser:
  primary: Brave Browser
  catches:
    - catch: "Need maximum anonymity over Tor network"
      alternative: Tor Browser
    - catch: "Refuse Chromium; prefer Gecko/Mozilla engine"
      alternative: Firefox
    - catch: "Zero crypto/rewards UI surface by default"
      alternative: Mullvad Browser

02-search:
  primary: Brave Search
  catches:
    - catch: "Want 100% self-hosted metasearch without telemetry"
      alternative: SearXNG
    - catch: "Prefer Google results proxied without cookies"
      alternative: Startpage

03-email:
  primary: Proton Mail
  catches:
    - catch: "Want post-quantum encryption and non-Swiss jurisdiction"
      alternative: Tuta Mail
    - catch: "Need self-hosted mail server"
      alternative: Stalwart or Mailcow

04-email-aliasing:
  primary: SimpleLogin
  catches:
    - catch: "Want independent non-Proton FOSS aliasing service"
      alternative: addy.io
    - catch: "Full self-host on private domain"
      alternative: SimpleLogin Docker

05-messenger:
  primary: Signal
  catches:
    - catch: "Zero user identifiers (no phone number, no usernames, metadata-free queues)"
      alternative: SimpleX Chat
    - catch: "Onion-routed cryptocurrency-incentivized network"
      alternative: Session
    - catch: "Federated decentralized team/community chat"
      alternative: Element (Matrix)

06-vpn:
  primary: Mullvad VPN
  catches:
    - catch: "Need a high-quality free VPN tier"
      alternative: Proton VPN Free
    - catch: "Audited commercial alternative with port forwarding options"
      alternative: IVPN
    - catch: "Self-host on private VPS"
      alternative: WireGuard

07-dns:
  primary: Quad9
  catches:
    - catch: "Custom per-device blocklists and analytics"
      alternative: NextDNS
    - catch: "Local recursive resolver without upstream trust"
      alternative: Unbound
    - catch: "Whole-home LAN ad blocking"
      alternative: Pi-hole

08-password-manager:
  primary: Bitwarden
  catches:
    - catch: "Pure local offline encrypted file vault"
      alternative: KeePassXC
    - catch: "Lightweight self-hosted Bitwarden API in Rust"
      alternative: Vaultwarden

09-2fa-authenticator:
  primary: Ente Auth
  catches:
    - catch: "Cross-platform offline/cloud backup without account lock-in"
      alternative: 2FAS
    - catch: "Android-only offline FOSS encrypted vault"
      alternative: Aegis Authenticator
    - catch: "Hardware security key"
      alternative: YubiKey (FIDO2/WebAuthn)

10-cloud-storage:
  primary: Proton Drive
  catches:
    - catch: "Self-hosted private cloud suite"
      alternative: Nextcloud
    - catch: "Device-to-device direct synchronization without cloud"
      alternative: Syncthing
    - catch: "Client-side encryption for existing commercial cloud storage"
      alternative: Cryptomator

11-file-sharing:
  primary: OnionShare
  catches:
    - catch: "Send simple HTTPS link to non-technical users"
      alternative: Send (timvisee fork)
    - catch: "Direct terminal-to-terminal file transfer"
      alternative: Magic Wormhole

12-notes:
  primary: Joplin
  catches:
    - catch: "Independent 100% FOSS E2EE notes with clean markdown editing"
      alternative: Notesnook
    - catch: "Local plaintext markdown vault"
      alternative: Obsidian / Logseq

13-calendar-contacts:
  primary: Proton Calendar
  catches:
    - catch: "Self-hosted CalDAV/CardDAV server"
      alternative: Nextcloud Calendar/Contacts

14-maps:
  primary: Organic Maps
  catches:
    - catch: "Advanced topographic, hiking, and detailed GIS navigation"
      alternative: OsmAnd

15-office-docs:
  primary: LibreOffice
  catches:
    - catch: "Browser-based E2EE real-time collaboration"
      alternative: CryptPad
    - catch: "High Microsoft Office format compatibility"
      alternative: OnlyOffice

16-photo-storage:
  primary: Ente Photos
  catches:
    - catch: "Self-hosted high-performance Google Photos replacement"
      alternative: Immich

17-analytics-selfhost:
  primary: Umami
  catches:
    - catch: "Hosted privacy analytics with EU cloud"
      alternative: Plausible Cloud
    - catch: "Single-binary cookieless micro analytics"
      alternative: GoatCounter

18-os-desktop:
  primary: Fedora Workstation
  catches:
    - catch: "Maximum isolation and security by compartmentalization"
      alternative: Qubes OS
    - catch: "Beginner-friendly Linux distribution"
      alternative: Linux Mint

19-os-mobile:
  primary: GrapheneOS
  catches:
    - catch: "Non-Pixel hardware (Fairphone, Motorola, SHIFTphone)"
      alternative: CalyxOS
    - catch: "Broader legacy Android device support"
      alternative: LineageOS for microG

20-app-store-android:
  primary: F-Droid
  catches:
    - catch: "Download apps directly from Google Play anonymously"
      alternative: Aurora Store
    - catch: "Update apps directly from GitHub / GitLab releases"
      alternative: Obtainium
    - catch: "Modern cryptographic signed APK repository"
      alternative: Accrescent

21-browser-extensions:
  primary: uBlock Origin
  catches:
    - catch: "Chromium browser where Manifest V2 is disabled"
      alternative: uBlock Origin Lite
    - catch: "Default browser built-in blocking"
      alternative: Brave Shields

22-ai-local:
  primary: Ollama
  catches:
    - catch: "Web browser UI for local models"
      alternative: Open WebUI
    - catch: "Desktop GUI for non-CLI users"
      alternative: LM Studio / Jan

23-video-calls:
  primary: Jitsi Meet
  catches:
    - catch: "E2EE calls for mobile/desktop 1:1 and small groups"
      alternative: Signal group calls
    - catch: "Matrix-native video rooms"
      alternative: Element Call

24-translation:
  primary: Firefox Translations
  catches:
    - catch: "Self-hosted translation API and web app"
      alternative: LibreTranslate

25-payments-privacy:
  primary: Cash + minimize stored cards
  catches:
    - catch: "Masking real card numbers from online merchants (US)"
      alternative: Privacy.com
    - catch: "Unlinkable, private cryptocurrency transactions"
      alternative: Monero (Cake Wallet)
```
