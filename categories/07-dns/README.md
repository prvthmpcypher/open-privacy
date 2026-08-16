# DNS Resolver

> Open Privacy · v0.2 · August 2026 · Poorvith M P  
> Category ID: `07-dns`  
> Replaces: ISP DNS (unencrypted, logging, censoring)

---

## Primary recommendation

<img src="../../assets/logos/quad9.svg" width="36" height="36" alt="Quad9 Logo">

| Field | Value |
|---|---|
| **Name** | Quad9 |
| **Website** | https://quad9.net |
| **Source / repo** | https://www.quad9.net/service/service-addresses-and-features/ |
| **Open source?** | **Service** — Swiss non-profit foundation operating recursive DNS |
| **Local / self-host?** | **No** as a global anycast service; Unbound / Pi-hole for local path |
| **Target audience** | Everyday users who want secure, malware-blocking DNS resolution without an account |
| **Platforms** | Any OS via network settings · Routers · Android Private DNS |
| **Pricing** | 100% Free |
| **Payment notes** | N/A |

### Why this is the one pick
1. Governed by a non-profit foundation based in Switzerland under strict Swiss data privacy regulations.
2. Does not log query data, IP addresses, or build advertising profiles.
3. Automatically blocks known malicious phishing and malware domains using real-time threat intelligence.
4. Supports modern encrypted DNS protocols: DNS-over-HTTPS (DoH), DNS-over-TLS (DoT), and DNSCrypt.
5. Zero account creation or app installation required.

### What it does not do
- Does not offer custom per-device ad-blocking rules or dashboard logs (NextDNS does).
- You still trust the resolver not to log queries.
- A DNS resolver encrypts domain lookups, but does not hide your destination IP from your ISP (a VPN is required for that).

---

## Install guide (primary)

### DNS Server Addresses
- **IPv4 Primary:** `9.9.9.9`
- **IPv4 Secondary:** `149.112.112.112`
- **IPv6 Primary:** `2620:fe::fe`
- **IPv6 Secondary:** `2620:fe::9`
- **DoH Endpoint:** `https://dns.quad9.net/dns-query`
- **DoT Endpoint:** `dns.quad9.net` (Port 853)
- **Android Private DNS Hostname:** `dns.quad9.net`

### Android (Private DNS)
1. Open **Settings** → **Network & Internet** (or **Connections**).
2. Tap **Private DNS** → Select **Private DNS provider hostname**.
3. Enter `dns.quad9.net` and tap **Save**.

### Windows 11 / 10
1. Settings → Network & Internet → Advanced network settings → Network adapters → Click your connection → Edit DNS.
2. Set IPv4 to **Manual**:
   - Preferred DNS: `9.9.9.9` (Set DNS over HTTPS to **On (automatic template)**).
   - Alternate DNS: `149.112.112.112`.
3. Save and flush cache in terminal: `ipconfig /flushdns`.

### macOS
1. System Settings → Network → Select active connection (Wi-Fi or Ethernet) → Details → **DNS**.
2. Click `+` and add `9.9.9.9` and `149.112.112.112`.
3. Click **OK** → **Apply**.

### Linux
Set in NetworkManager or `/etc/systemd/resolved.conf`:
```ini
[Resolve]
DNS=9.9.9.9 149.112.112.112 2620:fe::fe 2620:fe::9
DNSOverTLS=yes
```

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| Want custom blocklists, parental controls, and query analytics | Quad9 is a fixed public resolver | **NextDNS** | Partial | All major | Don’t switch if you want a zero-account setup |
| Want fully local recursive resolution without upstream trust | Public DNS requires trusting an external resolver | **Unbound** | Yes | Linux · Self-Host | Don’t run Unbound if you cannot maintain recursive cache updates |
| Want whole-home ad and tracker blocking on your LAN | DNS resolution alone does not block in-app telemetry | **Pi-hole** | Yes | Linux / Raspberry Pi | Don’t deploy Pi-hole on a machine that doesn't stay online 24/7 |

### Alternative installs

#### NextDNS
- Setup dashboard and configs: https://nextdns.io

#### Unbound (Recursive DNS)
- Official documentation: https://nlnetlabs.nl/projects/unbound/about/

#### Pi-hole (Network-Wide Ad Blocker)
- Official install script: https://docs.pi-hole.net/main/basic-install/

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | Unbound / Pi-hole |
| **Repo** | https://github.com/NLnetLabs/unbound |
| **What local means** | Resolves root zone DNS directly on your local hardware |
| **Who it’s for** | Homelab operators and privacy power users |
| **Ops burden** | Medium |
| **When primary still wins** | You want instant malware filtering with zero maintenance |

---

## Quick decision box

```text
Default secure public DNS           →  Quad9
Custom blocklists & per-device logs  →  NextDNS
Local recursive resolver             →  Unbound
Whole-home LAN ad-blocking filter    →  Pi-hole
```
