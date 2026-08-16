# Maps & Navigation

> Open Privacy · v1.0 · August 2026 · Poorvith M P  
> Category ID: `14-maps`  
> Replaces: Google Maps (continuous location history, ad profiles, route tracking)

---

## Primary recommendation

<img src="../../assets/logos/organicmaps.svg" width="36" height="36" alt="Organic Maps Logo">

| Field | Value |
|---|---|
| **Name** | Organic Maps |
| **Website** | https://organicmaps.app |
| **Source / repo** | https://github.com/organicmaps/organicmaps |
| **Open source?** | **Yes** (Apache 2.0) |
| **Local / self-host?** | **Yes** — runs 100% offline from local map packages on your device |
| **Target audience** | Drivers, hikers, cyclists, and pedestrians who want turn-by-turn navigation with zero telemetry |
| **Platforms** | <img src="../../assets/logos/android.svg" width="14" height="14" alt="Android"> Android · <img src="../../assets/logos/ios.svg" width="14" height="14" alt="iOS"> iOS · <img src="../../assets/logos/linux.svg" width="14" height="14" alt="Linux"> Linux (experimental) |
| **Pricing** | 100% Free (crowdfunded) |
| **Payment notes** | N/A |

### Why this is the one pick
1. 100% offline navigation powered by crowd-sourced OpenStreetMap (OSM) data.
2. Zero user tracking, zero data collection, zero telemetry, and zero ads.
3. Turn-by-turn voice navigation for driving, cycling, and walking.
4. Extremely battery-efficient and fast rendering engine.
5. Search, routing, and bookmarks work without an internet connection once map regions are downloaded.

### What it does not do
- Does not offer live crowdsourced traffic congestion layers like Google Maps / Waze.
- Satellite imagery is not included (vector map data only).
- Business opening hours and reviews are limited to OpenStreetMap community contributions.

---

## Install guide (primary)

### <img src="../../assets/logos/android.svg" width="18" height="18" alt="Android"> Android
- **F-Droid:** https://f-droid.org/packages/app.organicmaps/
- **Google Play:** https://play.google.com/store/apps/details?id=app.organicmaps
- **Direct APK:** https://github.com/organicmaps/organicmaps/releases

### <img src="../../assets/logos/ios.svg" width="18" height="18" alt="iOS"> iOS
- **App Store:** https://apps.apple.com/app/organic-maps-offline-hiking/id1567437057

### First-run checklist
1. Open the app while connected to Wi-Fi and download your home region/state map.
2. Download any route maps before traveling to areas with poor mobile reception.
3. Enable GPS location permissions (set to "Only while using app").

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| Need rich topographic contours, nautical charts, GPX recording, and advanced GIS layers | Organic Maps is designed for simplicity | <img src="../../assets/logos/organicmaps.svg" width="16" height="16" alt="OsmAnd"> **OsmAnd** | Yes (GPL 3.0) | Android · iOS | Don’t switch if you just want simple, fast driving or walking directions |
| Need turn-by-turn navigation in an existing Apple ecosystem with live traffic | Prefer Apple’s built-in platform privacy over OpenStreetMap | <img src="../../assets/logos/apple.svg" width="16" height="16" alt="Apple Maps"> **Apple Maps** | No | iOS · macOS | Don’t switch if you need cross-platform Android or Linux support |
| Need a quick web browser map without installing an app | Organic Maps is a mobile app | <img src="../../assets/logos/openstreetmap.svg" width="16" height="16" alt="OpenStreetMap"> **OpenStreetMap.org** | Yes | Web | Don’t use web maps for turn-by-turn driving navigation |

### Alternative installs

#### OsmAnd (Advanced Offline OSM)
- F-Droid: https://f-droid.org/packages/net.osmand.plus/
- Website: https://osmand.net

#### Apple Maps
- Built into iOS and macOS.

#### OpenStreetMap Web
- Navigate to: https://www.openstreetmap.org

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | Organic Maps / OsmAnd (Offline Map Packs) |
| **Repo** | https://github.com/organicmaps/organicmaps |
| **What local means** | Map databases and routing calculations reside 100% on your local device storage |
| **Who it’s for** | Everyone traveling without cellular data or seeking zero location leakage |
| **Ops burden** | Low (download map files once per month) |
| **When primary still wins** | Primary is already the offline local standard |

---

## Quick decision box

```text
Default offline navigation           →  Organic Maps
Advanced GIS / topography / hiking   →  OsmAnd
Live traffic in Apple ecosystem      →  Apple Maps
Quick browser web map lookup         →  OpenStreetMap.org
```
