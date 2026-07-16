# Instant Messaging

> Open Privacy · v0.1 · July 2026 · Poorvith M P  
> Category ID: `05-messenger`  
> Replaces: WhatsApp / SMS as default private chat

---

## Primary recommendation

| Field | Value |
|---|---|
| **Name** | Signal |
| **Website** | https://signal.org |
| **Source / repo** | https://github.com/signalapp |
| **Open source?** | **Yes** — clients open source |
| **Local / self-host?** | **No** — uses Signal service |
| **Target audience** | People who need E2EE chat with strong defaults |
| **Platforms** | Windows · macOS · Linux · Android · iOS |
| **Pricing** | Free |
| **Payment notes** | N/A |

### Why this is the one pick
1. Strong E2EE defaults for everyday messaging.
2. Official apps on all major platforms.
3. Open-source clients.
4. Usable UX for non-technical contacts relative to many alternatives.
5. Safety number verification for high-risk contacts.

### What it does not do
- Requires a phone number for registration.
- Not ideal as a large public community platform.
- Network effect still favors WhatsApp in some regions.

---

## Install guide (primary)

### Download hubs
- https://signal.org/download/

### Windows
1. Download Signal Desktop from https://signal.org/download/
2. Install and open Signal.
3. Link to your primary Signal mobile app via QR code.

### macOS
1. Download macOS build from https://signal.org/download/
2. Open the `.dmg` and drag Signal to Applications.
3. Link device via QR from the mobile app.

### Linux
1. Follow the official Linux install instructions on https://signal.org/download/
2. Launch Signal and link to mobile.

### Android
1. Install Signal from the Play Store link on https://signal.org/download/ (or official APK channel Signal documents).
2. Register with your phone number.
3. Set a Signal PIN / registration lock if offered.

### iOS
1. Install Signal from the App Store (link via signal.org/download).
2. Register with phone number.
3. Configure notifications; review backup settings for privacy preference.

### First-run checklist
1. Set a strong Signal PIN.
2. Remove unknown linked devices.
3. Enable disappearing messages for sensitive threads.
4. Verify safety numbers for high-risk contacts.

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| Refuse phone-number registration | Signal requires a phone number | **Session** | Yes | Desktop · mobile | Don’t switch if your contacts only use Signal |
| Need federated/self-hostable chat | Signal is centralized | **Element (Matrix)** | Yes | All major + self-host | Don’t use Matrix if you need the simplest UX for non-tech family |
| Need large public groups/channels | Different product model | **Element spaces** | Yes | All major | Don’t sacrifice E2EE defaults for public broadcast features |

### Alternative installs

#### Session
- https://getsession.org/download — install official desktop/mobile packages only

#### Element (Matrix)
- Apps: https://element.io/download
- Homeserver self-host: Matrix server docs (e.g. Synapse install guides)

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | Matrix (Synapse/Conduit) + Element |
| **Repo** | https://github.com/element-hq/element-web |
| **What local means** | Self-hosted chat homeserver + open clients |
| **Who it’s for** | Communities and technical households |
| **Ops burden** | Medium–High |
| **When primary still wins** | You need the simplest E2EE messenger for phone contacts |

### Local install
- **Server:** install a Matrix homeserver on Linux per upstream docs
- **Clients:** Element from https://element.io/download on all OSes

---

## Quick decision box

```text
Default private messenger           →  Signal
No phone number                      →  Session
Federated / self-host                →  Element (Matrix)
```
