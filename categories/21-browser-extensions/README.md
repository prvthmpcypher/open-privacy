# Browser Extensions (Tracker Block)

> Open Privacy · v1.0 · August 2026 · Poorvith M P  
> Category ID: `21-browser-extensions`  
> Replaces: Browsing without content blocking, ad-tech malware, fingerprinting scripts

---

## Primary recommendation

<img src="../../assets/logos/ublockorigin.svg" width="36" height="36" alt="uBlock Origin Logo">

| Field | Value |
|---|---|
| **Name** | uBlock Origin |
| **Website** | https://ublockorigin.com |
| **Source / repo** | https://github.com/gorhill/uBlock |
| **Open source?** | **Yes** (GPL 3.0) |
| **Local / self-host?** | **Yes** — runs 100% locally in your browser engine |
| **Target audience** | Everyone browsing the web on desktop and mobile browsers |
| **Platforms** | <img src="../../assets/logos/firefox.svg" width="14" height="14" alt="Firefox"> Firefox (Full MV2) · <img src="../../assets/logos/brave.svg" width="14" height="14" alt="Brave"> Brave · <img src="../../assets/logos/windows.svg" width="14" height="14" alt="Windows"> Windows · <img src="../../assets/logos/macos.svg" width="14" height="14" alt="macOS"> macOS · <img src="../../assets/logos/linux.svg" width="14" height="14" alt="Linux"> Linux |
| **Pricing** | 100% Free (Accepts zero donations) |
| **Payment notes** | N/A |

### Why this is the one pick
1. Wide-spectrum, open-source content blocker developed by Raymond Hill (gorhill).
2. Extremely light CPU and memory footprint compared to commercial adblockers.
3. Provides comprehensive protection against tracking scripts, third-party CNAME uncloaking, and cosmetic ad clutter.
4. Allows dynamic filtering rules and custom element zapping.
5. Operates with strict ethical principles: no "acceptable ads" whitelist programs or monetization.

### What it does not do
- Does not encrypt your network traffic (not a VPN).
- Google has disabled Manifest V2 extensions in Chrome/Chromium, restricting full uBlock Origin capabilities on Chrome (use **uBlock Origin Lite** or switch to **Firefox** / **Brave** for full capability).

---

## Install guide (primary)

### Firefox (Recommended for Maximum Capability)
1. Install from Firefox Add-ons: https://addons.mozilla.org/en-US/firefox/addon/ublock-origin/
2. Open extension dashboard → Filter lists → Enable **EasyList Cookie**, **Fanboy's Annoyance**, and regional lists as desired.

### Brave Browser
- Brave includes built-in Shields (see `01-browser`). You can add uBlock Origin on desktop from the Chrome Web Store for secondary advanced dynamic filtering if desired.

### Chrome / Chromium (Manifest V3 Environments)
- If your browser disables Manifest V2 extensions, install **uBlock Origin Lite**: https://chromewebstore.google.com/detail/ublock-origin-lite/ddkjiahejlhfcafbddmgiahcphecmpfh

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| Browser forces Manifest V3 (Google Chrome / Edge) | Full uBlock Origin requires the declarative webRequest API | <img src="../../assets/logos/ublockorigin.svg" width="16" height="16" alt="uBO Lite"> **uBlock Origin Lite** | Yes | Chromium (MV3) | Don’t switch away from full uBlock Origin if you are on Firefox or Brave |
| Already using Brave Browser with native Rust ad blocker | Brave Shields provides built-in blocking without extensions | <img src="../../assets/logos/brave.svg" width="16" height="16" alt="Brave Shields"> **Brave Shields (Built-in)** | Yes | All major | Don’t add extra extension bloat if built-in Shields satisfy your blocking needs |
| iOS Safari user seeking native WebKit content blocking | iOS Safari requires native Content Blocker APIs | <img src="../../assets/logos/safari.svg" width="16" height="16" alt="Safari"> **AdGuard for Safari** or Brave iOS | Open Source | iOS · macOS | Don’t switch on desktop where full uBlock Origin provides superior filtering |

### Alternative installs

#### uBlock Origin Lite (Manifest V3)
- Chrome Web Store: https://chromewebstore.google.com/detail/ublock-origin-lite/ddkjiahejlhfcafbddmgiahcphecmpfh

#### AdGuard for Safari
- Mac App Store / iOS App Store.

---

## Real-world gotcha: The Manifest V3 trap

Google's transition to **Manifest V3** in Chromium limits how extensions can inspect and modify network requests in real time.

- **On Firefox**: Mozilla maintains full support for the `webRequest` API. uBlock Origin operates at 100% capability, including advanced scriptlet injection and CNAME uncloaking.
- **On Brave**: Built-in Brave Shields operate at the browser engine level (Rust-based), completely bypassing Manifest V3 limits.
- **On Google Chrome / Edge**: Full uBlock Origin is phased out. You must use **uBlock Origin Lite**, which relies on static declarative rules and cannot execute complex dynamic filtering.

If content blocking matters to you, stop using Google Chrome as your daily browser.

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | uBlock Origin |
| **Repo** | https://github.com/gorhill/uBlock |
| **What local means** | Filter rules and blocking decisions evaluate entirely inside the local browser process |
| **Who it’s for** | All internet users |
| **Ops burden** | Low |
| **When primary still wins** | Primary is already the open-source industry benchmark |

---

## Quick decision box

```text
Default content blocker (Firefox)    →  uBlock Origin
Chromium browser with Manifest V3   →  uBlock Origin Lite
Brave browser native blocking        →  Brave Shields
iOS Safari native blocking           →  AdGuard for Safari / Brave iOS
```
