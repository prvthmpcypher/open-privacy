# Translation

> Open Privacy · v0.2 · August 2026 · Poorvith M P  
> Category ID: `24-translation`  
> Replaces: Google Translate (cloud logging, tracking untrusted web text)

---

## Primary recommendation

<img src="../../assets/logos/firefox.svg" width="36" height="36" alt="Firefox Translations Logo">

| Field | Value |
|---|---|
| **Name** | Firefox Translations (Built-in On-Device) |
| **Website** | https://support.mozilla.org/en-US/kb/firefox-translations |
| **Source / repo** | https://github.com/mozilla/firefox-translations |
| **Open source?** | **Yes** (MPL 2.0 / Bergamot project) |
| **Local / self-host?** | **Yes** — neural machine translation models run 100% locally in your browser engine |
| **Target audience** | Everyday web users who want full-page and text translations without sending text to Google servers |
| **Platforms** | Firefox Desktop · Firefox Android (Native Feature) |
| **Pricing** | 100% Free |
| **Payment notes** | N/A |

### Why this is the one pick
1. 100% on-device translation: language models and vocabulary files download directly to your machine and execute translation locally on your CPU.
2. Zero text, URLs, or personal data are ever transmitted to Mozilla, Google, or any third-party cloud.
3. Fully integrated natively into Firefox (no external add-on or API key required).
4. Translates entire foreign webpages seamlessly with one click from the address bar icon.
5. Developed under the EU-funded Project Bergamot for privacy-preserving client-side neural machine translation.

### What it does not do
- Translation quality for highly complex or rare idiomatic language pairs may lag massive cloud AI models like DeepL or Google Translate.
- Requires downloading offline language model packs (~20–40 MB per language pair) on first use.
- Native integration is specific to Firefox; other browsers need an external extension or API.

---

## Install guide (primary)

### Enabling in Firefox Desktop
1. Open **Firefox**.
2. Visit any website written in a language other than your system language (e.g. `https://lemonde.fr` or `https://spiegel.de`).
3. The **Translation icon** will appear in the URL address bar.
4. Click **Translate** to download the offline language model and translate the page.
5. In Firefox **Settings** → **General** → **Language and Appearance** → **Translations**, you can manage downloaded offline language packs and set automatic translation preferences.

### Enabling in Firefox Android
- Tap the three-dot menu → Tap **Translate page** to run local translation on mobile.

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| Need a self-hosted translation API for external apps and servers | Firefox Translations is built into the browser UI | **LibreTranslate** | Yes (AGPL 3.0) | Docker · Python API | Don’t deploy a local API server if you only need browser page translation |
| Require highest linguistic translation quality for professional documents | On-device models have smaller parameter counts | **DeepL (Web/Desktop)** | No | All major | Don’t send sensitive unencrypted personal text to proprietary cloud translation |
| Browsing outside Firefox (Brave, Chrome, Safari) | Native translation is built into the Gecko engine | **LibreTranslate Web UI / SimplyTranslate** | Yes | Web | Don’t switch if you can use Firefox for reading foreign language websites |

### Alternative installs

#### LibreTranslate (Self-Hosted Translation API & Web)
- Official GitHub: https://github.com/LibreTranslate/LibreTranslate
- Docker run command:
```bash
docker run -ti --rm -p 5000:5000 libretranslate/libretranslate
```
Open `http://localhost:5000` to translate text or connect via REST API.

#### DeepL
- Website: https://www.deepl.com

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | Firefox Translations / LibreTranslate |
| **Repo** | https://github.com/LibreTranslate/LibreTranslate |
| **What local means** | Machine translation neural networks run entirely on your local CPU hardware |
| **Who it’s for** | Privacy-first readers and developers needing translation APIs |
| **Ops burden** | Low (Firefox) / Medium (LibreTranslate Docker) |
| **When primary still wins** | Firefox provides seamless one-click in-page translation with zero setup |

---

## Quick decision box

```text
Default private web page translation→  Firefox Translations (Native)
Self-hosted translation REST API     →  LibreTranslate
Highest raw linguistic nuance (cloud)→  DeepL
Independent web proxy translation    →  SimplyTranslate
```
