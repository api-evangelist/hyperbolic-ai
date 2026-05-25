# Hyperbolic (hyperbolic-ai)
Hyperbolic is an open-access AI cloud and decentralized GPU marketplace serving 200,000+ builders with affordable inference and bare-metal compute. The platform combines a serverless OpenAI-compatible inference API spanning 25+ open-source LLMs (including the only public Llama-3.1-405B-Base in BF16), image and audio models, with an on-demand GPU rental marketplace aggregating idle H100 / H200 / A100 / RTX 4090 capacity from third-party suppliers at 3-10x lower cost than hyperscalers. Reserved clusters, dedicated endpoints, an OpenAI-drop-in Python and TypeScript SDK, a Go CLI, an MCP server, the Hyperbolic AgentKit, the open-source Hyper-dOS distributed operating system, and Coinbase x402 crypto payments round out the stack.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/hyperbolic-ai/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

 - AI, Artificial Intelligence, Compute, Decentralized, DePIN, GPU, Image Generation, Inference, LLM, Marketplace, Open Source

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## Base URL

`https://api.hyperbolic.xyz/v1` — OpenAI-compatible. Authenticate with `Authorization: Bearer <YOUR_API_KEY>`. Issue keys at [app.hyperbolic.ai/settings/api-keys](https://app.hyperbolic.ai/settings/api-keys).

## Pricing Snapshot

| Surface | Model / SKU | Unit | Price |
|---|---|---|---|
| Inference (chat) | Llama 3.1 405B Instruct | per 1M tokens | $4.00 |
| Inference (chat) | DeepSeek R1 | per 1M tokens | $3.00 |
| Inference (chat) | Llama 3.3 70B | per 1M tokens | $0.40 |
| Inference (chat) | 7B/8B class floor | per 1M tokens | $0.10 |
| Inference (vision) | Llama 3.2 / Qwen2-VL floor | per 1M tokens | $0.15 |
| Image | SDXL / SD3.5 / FLUX (sunset) | per image | from $0.0025 |
| Audio | Melo TTS (sunset) | per 1000 chars | from $0.001 |
| GPU On-Demand | RTX 4090 | per GPU/hr | $0.50 |
| GPU On-Demand | A100 | per GPU/hr | $1.80 |
| GPU On-Demand | H100 (marketplace entry) | per GPU/hr | $1.39 |
| GPU On-Demand | H100 (dedicated) | per GPU/hr | $3.20 |
| Reserved Clusters | 3-12 month commitment | — | up to 40% off on-demand |
| Marketplace fee | Platform commission | percent | 10% |

## Tiers

| Tier | RPM | Minimum Deposit | Support |
|---|---|---|---|
| Basic | 60 | $0 | Community |
| Pro | 600 | $5+ | Priority + Email |
| Enterprise | Unlimited | Contract | 24/7 Dedicated |

## APIs

### Hyperbolic Chat Completions API
OpenAI-compatible `POST /v1/chat/completions`. 25+ open-source LLMs: Llama 3.1 (8B/70B/405B), Qwen 2.5, DeepSeek V3, DeepSeek R1, Hermes 3, Mistral, plus vision (Llama 3.2 Vision, Qwen2-VL). Streaming, tools, structured output, reasoning.

**Human URL:** [https://docs.hyperbolic.ai/inference/overview](https://docs.hyperbolic.ai/inference/overview)

- [OpenAPI](openapi/hyperbolic-chat-completions-api-openapi.yml)
- [JSON Schema](json-schema/hyperbolic-chat-completion-schema.json)
- [JSON-LD](json-ld/hyperbolic-ai-context.jsonld)
- [Naftiko Capability — Chat Completions](capabilities/inference-chat-completions.yaml)
- [Example](examples/hyperbolic-chat-completion-example.json)

### Hyperbolic Completions API
Legacy `POST /v1/completions` for base-model prompting. Notably exposes `meta-llama/Meta-Llama-3.1-405B` in both BF16 (high-throughput precision) and FP8 (low-latency) — Hyperbolic is the only public provider serving the base model in BF16.

- [OpenAPI](openapi/hyperbolic-completions-api-openapi.yml)
- [Naftiko Capability — Completions](capabilities/inference-completions.yaml)

### Hyperbolic Image Generation API
`POST /v1/image/generation` for diffusion text-to-image: SDXL, SD 3.5, FLUX.1 [schnell] / [dev] (sunset), ControlNet, custom LoRAs. Base64-encoded image output.

- [OpenAPI](openapi/hyperbolic-image-generation-api-openapi.yml)
- [Naftiko Capability — Image Generation](capabilities/inference-image-generation.yaml)
- [Example](examples/hyperbolic-image-generation-example.json)

### Hyperbolic Audio Generation API
`POST /v1/audio/generation` for text-to-speech using Melo TTS (sunset) and Whisper (coming soon). Base64-encoded audio output.

- [OpenAPI](openapi/hyperbolic-audio-generation-api-openapi.yml)
- [Naftiko Capability — Audio Generation](capabilities/inference-audio-generation.yaml)
- [Example](examples/hyperbolic-audio-generation-example.json)

### Hyperbolic Models API
`GET /v1/models` — OpenAI-compatible model catalog covering chat, base completion, image, vision, and audio surfaces.

- [OpenAPI](openapi/hyperbolic-models-api-openapi.yml)
- [Naftiko Capability — Models](capabilities/inference-models.yaml)
- [Example](examples/hyperbolic-models-list-example.json)

### Hyperbolic GPU Marketplace
Decentralized on-demand GPU rental of H100, H200, A100, RTX 4090 capacity sourced from third-party suppliers. Reserved clusters (3-12 month, up to 40% discount) and dedicated single-tenant endpoints. Hyperbolic charges a 10% platform fee on supplier rental income. Managed via the [Console](https://app.hyperbolic.ai/), the [hyperbolic-cli](https://github.com/HyperbolicLabs/hyperbolic-cli), the [hyperbolic-mcp](https://github.com/HyperbolicLabs/hyperbolic-mcp) MCP server, the [Hyperbolic-AgentKit](https://github.com/HyperbolicLabs/Hyperbolic-AgentKit), and the open-source [Hyper-dOS](https://github.com/HyperbolicLabs/Hyper-dOS) distributed operating system.

**Human URLs:**
- [On-Demand Overview](https://docs.hyperbolic.ai/on-demand/overview)
- [On-Demand Quick Start](https://docs.hyperbolic.ai/on-demand/quickstart)
- [Reserved Clusters](https://docs.hyperbolic.ai/reserved/overview)

## GitHub Ecosystem

| Repo | Purpose |
|---|---|
| [Hyper-dOS](https://github.com/HyperbolicLabs/Hyper-dOS) | Distributed Operating System for GPU orchestration (Go) |
| [Hyperbolic-AgentKit](https://github.com/HyperbolicLabs/Hyperbolic-AgentKit) | Python agent framework |
| [hyperbolic-cli](https://github.com/HyperbolicLabs/hyperbolic-cli) | Go CLI for marketplace operations |
| [homebrew-hyperbolic](https://github.com/HyperbolicLabs/homebrew-hyperbolic) | Homebrew tap for hyperbolic-cli |
| [hyperbolic-mcp](https://github.com/HyperbolicLabs/hyperbolic-mcp) | MCP server for Claude |
| [hyperbolic-ts](https://github.com/HyperbolicLabs/hyperbolic-ts) | TypeScript open-source projects |
| [hyperbolic-gradio](https://github.com/HyperbolicLabs/hyperbolic-gradio) | Gradio integration |
| [hyperbolic-x402](https://github.com/HyperbolicLabs/hyperbolic-x402) | Coinbase x402 chat completions |
| [jungle.proto](https://github.com/HyperbolicLabs/jungle.proto) | Jungle Protocol |
| [skypilot](https://github.com/HyperbolicLabs/skypilot) / [skypilot-catalog](https://github.com/HyperbolicLabs/skypilot-catalog) | SkyPilot integration |
| [inference-benchmarks](https://github.com/HyperbolicLabs/inference-benchmarks) | Inference benchmarking |
| [feature-requests](https://github.com/HyperbolicLabs/feature-requests) | Public roadmap intake |

## Commercial Artifacts

- [Plans](plans/hyperbolic-ai-plans-pricing.yml) — API Commons Plans 0.1
- [Rate Limits](rate-limits/hyperbolic-ai-rate-limits.yml) — API Commons Rate Limits 0.1
- [FinOps](finops/hyperbolic-ai-finops.yml) — FOCUS 1.3 aligned
- [Vocabulary](vocabulary/hyperbolic-ai-vocabulary.yml)
- [Spectral Ruleset](rules/hyperbolic-ai-rules.yml)
