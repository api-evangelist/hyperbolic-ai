# Hyperbolic (hyperbolic-ai)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Hyperbolic is an open-access AI cloud and decentralized GPU marketplace serving 200,000+ builders with affordable inference and bare-metal compute. The platform combines a serverless OpenAI-compatible inference API spanning 25+ open-source LLMs (including the only public Llama-3.1-405B-Base in BF16), image and audio models, with an on-demand GPU rental marketplace aggregating idle H100 / H200 / A100 / RTX 4090 capacity from third-party suppliers at 3-10x lower cost than hyperscalers. Reserved clusters, dedicated endpoints, an OpenAI-drop-in Python and TypeScript SDK, a Go CLI, an MCP server, the Hyperbolic AgentKit, the open-source Hyper-dOS distributed operating system, and Coinbase x402 crypto payments round out the stack.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/hyperbolic-ai/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/hyperbolic-ai/refs/heads/main/apis.yml)

## Scope

- **Position:** Consuming
- **Access:** 3rd-Party

## Tags

- AI
- Artificial Intelligence
- Compute
- Decentralized
- DePIN
- GPU
- Image Generation
- Inference
- LLM
- Marketplace
- Open Source

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### Hyperbolic Chat Completions API

OpenAI-compatible chat completions endpoint serving 25+ open-source LLMs including Llama 3.1 8B/70B/405B, Qwen 2.5, DeepSeek V3, DeepSeek R1, Hermes 3, Mistral, and vision models (Llama 3.2 Vision, Qwen2-VL). Supports streaming, tool/function calling, structured JSON output, and chain-of-thought reasoning. Drop-in OpenAI replacement — change api_key and base_url to https://api.hyperbolic.xyz/v1.

