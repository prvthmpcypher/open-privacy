# Web Browser

> Open Privacy · v0.1 · July 2026 · Poorvith M P  
> Category ID: `01-browser`  
> Replaces: Google Chrome (default), unhardened stock browsers

---

## Primary recommendation

| Field | Value |
|---|---|
| **Name** | Brave Browser |
| **Website** | https://brave.com |
| **Source / repo** | https://github.com/brave/brave-browser |
| **Open source?** | **Partial** — browser is open source; some product services are not fully open |
| **Local / self-host?** | **No** — on-device client only |
| **Target audience** | Everyday users who want a Chrome-like browser with built-in tracker/ad blocking |
| **Platforms** | Linux · Windows · macOS · Android · iOS |
| **Pricing** | Free for core browsing |
| **Payment notes** | N/A for core browser |

### Why this is the one pick
1. Same product on desktop and mobile with low setup cost.
2. Built-in Shields reduce the need for a large extension stack on day one.
3. Chromium extension ecosystem on desktop eases switching from Chrome.
4. Actively maintained with install paths on all major OSes.
5. Usable without manual hardening guides.

### What it does not do
- Does not make you anonymous on the network (not a Tor replacement).
- Does not remove Chromium heritage entirely.
- Does not replace a password manager, VPN, or good account hygiene.

---

## Install guide (primary)

### Download hubs
- Desktop + mobile: https://brave.com/download/
- Windows direct: https://laptop-updates.brave.com/latest/winx64
- macOS direct: https://laptop-updates.brave.com/latest/osx
- Linux: https://brave.com/linux/
- System requirements: https://support.brave.app/hc/en-us/articles/360021357112-What-are-the-system-requirements-to-install-Brave

### Windows
1. Download the installation file from https://www.brave.com/download
2. If prompted, click **Run** or **Save**.
3. If you chose **Save**, double-click the download to start installing.
4. A Brave window opens after installation finishes.

Alternate channel: Microsoft Store (listed on Brave’s download page).

### macOS
1. Download the installation file from https://www.brave.com/download
2. Open the file.
3. In the window that opens, find **Brave**.
4. Drag **Brave** to the **Applications** folder.
   - You might be asked to enter the admin password.
   - If you don't know the admin password, drag Brave to a place you can edit (for example the desktop).
5. Open Brave.
6. Open **Finder**.
7. In the sidebar, to the right of Brave, click **Eject**.

### Linux
Supported: 64-bit AMD/Intel (`amd64` / `x86_64`) and ARM (`arm64` / `aarch64`).

#### Debian, Ubuntu, Mint
```bash
sudo apt install curl
sudo curl -fsSLo /usr/share/keyrings/brave-browser-archive-keyring.gpg https://brave-browser-apt-release.s3.brave.com/brave-browser-archive-keyring.gpg
sudo curl -fsSLo /etc/apt/sources.list.d/brave-browser-release.sources https://brave-browser-apt-release.s3.brave.com/brave-browser.sources
sudo apt update
sudo apt install brave-browser
```

#### Fedora 41+ (dnf5)
```bash
sudo dnf install dnf-plugins-core
sudo dnf config-manager addrepo --from-repofile=https://brave-browser-rpm-release.s3.brave.com/brave-browser.repo
sudo dnf install brave-browser
```

#### Fedora <41, Rocky/RHEL
```bash
sudo dnf install dnf-plugins-core
sudo dnf config-manager --add-repo https://brave-browser-rpm-release.s3.brave.com/brave-browser.repo
sudo dnf install brave-browser
```

#### openSUSE
```bash
sudo zypper addrepo https://brave-browser-rpm-release.s3.brave.com/brave-browser.repo
sudo zypper install brave-browser
```

#### Arch (AUR helper example: yay)
```bash
yay -Sy brave-bin
```

Prefer official package repositories over Flatpak/Snap when available. One-command script: https://brave.com/linux/

### Android
1. Install from Google Play: https://play.google.com/store/apps/details?id=com.brave.browser
2. Optional: APK builds via Brave’s Android release channels as documented by Brave.
3. Optional: Brave F-Droid repository (https://brave.com/blog/f-droid/).

### iOS
1. Install **Brave** from the App Store: https://apps.apple.com/app/brave-private-web-browser-vpn/id1052879175
2. Open the app once and complete first-run prompts.
3. Set as default browser in iOS Settings → Brave → Default Browser App (when available).

### First-run checklist
1. Confirm Shields are enabled on a normal website.
2. Turn off optional surfaces you do not want (Rewards, VPN upsell, wallet) if you only want a browser.
3. Set a privacy-oriented search engine (see category `02-search`).
4. Enable Brave as default browser in OS settings when ready.
5. Import bookmarks/passwords only if you intend to leave the old browser.

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| Need stronger anonymity, not a daily convenience browser | Brave is a normal browser with privacy features, not an anonymity network | **Tor Browser** | Yes | Desktop primary | Don’t use Tor as the only browser for everyday banking/logins |
| Refuse Chromium; want Mozilla stack | Brave is Chromium-based | **Firefox** | Yes | Linux · Windows · macOS · Android · iOS | Don’t switch if you depend on Chrome-only extensions with no Firefox port |
| Want zero Rewards/crypto product surface by default | Optional Brave extras annoy some users | **Mullvad Browser** | Yes | Desktop | Don’t switch if you need heavy extensions + multi-profile daily use |
| iOS user wants maximum system integration | iOS browsers share WebKit limits; some prefer Safari | **Safari** | No | iOS · macOS | Don’t drop cross-platform Brave if you need one setup everywhere |

### Alternative installs

#### Tor Browser
- **Linux / Windows / macOS:** https://www.torproject.org/download/
- **Android:** only via Tor Project’s official Android guidance
- **iOS:** limited; avoid unofficial “Tor” apps

#### Firefox
- **Linux / Windows / macOS:** https://www.mozilla.org/firefox/
- **Android / iOS:** official Firefox apps from store listings linked by Mozilla

#### Mullvad Browser
- **Linux / Windows / macOS:** https://mullvad.net/en/browser
- **Android / iOS:** not offered

#### Safari
- **macOS / iOS:** built into Apple platforms
- **Linux / Windows / Android:** not available

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | Firefox (distro package or official binary) |
| **Repo** | https://www.mozilla.org/firefox/ · https://github.com/mozilla/gecko-dev |
| **What local means** | On-device FOSS client; no account required |
| **Who it’s for** | Users who want a fully open-source browser stack |
| **Ops burden** | Low |
| **When primary still wins** | User wants built-in blocking and simpler multi-OS product defaults |

### Local install
- **Linux:** e.g. `sudo apt install firefox` (or distro equivalent) / Mozilla official build
- **Windows / macOS:** https://www.mozilla.org/firefox/
- **Android / iOS:** official Firefox apps
- **Docker / self-host:** not applicable

---

## Quick decision box

```text
Default daily browser              →  Brave
Need anonymity network             →  Tor Browser
Want pure FOSS Mozilla stack       →  Firefox (also local FOSS path)
Hate Rewards/crypto surface        →  Mullvad Browser
iOS system-native preference       →  Safari
```
