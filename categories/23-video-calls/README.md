# Video / Audio Calls

> Open Privacy · v0.1 · July 2026 · Poorvith M P  
> Category ID: `23-video-calls`  
> Replaces: Zoom / Google Meet defaults

---

## Primary recommendation

| Field | Value |
|---|---|
| **Name** | Jitsi Meet |
| **Website** | https://meet.jit.si |
| **Source / repo** | https://github.com/jitsi/jitsi-meet |
| **Open source?** | **Yes** |
| **Local / self-host?** | **Yes** |
| **Target audience** | Users needing browser-based group calls without a Google/Zoom account |
| **Platforms** | Web · desktop/mobile apps · self-host |
| **Pricing** | Free public instance; self-host is your infra |
| **Payment notes** | N/A for public/self-host |

### Why this is the one pick
1. Open-source video conferencing.
2. Works in the browser with low friction.
3. Self-host option for higher trust.
4. No mandatory big-tech account on public instances.
5. Practical group-call alternative to Meet/Zoom.

### What it does not do
- Public instances are still third-party infrastructure.
- Large webinars may need dedicated hosting/config.
- Not a full enterprise suite by default.

---

## Install guide (primary)

### Download hubs
- Public meet: https://meet.jit.si
- Project: https://jitsi.org/downloads/

### Windows
1. For quick calls: open https://meet.jit.si in Brave/Firefox → start a meeting → share link.
2. Optional: install Jitsi desktop app from official downloads if listed.
3. Grant mic/camera permissions only for the browser/app you trust.

### macOS
1. Use https://meet.jit.si in a privacy browser.
2. Allow camera/mic prompts for that site only.
3. Optional official apps from jitsi.org/downloads if needed.

### Linux
1. Browser to https://meet.jit.si for zero install.
2. For self-host: follow Jitsi Docker/install docs on a Linux VPS.
3. Point your domain and TLS correctly.

### Android
1. Install Jitsi Meet from official store links on jitsi.org if you want an app.
2. Or join via mobile browser meeting links.
3. Deny unrelated permissions.

### iOS
1. Install official Jitsi Meet iOS app from App Store link via jitsi.org, or join via browser where supported.
2. Allow camera/mic for calls only.
3. Prefer Signal for 1:1 private calls when possible (see catch).

### First-run checklist
1. Prefer self-hosted or trusted instances for sensitive meetings.
2. Use waiting room/moderator controls when available.
3. Share links over Signal, not public social posts.

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| Need strongest 1:1 mobile call privacy with contacts already on it | Group/browser model differs | **Signal calls** | Yes | Mobile · desktop | Don’t force Signal for large webinars |
| Need full self-host team chat+calls suite | Jitsi is primarily meetings | **Element Call / Matrix** | Yes | All major + self-host | Don’t operate Matrix if you only need occasional meetings |
| Corporate requires Zoom | Policy lock-in | **Zoom with least privilege + no unnecessary cloud recording** | No | All major | Still prefer Jitsi/Signal when policy allows |

### Alternative installs

#### Signal calls
- https://signal.org/download/

#### Element / Matrix
- https://element.io/download

#### Zoom (compromise)
- Official zoom.us only; disable recording/AI features you don’t need

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | Self-hosted Jitsi |
| **Repo** | https://github.com/jitsi/docker-jitsi-meet |
| **What local means** | Meeting server on your infrastructure |
| **Who it’s for** | Teams/homelabs with a VPS |
| **Ops burden** | Medium–High |
| **When primary still wins** | Public meet.jit.si is enough for low-sensitivity calls |

### Local install
- Linux server: official Jitsi Docker guide
- Clients: browser or official mobile apps against your domain

---

## Quick decision box

```text
Default group calls                  →  Jitsi Meet
Private 1:1 with Signal contacts     →  Signal calls
Self-host meetings                   →  Jitsi Docker
Federated team stack                 →  Element/Matrix
```