- **Human URL:** [https://docs.hyperbolic.ai/inference/overview](https://docs.hyperbolic.ai/inference/overview)

#### Tags

- AI
- Chat
- Completions
- Inference
- LLM

#### Properties

- [Documentation](https://docs.hyperbolic.ai/inference/overview)
- [Documentation](https://docs.hyperbolic.ai/inference/chat-completion)
- [OpenAPI](openapi/hyperbolic-chat-completions-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/hyperbolic-chat-completions-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/hyperbolic-chat-completions-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/hyperbolic-chat-completion-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/hyperbolic-ai-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)

### Hyperbolic Completions API

Legacy OpenAI-compatible text completions endpoint for base-model prompting. Notably exposes Llama-3.1-405B-Base in both BF16 (high-throughput precision) and FP8 (low-latency) — Hyperbolic is the only public provider serving the base model in BF16.

- **Human URL:** [https://docs.hyperbolic.ai/inference/overview](https://docs.hyperbolic.ai/inference/overview)

#### Tags

- AI
- Completions
- Inference
- LLM

#### Properties

- [Documentation](https://docs.hyperbolic.ai/inference/overview)
- [OpenAPI](openapi/hyperbolic-completions-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/hyperbolic-completions-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/hyperbolic-completions-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Hyperbolic Image Generation API

Generate images from text prompts using diffusion models including Stable Diffusion XL, Stable Diffusion 3.5, FLUX.1 [schnell] / [dev] (sunset), and ControlNet variants. Supports custom LoRAs. Pricing from $0.0025 per image. POST /v1/image/generation accepts model_name, prompt, steps, cfg_scale, height, width.

- **Human URL:** [https://docs.hyperbolic.ai/inference/overview](https://docs.hyperbolic.ai/inference/overview)

#### Tags

- AI
- Diffusion
- Image Generation
- Inference

#### Properties

- [Documentation](https://docs.hyperbolic.ai/inference/overview)
- [OpenAPI](openapi/hyperbolic-image-generation-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/hyperbolic-image-generation-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/hyperbolic-image-generation-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Hyperbolic Audio Generation API

Convert text to natural-sounding speech using Melo TTS (sunset) and Whisper (coming soon). POST /v1/audio/generation accepts text and speed; returns base64-encoded audio. Pricing from $0.001 per 1000 characters.

- **Human URL:** [https://docs.hyperbolic.ai/inference/overview](https://docs.hyperbolic.ai/inference/overview)

#### Tags

- AI
- Audio
- Inference
- Text To Speech

#### Properties

- [Documentation](https://docs.hyperbolic.ai/inference/overview)
- [OpenAPI](openapi/hyperbolic-audio-generation-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/hyperbolic-audio-generation-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/hyperbolic-audio-generation-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Hyperbolic Models API

OpenAI-compatible model discovery endpoint. GET /v1/models returns the catalog of currently served inference models — chat, base completion, image, vision, and audio — so clients can route requests by capability without hard-coded model IDs.

- **Human URL:** [https://docs.hyperbolic.ai/inference/overview](https://docs.hyperbolic.ai/inference/overview)

#### Tags

- AI
- Inference
- Models

#### Properties

- [Documentation](https://docs.hyperbolic.ai/inference/overview)
- [OpenAPI](openapi/hyperbolic-models-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/hyperbolic-models-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/hyperbolic-models-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Hyperbolic GPU Marketplace API

Decentralized on-demand GPU compute marketplace renting idle H100, H200, A100, and RTX 4090 capacity from third-party suppliers. Pricing starts at $0.50/GPU/hr (RTX 4090), $1.39-$1.49/hr (H100), up to $3.20/hr (H100 dedicated). Up to 75% cheaper than AWS/Azure/GCP. Instances deploy in under one minute. Reserved clusters and dedicated single-tenant endpoints available. Hyperbolic charges a 10% platform fee on rental income. Managed via app.hyperbolic.ai dashboard, the `hyperbolic-cli` Go CLI, the MCP server, and the Hyperbolic AgentKit.

- **Human URL:** [https://docs.hyperbolic.ai/on-demand/overview](https://docs.hyperbolic.ai/on-demand/overview)

#### Tags

- AI
- Compute
- GPU
- Infrastructure
- Marketplace

#### Properties

- [Documentation](https://docs.hyperbolic.ai/on-demand/overview)
- [Documentation](https://docs.hyperbolic.ai/on-demand/quickstart)
- [GitHub Repository](https://github.com/HyperbolicLabs/hyperbolic-cli)
- [GitHub Repository](https://github.com/HyperbolicLabs/hyperbolic-mcp)
- [Postman Collection](collections/hyperbolic-audio-generation-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/hyperbolic-audio-generation-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/hyperbolic-chat-completions-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/hyperbolic-chat-completions-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/hyperbolic-completions-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/hyperbolic-completions-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/hyperbolic-image-generation-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/hyperbolic-image-generation-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/hyperbolic-models-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/hyperbolic-models-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Arazzo Workflows](arazzo/) — [Arazzo Specification](https://spec.openapis.org/arazzo/latest.html)
- [Portal](https://www.hyperbolic.ai/)
- [Documentation](https://docs.hyperbolic.ai/)
- [Documentation](https://docs.hyperbolic.ai/overview)
- [Documentation](https://docs.hyperbolic.ai/overview/platform-comparison)
- [Documentation](https://docs.hyperbolic.ai/inference/overview)
- [Getting Started](https://docs.hyperbolic.ai/inference/quickstart)
- [Documentation](https://docs.hyperbolic.ai/on-demand/overview)
- [Getting Started](https://docs.hyperbolic.ai/on-demand/quickstart)
- [Documentation](https://docs.hyperbolic.ai/reserved/overview)
- [Sign Up](https://app.hyperbolic.ai/)
- [Documentation](https://app.hyperbolic.ai/settings/api-keys)
- [Sandbox](https://app.hyperbolic.ai/models)
- [Blog](https://www.hyperbolic.ai/blog)
- [About Us](https://www.hyperbolic.ai/about)
- [Careers](https://www.hyperbolic.ai/careers)
- [Careers](https://jobs.ashbyhq.com/hyperbolic)
- [Press Kit](https://www.hyperbolic.ai/media-kit)
- [Privacy Policy](https://www.hyperbolic.ai/privacy-policy)
- [Terms of Service](https://www.hyperbolic.ai/terms-of-use)
- [Contact Form](mailto:contact@hyperbolic.ai)
- [Contact Form](mailto:sales@hyperbolic.ai)
- [Support](mailto:support@hyperbolic.ai)
- [Contact Form](https://calendly.com/d/cq79-jyv-jg4/hyperbolic-sales-demo)
- [Twitter](https://twitter.com/hyperbolic_labs)
- [LinkedIn](https://www.linkedin.com/company/hyperbolic-labs/)
- [YouTube](https://www.youtube.com/@hyperboliclabs)
- [GitHub Organization](https://github.com/HyperbolicLabs)
- [Open Source Project](https://github.com/HyperbolicLabs/Hyper-dOS)
- [SDK](https://github.com/HyperbolicLabs/Hyperbolic-AgentKit)
- [SDK](https://github.com/HyperbolicLabs/hyperbolic-ts)
- [Tool](https://github.com/HyperbolicLabs/hyperbolic-mcp)
- [Tool](https://github.com/HyperbolicLabs/hyperbolic-cli)
- [Tool](https://github.com/HyperbolicLabs/homebrew-hyperbolic)
- [SDK](https://github.com/HyperbolicLabs/hyperbolic-gradio)
- [Tool](https://github.com/HyperbolicLabs/hyperbolic-x402)
- [Tool](https://github.com/HyperbolicLabs/skypilot)
- [Tool](https://github.com/HyperbolicLabs/skypilot-catalog)
- [Open Source Project](https://github.com/HyperbolicLabs/jungle.proto)
- [Code Examples](https://github.com/HyperbolicLabs/inference-benchmarks)
- [Forum](https://github.com/HyperbolicLabs/feature-requests)
- [Documentation](https://huggingface.co/docs/inference-providers/en/providers/hyperbolic)
- [Api Base U R L](https://api.hyperbolic.xyz/v1)
- [Plans](plans/hyperbolic-ai-plans-pricing.yml)
- [Rate Limits](rate-limits/hyperbolic-ai-rate-limits.yml)
- [Fin Ops](finops/hyperbolic-ai-finops.yml)
- [Vocabulary](vocabulary/hyperbolic-ai-vocabulary.yml)
- [Spectral Rules](rules/hyperbolic-ai-rules.yml)
- [Features](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** info@apievangelist.com
**URL:** https://apievangelist.com
