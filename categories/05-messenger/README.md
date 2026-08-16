# Instant Messaging

> Open Privacy · v1.0 · August 2026 · Poorvith M P  
> Category ID: `05-messenger`  
> Replaces: WhatsApp (Meta surveillance metadata), Telegram (unencrypted cloud chats by default)

---

## Primary recommendation

<img src="../../assets/logos/signal.svg" width="36" height="36" alt="Signal Logo">

| Field | Value |
|---|---|
| **Name** | Signal |
| **Website** | https://signal.org |
| **Source / repo** | https://github.com/signalapp |
| **Open source?** | **Yes** (GPL 3.0 / AGPL 3.0) |
| **Local / self-host?** | **No** — centralized cryptographic server |
| **Target audience** | Everyday users who want gold-standard end-to-end encrypted messaging with friends and family |
| **Platforms** | <img src="../../assets/logos/android.svg" width="14" height="14" alt="Android"> Android · <img src="../../assets/logos/ios.svg" width="14" height="14" alt="iOS"> iOS · <img src="../../assets/logos/linux.svg" width="14" height="14" alt="Linux"> Linux · <img src="../../assets/logos/windows.svg" width="14" height="14" alt="Windows"> Windows · <img src="../../assets/logos/macos.svg" width="14" height="14" alt="macOS"> macOS |
| **Pricing** | 100% Free (non-profit funded) |
| **Payment notes** | N/A |

### Why this is the one pick
1. Gold-standard Signal Protocol providing end-to-end encryption and forward secrecy by default for all 1:1 chats, group chats, voice calls, and video calls.
2. Sealed Sender technology strips metadata so Signal servers do not know who is messaging whom.
3. Usernames allow sharing your contact without exposing your phone number to contacts.
4. Non-profit foundation with no ad-tech business model.
5. Large enough user base that non-technical contacts will actually install it.

### What it does not do
- Still requires a phone number during initial SMS verification (though usernames hide it afterward).
- Centralized server architecture (not federated or p2p).
- Does not replace large public discussion forums.

---

## Install guide (primary)

### <img src="../../assets/logos/android.svg" width="18" height="18" alt="Android"> Android & iOS
- **Android:** https://play.google.com/store/apps/details?id=org.thoughtcrime.securesms (or direct APK from https://signal.org/android/apk/)
- **iOS:** https://apps.apple.com/app/signal-private-messenger/id874135377

### <img src="../../assets/logos/linux.svg" width="18" height="18" alt="Linux"> Linux (Debian, Ubuntu, Linux Mint)
```bash
wget -O- https://updates.signal.org/desktop/apt/keys.asc | gpg --dearmor > signal-desktop-keyring.gpg
cat signal-desktop-keyring.gpg | sudo tee /usr/share/keyrings/signal-desktop-keyring.gpg > /dev/null
echo 'deb [arch=amd64 signed-by=/usr/share/keyrings/signal-desktop-keyring.gpg] https://updates.signal.org/desktop/apt xenial main' | sudo tee /etc/apt/sources.list.d/signal-xenial.list
sudo apt update && sudo apt install signal-desktop
```

### <img src="../../assets/logos/windows.svg" width="18" height="18" alt="Windows"> Windows & macOS
- **Windows:** Download `.exe` from https://signal.org/download/ (or `winget install OpenWhisperSystems.Signal`).
- **macOS:** Download `.dmg` from https://signal.org/download/ (or `brew install --cask signal`).

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| Refuse user identifiers (no phone number, no username, no central servers) | Signal requires phone number for initial registration | <img src="../../assets/logos/simplex.svg" width="16" height="16" alt="SimpleX"> **SimpleX Chat** | Yes | Linux · Windows · macOS · Android · iOS · CLI | Don’t switch if your social circle is already established on Signal |
| Want decentralized onion-routed chat with session IDs | Signal uses centralized routing servers | <img src="../../assets/logos/signal.svg" width="16" height="16" alt="Session"> **Session** | Yes | All major | Don’t switch if you need real-time high-quality voice/video calls |
| Need federated team chat and public spaces | Signal is optimized for personal/small group messaging | <img src="../../assets/logos/element.svg" width="16" height="16" alt="Element"> **Element (Matrix)** | Yes | All major | Don’t switch if you want simple, reliable contact-to-contact messaging |

### Alternative installs

#### SimpleX Chat
- Website: https://simplex.chat
- Android: Google Play or F-Droid
- iOS: App Store
- Desktop / Terminal: https://github.com/simplex-chat/simplex-chat/releases

#### Session
- Website: https://getsession.org/download

#### Element (Matrix)
- Website: https://element.io/download

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | Matrix (Synapse / Conduit) + Element |
| **Repo** | https://github.com/matrix-org/synapse |
| **What local means** | Self-hosted federated home server on your hardware |
| **Who it’s for** | Communities, teams, and self-hosters |
| **Ops burden** | High |
| **When primary still wins** | You want simple messaging that your non-tech friends will actually use |

---

## Quick decision box

```text
Default private messaging           →  Signal
Zero user identifiers (no ID/phone)  →  SimpleX Chat
Onion-routed anonymity               →  Session
Federated team/community chat        →  Element (Matrix)
```
