# Web Analytics (Self-Host)

> Open Privacy · v0.1 · July 2026 · Poorvith M P  
> Category ID: `17-analytics-selfhost`  
> Replaces: Google Analytics

---

## Primary recommendation

| Field | Value |
|---|---|
| **Name** | Umami |
| **Website** | https://umami.is |
| **Source / repo** | https://github.com/umami-software/umami |
| **Open source?** | **Yes** (MIT) |
| **Local / self-host?** | **Yes** |
| **Target audience** | Site owners who need privacy-friendly analytics they control |
| **Platforms** | Self-host on Linux/Docker; dashboards via web |
| **Pricing** | Free self-host; optional cloud |
| **Payment notes** | N/A for self-host |

### Why this is the one pick
1. Simple, privacy-oriented analytics.
2. Fully open source and self-hostable.
3. Lightweight compared to enterprise suites.
4. Easy script tag integration.
5. Good default away from Google Analytics.

### What it does not do
- Not a full marketing attribution suite.
- You must secure and update the server.
- Cookie/consent needs still depend on your jurisdiction and config.

---

## Install guide (primary)

### Download hubs
- https://umami.is
- Docs: https://umami.is/docs

### Windows
1. Prefer running the server on Linux/Docker host, not Windows desktop.
2. Use Docker Desktop only for lab installs if needed.
3. Manage production on a VPS/Linux box.

### macOS
1. Same as Windows: local Docker only for testing.
2. Production on Linux server.
3. Open the web UI from any browser after deploy.

### Linux
1. Follow official install docs: https://umami.is/docs/install
2. Typical path: Docker Compose with Postgres + Umami container.
3. Create admin user; add your website; copy tracking snippet to your site.

### Android
1. Not applicable as a server install target.
2. View dashboards in a mobile browser if needed.
3. Do not install random “analytics” apps claiming Umami.

### iOS
1. Not applicable as a server install target.
2. Use mobile Safari/Brave for dashboard access.
3. Keep admin 2FA on the host account where possible.

### First-run checklist
1. Put Umami behind HTTPS.
2. Restrict admin panel exposure.
3. Verify only expected events appear after adding the script.

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| Want hosted privacy analytics without ops | Self-host burden | **Plausible Cloud** | Partial (core OSS) | Hosted | Don’t pay for cloud if you already run homelab happily |
| Need Matomo-level feature depth | Umami is intentionally simple | **Matomo** | Yes | Self-host | Don’t take Matomo complexity if simple counts suffice |
| Want cookieless tiny self-host | Preference | **GoatCounter** | Yes | Self-host / hosted | Don’t switch for branding alone |

### Alternative installs

#### Plausible Cloud
- https://plausible.io

#### Matomo
- https://matomo.org/docs/installation/

#### GoatCounter
- https://www.goatcounter.com — self-host instructions on site/docs

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | Umami (self-host) |
| **Repo** | https://github.com/umami-software/umami |
| **What local means** | Analytics data stays on your server |
| **Who it’s for** | Site operators |
| **Ops burden** | Medium |
| **When primary still wins** | Primary is already self-host FOSS |

### Local install
- Docker Compose per https://umami.is/docs/install on Linux

---

## Quick decision box

```text
Default self-host analytics          →  Umami
Hosted simple privacy analytics      →  Plausible Cloud
Feature-rich self-host               →  Matomo
Tiny alternative                     →  GoatCounter
```
