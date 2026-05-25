# NVIDIA NIM (nvidia-nim)
NVIDIA NIM (NVIDIA Inference Microservices) is a catalog of GPU-accelerated, containerized AI inference microservices that package optimized model engines (TensorRT-LLM, vLLM, SGLang, Triton) behind industry-standard OpenAI-compatible REST APIs. NIM covers large language models, embeddings and reranking, vision-language models, speech (Riva), visual generative AI, and biology (BioNeMo) — exposed identically whether consumed from the hosted endpoint at integrate.api.nvidia.com or self-hosted via Docker containers and the Kubernetes-native NIM Operator. NIM ships with NVIDIA AI Enterprise for commercial deployment and is the inference layer underneath NVIDIA AI Blueprints, NeMo Retriever, NeMo Guardrails, and the broader NVIDIA developer stack.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/nvidia-nim/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

 - AI, Artificial Intelligence, Inference, Microservices, LLM, Foundation Models, GPU, Kubernetes, NVIDIA, OpenAI Compatible

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## Surfaces

| Surface | Base URL | Auth | Notes |
|---|---|---|---|
| Hosted (DGX Cloud) | `https://integrate.api.nvidia.com/v1` | `Authorization: Bearer nvapi-...` | Free developer endpoint, 40 RPM, 1,000 signup credits |
| Self-hosted container | `http://localhost:8000/v1` | optional bearer | Single Docker image per model, pulled from NGC |
| Kubernetes (NIM Operator) | cluster `Service` | depends on ingress | Driven by `NIMService` / `NIMCache` / `NIMPipeline` CRDs |

## APIs

### NVIDIA NIM Chat Completions API
OpenAI-compatible `/v1/chat/completions` exposing 100+ foundation models — Llama 3.1/3.2/3.3, Mistral, Mixtral, NVIDIA Nemotron, DeepSeek-R1, Qwen 2.5, Phi, Gemma, Granite, Falcon. Streaming, tool calling, JSON mode.

