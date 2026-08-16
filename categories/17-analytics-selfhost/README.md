# Web Analytics (Self-Host)

> Open Privacy · v0.2 · August 2026 · Poorvith M P  
> Category ID: `17-analytics-selfhost`  
> Replaces: Google Analytics 4 (GA4 cross-site tracking, cookie banners)

---

## Primary recommendation

<img src="../../assets/logos/umami.svg" width="36" height="36" alt="Umami Logo">

| Field | Value |
|---|---|
| **Name** | Umami |
| **Website** | https://umami.is |
| **Source / repo** | https://github.com/umami-software/umami |
| **Open source?** | **Yes** (MIT) |
| **Local / self-host?** | **Yes** — lightweight Docker container with PostgreSQL |
| **Target audience** | Website owners and developers who need clean, GDPR-compliant analytics without cookies |
| **Platforms** | Linux · Docker · Node.js · Cloud hosted available |
| **Pricing** | 100% Free self-hosted; optional paid cloud tier |
| **Payment notes** | N/A for self-hosted |

### Why this is the one pick
1. 100% open source under the permissive MIT license.
2. Privacy-first by design: does not collect personal data, does not use cookies, does not track users across websites, and is fully GDPR and CCPA compliant out of the box.
3. Extremely lightweight tracking script (< 3 KB) with fast page load performance.
4. Clean, real-time dashboard displaying visitors, pageviews, referrers, devices, and countries.
5. Self-hostable on a $5/mo VPS using Docker Compose.

### What it does not do
- Does not build persistent user profiles across the web like Google Analytics.
- Does not offer deep marketing attribution funnels for complex enterprise advertising campaigns.

---

## Install guide (primary)

### Self-Hosted Docker Compose
Create a `docker-compose.yml` file:
```yaml
version: '3'
services:
  umami-db:
    image: postgres:16-alpine
    environment:
      POSTGRES_DB: umami
      POSTGRES_USER: umami
      POSTGRES_PASSWORD: your_db_password_here
    volumes:
      - umami-db-data:/var/lib/postgresql/data
    restart: always

  umami:
    image: ghcr.io/umami-software/umami:postgresql-latest
    ports:
      - "3000:3000"
    environment:
      DATABASE_URL: postgresql://umami:your_db_password_here@umami-db:5432/umami
      DATABASE_TYPE: postgresql
      APP_SECRET: replace_with_random_secret_string
    depends_on:
      - umami-db
    restart: always

volumes:
  umami-db-data:
```

Run:
```bash
docker compose up -d
```
Log in at `http://localhost:3000` (Default credentials: `admin` / `umami` — change password immediately).

### Adding Tracking Script to Your Website
```html
<script defer src="https://your-umami-domain.com/script.js" data-website-id="your-website-id"></script>
```

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| Want zero server maintenance with hosted EU cloud | Prefer not running your own Docker infrastructure | **Plausible Cloud** | Partial | Cloud | Don’t switch if you want 100% free self-hosting on your own VPS |
| Need ultra-light single-binary Go analytics with SQLite | Umami requires PostgreSQL and Node/Docker | **GoatCounter** | Yes (EUPL) | Single Binary · Web | Don’t switch if you want a rich graphical dashboard with custom event tracking |
| Need enterprise feature depth and heatmaps | Umami focuses on essential traffic metrics | **Matomo** | Yes | PHP / MySQL | Don’t deploy Matomo if you want a modern, lightweight, non-resource-heavy dashboard |

### Alternative installs

#### Plausible Analytics
- Website: https://plausible.io

#### GoatCounter (Single Binary Analytics)
- Website: https://www.goatcounter.com / https://github.com/arp242/goatcounter

#### Matomo
- Website: https://matomo.org

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | Umami / GoatCounter |
| **Repo** | https://github.com/umami-software/umami |
| **What local means** | Analytics server and visitor database run on your physical hardware or private VPS |
| **Who it’s for** | Web developers, bloggers, and site operators |
| **Ops burden** | Low (Docker Compose) |
| **When primary still wins** | Primary is already the self-hosted open-source standard |

---

## Quick decision box

```text
Default self-hosted web analytics   →  Umami
Hosted zero-maintenance EU cloud    →  Plausible Cloud
Ultra-light single Go binary         →  GoatCounter
Deep enterprise tracking suite       →  Matomo
```
