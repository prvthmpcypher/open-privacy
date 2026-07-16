# File Sharing

> Open Privacy · v0.1 · July 2026 · Poorvith M P  
> Category ID: `11-file-sharing`  
> Replaces: WeTransfer / random file hosts

---

## Primary recommendation

| Field | Value |
|---|---|
| **Name** | OnionShare |
| **Website** | https://onionshare.org |
| **Source / repo** | https://github.com/onionshare/onionshare |
| **Open source?** | **Yes** |
| **Local / self-host?** | **Yes** — runs on your machine over Tor |
| **Target audience** | Users sending sensitive files without a third-party upload host |
| **Platforms** | Windows · macOS · Linux (mobile companions limited; primarily desktop) |
| **Pricing** | Free |
| **Payment notes** | N/A |

### Why this is the one pick
1. Share files without uploading to a commercial file host.
2. Open source and privacy-oriented by design.
3. Works for one-off sensitive sends.
4. No account required.
5. Strong fit when confidentiality matters more than convenience.

### What it does not do
- Recipient experience can be harder than a simple HTTPS link.
- Depends on Tor network availability.
- Not ideal for huge public downloads or non-tech recipients.

---

## Install guide (primary)

### Download hubs
- https://onionshare.org
- Releases: https://github.com/onionshare/onionshare/releases

### Windows
1. Download the Windows installer from https://onionshare.org or GitHub releases.
2. Run the installer.
3. Open OnionShare → start a share → send the onion address only over a trusted channel.

### macOS
1. Download the macOS build from onionshare.org / releases.
2. Open the app (approve Gatekeeper if prompted).
3. Start a share and copy the onion URL.

### Linux
1. Install via distro package if available, or download from onionshare.org / Flatpak/GitHub as published.
2. Launch OnionShare.
3. Share files; keep the app running until transfer completes.

### Android
1. Check current official mobile options on onionshare.org (desktop is primary).
2. If no suitable mobile client, use desktop for sending/receiving.
3. Avoid unofficial APKs claiming OnionShare support.

### iOS
1. Official iOS support is limited/not the primary workflow.
2. Prefer desktop OnionShare or an alternative catch path for iOS recipients.
3. Do not install random App Store clones.

### First-run checklist
1. Verify you downloaded from onionshare.org or the official GitHub org.
2. Send the onion link out-of-band (Signal), not in the same untrusted email if avoidable.
3. Stop the share when finished.

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| Need simple HTTPS link for non-tech recipients | Tor onion UX is harder | **Send (timvisee/send)** | Yes | Self-host / public instances | Don’t use random unknown Send instances for highly sensitive files |
| Need ongoing sync not one-off send | Different problem | **Syncthing** | Yes | Desktop · Android | Don’t use Syncthing for one anonymous public drop |
| Recipient is iOS-only and struggles with Tor | Client/UX limits | **Magic Wormhole** (desktop) or encrypted container + Proton Drive link | Varies | Varies | Prefer teaching OnionShare when sensitivity is high |

### Alternative installs

#### Send (timvisee/send)
- Project: https://github.com/timvisee/send
- Self-host with Docker; or use a trusted public instance you verify

#### Syncthing
- https://syncthing.net/downloads/

#### Magic Wormhole
- https://github.com/magic-wormhole/magic-wormhole — `pip install magic-wormhole` / distro packages on Linux/macOS/Windows environments with Python

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | OnionShare itself, or self-hosted Send |
| **Repo** | https://github.com/onionshare/onionshare · https://github.com/timvisee/send |
| **What local means** | Transfer without a commercial SaaS file host |
| **Who it’s for** | Privacy-sensitive senders |
| **Ops burden** | Low (OnionShare) / Medium (Send server) |
| **When primary still wins** | OnionShare already is local/Tor-based |

### Local install
- **OnionShare:** onionshare.org downloads
- **Send:** Docker compose per timvisee/send docs

---

## Quick decision box

```text
Sensitive one-off send               →  OnionShare
Simple HTTPS expiring link           →  Send (self-host/trusted instance)
Continuous folder sync               →  Syncthing
```
