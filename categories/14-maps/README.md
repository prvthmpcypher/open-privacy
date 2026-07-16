# Maps & Navigation

> Open Privacy · v0.1 · July 2026 · Poorvith M P  
> Category ID: `14-maps`  
> Replaces: Google Maps as default

---

## Primary recommendation

| Field | Value |
|---|---|
| **Name** | Organic Maps |
| **Website** | https://organicmaps.app |
| **Source / repo** | https://github.com/organicmaps/organicmaps |
| **Open source?** | **Yes** |
| **Local / self-host?** | **Yes** — offline maps on device |
| **Target audience** | Everyday navigation without Google account tracking |
| **Platforms** | Android · iOS · desktop builds per project |
| **Pricing** | Free |
| **Payment notes** | N/A |

### Why this is the one pick
1. Open-source offline maps based on OpenStreetMap.
2. No Google account required.
3. Strong privacy posture for navigation.
4. Works offline after downloading regions.
5. Practical daily driver for many cities.

### What it does not do
- Business data/reviews can lag Google Maps.
- Transit features vary by region.
- Live traffic density may be weaker than Google.

---

## Install guide (primary)

### Download hubs
- https://organicmaps.app
- Stores linked from the site (Play Store, App Store, F-Droid, etc.)

### Windows
1. Check organicmaps.app for current desktop options.
2. If desktop build is listed, install from official links only.
3. Otherwise use Android/iOS as primary navigation clients.

### macOS
1. Check organicmaps.app for macOS availability.
2. Install only from official project links.
3. Download offline map regions after install.

### Linux
1. Install via Flatpak/package if published on organicmaps.app, or build from GitHub releases.
2. Launch and download offline maps for your region.

### Android
1. Install Organic Maps from F-Droid / Play Store link on organicmaps.app.
2. Open app → download offline maps for your areas.
3. Grant location permission only while using the app if preferred.

### iOS
1. Install from App Store link on organicmaps.app.
2. Download offline regions over Wi‑Fi.
3. Set as preferred navigation app where iOS allows.

### First-run checklist
1. Download offline maps before travel.
2. Disable unnecessary background location.
3. Keep OSM edits separate from navigation accountless use.

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| Need richer OSM app with more modes | Feature preference | **OsmAnd** | Yes | Android · iOS | Don’t switch if Organic Maps already meets offline needs |
| Need turn-by-turn in a full private phone stack already using Apple | Ecosystem convenience | **Apple Maps** | No | iOS · macOS | Don’t use if you are leaving Apple ecosystem |
| Need web maps without app install | No install allowed | **OpenStreetMap.org web** | Yes (data) | Web | Don’t rely on web-only for offline hiking |

### Alternative installs

#### OsmAnd
- https://osmand.net/docs/versions/ — Android/iOS downloads

#### Apple Maps
- Built into iOS/macOS

#### OpenStreetMap web
- https://www.openstreetmap.org

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | Organic Maps / OsmAnd offline map packs |
| **Repo** | https://github.com/organicmaps/organicmaps |
| **What local means** | Map data stored on device |
| **Who it’s for** | Travelers and privacy users |
| **Ops burden** | Low |
| **When primary still wins** | Primary already is local offline FOSS |

### Local install
- Install Organic Maps; download offline regions in-app

---

## Quick decision box

```text
Default private offline maps         →  Organic Maps
More power-user OSM features         →  OsmAnd
iOS system maps                      →  Apple Maps
Web only                             →  openstreetmap.org
```
