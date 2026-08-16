# Calendar & Contacts

> Open Privacy · v0.2 · August 2026 · Poorvith M P  
> Category ID: `13-calendar-contacts`  
> Replaces: Google Calendar & Google Contacts (cloud profile tracking)

---

## Primary recommendation

<img src="../../assets/logos/protoncalendar.svg" width="36" height="36" alt="Proton Calendar Logo">

| Field | Value |
|---|---|
| **Name** | Proton Calendar |
| **Website** | https://proton.me/calendar |
| **Source / repo** | https://github.com/ProtonMail |
| **Open source?** | **Yes** (Client apps and cryptographic libraries) |
| **Local / self-host?** | **No** as a hosted service; Nextcloud CalDAV for self-host |
| **Target audience** | Everyday users who want zero-access encrypted schedules and contacts |
| **Platforms** | Web · Android · iOS |
| **Pricing** | Free tier included with Proton account |
| **Payment notes** | N/A for free tier |

### Why this is the one pick
1. Zero-access encryption protects event titles, descriptions, locations, and attendees; Proton cannot read your schedule.
2. Encrypted contacts store phone numbers, addresses, and personal notes securely with digital signatures.
3. Automatically integrates with Proton Mail to parse invitations without exposing data to third parties.
4. Clean web and mobile apps with widget support.
5. Compliant with Swiss data protection laws.

### What it does not do
- Direct CalDAV/CardDAV sync to third-party desktop calendar clients requires Proton Bridge (paid plan).
- Public calendar sharing links reveal unencrypted event times to designated participants.

---

## Install guide (primary)

### Web
- Access your calendar directly via web browser: https://calendar.proton.me.

### Mobile Apps
- **Android:** https://play.google.com/store/apps/details?id=me.proton.android.calendar
- **iOS:** https://apps.apple.com/app/proton-calendar-secure-events/id1524373408

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| Need standard CalDAV/CardDAV server on your private hardware | Proton uses custom zero-access crypto rather than standard CalDAV | **Nextcloud Calendar/Contacts** | Yes | Linux / Docker | Don’t self-host unless you manage your own server backups |
| Prefer the German Tuta encrypted ecosystem | Standardizing on Tuta Mail rather than Proton | **Tuta Calendar** | Yes | All major | Don’t switch if you already use Proton Mail |
| Need a 100% offline desktop calendar and address book | Do not want your calendar synced to any cloud | **Thunderbird (Local Calendar)** | Yes | Linux · Windows · macOS | Don’t switch if you need real-time sync with a mobile phone |

### Alternative installs

#### Nextcloud Calendar & Contacts
- Deploy Nextcloud → Enable Calendar & Contacts apps → Sync with Android using **DAVx5** (F-Droid).

#### Tuta Calendar
- Website: https://tuta.com/calendar

#### Thunderbird (Local)
- Website: https://www.thunderbird.net

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | Nextcloud Calendar + Contacts (CalDAV / CardDAV) |
| **Repo** | https://github.com/nextcloud/server |
| **What local means** | Industry-standard CalDAV/CardDAV server running on your own VPS or homelab |
| **Who it’s for** | Homelab operators and multi-device syncing with native OS accounts |
| **Ops burden** | Medium |
| **When primary still wins** | You want zero maintenance and turnkey web/mobile apps |

---

## Quick decision box

```text
Default E2EE calendar & contacts    →  Proton Calendar
Self-hosted standard CalDAV/CardDAV  →  Nextcloud
German post-quantum calendar         →  Tuta Calendar
Offline desktop local calendar       →  Thunderbird
```
