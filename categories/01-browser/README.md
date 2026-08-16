# Web Browser

> Open Privacy · v0.2 · August 2026 · Poorvith M P  
> Category ID: `01-browser`  
> Replaces: Google Chrome (default), unhardened stock browsers

---

## Primary recommendation

<img src="../../assets/logos/brave.svg" width="36" height="36" alt="Brave Browser Logo">

| Field | Value |
|---|---|
| **Name** | Brave Browser |
| **Website** | https://brave.com |
| **Source / repo** | https://github.com/brave/brave-browser |
| **Open source?** | **Partial** — browser client is open source (MPL 2.0); some backend services are proprietary |
| **Local / self-host?** | **No** — on-device client only |
| **Target audience** | Everyday users who want a Chrome-like browser with built-in tracker/ad blocking |
| **Platforms** | <img src="../../assets/logos/linux.svg" width="14" height="14" alt="Linux"> Linux · <img src="../../assets/logos/windows.svg" width="14" height="14" alt="Windows"> Windows · <img src="../../assets/logos/macos.svg" width="14" height="14" alt="macOS"> macOS · <img src="../../assets/logos/android.svg" width="14" height="14" alt="Android"> Android · <img src="../../assets/logos/ios.svg" width="14" height="14" alt="iOS"> iOS |
| **Pricing** | Free for core browsing |
| **Payment notes** | N/A for core browser |

### Why this is the one pick
1. Same clean experience on desktop and mobile with zero required setup.
2. Built-in Shields block ads, trackers, and fingerprinting out of the box.
3. Chromium extension compatibility makes switching painless.
4. Actively maintained with official packages for every major OS.
5. Works out of the box without manual user.js hardening scripts.

### What it does not do
- Does not make you anonymous on the network (it is not a Tor replacement).
- Does not remove Chromium base heritage entirely.
- Does not replace a password manager, VPN, or basic operational hygiene.

---

## Install guide (primary)

### Download hubs
- Desktop & Mobile: https://brave.com/download/
- Windows direct: https://laptop-updates.brave.com/latest/winx64
- macOS direct: https://laptop-updates.brave.com/latest/osx
- Linux repository guide: https://brave.com/linux/

### <img src="../../assets/logos/windows.svg" width="18" height="18" alt="Windows"> Windows
1. Download the installer from https://brave.com/download (or run `winget install Brave.Brave`).
2. Run the installer and follow the prompts.
3. Brave opens automatically once installed.

### <img src="../../assets/logos/macos.svg" width="18" height="18" alt="macOS"> macOS
1. Download the DMG from https://brave.com/download (or run `brew install --cask brave-browser`).
2. Open the downloaded DMG and drag **Brave** to your **Applications** folder.
3. Launch Brave from Spotlight or Applications.

### <img src="../../assets/logos/linux.svg" width="18" height="18" alt="Linux"> Linux
Supported architectures: 64-bit AMD/Intel (`amd64` / `x86_64`) and ARM (`arm64` / `aarch64`).

#### Debian, Ubuntu, Linux Mint
```bash
sudo apt install curl
sudo curl -fsSLo /usr/share/keyrings/brave-browser-archive-keyring.gpg https://brave-browser-apt-release.s3.brave.com/brave-browser-archive-keyring.gpg
sudo curl -fsSLo /etc/apt/sources.list.d/brave-browser-release.sources https://brave-browser-apt-release.s3.brave.com/brave-browser.sources
sudo apt update
sudo apt install brave-browser
```

#### Fedora 41+ (DNF5)
```bash
sudo dnf install dnf-plugins-core
sudo dnf config-manager addrepo --from-repofile=https://brave-browser-rpm-release.s3.brave.com/brave-browser.repo
sudo dnf install brave-browser
```

#### Fedora <41, RHEL, Rocky Linux
```bash
sudo dnf install dnf-plugins-core
sudo dnf config-manager --add-repo https://brave-browser-rpm-release.s3.brave.com/brave-browser.repo
sudo dnf install brave-browser
```

#### Arch Linux (AUR)
```bash
yay -S brave-bin
```

### <img src="../../assets/logos/android.svg" width="18" height="18" alt="Android"> Android
1. Install from Google Play: https://play.google.com/store/apps/details?id=com.brave.browser
2. Or download APK directly from GitHub releases: https://github.com/brave/brave-browser/releases

### <img src="../../assets/logos/ios.svg" width="18" height="18" alt="iOS"> iOS
1. Install from the App Store: https://apps.apple.com/app/brave-private-web-browser-vpn/id1052879175
2. Open the app and set as default browser in iOS Settings → Brave → Default Browser App.

### First-run checklist
1. Verify Shields are enabled (orange lion icon in URL bar).
2. Turn off optional crypto and rewards surfaces in settings if you want a clean browser.
3. Set your search engine to a privacy-respecting provider (see `02-search`).
4. Set Brave as your OS default browser.

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| Need network anonymity, not just everyday privacy | Brave is a normal clearnet browser | <img src="../../assets/logos/tor.svg" width="16" height="16" alt="Tor"> **Tor Browser** | Yes | Desktop · Android | Don’t use Tor as your daily browser for personal logins/banking |
| Refuse Chromium; want pure Gecko/Mozilla stack | Brave is Chromium-based | <img src="../../assets/logos/firefox.svg" width="16" height="16" alt="Firefox"> **Firefox** | Yes | Linux · Windows · macOS · Android · iOS | Don’t switch if you rely on Chrome-only extensions |
| Want zero crypto/rewards UI surface by default | Optional Brave features annoy some users | <img src="../../assets/logos/mullvad.svg" width="16" height="16" alt="Mullvad"> **Mullvad Browser** | Yes | Linux · Windows · macOS | Don’t switch if you need persistent account logins across sessions |
| iOS user wants native WebKit integration | iOS third-party browsers use WebKit anyway | <img src="../../assets/logos/safari.svg" width="16" height="16" alt="Safari"> **Safari** | No | iOS · macOS | Don’t switch if you need cross-platform sync with Windows or Linux |

### Alternative installs

#### Tor Browser
- Download official binary: https://www.torproject.org/download/

#### Firefox
- Desktop: https://www.mozilla.org/firefox/ (or `sudo apt install firefox` / `sudo dnf install firefox`)
- Mobile: Official Firefox app on Google Play or iOS App Store.

#### Mullvad Browser
- Download official package: https://mullvad.net/en/browser

#### Safari
- Built into macOS and iOS.

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | Firefox (distro package or official binary) |
| **Repo** | https://github.com/mozilla/gecko-dev |
| **What local means** | On-device FOSS client; no account required |
| **Who it’s for** | Users who want a fully open-source browser stack |
| **Ops burden** | Low |
| **When primary still wins** | You want stronger built-in blocking and out-of-the-box defaults without manual tweaking |

### Local install
- **Linux:** `sudo apt install firefox` or `sudo dnf install firefox`
- **Windows / macOS:** https://www.mozilla.org/firefox/

---

## Quick decision box

```text
Default daily browser              →  Brave Browser
Need anonymity network             →  Tor Browser
Want pure FOSS Mozilla stack       →  Firefox
Hate crypto/rewards surface        →  Mullvad Browser
iOS system-native preference       →  Safari
```
