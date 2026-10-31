# NVIDIA NIM

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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

NVIDIA NIM (NVIDIA Inference Microservices) is a catalog of GPU-accelerated, containerized AI inference microservices that package optimized model engines (TensorRT-LLM, vLLM, SGLang, Triton) behind industry-standard OpenAI-compatible REST APIs. NIM covers large language models, embeddings and reranking, vision-language models, speech (Riva), visual generative AI, and biology (BioNeMo) — exposed identically whether consumed from the hosted endpoint at integrate.api.nvidia.com or self-hosted via Docker containers and the Kubernetes-native NIM Operator. NIM ships with NVIDIA AI Enterprise for commercial deployment and is the inference layer underneath NVIDIA AI Blueprints, NeMo Retriever, NeMo Guardrails, and the broader NVIDIA developer stack.

**Areas:** Artificial Intelligence · Inference · Microservices · LLM · Foundation Models · GPU · Kubernetes · NVIDIA · OpenAI-Compatible

## NVIDIA NIM on APIs.io

Everything profiled for NVIDIA NIM is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/nvidia-nim/](https://apis.io/providers/nvidia-nim/)** — or go straight to one of the APIs or properties below.

### APIs (10)

- [NVIDIA NIM Completions API](https://apis.io/apis/nvidia-nim/nvidia-nim-completions-api/) — Legacy OpenAI-compatible text completion endpoint (/v1/completions) for non-chat foundation models served by NIM. Accepts a raw prompt and returns generated…
- [NVIDIA NIM Embeddings API](https://apis.io/apis/nvidia-nim/nvidia-nim-embeddings-api/) — OpenAI-compatible embeddings endpoint (/v1/embeddings) backed by NVIDIA NeMo Retriever text embedding models including NV-Embed, NV-EmbedQA-E5,…
- [NVIDIA NIM Reranking API](https://apis.io/apis/nvidia-nim/nvidia-nim-reranking-api/) — NeMo Retriever cross-encoder reranking endpoint (/v1/ranking) for scoring candidate passages against a query. Improves retrieval relevance on RAG pipelines…
- [NVIDIA NIM Models API](https://apis.io/apis/nvidia-nim/nvidia-nim-models-api/) — OpenAI-compatible model catalog endpoint (/v1/models) returning the list of models served by the NIM endpoint or container. Each entry includes id,…
- [NVIDIA NIM Health API](https://apis.io/apis/nvidia-nim/nvidia-nim-health-api/) — Liveness, readiness, and startup probes exposed by self-hosted NIM containers (/v1/health/live, /v1/health/ready) and a Prometheus /v1/metrics scrape…
- [NVIDIA NIM Biology (BioNeMo) API](https://apis.io/apis/nvidia-nim/nvidia-nim-biology-api/) — BioNeMo NIMs for protein structure prediction (AlphaFold2, ESMFold, OpenFold), protein generation (ProtGPT2, RFDiffusion), molecular property prediction…
- [NVIDIA NIM ASR API](https://apis.io/apis/nvidia-nim/nvidia-nim-asr-api/) — Automatic speech recognition (speech-to-text)
- [NVIDIA NIM Images API](https://apis.io/apis/nvidia-nim/nvidia-nim-images-api/) — Text-to-image and image-to-image generation
- [NVIDIA NIM TTS API](https://apis.io/apis/nvidia-nim/nvidia-nim-tts-api/) — Text-to-speech synthesis
- [NVIDIA NIM Chat Completions API](https://apis.io/apis/nvidia-nim/nvidia-nim-chat-completions-api/) — OpenAI-compatible chat completion operations

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Arazzo workflows (7)

Multi-step workflows that chain operations into a business task.

- [NVIDIA NIM BioNeMo Drug Discovery](https://apis.io/arazzos/nvidia-nim/nvidia-nim-bionemo-drug-discovery-workflow/)
- [NVIDIA NIM Discover And Chat](https://apis.io/arazzos/nvidia-nim/nvidia-nim-discover-and-chat-workflow/)
- [NVIDIA NIM Generate Image And Caption](https://apis.io/arazzos/nvidia-nim/nvidia-nim-generate-image-and-caption-workflow/)
- [NVIDIA NIM Health Gated Completion](https://apis.io/arazzos/nvidia-nim/nvidia-nim-health-gated-completion-workflow/)
- [NVIDIA NIM RAG Rerank And Answer](https://apis.io/arazzos/nvidia-nim/nvidia-nim-rag-rerank-answer-workflow/)
- [NVIDIA NIM Vision Describe And Summarize](https://apis.io/arazzos/nvidia-nim/nvidia-nim-vision-describe-and-summarize-workflow/)
- [NVIDIA NIM Voice Assistant Loop](https://apis.io/arazzos/nvidia-nim/nvidia-nim-voice-assistant-loop-workflow/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [nvidia-nim](https://apis.io/servers/nvidia-nim/nvidia-nim/)

#### Agent skills (237)

Agent skills built on the API.

- [accelerated-computing-cudf](https://apis.io/agent-skills/nvidia-nim/accelerated-computing-cudf/)
- [aiq-deploy](https://apis.io/agent-skills/nvidia-nim/aiq-deploy/)
- [aiq-deploy](https://apis.io/agent-skills/nvidia-nim/aiq-deploy-2/)
- [aiq-research](https://apis.io/agent-skills/nvidia-nim/aiq-research/)
- [aiq-research](https://apis.io/agent-skills/nvidia-nim/aiq-research-2/)
- [cudaq-guide](https://apis.io/agent-skills/nvidia-nim/cudaq-guide/)
- [cufolio](https://apis.io/agent-skills/nvidia-nim/cufolio/)
- [cuopt-developer](https://apis.io/agent-skills/nvidia-nim/cuopt-developer/)
- [cuopt-install](https://apis.io/agent-skills/nvidia-nim/cuopt-install/)
- [cuopt-numerical-optimization-api-c](https://apis.io/agent-skills/nvidia-nim/cuopt-numerical-optimization-api-c/)
- [cuopt-numerical-optimization-api-cli](https://apis.io/agent-skills/nvidia-nim/cuopt-numerical-optimization-api-cli/)
- [cuopt-numerical-optimization-api-python](https://apis.io/agent-skills/nvidia-nim/cuopt-numerical-optimization-api-python/)
- [cuopt-numerical-optimization-formulation](https://apis.io/agent-skills/nvidia-nim/cuopt-numerical-optimization-formulation/)
- [cuopt-routing-api-python](https://apis.io/agent-skills/nvidia-nim/cuopt-routing-api-python/)
- [cuopt-routing-formulation](https://apis.io/agent-skills/nvidia-nim/cuopt-routing-formulation/)
- [cuopt-server-api-python](https://apis.io/agent-skills/nvidia-nim/cuopt-server-api-python/)
- [cuopt-server-common](https://apis.io/agent-skills/nvidia-nim/cuopt-server-common/)
- [cuopt-skill-evolution](https://apis.io/agent-skills/nvidia-nim/cuopt-skill-evolution/)
- [cuopt-user-rules](https://apis.io/agent-skills/nvidia-nim/cuopt-user-rules/)
- [cuopt-user-rules](https://apis.io/agent-skills/nvidia-nim/cuopt-user-rules-2/)
- [cupynumeric-hdf5](https://apis.io/agent-skills/nvidia-nim/cupynumeric-hdf5/)
- [cupynumeric-install](https://apis.io/agent-skills/nvidia-nim/cupynumeric-install/)
- [cupynumeric-migration-readiness](https://apis.io/agent-skills/nvidia-nim/cupynumeric-migration-readiness/)
- [cupynumeric-parallel-data-load](https://apis.io/agent-skills/nvidia-nim/cupynumeric-parallel-data-load/)
- [dali-dynamic-mode](https://apis.io/agent-skills/nvidia-nim/dali-dynamic-mode/)
- …and 212 more published on APIs.io

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Nvidia Nim Agentic Access](https://apis.io/agentic-access/nvidia-nim/nvidia-nim-agentic-access/)

#### JSON Schema (2)

The data models the API reads and writes.

- [NVIDIA NIM Chat Completion](https://apis.io/schemas/nvidia-nim/nvidia-nim-chat-completion/)
- [NVIDIA NIM Embedding](https://apis.io/schemas/nvidia-nim/nvidia-nim-embedding/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Nvidia Nim Context](https://apis.io/jsonld/nvidia-nim/nvidia-nim-context/)

#### Collections (24)

Postman and Open Collection request collections.

- [NVIDIA NIM Biology (BioNeMo) ASR API](https://apis.io/collections/nvidia-nim/open-nvidia-nim-asr-api/)
- [NVIDIA NIM (BioNeMo) ASR Biology API](https://apis.io/collections/nvidia-nim/open-nvidia-nim-biology-api/)
- [NVIDIA NIM Biology (BioNeMo) ASR Chat API](https://apis.io/collections/nvidia-nim/open-nvidia-nim-chat-api/)
- [NVIDIA NIM Chat Completions API](https://apis.io/collections/nvidia-nim/open-nvidia-nim-chat-completions-api/)
- [NVIDIA NIM Biology (BioNeMo) ASR Completions API](https://apis.io/collections/nvidia-nim/open-nvidia-nim-completions-api/)
- [NVIDIA NIM Biology (BioNeMo) ASR Embeddings API](https://apis.io/collections/nvidia-nim/open-nvidia-nim-embeddings-api/)
- [NVIDIA NIM Biology (BioNeMo) ASR Health API](https://apis.io/collections/nvidia-nim/open-nvidia-nim-health-api/)
- [NVIDIA NIM Image Generation API](https://apis.io/collections/nvidia-nim/open-nvidia-nim-image-generation-api/)
- [NVIDIA NIM Biology (BioNeMo) ASR Images API](https://apis.io/collections/nvidia-nim/open-nvidia-nim-images-api/)
- [NVIDIA NIM Biology (BioNeMo) ASR Models API](https://apis.io/collections/nvidia-nim/open-nvidia-nim-models-api/)
- [NVIDIA NIM Biology (BioNeMo) ASR Reranking API](https://apis.io/collections/nvidia-nim/open-nvidia-nim-reranking-api/)
- [NVIDIA NIM Speech API](https://apis.io/collections/nvidia-nim/open-nvidia-nim-speech-api/)
- [NVIDIA NIM Biology (BioNeMo) ASR TTS API](https://apis.io/collections/nvidia-nim/open-nvidia-nim-tts-api/)
- [NVIDIA NIM Biology (BioNeMo) ASR Vision API](https://apis.io/collections/nvidia-nim/open-nvidia-nim-vision-api/)
- [NVIDIA NIM Biology (BioNeMo) API](https://apis.io/collections/nvidia-nim/postman-nvidia-nim-biology-api/)
- [NVIDIA NIM Chat Completions API](https://apis.io/collections/nvidia-nim/postman-nvidia-nim-chat-completions-api/)
- [NVIDIA NIM Completions API](https://apis.io/collections/nvidia-nim/postman-nvidia-nim-completions-api/)
- [NVIDIA NIM Embeddings API](https://apis.io/collections/nvidia-nim/postman-nvidia-nim-embeddings-api/)
- [NVIDIA NIM Health API](https://apis.io/collections/nvidia-nim/postman-nvidia-nim-health-api/)
- [NVIDIA NIM Image Generation API](https://apis.io/collections/nvidia-nim/postman-nvidia-nim-image-generation-api/)
- [NVIDIA NIM Models API](https://apis.io/collections/nvidia-nim/postman-nvidia-nim-models-api/)
- [NVIDIA NIM Reranking API](https://apis.io/collections/nvidia-nim/postman-nvidia-nim-reranking-api/)
- [NVIDIA NIM Speech API](https://apis.io/collections/nvidia-nim/postman-nvidia-nim-speech-api/)
- [NVIDIA NIM Vision Language Models API](https://apis.io/collections/nvidia-nim/postman-nvidia-nim-vision-api/)

#### Overlays (20)

OpenAPI overlays, including conversational phrasing for each operation.

- [Nvidia Nim Asr Api Phrasing Overlay](https://apis.io/overlays/nvidia-nim/nvidia-nim-asr-api-phrasing-overlay/)
- [Nvidia Nim Biology Api Phrasing Overlay](https://apis.io/overlays/nvidia-nim/nvidia-nim-biology-api-phrasing-overlay/)
- [Nvidia Nim Biology Overlay](https://apis.io/overlays/nvidia-nim/nvidia-nim-biology-overlay/)
- [Nvidia Nim Chat Api Phrasing Overlay](https://apis.io/overlays/nvidia-nim/nvidia-nim-chat-api-phrasing-overlay/)
- [Nvidia Nim Chat Completions Overlay](https://apis.io/overlays/nvidia-nim/nvidia-nim-chat-completions-overlay/)
- [Nvidia Nim Completions Api Phrasing Overlay](https://apis.io/overlays/nvidia-nim/nvidia-nim-completions-api-phrasing-overlay/)
- [Nvidia Nim Completions Overlay](https://apis.io/overlays/nvidia-nim/nvidia-nim-completions-overlay/)
- [Nvidia Nim Embeddings Api Phrasing Overlay](https://apis.io/overlays/nvidia-nim/nvidia-nim-embeddings-api-phrasing-overlay/)
- [Nvidia Nim Embeddings Overlay](https://apis.io/overlays/nvidia-nim/nvidia-nim-embeddings-overlay/)
- [Nvidia Nim Health Api Phrasing Overlay](https://apis.io/overlays/nvidia-nim/nvidia-nim-health-api-phrasing-overlay/)
- [Nvidia Nim Health Overlay](https://apis.io/overlays/nvidia-nim/nvidia-nim-health-overlay/)
- [Nvidia Nim Image Generation Overlay](https://apis.io/overlays/nvidia-nim/nvidia-nim-image-generation-overlay/)
- [Nvidia Nim Images Api Phrasing Overlay](https://apis.io/overlays/nvidia-nim/nvidia-nim-images-api-phrasing-overlay/)
- [Nvidia Nim Models Api Phrasing Overlay](https://apis.io/overlays/nvidia-nim/nvidia-nim-models-api-phrasing-overlay/)
- [Nvidia Nim Models Overlay](https://apis.io/overlays/nvidia-nim/nvidia-nim-models-overlay/)
- [Nvidia Nim Reranking Api Phrasing Overlay](https://apis.io/overlays/nvidia-nim/nvidia-nim-reranking-api-phrasing-overlay/)
- [Nvidia Nim Reranking Overlay](https://apis.io/overlays/nvidia-nim/nvidia-nim-reranking-overlay/)
- [Nvidia Nim Speech Overlay](https://apis.io/overlays/nvidia-nim/nvidia-nim-speech-overlay/)
- [Nvidia Nim Tts Api Phrasing Overlay](https://apis.io/overlays/nvidia-nim/nvidia-nim-tts-api-phrasing-overlay/)
- [Nvidia Nim Vision Overlay](https://apis.io/overlays/nvidia-nim/nvidia-nim-vision-overlay/)

#### Governance rules (1)

Spectral rulesets for the provider's contracts.

- [NVIDIA NIM — jsonschema rules](https://apis.io/rules/nvidia-nim/nvidia-nim-jsonschema-spectral-rules/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Nvidia Nim Authentication](https://apis.io/security/nvidia-nim/nvidia-nim-authentication/)
- [Nvidia Nim Domain Security](https://apis.io/security/nvidia-nim/nvidia-nim-domain-security/)
- [Nvidia Nim Vulnerability Disclosure](https://apis.io/security/nvidia-nim/nvidia-nim-vulnerability-disclosure/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Nvidia Nim Plans Pricing](https://apis.io/plans/nvidia-nim/nvidia-nim-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Nvidia Nim Rate Limits](https://apis.io/rate-limits/nvidia-nim/nvidia-nim-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Nvidia Nim Finops](https://apis.io/finops/nvidia-nim/nvidia-nim-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.nvidia.com/)
- [Documentation](https://docs.nvidia.com/nim/index.html)
- [Getting started](https://docs.nvidia.com/nim/large-language-models/latest/getting-started.html)
- [Pricing](https://www.nvidia.com/en-us/data-center/products/ai-enterprise/)
- [Blog](https://developer.nvidia.com/blog/category/generative-ai/)
- [Trust centre](https://www.nvidia.com/en-us/about-nvidia/legal-info/)
- [Terms of service](https://www.nvidia.com/en-us/about-nvidia/terms-of-service/)
- [Privacy policy](https://www.nvidia.com/en-us/about-nvidia/privacy-policy/)
- [GitHub](https://github.com/NVIDIA)
- [Status](https://status.nvidia.com)

## API Evangelist rating

**Kin Score 60.6** — strong · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 69.6 |
| Contract quality | 64.0 |
| Contract governance | 14.4 |
| Operational transparency | 44.7 |
| Developer ergonomics | 82.6 |
| Access clarity | 60.5 |

**Agent readiness 26.9** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | derived (partial credit) |
| OpenAPI Examples | partial |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | — |
| Agent Skills | unknown |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | distinct |

**Regulatory alignment 32.7** — AI & Biometrics

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/nvidia-nim/](https://apis.io/providers/nvidia-nim/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for NVIDIA NIM: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/nvidia-nim/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
