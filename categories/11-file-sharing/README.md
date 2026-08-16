# File Sharing

> Open Privacy · v0.2 · August 2026 · Poorvith M P  
> Category ID: `11-file-sharing`  
> Replaces: WeTransfer, Google Drive public links, unencrypted messaging attachments

---

## Primary recommendation

<img src="../../assets/logos/onionshare.svg" width="36" height="36" alt="OnionShare Logo">

| Field | Value |
|---|---|
| **Name** | OnionShare |
| **Website** | https://onionshare.org |
| **Source / repo** | https://github.com/onionshare/onionshare |
| **Open source?** | **Yes** (GPL 3.0) |
| **Local / self-host?** | **Yes** — runs directly on your computer over the Tor network |
| **Target audience** | Anyone needing anonymous, unblockable, peer-to-peer file sending and receiving |
| **Platforms** | <img src="../../assets/logos/windows.svg" width="14" height="14" alt="Windows"> Windows · <img src="../../assets/logos/macos.svg" width="14" height="14" alt="macOS"> macOS · <img src="../../assets/logos/linux.svg" width="14" height="14" alt="Linux"> Linux · CLI |
| **Pricing** | 100% Free |
| **Payment notes** | N/A |

### Why this is the one pick
1. Transfers files directly from your computer to the recipient over ephemeral Tor onion services.
2. Zero third-party cloud servers ever store or see your data.
3. Recipient only needs a Tor Browser (or onion-capable browser) to download or upload files.
4. Includes anonymous file receiving (dropboxes), temporary static website hosting, and anonymous chat rooms.
5. End-to-end encrypted by the Tor onion service architecture itself.

### What it does not do
- Both computers must be online at the same time for the transfer to complete.
- Transfer speed is limited by Tor network relay speeds.
- Recipient must be able to open `.onion` links.

---

## Install guide (primary)

### <img src="../../assets/logos/windows.svg" width="18" height="18" alt="Windows"> Windows & macOS
- **Windows:** Download `.msi` from https://onionshare.org/download/ (or `winget install MicahLee.OnionShare`).
- **macOS:** Download `.dmg` from https://onionshare.org/download/ (or `brew install --cask onionshare`).

### <img src="../../assets/logos/linux.svg" width="18" height="18" alt="Linux"> Linux
```bash
flatpak install flathub org.onionshare.OnionShare
```
Or via distro packages: `sudo apt install onionshare` / `sudo dnf install onionshare`.

### First-run checklist
1. Open OnionShare and let it connect to the Tor network.
2. Select **Share Files** → drag files in → click **Start Sharing**.
3. Send the generated `.onion` address and private key to the recipient via an encrypted messenger (see `05-messenger`).

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| Recipient cannot install Tor Browser; need simple clearnet HTTPS link | OnionShare `.onion` URLs require Tor | <img src="../../assets/logos/onionshare.svg" width="16" height="16" alt="Send"> **Send (timvisee fork)** | Yes | Web · Docker | Don’t switch if sender/recipient anonymity is mandatory |
| Transferring files terminal-to-terminal between technical users | Tor routing has overhead for large local transfers | <img src="../../assets/logos/onionshare.svg" width="16" height="16" alt="Magic Wormhole"> **Magic Wormhole** | Yes | CLI (Linux/Win/Mac) | Don’t switch if recipient needs a simple graphical web interface |
| Need continuous folder sync rather than one-off transfers | OnionShare is an ephemeral transfer tool | **Syncthing** (see cloud category) | Yes | All major | Don’t use Syncthing for one-off sends to external contacts |

### Alternative installs

#### Send (timvisee / Firefox Send Fork)
- Official repo: https://github.com/timvisee/send
- Web instances or self-hosted Docker container.

#### Magic Wormhole (Terminal P2P Transfer)
- Install: `pip install magic-wormhole` or `sudo apt install magic-wormhole`
- Send: `wormhole send filename.zip`
- Receive: `wormhole receive <code>`

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | OnionShare / Magic Wormhole |
| **Repo** | https://github.com/onionshare/onionshare |
| **What local means** | Direct point-to-point transfer with zero third-party cloud intermediaries |
| **Who it’s for** | Privacy-conscious users and developers |
| **Ops burden** | Low |
| **When primary still wins** | You need maximum sender and receiver anonymity over Tor |

---

## Quick decision box

```text
Anonymous P2P Tor transfer          →  OnionShare
Simple clearnet E2EE web link        →  Send (timvisee)
Fast CLI-to-CLI code-word transfer   →  Magic Wormhole
Ongoing folder synchronization       →  Syncthing
```
