# Browser Extensions (Tracker Block)

> Open Privacy · v0.1 · July 2026 · Poorvith M P  
> Category ID: `21-browser-extensions`  
> Replaces: Browsing with no tracker blocking; “cleaner” adware extensions

---

## Primary recommendation

| Field | Value |
|---|---|
| **Name** | uBlock Origin |
| **Website** | https://ublockorigin.com |
| **Source / repo** | https://github.com/gorhill/uBlock |
| **Open source?** | **Yes** |
| **Local / self-host?** | **Yes** — runs entirely in the browser |
| **Target audience** | Everyone who browses the web on a desktop browser |
| **Platforms** | Firefox (best support) · Chromium browsers where still available |
| **Pricing** | Free |
| **Payment notes** | N/A |

### Why this is the one pick
1. Effective, open-source content blocker.
2. Low resource use relative to heavy “suite” extensions.
3. Transparent filter lists you control.
4. Standard recommendation across privacy communities.
5. Works well alongside a privacy browser.

### What it does not do
- Not a VPN.
- Manifest V3 / Chromium store policy can limit some browsers—prefer Firefox when possible.
- Will not fix malicious sites you intentionally visit.

---

## Install guide (primary)

### Download hubs
- https://ublockorigin.com
- Firefox: https://addons.mozilla.org/firefox/addon/ublock-origin/

### Windows
1. Open Firefox (recommended) or a Chromium browser that still offers uBlock Origin.
2. Install from the official add-ons listing linked via ublockorigin.com.
3. Pin the extension; leave default lists enabled initially.

### macOS
1. Same as Windows: install from official browser add-on stores only.
2. Avoid third-party “uBlock” clones.
3. Confirm the publisher is Raymond Hill / uBlock Origin.

### Linux
1. Install Firefox from your distro or Mozilla.
2. Install uBlock Origin from addons.mozilla.org.
3. Keep the extension updated with the browser.

### Android
1. Use Firefox for Android.
2. Install uBlock Origin from the Firefox Add-ons site/add-ons manager.
3. Chromium Android browsers generally lack full extension support.

### iOS
1. Full uBlock Origin is not available like desktop Firefox.
2. Use content blockers built into Brave/Firefox iOS or Safari content blockers carefully.
3. Prefer a privacy browser’s built-in shields on iOS.

### First-run checklist
1. Do not install five overlapping blockers.
2. Disable cosmetic filtering only if a site breaks and you must.
3. Review filter list updates occasionally.

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| On Brave already with Shields | Extra extension may be redundant | **Brave Shields only** | Partial | Brave | Add uBO on Firefox profiles still |
| Need strict cookie/tracker UI different from uBO | UX preference | **Firefox Strict Tracking Protection** | Yes | Firefox | Don’t disable uBO if you rely on custom filters |
| iOS-only user | Extension model differs | **Brave iOS Shields / Safari content blocker** | Varies | iOS | Don’t install fake “uBlock” iOS apps |

### Alternative installs

#### Brave Shields only
- Built into Brave — no separate install

#### Firefox Strict Tracking Protection
- Firefox Settings → Privacy & Security → Strict

#### Brave iOS / Safari content blockers
- Configure in iOS Settings → Brave/Safari → content blockers

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | uBlock Origin |
| **Repo** | https://github.com/gorhill/uBlock |
| **What local means** | Filtering runs on-device in the browser |
| **Who it’s for** | All desktop browser users |
| **Ops burden** | Low |
| **When primary still wins** | Primary is already local FOSS |

### Local install
- Install only from official browser add-on stores linked via ublockorigin.com

---

## Quick decision box

```text
Default tracker block                →  uBlock Origin (Firefox)
Already on Brave                     →  Shields (+ optional uBO where supported)
iOS                                  →  Browser built-in blockers
```
