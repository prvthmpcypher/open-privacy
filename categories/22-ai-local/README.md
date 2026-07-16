# Local AI Chat

> Open Privacy · v0.1 · July 2026 · Poorvith M P  
> Category ID: `22-ai-local`  
> Replaces: Cloud ChatGPT as default for private prompts

---

## Primary recommendation

| Field | Value |
|---|---|
| **Name** | Ollama |
| **Website** | https://ollama.com |
| **Source / repo** | https://github.com/ollama/ollama |
| **Open source?** | **Yes** |
| **Local / self-host?** | **Yes** |
| **Target audience** | Users who want on-device/local LLM inference |
| **Platforms** | Windows · macOS · Linux |
| **Pricing** | Free software; hardware is yours |
| **Payment notes** | N/A |

### Why this is the one pick
1. Simple local model runner.
2. Open source with broad model ecosystem.
3. Easy CLI + app installs on major desktops.
4. Keeps prompts off cloud providers by default when used offline.
5. Pairs cleanly with open UIs (Open WebUI).

### What it does not do
- Quality depends on your hardware/model size.
- Not a full cloud SaaS replacement for every task.
- Mobile support is not the primary path.

---

## Install guide (primary)

### Download hubs
- https://ollama.com/download
- Docs: https://github.com/ollama/ollama

### Windows
1. Download Windows installer from https://ollama.com/download
2. Install and open Ollama.
3. Pull a model, e.g. `ollama pull llama3.2` (choose models appropriate to your RAM/GPU).
4. Chat via `ollama run <model>` or a UI.

### macOS
1. Download macOS app from https://ollama.com/download
2. Install to Applications; complete first-run.
3. Pull and run a model from Terminal or the app UI.

### Linux
1. Follow install script/package instructions on https://ollama.com/download
2. Typical: install package → `ollama serve` if needed → `ollama pull <model>`.
3. Verify with `ollama list`.

### Android
1. Official Ollama is desktop-first.
2. For mobile local LLMs, use a dedicated Android local LLM app (evaluate carefully) or remote into your home Ollama server on LAN/VPN only.
3. Do not send private prompts to random third-party mobile AI apps.

### iOS
1. On-device large models are limited.
2. Prefer desktop Ollama for private inference.
3. If using any iOS AI app, assume cloud unless proven on-device.

### First-run checklist
1. Prefer smaller models first to validate setup.
2. Do not expose Ollama port to the public internet without auth/reverse proxy.
3. Keep models and chats off shared cloud folders if prompts are sensitive.

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| Want a ChatGPT-like web UI locally | CLI-first UX | **Open WebUI** | Yes | Docker · desktop | Don’t expose UI publicly without auth |
| Weak hardware can’t run local models well | RAM/GPU limits | **llama.cpp** with tiny models | Yes | Desktop | Don’t expect GPT-4 class quality on weak CPUs |
| Need cloud AI but privacy-filtered proxy | Local not enough | **PasteGuard-style proxy / self-hosted gateway** (advanced) or simply **don’t use cloud** | Varies | Server | Prefer local when possible |

### Alternative installs

#### Open WebUI
- https://docs.openwebui.com — Docker install; point at local Ollama

#### llama.cpp
- https://github.com/ggml-org/llama.cpp — build/run local GGUF models

#### Cloud avoidance note
- If local is impossible, minimize secrets in prompts; prefer enterprise/privacy providers you vetted—not random free bots

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | Ollama + Open WebUI |
| **Repo** | https://github.com/ollama/ollama · Open WebUI docs |
| **What local means** | Models and chats on your machine/LAN |
| **Who it’s for** | Privacy-sensitive AI users with a PC |
| **Ops burden** | Low–Medium |
| **When primary still wins** | Primary is already local FOSS |

### Local install
- Install Ollama from ollama.com/download
- Optional UI: Open WebUI via Docker docs

---

## Quick decision box

```text
Default local LLM runner             →  Ollama
ChatGPT-like local UI                →  Open WebUI
Minimal C++ inference                →  llama.cpp
```
