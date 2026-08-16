# Video / Audio Calls

> Open Privacy · v1.0 · August 2026 · Poorvith M P  
> Category ID: `23-video-calls`  
> Replaces: Zoom, Google Meet, Microsoft Teams (account lock-in, telemetry, AI call scraping)

---

## Primary recommendation

<img src="../../assets/logos/jitsi.svg" width="36" height="36" alt="Jitsi Meet Logo">

| Field | Value |
|---|---|
| **Name** | Jitsi Meet |
| **Website** | https://meet.jit.si |
| **Source / repo** | https://github.com/jitsi/jitsi-meet |
| **Open source?** | **Yes** (Apache 2.0) |
| **Local / self-host?** | **Yes** — official Docker Compose stack |
| **Target audience** | Groups and teams who need instant, browser-based video meetings without requiring an account |
| **Platforms** | Web · <img src="../../assets/logos/android.svg" width="14" height="14" alt="Android"> Android · <img src="../../assets/logos/ios.svg" width="14" height="14" alt="iOS"> iOS · Self-Host |
| **Pricing** | 100% Free public instance; self-host costs are your VPS |
| **Payment notes** | N/A |

### Why this is the one pick
1. 100% open source and works directly in any modern web browser with zero software installation for participants.
2. Supports room passwords, lobby mode, and optional end-to-end encryption (E2EE) in Chromium browsers.
3. Participants do not need to register an account, sign in, or disclose personal identifying info.
4. Includes screen sharing, meeting recording, and live YouTube streaming integrations.
5. Can be completely self-hosted on a Debian/Ubuntu VPS or via Docker in under 15 minutes.

### What it does not do
- Public instance (`meet.jit.si`) requires moderator authentication (via GitHub/Google/anonymous) to create rooms to prevent spam.
- Large meetings (50+ participants) require a well-provisioned dedicated self-hosted server.

---

## Install guide (primary)

### Instant Browser Meeting
1. Open your browser and navigate to https://meet.jit.si.
2. Enter a unique room name and start the call.
3. Share the room link with participants.
4. (Optional) Set a room password or enable End-to-End Encryption in the meeting security settings.

### Mobile Apps
- **Android:** https://play.google.com/store/apps/details?id=org.jitsi.meet (or F-Droid)
- **iOS:** https://apps.apple.com/app/jitsi-meet/id1165103905

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| Need mobile-first 1:1 and small group encrypted voice/video calls with family | Jitsi is room-based rather than contact-based | <img src="../../assets/logos/signal.svg" width="16" height="16" alt="Signal"> **Signal Group Calls** | Yes | All major | Don’t switch if participants don’t have Signal accounts |
| Need a complete decentralized team workspace with persistent rooms and calls | Jitsi is focused on standalone meetings | <img src="../../assets/logos/element.svg" width="16" height="16" alt="Element Call"> **Element Call (Matrix)** | Yes | All major | Don’t deploy Matrix if you just need quick one-off video links |
| Corporate requirement mandates Zoom | Workplace policy restricts open-source web conferencing | **Zoom (Least Privilege Mode)** | No | All major | Don’t use Zoom for private personal communication |

### Alternative installs

#### Signal Group Calls
- Up to 50 participants with end-to-end encryption built into Signal (see `05-messenger`).

#### Element Call (Native Matrix Video)
- Website: https://call.element.io

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | Jitsi Meet (Self-Hosted Docker) |
| **Repo** | https://github.com/jitsi/docker-jitsi-meet |
| **What local means** | WebRTC signaling and media bridge run entirely on your private server infrastructure |
| **Who it’s for** | Organizations, teams, and homelab operators |
| **Ops burden** | Medium |
| **When primary still wins** | Public instance provides instant zero-ops meetings |

### Self-Hosted Quickstart (Docker)
```bash
git clone https://github.com/jitsi/docker-jitsi-meet && cd docker-jitsi-meet
cp env.example .env
./gen-passwords.sh
mkdir -p ~/.jitsi-meet-cfg/{web,transcripts,prosody/config,prosody/prosody-plugins-custom,jicofo,jvb,jigasi,jibri}
docker compose up -d
```

---

## Quick decision box

```text
Default browser-based group meetings→  Jitsi Meet
Encrypted mobile 1:1 & small groups  →  Signal Calls
Decentralized team room calls        →  Element Call
Self-hosted dedicated video bridge   →  Jitsi Docker
```
