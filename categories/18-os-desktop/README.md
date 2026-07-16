# Desktop OS Privacy Path

> Open Privacy · v0.1 · July 2026 · Poorvith M P  
> Category ID: `18-os-desktop`  
> Replaces: Stock Windows/macOS defaults without privacy hardening

---

## Primary recommendation

| Field | Value |
|---|---|
| **Name** | Fedora Workstation |
| **Website** | https://fedoraproject.org/workstation/ |
| **Source / repo** | https://src.fedoraproject.org / https://github.com/fedora-silverblue (related variants) |
| **Open source?** | **Yes** |
| **Local / self-host?** | **Yes** — local operating system |
| **Target audience** | Users ready to daily-drive a modern Linux desktop for privacy |
| **Platforms** | PC (x86_64; ARM where supported) |
| **Pricing** | Free |
| **Payment notes** | N/A |

### Why this is the one pick
1. Up-to-date packages and strong open-source defaults.
2. Practical daily driver for developers and power users.
3. No Windows advertising/telemetry stack.
4. Large community and documentation.
5. Good baseline before more extreme hardening distros.

### What it does not do
- Not a drop-in for all Windows-only software (use VMs/alternatives).
- Not as “locked down appliance” as Qubes.
- Hardware compatibility still varies by machine.

---

## Install guide (primary)

### Download hubs
- https://fedoraproject.org/workstation/download/

### Windows
1. Download Fedora Workstation ISO from the official download page.
2. Write ISO to USB with Rufus or Fedora Media Writer (official guidance).
3. Boot USB → install alongside/instead of Windows (backup first).
4. Finish user setup; install updates.

### macOS
1. Linux-on-Mac is hardware-dependent; prefer Intel/Apple Silicon docs carefully.
2. Download ISO only if your hardware path is supported by current Fedora docs.
3. Otherwise use Fedora on PC hardware; keep macOS hardened as catch path.

### Linux
1. If already on Linux, flash Fedora ISO and install, or upgrade path per Fedora docs.
2. After install: `sudo dnf upgrade --refresh`
3. Enable firewall defaults; create a standard user (not daily root).

### Android
1. Not applicable (mobile OS category is separate).
2. Use Fedora on computers only.
3. See `19-os-mobile` for phones.

### iOS
1. Not applicable.
2. See mobile OS category for phone privacy path.
3. Desktop privacy path is PC/Linux-focused here.

### First-run checklist
1. Full disk encryption during install when offered.
2. Install browser/password manager from this library.
3. Avoid enabling proprietary third-party repos casually.

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| Need maximum compartmentalization | Fedora is a standard desktop | **Qubes OS** | Yes | PC (specific hardware) | Don’t use Qubes if you need simple laptop UX |
| Must stay on Windows for work software | App compatibility | **Windows 11 + hard privacy config + browser isolation** | No | PC | Still migrate high-risk browsing to Linux VM when possible |
| Prefer beginner-friendly Linux UX | Learning curve | **Linux Mint** | Yes | PC | Don’t pick Mint solely if you want newest packages always |

### Alternative installs

#### Qubes OS
- https://www.qubes-os.org/downloads/

#### Windows stay path
- Official Windows install media only; apply least-privilege account + privacy settings + this library’s apps

#### Linux Mint
- https://linuxmint.com/download.php

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | Fedora / Mint / Qubes (all local OS installs) |
| **Repo** | Upstream distro sources |
| **What local means** | OS runs on your hardware |
| **Who it’s for** | Desktop users |
| **Ops burden** | Low–Medium (Fedora/Mint) / High (Qubes) |
| **When primary still wins** | Fedora balances freshness and usability |

### Local install
- Download official ISOs only; verify checksums when published

---

## Quick decision box

```text
Default private desktop path         →  Fedora Workstation
Maximum isolation                    →  Qubes OS
Beginner Linux                       →  Linux Mint
Forced Windows                       →  Harden + private apps
```
