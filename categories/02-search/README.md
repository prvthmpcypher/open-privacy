# Search Engine

> Open Privacy · v0.1 · July 2026 · Poorvith M P  
> Category ID: `02-search`  
> Replaces: Google Search

---

## Primary recommendation

| Field | Value |
|---|---|
| **Name** | Brave Search |
| **Website** | https://search.brave.com |
| **Source / repo** | https://brave.com/search/ |
| **Open source?** | **Partial** — hosted service; not a full self-hosted search stack |
| **Local / self-host?** | **No** (use SearXNG for self-host) |
| **Target audience** | Everyday users leaving Google Search |
| **Platforms** | Web · browser default · mobile browsers |
| **Pricing** | Free |
| **Payment notes** | N/A |

### Why this is the one pick
1. Independent index ambition with privacy-oriented defaults.
2. Works in any browser; pairs cleanly with Brave or Firefox.
3. Simple default-search setup without an account.
4. Practical result quality for daily queries.
5. Documented set-as-default flows.

### What it does not do
- Review the current privacy policy yourself; hosted search is not self-host.
- AI answer features are optional product surface.
- Not a replacement for specialized academic search.

---

## Install guide (primary)

### Download hubs
- Search: https://search.brave.com
- Set as default: https://search.brave.com/default

### Windows
1. Open browser settings (Brave / Firefox / Edge / Chrome).
2. Find **Search engine** / **Default search engine**.
3. Add or select **Brave Search** (https://search.brave.com).
4. Confirm a test query runs on search.brave.com.

### macOS
1. Open browser settings.
2. Set **Brave Search** as default search engine.
3. Optionally use https://search.brave.com/default for browser-specific buttons.

### Linux
1. Open browser settings.
2. Set default search engine to **Brave Search**.
3. Firefox: Settings → Search → Default Search Engine → add/select Brave Search.

### Android
1. Open Brave or Firefox for Android.
2. Settings → Search engine → choose **Brave Search** if listed, or set custom search URL per browser docs.
3. Run a test search from the address bar.

### iOS
1. Open Brave or Firefox for iOS.
2. Settings → default search engine → select **Brave Search** when available.
3. Safari has limited third-party search options; prefer Brave/Firefox app for Brave Search defaults.

### First-run checklist
1. Disable Google as default in every browser profile you use.
2. Clear old search shortcuts if the address bar still suggests Google.
3. Turn off AI answer features if you do not want them.

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| Want fully open-source metasearch you control | Brave Search is a hosted service | **SearXNG** | Yes | Self-host / public instances | Don’t self-host if you only need one-click hosted search |
| Prefer Google-like results with a privacy proxy | Some want Google results without Google account tracking | **Startpage** | No | Web | Don’t switch if you specifically want non-Google ranking |
| Want a long-standing no-profile brand with simple UX | Some users prefer DuckDuckGo defaults | **DuckDuckGo** | Partial | Web · apps | Don’t switch solely for branding if Brave Search already meets needs |

### Alternative installs

#### SearXNG
- **Linux self-host:** https://docs.searxng.org/admin/installation.html
- **Windows / macOS:** Docker Desktop + SearXNG Docker docs
- **Android / iOS:** open your instance URL in a mobile browser
- Public instances: https://searx.space/

#### Startpage
- **All platforms:** https://www.startpage.com — set as browser default search

#### DuckDuckGo
- **Web:** https://duckduckgo.com
- **Desktop / mobile:** browser default or DuckDuckGo apps where offered

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | SearXNG |
| **Repo** | https://github.com/searxng/searxng |
| **What local means** | Self-hosted metasearch |
| **Who it’s for** | Technical users with a small always-on host |
| **Ops burden** | Medium |
| **When primary still wins** | You want zero server maintenance |

### Local install
- **Docker:** https://docs.searxng.org/admin/installation-docker.html
- **Linux bare metal:** https://docs.searxng.org/admin/installation.html
- **Mobile:** use the instance URL in any browser

---

## Quick decision box

```text
Default private search              →  Brave Search
Self-host metasearch                →  SearXNG
Google results via privacy proxy    →  Startpage
Simple hosted alternative brand     →  DuckDuckGo
```
