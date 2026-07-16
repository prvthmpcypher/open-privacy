# VPN

> Open Privacy · v0.1 · July 2026 · Poorvith M P  
> Category ID: `06-vpn`  
> Replaces: Exposing all traffic to the ISP on untrusted networks; sketchy free VPNs

---

## Primary recommendation

| Field | Value |
|---|---|
| **Name** | Mullvad VPN |
| **Website** | https://mullvad.net |
| **Source / repo** | https://github.com/mullvad/mullvadvpn-app |
| **Open source?** | **Yes** — apps open source; service is commercial |
| **Local / self-host?** | **No** as a global VPN service |
| **Target audience** | Users who want a no-logs VPN with anonymous account numbers |
| **Platforms** | Windows · macOS · Linux · Android · iOS |
| **Pricing** | Paid flat fee |
| **Payment notes** | Cash, cards, crypto — see mullvad.net |

### Why this is the one pick
1. Account model without email identity by default.
2. Open-source apps.
3. Transparent pricing.
4. Broad platform coverage.
5. Frequently recommended among privacy-focused VPN sets.

### What it does not do
- A VPN is not anonymity (Tor is different).
- Does not fix malicious sites or weak account security.
- Paid only.

---

## Install guide (primary)

### Download hubs
- Apps: https://mullvad.net/download
- Account: https://mullvad.net/account

### Windows
1. Create a Mullvad account number at https://mullvad.net/account
2. Add time/payment per site instructions.
3. Download Windows app from https://mullvad.net/download and install.
4. Log in with account number → connect → enable lockdown/kill switch as desired.

### macOS
1. Create/fund account.
2. Download macOS app from https://mullvad.net/download
3. Install; approve VPN/system extension prompts.
4. Connect and verify IP.

### Linux
1. Follow Linux instructions on https://mullvad.net/download/app/linux/
2. Install package → login with account number → connect.
3. Enable auto-connect if desired.

### Android
1. Install Mullvad VPN from Play Store or official APK link on Mullvad download page.
2. Enter account number → connect.
3. Enable Always-on VPN + block connections without VPN.

### iOS
1. Install Mullvad VPN from the App Store (official link via mullvad.net/download).
2. Allow VPN configuration.
3. Login with account number → connect.

### First-run checklist
1. Enable kill switch / lockdown mode.
2. Test for DNS leaks.
3. Avoid free random “VPN” store apps.

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| Need a free tier to try VPN basics | Mullvad is paid-only | **Proton VPN Free** | Yes (apps) | All major | Don’t stay on free tier if you need full server choice |
| Prefer a different audited commercial VPN | Jurisdiction/feature preference | **IVPN** | Yes (apps) | All major | Don’t hop providers weekly without reason |
| Need self-hosted VPN on your VPS | Commercial VPN is still a third party | **WireGuard (self-host)** | Yes | Server + clients | Don’t self-host if you need multi-country egress |

### Alternative installs

#### Proton VPN Free
- https://protonvpn.com/download — create Proton account → install apps → Free servers

#### IVPN
- https://www.ivpn.net/apps/ — create account → install → connect

#### WireGuard (self-host)
- https://www.wireguard.com/install/
- Deploy on Linux VPS; import configs into official WireGuard clients

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | WireGuard (self-hosted) |
| **Repo** | https://www.wireguard.com |
| **What local means** | You run the VPN endpoint |
| **Who it’s for** | Users with a VPS and basic networking skill |
| **Ops burden** | Medium |
| **When primary still wins** | You want multi-country egress and less ops |

### Local install
- **Linux server:** install wireguard; configure keys/interface
- **Windows / macOS / Android / iOS:** official WireGuard apps from wireguard.com/install

---

## Quick decision box

```text
Default privacy VPN                 →  Mullvad
Need free tier                       →  Proton VPN Free
Alt commercial                       →  IVPN
Self-host endpoint                   →  WireGuard
```
