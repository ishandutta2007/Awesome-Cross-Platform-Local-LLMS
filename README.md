# Awesome-Cross-Platform-Local-LLMS

## Top Cross-Platform Local LLMs Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**  

*Focused on On-Device Inference, Cross-Language SDKs & Offline AI Applications*  

**Last updated: October 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Cross-Platform Local LLMs**. These tools enable developers to embed large language models directly into applications running on mobile, desktop, and edge devices—no cloud APIs, no API keys, and no data leaving the device.



**Examples** include NobodyWho, Ollama, LM Studio, Jan, LocalAI, GPT4All, LiteRT-LM, Off Grid, Quaynor, and llamadart (the category leaders).



**Open-source emphasis**: This section is heavily expanded with every major active project for on-device inference, cross-platform SDKs, and privacy-first local AI—ideal for mobile developers, privacy engineers, and organizations seeking transparent, vendor-independent local LLM deployment.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **Ollama Cloud**  

  Managed cloud models billed through usage credits, complementing the local Ollama runtime . **Free tier** allows 1 concurrent request; **Pro** ($20/mo) allows 3; **Max and Team** allow 10 . **Best for**: teams wanting to prototype locally then scale to cloud without changing code.



- **Google AI Edge Gallery**  

  **Google's open-source showcase app** for on-device AI, surpassing **500,000 downloads** in two months . Features **Agent Skills** (extend LLM capabilities with JavaScript modules), **Thinking Mode** (view model reasoning), **Prompt Lab** for benchmarking, and **MCP support** with per-call approval . **Available on App Store and Google Play** .



## Open-Source GitHub Projects



