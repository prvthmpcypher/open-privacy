# DNS Resolver

> Open Privacy · v0.1 · July 2026 · Poorvith M P  
> Category ID: `07-dns`  
> Replaces: ISP DNS

---

## Primary recommendation

| Field | Value |
|---|---|
| **Name** | Quad9 |
| **Website** | https://quad9.net |
| **Source / repo** | https://www.quad9.net/service/service-addresses-and-features/ |
| **Open source?** | **Service** — public recursive resolver |
| **Local / self-host?** | **No** as primary; Unbound/Pi-hole is local path |
| **Target audience** | Users who want a simple secure DNS drop-in |
| **Platforms** | Any OS via network DNS settings · routers |
| **Pricing** | Free |
| **Payment notes** | N/A |

### Why this is the one pick
1. Easy public DNS with security-oriented resolution.
2. Works on every OS and many routers.
3. No account required.
4. Clear endpoint addresses.
5. Good first step away from ISP DNS.

### What it does not do
- You still trust a third-party resolver.
- Not a VPN.
- Less customizable than NextDNS profiles.

---

## Install guide (primary)

### Download hubs
- https://quad9.net — use current resolver addresses from the site (commonly `9.9.9.9` and `149.112.112.112`)

### Windows
1. Settings → Network & Internet → active adapter → DNS → Edit.
2. Set Quad9 DNS addresses from quad9.net.
3. Save → run `ipconfig /flushdns`.

### macOS
1. System Settings → Network → service → Details → DNS.
2. Add Quad9 addresses.
3. Apply.

### Linux
1. Set DNS in NetworkManager or systemd-resolved per your distro.
2. Example: IPv4 DNS fields → Quad9 addresses.
3. Reconnect or restart NetworkManager.

### Android
1. Settings → Network → Private DNS if hostname mode is documented by Quad9, **or** set DNS per Wi‑Fi advanced options.
2. Use values/hostnames published on quad9.net for Android.
3. Test browsing.

### iOS
1. Wi‑Fi → (i) → Configure DNS → Manual → add Quad9 servers.
2. For cellular, use only trusted configuration methods if required.
3. Verify connectivity.

### First-run checklist
1. Run a DNS leak test.
2. Check VPN DNS settings for conflicts.
3. Document settings so you can revert.

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| Want account-based blocklists and per-device analytics | Quad9 is simple public DNS | **NextDNS** | Partial | All | Don’t add complexity if basic secure DNS is enough |
| Want fully local recursive resolver | Public DNS is still third-party | **Unbound** | Yes | Linux primarily | Don’t run local recursive if you cannot keep it updated |
| Want network-wide ad blocking at home | DNS choice alone isn’t a home gateway filter | **Pi-hole** | Yes | Linux / self-host | Don’t deploy Pi-hole on a machine you can’t keep online |

### Alternative installs

#### NextDNS
- https://nextdns.io — create config → set DoH/Private DNS endpoints shown for each OS

#### Unbound
- https://nlnetlabs.nl/projects/unbound/about/ — install `unbound` on Linux; point LAN clients to it

#### Pi-hole
- https://docs.pi-hole.net/main/basic-install/
- Set upstream DNS to Quad9/NextDNS/Mullvad DNS as preferred

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | Unbound |
| **Repo** | https://github.com/NLnetLabs/unbound |
| **What local means** | DNS resolution on hardware you control |
| **Who it’s for** | Homelab users |
| **Ops burden** | Medium |
| **When primary still wins** | You want zero local services |

### Local install
- **Linux:** install and configure `unbound`
- **Clients:** point devices at your Unbound host

---

## Quick decision box

```text
Default easy private DNS            →  Quad9
Custom blocklists                    →  NextDNS
Local resolver                       →  Unbound
Home network blocking                →  Pi-hole
```
