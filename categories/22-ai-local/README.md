# Local AI Chat

> Open Privacy · v0.2 · August 2026 · Poorvith M P  
> Category ID: `22-ai-local`  
> Replaces: Cloud ChatGPT / Gemini / Claude logging all personal prompts and training on private data

---

## Primary recommendation

<img src="../../assets/logos/ollama.svg" width="36" height="36" alt="Ollama Logo">

| Field | Value |
|---|---|
| **Name** | Ollama |
| **Website** | https://ollama.com |
| **Source / repo** | https://github.com/ollama/ollama |
| **Open source?** | **Yes** (MIT) |
| **Local / self-host?** | **Yes** — runs 100% on your local CPU / GPU hardware |
| **Target audience** | Users who want to run large language models privately on their own computer |
| **Platforms** | <img src="../../assets/logos/linux.svg" width="14" height="14" alt="Linux"> Linux · <img src="../../assets/logos/macos.svg" width="14" height="14" alt="macOS"> macOS · <img src="../../assets/logos/windows.svg" width="14" height="14" alt="Windows"> Windows |
| **Pricing** | 100% Free |
| **Payment notes** | N/A |

### Why this is the one pick
1. Zero data leaves your computer: prompts, documents, code, and chat history execute 100% on local hardware.
2. Extremely simple CLI and background service that manages model downloads, quantizations, and GPU acceleration (NVIDIA CUDA, Apple Metal, AMD ROCm).
3. Access to leading open-weight models (Llama 3.x, Mistral, Gemma 2, DeepSeek, Qwen).
4. Provides an OpenAI-compatible local REST API endpoint (`http://localhost:11434/v1`).
5. Seamlessly pairs with graphical frontends like Open WebUI.

### What it does not do
- Inference speed and context length depend entirely on your physical hardware (RAM and VRAM).
- Smaller local models (3B to 8B parameters) have less reasoning depth than multi-hundred-billion parameter cloud frontier models.

---

## Install guide (primary)

### <img src="../../assets/logos/linux.svg" width="18" height="18" alt="Linux"> Linux (One-Line Script)
```bash
curl -fsSL https://ollama.com/install.sh | sh
```

### <img src="../../assets/logos/windows.svg" width="18" height="18" alt="Windows"> Windows & macOS
- **Windows:** Download `.exe` installer from https://ollama.com/download.
- **macOS:** Download `.zip` application from https://ollama.com/download.

### Running Your First Model
Open your terminal:
```bash
# Run lightweight fast model (great for 8GB RAM)
ollama run llama3.2

# Run high-quality general assistant (great for 16GB RAM)
ollama run llama3.1:8b

# Run coding specialist model
ollama run deepseek-coder-v2
```

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| Want a ChatGPT-like web interface with document uploads (RAG) | Ollama is primarily a CLI / background daemon | <img src="../../assets/logos/ollama.svg" width="16" height="16" alt="Open WebUI"> **Open WebUI** | Yes (MIT) | Docker · Web | Don’t switch if you just want quick terminal generation |
| Prefer a standalone desktop GUI without Docker or terminal commands | Setting up Open WebUI requires Docker | **LM Studio** or **Jan** | Partial / Yes | Desktop (Win/Mac/Linux) | Don’t switch if you need a standard headless API server for other apps |
| Running on very low-spec hardware without GPU acceleration | Heavy frameworks have memory overhead | **llama.cpp (Direct CLI)** | Yes | Any hardware | Don’t drop Ollama’s simple model management unless resource-constrained |

### Alternative installs

#### Open WebUI (Local ChatGPT Clone)
- Docker run command:
```bash
docker run -d -p 3000:8080 --add-host=host.docker.internal:host-gateway -v open-webui:/app/backend/data --name open-webui --restart always ghcr.io/open-webui/open-webui:main
```
Open `http://localhost:3000` in your browser.

#### Jan (FOSS Desktop GUI)
- Website: https://jan.ai

#### LM Studio
- Website: https://lmstudio.ai

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | Ollama + Open WebUI |
| **Repo** | https://github.com/ollama/ollama |
| **What local means** | Machine learning weights and context windows evaluate strictly in your computer's RAM/VRAM |
| **Who it’s for** | Privacy-conscious developers, researchers, and writers |
| **Ops burden** | Low |
| **When primary still wins** | Primary is already the open-source local benchmark |

---

## Quick decision box

```text
Default local model runtime          →  Ollama
ChatGPT-like web UI with document RAG→  Open WebUI
Turnkey desktop graphical app        →  Jan / LM Studio
Low-spec CPU terminal runner         →  llama.cpp
```
