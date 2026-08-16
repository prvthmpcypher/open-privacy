# Desktop OS Privacy Path

> Open Privacy · v0.2 · August 2026 · Poorvith M P  
> Category ID: `18-os-desktop`  
> Replaces: Windows 11 telemetry & Recall AI scraping, macOS telemetry

---

## Primary recommendation

<img src="../../assets/logos/fedora.svg" width="36" height="36" alt="Fedora Workstation Logo">

| Field | Value |
|---|---|
| **Name** | Fedora Workstation |
| **Website** | https://fedoraproject.org/workstation/ |
| **Source / repo** | https://src.fedoraproject.org |
| **Open source?** | **Yes** (GPL and open source licenses) |
| **Local / self-host?** | **Yes** — runs natively on your hardware |
| **Target audience** | Everyday computer users wanting a modern, secure, privacy-first Linux workstation |
| **Platforms** | x86_64 · AArch64 (ARM) |
| **Pricing** | 100% Free |
| **Payment notes** | N/A |

### Why this is the one pick
1. Upstream-first Linux distribution with modern GNOME desktop and pure Wayland display server.
2. SELinux (Security-Enhanced Linux) enabled and enforcing by default for kernel-level access control.
3. System-wide Flatpak sandbox integration with fine-grained portal permissions for apps.
4. Up-to-date kernel, graphics drivers, and hardware support without compromising stability.
5. Zero telemetry, ad IDs, or operating-system-level keylogging/AI screen scrapers.

### What it does not do
- Does not run proprietary anti-cheat Windows games or macOS-exclusive software (Final Cut Pro, Logic Pro).
- Full disk compartmentalization across virtual machines requires Qubes OS.

---

## Install guide (primary)

### Download & USB Preparation
1. Download **Fedora Media Writer** or ISO from https://fedoraproject.org/workstation/download/.
2. Flash the ISO to a USB flash drive (minimum 8 GB) using Fedora Media Writer or Balena Etcher.
3. Boot your PC from the USB drive and select **Test & Install Fedora**.

### Installation Steps
1. Select your language and keyboard layout.
2. Select your target SSD/HDD in **Installation Destination**.
3. **Important:** Check **Encrypt my data** and set a strong LUKS disk encryption passphrase.
4. Click **Begin Installation** → Reboot into your new OS.

### First-run checklist
1. Complete GNOME setup (create username and password; disable optional telemetry toggle).
2. Enable third-party Flatpak repositories in GNOME Software.
3. Update system using DNF5:
```bash
sudo dnf upgrade --refresh
```

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| Need extreme security through virtual machine compartmentalization | Standard Linux shares one unified kernel across apps | **Qubes OS** | Yes | x86_64 Desktop | Don’t use Qubes on low-spec laptops or without virtualization expertise |
| Must remain on Windows 11 for corporate software or gaming | Work constraints prevent bare-metal Linux | **Windows 11 (Hardened Privacy Script + Browser Isolation)** | No | x86_64 / ARM | Don’t expect true OS privacy from a proprietary closed-source kernel |
| Prefer a traditional desktop UX with simple Debian-style packages | GNOME workflow feels unfamiliar | **Linux Mint** | Yes | x86_64 | Don’t switch if you want modern Wayland defaults and SELinux enforcement |

### Alternative installs

#### Qubes OS (Compartmentalized Security)
- Website: https://www.qubes-os.org/intro/

#### Linux Mint (Cinnamon Edition)
- Website: https://linuxmint.com/download.php

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | Fedora Workstation / Linux Mint / Qubes OS |
| **Repo** | https://fedoraproject.org |
| **What local means** | Operating system runs entirely on bare-metal hardware with full disk encryption |
| **Who it’s for** | Anyone with a laptop or desktop computer |
| **Ops burden** | Low (Fedora/Mint) / High (Qubes OS) |
| **When primary still wins** | Fedora provides the ideal balance of hardware support, modern sandboxing, and security |

---

## Quick decision box

```text
Default modern secure desktop OS     →  Fedora Workstation
Extreme security compartmentalization→  Qubes OS
Beginner-friendly traditional desktop→  Linux Mint
Amnesic live boot from USB           →  Tails
```
