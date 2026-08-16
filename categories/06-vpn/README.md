# VPN

> Open Privacy · v0.2 · August 2026 · Poorvith M P  
> Category ID: `06-vpn`  
> Replaces: Commercial logging VPNs, ISP surveillance on public/home networks

---

## Primary recommendation

<img src="../../assets/logos/mullvad.svg" width="36" height="36" alt="Mullvad VPN Logo">

| Field | Value |
|---|---|
| **Name** | Mullvad VPN |
| **Website** | https://mullvad.net |
| **Source / repo** | https://github.com/mullvad/mullvadvpn-app |
| **Open source?** | **Yes** (GPL 3.0 Apps) |
| **Local / self-host?** | **No** as a multi-country VPN service; WireGuard on a VPS for self-host |
| **Target audience** | Users who want a strict no-logs VPN with zero personal identifying information required |
| **Platforms** | <img src="../../assets/logos/windows.svg" width="14" height="14" alt="Windows"> Windows · <img src="../../assets/logos/macos.svg" width="14" height="14" alt="macOS"> macOS · <img src="../../assets/logos/linux.svg" width="14" height="14" alt="Linux"> Linux · <img src="../../assets/logos/android.svg" width="14" height="14" alt="Android"> Android · <img src="../../assets/logos/ios.svg" width="14" height="14" alt="iOS"> iOS · Routers |
| **Pricing** | Flat €5 / month |
| **Payment notes** | Cash (by mail), Monero, Bitcoin, Credit Card, PayPal |

### Why this is the one pick
1. Generates a random 16-digit account number; no email, username, or phone number required to sign up.
2. Accepts cash by mail and Monero for unlinkable payments.
3. 100% open-source desktop and mobile client applications.
4. Uses modern WireGuard protocol with post-quantum cryptography support and multi-hop routing.
5. Strict audited no-logs infrastructure under Swedish jurisdiction.

### What it does not do
- A VPN protects network transit; it does not make you anonymous against browser fingerprinting (Tor Browser is needed for anonymity).
- Paid only (flat €5/mo); does not have a perpetual free tier.
- Port forwarding is disabled.

---

## Install guide (primary)

### Account Setup
1. Visit https://mullvad.net/account and click **Generate account number**.
2. Save your 16-digit account number in your password manager.
3. Add time via cash, crypto, or card.

### <img src="../../assets/logos/linux.svg" width="18" height="18" alt="Linux"> Linux (Debian, Ubuntu)
```bash
sudo curl -fsSLo /usr/share/keyrings/mullvad-keyring.asc https://repository.mullvad.net/deb/mullvad-keyring.asc
echo "deb [signed-by=/usr/share/keyrings/mullvad-keyring.asc arch=$(dpkg --print-architecture)] https://repository.mullvad.net/deb/stable $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/mullvad.list
sudo apt update && sudo apt install mullvad-vpn
```

### <img src="../../assets/logos/windows.svg" width="18" height="18" alt="Windows"> Windows & macOS
- **Windows:** Download `.exe` from https://mullvad.net/download (or `winget install MullvadVPN.MullvadVPN`).
- **macOS:** Download `.pkg` from https://mullvad.net/download (or `brew install --cask mullvadvpn`).

### <img src="../../assets/logos/android.svg" width="18" height="18" alt="Android"> Android & iOS
- **Android:** https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn (or F-Droid / GitHub APK)
- **iOS:** https://apps.apple.com/app/mullvad-vpn/id1488466513

### First-run checklist
1. Enter your 16-digit account number and connect.
2. In app settings, enable **Always-on VPN** and **Kill Switch / Lockdown Mode**.
3. Verify DNS leak protection at https://mullvad.net/check.

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| Need a free tier to protect basic Wi-Fi browsing | Mullvad is paid-only (€5/mo) | <img src="../../assets/logos/protonvpn.svg" width="16" height="16" alt="Proton VPN"> **Proton VPN Free** | Yes | All major | Don’t stay on free tier if you need custom server locations or P2P/streaming |
| Prefer a commercial provider with dynamic multi-hop and port options | Feature or jurisdiction preference | <img src="../../assets/logos/wireguard.svg" width="16" height="16" alt="IVPN"> **IVPN** | Yes | All major | Don’t switch without a concrete need |
| Need a dedicated static IP on your own VPS | Commercial VPN shares egress IPs with other users | <img src="../../assets/logos/wireguard.svg" width="16" height="16" alt="WireGuard"> **WireGuard (Self-Hosted)** | Yes | Linux VPS | Don’t self-host if you need multi-country geo-unblocking |

### Alternative installs

#### Proton VPN Free
- Website: https://protonvpn.com/download — create free Proton account → install app.

#### IVPN
- Website: https://www.ivpn.net/apps/

#### WireGuard (Self-Host)
- Official guide: https://www.wireguard.com/install/

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | WireGuard (Self-Hosted) |
| **Repo** | https://github.com/WireGuard/wireguard-tools |
| **What local means** | VPN endpoint running entirely on a server you control |
| **Who it’s for** | Homelab and VPS operators |
| **Ops burden** | Medium |
| **When primary still wins** | You want zero maintenance and multi-country exit nodes |

---

## Quick decision box

```text
Default privacy VPN                 →  Mullvad VPN
Reliable zero-cost tier              →  Proton VPN Free
Alternative audited VPN              →  IVPN
Self-hosted single VPS tunnel        →  WireGuard
```