**Human URL:** [https://docs.api.nvidia.com/nim/reference/llm-apis](https://docs.api.nvidia.com/nim/reference/llm-apis)

- [Documentation](https://docs.api.nvidia.com/nim/reference/llm-apis)
- [OpenAPI](openapi/nvidia-nim-chat-completions-api-openapi.yml)
- [JSON Schema — Chat Completion](json-schema/nvidia-nim-chat-completion-schema.json)
- [JSON-LD](json-ld/nvidia-nim-context.jsonld)
- [Naftiko Capability — Chat](capabilities/chat-completions-chat.yaml)

### NVIDIA NIM Completions API
Legacy OpenAI-compatible `/v1/completions` for non-chat prompt completion against the same model catalog.

**Human URL:** [https://docs.nvidia.com/nim/large-language-models/latest/api-reference.html](https://docs.nvidia.com/nim/large-language-models/latest/api-reference.html)

- [OpenAPI](openapi/nvidia-nim-completions-api-openapi.yml)
- [Naftiko Capability — Completions](capabilities/completions-completions.yaml)

### NVIDIA NIM Embeddings API
OpenAI-compatible `/v1/embeddings` backed by NeMo Retriever models — NV-EmbedQA-E5, llama-3.2-nv-embedqa-1b, BAAI BGE-M3. Asymmetric `input_type=passage|query`.

**Human URL:** [https://docs.nvidia.com/nim/nemo-retriever/text-embedding/latest/api-reference.html](https://docs.nvidia.com/nim/nemo-retriever/text-embedding/latest/api-reference.html)

- [OpenAPI](openapi/nvidia-nim-embeddings-api-openapi.yml)
- [JSON Schema — Embedding](json-schema/nvidia-nim-embedding-schema.json)
- [Naftiko Capability — Embeddings](capabilities/embeddings-embeddings.yaml)

### NVIDIA NIM Reranking API
NeMo Retriever cross-encoder reranker at `/v1/ranking`. Models include llama-3.2-nv-rerankqa-1b and NV-RerankQA-Mistral-4B-v3.

**Human URL:** [https://docs.nvidia.com/nim/nemo-retriever/text-reranking/latest/api-reference.html](https://docs.nvidia.com/nim/nemo-retriever/text-reranking/latest/api-reference.html)

- [OpenAPI](openapi/nvidia-nim-reranking-api-openapi.yml)
- [Naftiko Capability — Reranking](capabilities/reranking-reranking.yaml)

### NVIDIA NIM Models API
OpenAI-compatible `/v1/models` catalog endpoint for discovering model IDs served by the endpoint or self-hosted container.

**Human URL:** [https://docs.nvidia.com/nim/large-language-models/latest/api-reference.html](https://docs.nvidia.com/nim/large-language-models/latest/api-reference.html)

- [OpenAPI](openapi/nvidia-nim-models-api-openapi.yml)
- [Naftiko Capability — Models](capabilities/models-models.yaml)

### NVIDIA NIM Vision Language Models API
Multimodal chat completions — image inputs are passed as `image_url` content parts in messages. NeVA, kosmos-2, Phi-3-vision, llama-3.2-90b-vision-instruct.

**Human URL:** [https://docs.api.nvidia.com/nim/reference/vlm-apis](https://docs.api.nvidia.com/nim/reference/vlm-apis)

- [OpenAPI](openapi/nvidia-nim-vision-api-openapi.yml)
- [Naftiko Capability — Vision](capabilities/vision-vision.yaml)

### NVIDIA NIM Health API
Self-hosted container probes: `/v1/health/live`, `/v1/health/ready`, and Prometheus `/v1/metrics`. Used by the NIM Operator for K8s lifecycle and HPA.

**Human URL:** [https://docs.nvidia.com/nim/large-language-models/latest/observability.html](https://docs.nvidia.com/nim/large-language-models/latest/observability.html)

- [OpenAPI](openapi/nvidia-nim-health-api-openapi.yml)
- [Naftiko Capability — Health](capabilities/health-health.yaml)

### NVIDIA NIM Image Generation API
Visual generative AI NIMs — FLUX.1, Stable Diffusion XL, Shutterstock Edify Image, NVIDIA Edify 3D. Returns base64-encoded PNG/JPEG.

**Human URL:** [https://docs.api.nvidia.com/nim/reference/visual-models](https://docs.api.nvidia.com/nim/reference/visual-models)

- [OpenAPI](openapi/nvidia-nim-image-generation-api-openapi.yml)
- [Naftiko Capability — Image Generation](capabilities/image-generation-images.yaml)

### NVIDIA NIM Speech API
NVIDIA Riva-powered ASR (Parakeet, Canary) and TTS (Magpie-TTS, FastPitch) NIMs with HTTP and gRPC surfaces.

**Human URL:** [https://docs.nvidia.com/nim/riva/latest/index.html](https://docs.nvidia.com/nim/riva/latest/index.html)

- [OpenAPI](openapi/nvidia-nim-speech-api-openapi.yml)
- [Naftiko Capability — ASR](capabilities/speech-asr.yaml)
- [Naftiko Capability — TTS](capabilities/speech-tts.yaml)

### NVIDIA NIM Biology (BioNeMo) API
Drug discovery and structural biology NIMs — AlphaFold2, ESMFold, OpenFold, ProtGPT2, RFDiffusion, MolMIM, DiffDock.

**Human URL:** [https://docs.nvidia.com/nim/bionemo/latest/index.html](https://docs.nvidia.com/nim/bionemo/latest/index.html)

- [OpenAPI](openapi/nvidia-nim-biology-api-openapi.yml)
- [Naftiko Capability — Biology](capabilities/biology-bionemo.yaml)

## Common Properties

- [Portal — build.nvidia.com](https://build.nvidia.com)
- [Documentation — docs.nvidia.com/nim](https://docs.nvidia.com/nim/index.html)
- [Documentation — docs.api.nvidia.com](https://docs.api.nvidia.com/nim/reference/llm-apis)
- [Developer Hub](https://developer.nvidia.com/nim)
- [GettingStarted](https://docs.nvidia.com/nim/large-language-models/latest/getting-started.html)
- [Pricing — NVIDIA AI Enterprise](https://www.nvidia.com/en-us/data-center/products/ai-enterprise/)
- [GitHubOrganization — NVIDIA](https://github.com/NVIDIA)
- [GitHubOrganization — NVIDIA AI Blueprints](https://github.com/NVIDIA-AI-Blueprints)
- [SignUp / Sandbox — build.nvidia.com](https://build.nvidia.com/explore/discover)
- [StatusPage](https://status.nvidia.com)
- [Blog — NVIDIA Developer](https://developer.nvidia.com/blog/category/generative-ai/)
- [Blog — NVIDIA Newsroom](https://blogs.nvidia.com/blog/category/generative-ai/)
- [Forum — Developer Forums](https://forums.developer.nvidia.com/c/ai-data-science/nemo-llm-service/)
- [SDK — NIM Deploy](https://github.com/NVIDIA/nim-deploy)
- [SDK — Kubernetes NIM Operator](https://github.com/NVIDIA/k8s-nim-operator)
- [SDK — NeMo](https://github.com/NVIDIA/NeMo)
- [SDK — NeMo Guardrails](https://github.com/NVIDIA/NeMo-Guardrails)
- [SDK — TensorRT-LLM](https://github.com/NVIDIA/TensorRT-LLM)
- [SDK — Triton Inference Server](https://github.com/triton-inference-server/server)
- [SDK — LangChain NVIDIA AI Endpoints](https://github.com/langchain-ai/langchain-nvidia)
- [SDK — OpenAI Python (compatible client)](https://pypi.org/project/openai/)
- [CodeExamples — Generative AI Examples](https://github.com/NVIDIA/GenerativeAIExamples)
- [CodeExamples — NVIDIA AI Blueprints](https://github.com/NVIDIA-AI-Blueprints)
- [KubernetesCRD — k8s-nim-operator API](https://github.com/NVIDIA/k8s-nim-operator/tree/main/api)
- [RateLimits](https://docs.api.nvidia.com/nim/reference/limits)
- [TermsOfService](https://www.nvidia.com/en-us/about-nvidia/terms-of-service/)
- [PrivacyPolicy](https://www.nvidia.com/en-us/about-nvidia/privacy-policy/)

## Artifacts

Machine-readable API specifications organized by format.

### OpenAPI

- [NVIDIA NIM Chat Completions API](openapi/nvidia-nim-chat-completions-api-openapi.yml)
- [NVIDIA NIM Completions API](openapi/nvidia-nim-completions-api-openapi.yml)
- [NVIDIA NIM Embeddings API](openapi/nvidia-nim-embeddings-api-openapi.yml)
- [NVIDIA NIM Reranking API](openapi/nvidia-nim-reranking-api-openapi.yml)
- [NVIDIA NIM Models API](openapi/nvidia-nim-models-api-openapi.yml)
- [NVIDIA NIM Vision Language Models API](openapi/nvidia-nim-vision-api-openapi.yml)
- [NVIDIA NIM Health API](openapi/nvidia-nim-health-api-openapi.yml)
- [NVIDIA NIM Image Generation API](openapi/nvidia-nim-image-generation-api-openapi.yml)
- [NVIDIA NIM Speech API](openapi/nvidia-nim-speech-api-openapi.yml)
- [NVIDIA NIM Biology (BioNeMo) API](openapi/nvidia-nim-biology-api-openapi.yml)

### JSON Schema

- [NVIDIA NIM Chat Completion Schema](json-schema/nvidia-nim-chat-completion-schema.json)
- [NVIDIA NIM Embedding Schema](json-schema/nvidia-nim-embedding-schema.json)

### JSON-LD

- [NVIDIA NIM Context](json-ld/nvidia-nim-context.jsonld)

### Capabilities (Naftiko)

- [Chat](capabilities/chat-completions-chat.yaml)
- [Completions](capabilities/completions-completions.yaml)
- [Embeddings](capabilities/embeddings-embeddings.yaml)
- [Reranking](capabilities/reranking-reranking.yaml)
- [Models](capabilities/models-models.yaml)
- [Vision](capabilities/vision-vision.yaml)
- [Health](capabilities/health-health.yaml)
- [Image Generation](capabilities/image-generation-images.yaml)
- [Speech — ASR](capabilities/speech-asr.yaml)
- [Speech — TTS](capabilities/speech-tts.yaml)
- [Biology (BioNeMo)](capabilities/biology-bionemo.yaml)

### Commercial artifacts

- [Plans / Pricing](plans/nvidia-nim-plans-pricing.yml)
- [Rate Limits](rate-limits/nvidia-nim-rate-limits.yml)
- [FinOps Definition](finops/nvidia-nim-finops.yml)

## Maintainers

**FN:** Kin Lane

**Email:** info@apievangelist.com