- **[NobodyWho](https://github.com/nobodywho-ooo/nobodywho)**  

  **Framework to run LLMs locally in Flutter, React Native, Swift, and Godot** (EUPL-1.2) . **The most cross-platform on-device inference engine available**—**official bindings for Kotlin, Swift, Python, Flutter, React Native, Expo, and Godot**, covering Android, iOS, Windows, macOS, Linux, and visionOS/watchOS . **Built on llama.cpp** with **simple, type-safe APIs**—no Docker, no GPU servers, no API keys . **Key capabilities**: **type-safe tool calling with automatic grammar generation** (no manual schema writing), **multimodal input** (image and audio), **Speech-to-Text** (Whisper models), **Text-to-Speech** (Kokoro, Pocket TTS, Supertonic), **conversation-aware context shifting**, **GPU acceleration via Metal, CUDA, and Vulkan**, and **Hugging Face model loading** for any GGUF model . **Started May 2023 as "Nimbus2000" for Godot** and expanded to six platforms by 2026 . **€2M fundraising round (December 2025)** to challenge Big Tech's cloud AI . **1,078 GitHub stars** and actively maintained with **React Native v3.0.0 and VAD support** added August 2026 . **The reference implementation for cross-platform local LLM integration** .



- **[Ollama](https://github.com/ollama/ollama)**  

  **The easiest way to run open models locally** (MIT) . **The most widely adopted local LLM runtime**—**one-command install on macOS, Windows, and Linux** with a large library of open models pulled by name . **Local REST API with official Python and JavaScript libraries** for programmatic integration . **First-class MCP server presence** lets Claude or Claude Code call into a running Ollama daemon as an MCP tool . **The reference implementation for local model running and serving** .



- **[LM Studio](https://lmstudio.ai/)**  

  **Desktop app for running open models locally** (proprietary, free for personal and commercial use) . **The best desktop experience for discovering and running local models**—**built-in model browser makes discovering and downloading models from Hugging Face effortless**, with **quantization preview** to see quality trade-offs before downloading . **Local server with OpenAI- and Anthropic-compatible endpoints**, **TypeScript and Python SDKs**, and **lms CLI** . **MCP support** for connecting to Model Context Protocol servers . **MLX engine for Apple Silicon** runs Llama, Qwen, and Gemma **30-50% faster** than llama.cpp Metal builds . **The best choice for non-terminal users who want GUI model management** .



- **[Jan](https://github.com/janhq/jan)**  

  **Open-source ChatGPT alternative that runs locally** (AGPL-3.0) . **The open-source choice when you want LM Studio's ergonomics with no proprietary client anywhere in the stack** . **MCP support via extension** and **OpenAI-shaped API** make it a clean drop-in for tooling expecting the OpenAI schema . **The best free alternative to LM Studio for users who prioritize open-source licensing** .



- **[LocalAI](https://github.com/mudler/LocalAI)**  

  **Drop-in OpenAI, Anthropic, and ElevenLabs replacement** (MIT) . **Treats OpenAI compatibility as the product rather than a feature**—**point any OpenAI SDK, Anthropic client, or ElevenLabs integration at your LocalAI instance and it responds on the same routes, with the same JSON shape** . **2026 releases pushed past single-machine runtime**: **LocalAI 4.1 added distributed cluster mode with VRAM-aware routing and autoscaling**, **4.0 rewrote the UI in React with Canvas mode**, **4.3 enabled llama.cpp prompt cache by default** so repeated system prompts collapse from minutes to seconds . **Native MCP client in agent flows**—LocalAI's agent runtime can call MCP servers directly when a model emits a tool call . **Ships an Ollama-compatible endpoint alongside OpenAI** . **Best for**: homelabs and small teams serving models to multiple callers who want one endpoint speaking OpenAI, Anthropic, and Ollama at once .



- **[GPT4All](https://github.com/nomic-ai/gpt4all)**  

  **Local LLM platform with document RAG and GPU acceleration** (MIT) . **77K+ GitHub stars**—**runs LLMs on Windows, macOS, and Linux with full customization** . **The killer feature is LocalDocs**—built-in document retrieval that lets you chat with your local files using RAG . **Vulkan acceleration brings AMD GPU users into the fold** on Windows and Linux, alongside Metal and CUDA . **Python SDK** for integration and automation . **Enterprise features**: usage analytics and centralized model distribution . **Code sandboxing** for safe local agent execution (2026) . **The best choice for enterprises wanting document RAG on local files with air-gapped deployment** .



- **[LiteRT-LM (Google AI Edge)](https://github.com/google-ai-edge/LiteRT-LM)**  

  **Production-ready orchestration layer to run LLMs with LiteRT** (Apache-2.0) . **Google's official on-device inference framework**—**engineered for high-performance, cross-platform execution** on **Android, iOS, Web, Desktop, and IoT (Raspberry Pi)** . **Hardware acceleration** via **GPU and NPU accelerators** across diverse hardware . **Multi-modality** with **vision and audio support**, **multimodal embeddings** for semantic search and RAG, and **tool use with constrained decoding** for agentic workflows . **Broad model support**: **Gemma, EmbeddingGemma 2, Llama, Phi-4, Qwen and more** . **Benchmarks**: **Gemma-4-E2B (2.58 GB)** achieves **85 tk/s decode on Android GPU**, **142 tk/s on macOS M4 Max GPU**, and **87.8 tk/s on Raspberry Pi 5 CPU** . **The reference implementation for production on-device AI with hardware acceleration** .



- **[Off Grid](https://github.com/off-grid-ai/off-grid)**  

  **Free offline AI app for iOS and Android** (MIT) . **The most complete mobile offline AI experience**—**combines text generation, image generation, image recognition, and tool execution in a single app** . **All processing on-device**—**models stored on phone, no cloud connection, no data leaves the device** . **Tested on Pixel 10 Pro** with **gemma-3-1b-it-GGUF** producing responses within seconds . **Developer describes it as a "Swiss Army knife for offline AI"** with **privacy first, zero internet connection** . **The best choice for mobile users wanting a general-purpose offline AI platform** .



- **[Quaynor](https://pub.dev/packages/quaynor)**  

  **Flutter library for running LLMs locally and offline** (MIT) . **The most accessible Flutter-native on-device AI package**—**free for commercial use, no API key required** . **Supports text, vision, embeddings, RAG, and tool calling** . **GGUF model format** with **Metal/Vulkan GPU acceleration** . **On-demand Hugging Face downloads** via `huggingface:owner/repo/filename.gguf` path syntax . **Minimum specs**: **iOS: iPhone 11+ with 4GB RAM**; **Android: Snapdragon 855 / Adreno 640 / 6GB RAM or better** . **The best Flutter-specific package for local LLM inference** .



- **[llamadart](https://pub.dev/packages/llamadart)**  

  **Dart/Flutter plugin for llama.cpp** (MIT) . **The zero-configuration Flutter option**—**uses Dart Native Assets (build hooks) system to automatically detect platform, download pre-compiled binary, and bundle it seamlessly** . **Full platform support**: **Android, iOS, macOS, Linux, Windows, and Web (WASM)** . **GPU acceleration** via **Metal (Apple) and Vulkan (Android/Linux/Windows)** . **LoRA support** for applying fine-tuned adapters dynamically at runtime . **Dart-first API with decoupled architecture** (LlamaEngine, LlamaBackend, LlamaBackendFactory) . **80%+ test coverage** . **The best choice for Flutter developers who want zero manual build configuration** .



### Additional Strong Open-Source Options



- **[Open WebUI](https://github.com/open-webui/open-webui)** — Extensible, feature-rich, self-hosted AI platform (BSD-3-Clause with branding clause) . **The application layer for local LLMs**—**connects to Ollama, LM Studio, or any OpenAI-compatible backend** to add **web access, knowledge bases (13 vector DBs), multi-user support (SSO, RBAC, SCIM), and full agentic platform capabilities** . **The best companion to any local runtime** .

- **[AnythingLLM](https://github.com/Mintplex-Labs/anything-llm)** — All-in-one AI application with RAG and agents (MIT) . **The most complete application layer**—adds **document ingestion, agents, and multi-user support** to local runtimes . **Best for**: teams wanting an all-in-one desktop app with document chat.

- **[Text Generation WebUI](https://github.com/oobabooga/text-generation-webui)** — Gradio web UI for local LLMs (AGPL-3.0) . **MCP support with per-call approval** . **Note**: AGPL copyleft—check compatibility before commercial embedding .

- Community **n8n** workflows for local LLM deployment orchestration and model management automation.



**Frameworks for building custom systems**: Combine **NobodyWho** for cross-platform mobile/desktop SDK integration with **Ollama** or **LM Studio** for local model serving, **Open WebUI** for team web access, **GPT4All** for document RAG, and **LiteRT-LM** for production edge deployment—creating a comprehensive local LLM stack.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Local LLM deployment must respect model licenses (GGUF models vary), hardware constraints, and data protection regulations where applicable.

- **Cross-platform local LLMs are mature and production-ready.** NobodyWho provides **official bindings for six platforms** with **type-safe tool calling, STT/TTS, and GPU acceleration** . Ollama is the **easiest way to run open models locally** . **These are genuine alternatives to cloud APIs for privacy-sensitive and offline use cases.**

- **The platform-specific SDK landscape is specialized.** **NobodyWho** for Flutter, React Native, Swift, Kotlin, Python, and Godot . **Quaynor** for Flutter with simpler API . **llamadart** for Flutter with zero-config build hooks . **LiteRT-LM** for Google AI Edge with NPU acceleration . **Choose based on your target platform and language.**

- **Runtime vs. application layer: pick both.** **Ollama** and **LM Studio** are runtimes that serve models. **Open WebUI** and **AnythingLLM** are application layers that add chat UIs, RAG, and multi-user support . **The dominant 2026 pattern is one runtime plus one application layer** .

- **Hardware constraints determine what you can run.** **Models under 1 GB run smoothly on mobile** . **iOS reserves 1-2 GB for the system**; Android overhead varies by manufacturer (2 GB stock, 2-4 GB Samsung/Xiaomi/Oppo) . **As a general rule, the device needs at least twice the available RAM as the model file size** .

- **The hybrid approach dominates production.** Run **local models for high-volume or sensitive work** and **reach for a frontier cloud model only for the hardest slice** . **Ollama Cloud** provides the escape hatch when you need more power .

- Self-hosted open-source solutions require proper model management, hardware provisioning, and ongoing maintenance. **Model downloads consume significant storage**—plan for Wi-Fi downloads and storage management on mobile devices .



---



**Made for mobile developers, privacy engineers, and organizations building transparent local LLM solutions.**  

Let's make Cross-Platform Local LLMs more open, data-driven, and on-device.
# Awesome-Cross-Platform-Local-LLMS

