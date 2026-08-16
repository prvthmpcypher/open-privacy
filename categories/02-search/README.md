# Search Engine

> Open Privacy · v0.2 · August 2026 · Poorvith M P  
> Category ID: `02-search`  
> Replaces: Google Search (default tracking), Bing

---

## Primary recommendation

<img src="../../assets/logos/brave-search.svg" width="36" height="36" alt="Brave Search Logo">

| Field | Value |
|---|---|
| **Name** | Brave Search |
| **Website** | https://search.brave.com |
| **Source / repo** | https://github.com/brave |
| **Open source?** | **No** — web service index is proprietary; client apps are open source |
| **Local / self-host?** | **No** as a web index; SearXNG is the local self-host path |
| **Target audience** | Everyday users who want an independent search index without profiling or user tracking |
| **Platforms** | Web (any browser) · Android · iOS |
| **Pricing** | Free (ad-supported or optional ad-free subscription) |
| **Payment notes** | N/A for free tier |

### Why this is the one pick
1. Builds its own independent web index rather than relying on Google or Bing APIs.
2. Does not build user profiles, track queries, or sell search history to advertisers.
3. Clean, fast UI with privacy-respecting AI answer summaries (Answer with AI).
4. Works out of the box in any browser by visiting `search.brave.com`.
5. No account required to search.

### What it does not do
- The backend search index is proprietary and hosted on Brave servers.
- Long-tail regional queries in smaller languages can sometimes lag Google.
- Does not replace network-level encryption or browser isolation.

---

## Install guide (primary)

### Web & Browser Default Setup
1. Open your browser and navigate to https://search.brave.com.
2. To set Brave Search as your default search engine:
   - **In Brave Browser**: Enabled by default.
   - **In Firefox**: Settings → Search → Default Search Engine → Select **Brave**.
   - **In Chrome / Safari**: Visit https://search.brave.com/default and follow the one-click prompt.

### Android / iOS
1. Use directly within your default mobile browser at https://search.brave.com.
2. Or set as default search engine in your mobile browser settings.

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| Want 100% self-hosted metasearch without telemetry | Brave Search is a hosted web service | **SearXNG** | Yes | Docker · Linux | Don’t self-host if you cannot maintain a server and proxy setup |
| Prefer Google result quality without Google tracking | Brave index differs on niche technical queries | **Startpage** | No | Web | Don’t switch if you prefer an independent web index over Google syndication |
| Want established brand with built-in email/app protection | Preference for DuckDuckGo ecosystem | **DuckDuckGo** | Partial | Web · Mobile | Don’t switch if independent web indexing is your top priority |

### Alternative installs

#### SearXNG
- Official repo: https://github.com/searxng/searxng
- Docker one-liner:
```bash
docker run -d -p 8080:8080 --name searxng -v "${PWD}/searxng:/etc/searxng" docker.io/searxng/searxng:latest
```

#### Startpage
- Navigate to https://www.startpage.com and set as default search engine.

#### DuckDuckGo
- Navigate to https://duckduckgo.com.

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | SearXNG |
| **Repo** | https://github.com/searxng/searxng |
| **What local means** | Self-hosted metasearch engine aggregating queries anonymously |
| **Who it’s for** | Homelab and self-hosters |
| **Ops burden** | Medium |
| **When primary still wins** | You want instant, zero-maintenance independent search results |

### Local install
- Follow SearXNG Docker installation guide: https://docs.searxng.org/admin/installation-docker.html

---

## Quick decision box

```text
Default independent search          →  Brave Search
Self-hosted metasearch               →  SearXNG
Google results without Google        →  Startpage
Simple privacy brand                 →  DuckDuckGo
```
