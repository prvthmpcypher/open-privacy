# Translation

> Open Privacy · v0.1 · July 2026 · Poorvith M P  
> Category ID: `24-translation`  
> Replaces: Google Translate as default

---

## Primary recommendation

| Field | Value |
|---|---|
| **Name** | Firefox Translations (on-device) |
| **Website** | https://browser.mt/ / Firefox add-on docs |
| **Source / repo** | https://github.com/mozilla/firefox-translations / Firefox built-in translations |
| **Open source?** | **Yes** (Mozilla translation stack components) |
| **Local / self-host?** | **Yes** — models run locally in the browser |
| **Target audience** | Users who want private page/text translation without Google cloud |
| **Platforms** | Firefox desktop (primary); mobile support varies by version |
| **Pricing** | Free |
| **Payment notes** | N/A |

### Why this is the one pick
1. On-device translation reduces private text from Google cloud by default.
2. Integrated into Firefox privacy-friendly browsing.
3. Open ecosystem rather than closed mobile translate apps.
4. Good enough for many everyday page translations.
5. Aligns with local-first privacy.

### What it does not do
- Quality can lag Google Translate for some language pairs.
- Not every platform has the same UX.
- Offline model downloads take space.

---

## Install guide (primary)

### Download hubs
- Firefox: https://www.mozilla.org/firefox/
- Enable Translations in Firefox settings / toolbar when offered by your Firefox version

### Windows
1. Install Firefox from https://www.mozilla.org/firefox/
2. Open a foreign-language page.
3. Use the Translations icon/prompt in the toolbar/address area to download language packs and translate locally.

### macOS
1. Install Firefox.
2. Use built-in Translations UI on supported versions.
3. Download language packs when prompted.

### Linux
1. Install Firefox via distro or Mozilla tarball.
2. Use Translations feature as in desktop Firefox.
3. Ensure you are on a recent Firefox ESR/release that includes translations.

### Android
1. Install Firefox for Android.
2. Check whether Translations is available in your version; if not, use a local/self-host catch path.
3. Avoid pasting secrets into cloud translate apps.

### iOS
1. Firefox iOS translation features may differ.
2. Prefer on-device OS translation features when they keep processing local, or translate on desktop Firefox.
3. Avoid Google Translate app for sensitive text.

### First-run checklist
1. Prefer full-page translation over pasting confidential paragraphs into cloud tools.
2. Delete unneeded language packs if storage is tight.
3. For batch/docs translation, use LibreTranslate self-host.

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| Need self-host API for many apps | Browser-only UX | **LibreTranslate** | Yes | Self-host · web | Don’t self-host if you only need occasional in-browser translation |
| Need best raw quality and accept cloud | Local quality gap | **DeepL** (privacy policy review required) | No | Web · apps | Don’t use cloud for secrets |
| Working outside Firefox | Browser lock-in | **LibreTranslate web UI** | Yes | Any browser | Keep local models when possible |

### Alternative installs

#### LibreTranslate
- https://github.com/LibreTranslate/LibreTranslate — Docker self-host; optional public instances you trust

#### DeepL
- https://www.deepl.com — cloud; avoid sensitive data

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | LibreTranslate |
| **Repo** | https://github.com/LibreTranslate/LibreTranslate |
| **What local means** | Translation API/UI on your machine/server |
| **Who it’s for** | Users needing private bulk translation |
| **Ops burden** | Medium |
| **When primary still wins** | Firefox on-device is enough for casual browsing |

### Local install
- Docker run/compose per LibreTranslate README on Linux/macOS/Windows Docker

---

## Quick decision box

```text
Default private page translate       →  Firefox Translations
Self-host translate API              →  LibreTranslate
Cloud quality (non-sensitive only)   →  DeepL
```
