# Calendar & Contacts

> Open Privacy · v0.1 · July 2026 · Poorvith M P  
> Category ID: `13-calendar-contacts`  
> Replaces: Google Calendar / Google Contacts defaults

---

## Primary recommendation

| Field | Value |
|---|---|
| **Name** | Proton Calendar (+ Proton contacts via Proton account) |
| **Website** | https://proton.me/calendar |
| **Source / repo** | https://proton.me |
| **Open source?** | **Partial** — Proton clients often open; service hosted |
| **Local / self-host?** | **No** as primary SaaS |
| **Target audience** | Users leaving Google Calendar who want encrypted-friendly hosted calendar |
| **Platforms** | Web · mobile apps · desktop via Proton ecosystem |
| **Pricing** | Free tier + paid |
| **Payment notes** | Card via Proton |

### Why this is the one pick
1. Practical hosted calendar alternative to Google.
2. Fits Proton Mail users.
3. Multi-platform access.
4. Lower ops than self-hosting CalDAV.
5. Clear privacy-oriented vendor positioning.

### What it does not do
- Not every Google Calendar power feature.
- Sharing with non-Proton users can be awkward.
- Not fully self-hosted.

---

## Install guide (primary)

### Download hubs
- https://proton.me/calendar
- Proton mobile apps from https://proton.me/mail/download (calendar included in Proton mobile suite flows)

### Windows
1. Create/login Proton account.
2. Use https://calendar.proton.me in browser, or Proton desktop apps where calendar is integrated.
3. Create calendars and optional import from Google ICS export.

### macOS
1. Use web calendar or Proton apps.
2. For Apple Calendar subscription/import, use export/ICS options Proton provides when available.
3. Prefer official Proton apps for encrypted features.

### Linux
1. Use https://calendar.proton.me in browser.
2. Optional: desktop integration via supported CalDAV/Bridge features on paid plans if offered—verify current Proton docs.

### Android
1. Install Proton Calendar / Proton Mail app suite components listed by Proton for calendar.
2. Sign in and enable notifications.
3. Disable Google Calendar sync for migrated accounts if leaving Google.

### iOS
1. Install Proton Calendar from App Store links on proton.me.
2. Sign in; allow calendar notifications.
3. Import existing calendars carefully.

### First-run checklist
1. Enable account 2FA.
2. Export Google Calendar ICS before cutting over.
3. Update shared calendars with collaborators.

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| Need full self-hosted CalDAV/CardDAV | Proton is SaaS | **Nextcloud Calendar/Contacts** | Yes | Self-host + clients | Don’t self-host without backups |
| Prefer Tuta stack | Vendor preference | **Tuta Calendar** | Partial | Apps · web | Don’t split mail/calendar vendors casually |
| Need offline-first FOSS desktop PIM | Different workflow | **Thunderbird + local address book/calendar** | Yes | Desktop | Don’t use if you need seamless mobile-first hosted UX |

### Alternative installs

#### Nextcloud Calendar/Contacts
- Server + apps: https://nextcloud.com/install/

#### Tuta Calendar
- https://tuta.com — calendar features in Tuta apps

#### Thunderbird
- https://www.thunderbird.net

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | Nextcloud Calendar + Contacts |
| **Repo** | https://github.com/nextcloud/server |
| **What local means** | CalDAV/CardDAV on your server |
| **Who it’s for** | Homelab users |
| **Ops burden** | Medium–High |
| **When primary still wins** | You want zero server maintenance |

### Local install
- Install Nextcloud server; enable Calendar/Contacts apps
- Connect DAVx⁵ (Android) / iOS accounts / desktop clients via CalDAV/CardDAV

---

## Quick decision box

```text
Default hosted private calendar      →  Proton Calendar
Self-host CalDAV                     →  Nextcloud
Tuta ecosystem                       →  Tuta Calendar
Desktop FOSS PIM                     →  Thunderbird
```
