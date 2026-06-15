# NVIDIA NIM (nvidia-nim)

NVIDIA NIM (NVIDIA Inference Microservices) is a catalog of GPU-accelerated, containerized AI inference microservices that package optimized model engines (TensorRT-LLM, vLLM, SGLang, Triton) behind industry-standard OpenAI-compatible REST APIs. NIM covers large language models, embeddings and reranking, vision-language models, speech (Riva), visual generative AI, and biology (BioNeMo) — exposed identically whether consumed from the hosted endpoint at integrate.api.nvidia.com or self-hosted via Docker containers and the Kubernetes-native NIM Operator. NIM ships with NVIDIA AI Enterprise for commercial deployment and is the inference layer underneath NVIDIA AI Blueprints, NeMo Retriever, NeMo Guardrails, and the broader NVIDIA developer stack.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/nvidia-nim/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/nvidia-nim/refs/heads/main/apis.yml)

## Scope

- **Position:** Consuming
- **Access:** 3rd-Party

## Tags

- AI
- Artificial Intelligence
- Inference
- Microservices
- LLM
- Foundation Models
- GPU
- Kubernetes
- NVIDIA
- OpenAI Compatible

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### NVIDIA NIM Chat Completions API

OpenAI-compatible chat completions endpoint exposing 100+ foundation models — Meta Llama, Mistral, Mixtral, NVIDIA Nemotron, DeepSeek, Qwen, Microsoft Phi, Google Gemma, IBM Granite, and more — through a single /v1/chat/completions surface. Supports streaming, tool/function calling, structured outputs, vision inputs on multimodal models, and the standard temperature/top_p/max_tokens parameters. Switching models is a one-line change to the model string. Available hosted on integrate.api.nvidia.com or self-hosted via NIM containers on any GPU.

- **Human URL:** [https://docs.api.nvidia.com/nim/reference/llm-apis](https://docs.api.nvidia.com/nim/reference/llm-apis)
- **Base URL:** `https://integrate.api.nvidia.com/v1`

#### Tags

- AI
- Artificial Intelligence
- Chat
- Completions
- LLM
- OpenAI Compatible

#### Properties

- [Documentation](https://docs.api.nvidia.com/nim/reference/llm-apis)
- [Documentation](https://docs.nvidia.com/nim/large-language-models/latest/api-reference.html)
- [OpenAPI](openapi/nvidia-nim-chat-completions-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/nvidia-nim-chat-completions-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/nvidia-nim-chat-completions-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/nvidia-nim-chat-completion-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/nvidia-nim-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)

### NVIDIA NIM Completions API

Legacy OpenAI-compatible text completion endpoint (/v1/completions) for non-chat foundation models served by NIM. Accepts a raw prompt and returns generated text with the same streaming, sampling, and stopping-criterion controls as the chat endpoint.

- **Human URL:** [https://docs.nvidia.com/nim/large-language-models/latest/api-reference.html](https://docs.nvidia.com/nim/large-language-models/latest/api-reference.html)
- **Base URL:** `https://integrate.api.nvidia.com/v1`

#### Tags

- AI
- Artificial Intelligence
- Completions
- LLM
- OpenAI Compatible

#### Properties

- [Documentation](https://docs.nvidia.com/nim/large-language-models/latest/api-reference.html)
- [OpenAPI](openapi/nvidia-nim-completions-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/nvidia-nim-completions-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/nvidia-nim-completions-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### NVIDIA NIM Embeddings API

OpenAI-compatible embeddings endpoint (/v1/embeddings) backed by NVIDIA NeMo Retriever text embedding models including NV-Embed, NV-EmbedQA-E5, llama-3.2-nv-embedqa-1b, and BAAI BGE-M3. Returns dense float vectors for documents or queries to power RAG, semantic search, and clustering. Supports `input_type=passage|query` for asymmetric retrieval and the standard `dimensions` parameter on models that permit dimension reduction.

- **Human URL:** [https://docs.nvidia.com/nim/nemo-retriever/text-embedding/latest/api-reference.html](https://docs.nvidia.com/nim/nemo-retriever/text-embedding/latest/api-reference.html)
- **Base URL:** `https://integrate.api.nvidia.com/v1`

#### Tags

- AI
- Artificial Intelligence
- Embeddings
- Retrieval
- RAG
- OpenAI Compatible

#### Properties

- [Documentation](https://docs.nvidia.com/nim/nemo-retriever/text-embedding/latest/api-reference.html)
- [OpenAPI](openapi/nvidia-nim-embeddings-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/nvidia-nim-embeddings-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/nvidia-nim-embeddings-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/nvidia-nim-embedding-schema.json) — [JSON Schema](https://json-schema.org/specification)

### NVIDIA NIM Reranking API

NeMo Retriever cross-encoder reranking endpoint (/v1/ranking) for scoring candidate passages against a query. Improves retrieval relevance on RAG pipelines and supports the llama-3.2-nv-rerankqa-1b and NV-RerankQA-Mistral-4B-v3 models. Accepts a query plus a list of passages and returns a sorted list of relevance scores.

- **Human URL:** [https://docs.nvidia.com/nim/nemo-retriever/text-reranking/latest/api-reference.html](https://docs.nvidia.com/nim/nemo-retriever/text-reranking/latest/api-reference.html)
- **Base URL:** `https://integrate.api.nvidia.com/v1`

#### Tags

- AI
- Artificial Intelligence
- Reranking
- Retrieval
- RAG

#### Properties

- [Documentation](https://docs.nvidia.com/nim/nemo-retriever/text-reranking/latest/api-reference.html)
- [OpenAPI](openapi/nvidia-nim-reranking-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/nvidia-nim-reranking-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/nvidia-nim-reranking-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### NVIDIA NIM Models API

OpenAI-compatible model catalog endpoint (/v1/models) returning the list of models served by the NIM endpoint or container. Each entry includes id, owned_by, and created timestamp. Used by clients to discover the model name strings to pass to chat-completions / completions / embeddings.

- **Human URL:** [https://docs.nvidia.com/nim/large-language-models/latest/api-reference.html](https://docs.nvidia.com/nim/large-language-models/latest/api-reference.html)
- **Base URL:** `https://integrate.api.nvidia.com/v1`

#### Tags

- AI
- Artificial Intelligence
- Models
- Catalog
- OpenAI Compatible

#### Properties

- [Documentation](https://docs.nvidia.com/nim/large-language-models/latest/api-reference.html)
- [OpenAPI](openapi/nvidia-nim-models-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/nvidia-nim-models-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/nvidia-nim-models-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### NVIDIA NIM Vision Language Models API

Vision-language model inference through the standard /v1/chat/completions surface with image inputs (base64 or URL) in the messages payload. Supports NVIDIA NeVA, microsoft/kosmos-2, Phi-3-vision, llama-3.2-90b-vision-instruct, and other VLMs hosted in the NIM catalog.

- **Human URL:** [https://docs.api.nvidia.com/nim/reference/vlm-apis](https://docs.api.nvidia.com/nim/reference/vlm-apis)
- **Base URL:** `https://integrate.api.nvidia.com/v1`

#### Tags

- AI
- Artificial Intelligence
- Vision
- Multimodal
- VLM

#### Properties

- [Documentation](https://docs.api.nvidia.com/nim/reference/vlm-apis)
- [OpenAPI](openapi/nvidia-nim-vision-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/nvidia-nim-vision-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/nvidia-nim-vision-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### NVIDIA NIM Health API

Liveness, readiness, and startup probes exposed by self-hosted NIM containers (/v1/health/live, /v1/health/ready) and a Prometheus /v1/metrics scrape endpoint for GPU utilization, request latency, and queue depth. Drives Kubernetes pod lifecycle and HPA scaling via the NIM Operator.

- **Human URL:** [https://docs.nvidia.com/nim/large-language-models/latest/observability.html](https://docs.nvidia.com/nim/large-language-models/latest/observability.html)

#### Tags

- Health
- Observability
- Kubernetes

#### Properties

- [Documentation](https://docs.nvidia.com/nim/large-language-models/latest/observability.html)
- [OpenAPI](openapi/nvidia-nim-health-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/nvidia-nim-health-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/nvidia-nim-health-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### NVIDIA NIM Image Generation API

Visual generative AI endpoints for text-to-image, image-to-image, and image editing using models such as Black Forest Labs FLUX.1, Stable Diffusion XL, Shutterstock-trained models, and NVIDIA-curated Edify Image. Returns base64-encoded PNG/JPEG artifacts.

- **Human URL:** [https://docs.api.nvidia.com/nim/reference/visual-models](https://docs.api.nvidia.com/nim/reference/visual-models)
- **Base URL:** `https://integrate.api.nvidia.com/v1`

#### Tags

- AI
- Artificial Intelligence
- Image Generation
- Visual

#### Properties

- [Documentation](https://docs.api.nvidia.com/nim/reference/visual-models)
- [OpenAPI](openapi/nvidia-nim-image-generation-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/nvidia-nim-image-generation-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/nvidia-nim-image-generation-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### NVIDIA NIM Speech API

NVIDIA Riva-powered speech NIMs delivering automatic speech recognition (Parakeet, Canary), neural machine translation, and text-to-speech (Magpie-TTS, FastPitch) through HTTP and gRPC surfaces. Hosted endpoints accept WAV/FLAC audio and return transcripts or synthesized speech.

- **Human URL:** [https://docs.nvidia.com/nim/riva/latest/index.html](https://docs.nvidia.com/nim/riva/latest/index.html)
- **Base URL:** `https://integrate.api.nvidia.com/v1`

#### Tags

- AI
- Artificial Intelligence
- Speech
- ASR
- TTS
- Riva

#### Properties

- [Documentation](https://docs.nvidia.com/nim/riva/latest/index.html)
- [OpenAPI](openapi/nvidia-nim-speech-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/nvidia-nim-speech-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/nvidia-nim-speech-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### NVIDIA NIM Biology (BioNeMo) API

BioNeMo NIMs for protein structure prediction (AlphaFold2, ESMFold, OpenFold), protein generation (ProtGPT2, RFDiffusion), molecular property prediction (MolMIM), small molecule generation, and molecular docking (DiffDock). Each model is a containerized microservice with the same OpenAPI surface.

- **Human URL:** [https://docs.nvidia.com/nim/bionemo/latest/index.html](https://docs.nvidia.com/nim/bionemo/latest/index.html)
- **Base URL:** `https://integrate.api.nvidia.com/v1`

#### Tags

- AI
- Biology
- BioNeMo
- Drug Discovery
- Healthcare

#### Properties

- [Documentation](https://docs.nvidia.com/nim/bionemo/latest/index.html)
- [OpenAPI](openapi/nvidia-nim-biology-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/nvidia-nim-biology-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/nvidia-nim-biology-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Arazzo Workflows](arazzo/) — [Arazzo Specification](https://spec.openapis.org/arazzo/latest.html)
- [Portal](https://build.nvidia.com)
- [Documentation](https://docs.nvidia.com/nim/index.html)
- [Documentation](https://docs.api.nvidia.com/nim/reference/llm-apis)
- [Documentation](https://developer.nvidia.com/nim)
- [Getting Started](https://docs.nvidia.com/nim/large-language-models/latest/getting-started.html)
- [Sign Up](https://build.nvidia.com/explore/discover)
- [Sandbox](https://build.nvidia.com/explore/discover)
- [Pricing](https://www.nvidia.com/en-us/data-center/products/ai-enterprise/)
- [GitHub Organization](https://github.com/NVIDIA)
- [GitHub Organization](https://github.com/NVIDIA-NIM-Agent-Blueprints)
- [Status Page](https://status.nvidia.com)
- [Blog](https://developer.nvidia.com/blog/category/generative-ai/)
- [Blog](https://blogs.nvidia.com/blog/category/generative-ai/)
- [Forum](https://forums.developer.nvidia.com/c/ai-data-science/nemo-llm-service/)
- [Trust Center](https://www.nvidia.com/en-us/about-nvidia/legal-info/)
- [Terms of Service](https://www.nvidia.com/en-us/about-nvidia/terms-of-service/)
- [Privacy Policy](https://www.nvidia.com/en-us/about-nvidia/privacy-policy/)
- [Documentation](https://docs.nvidia.com/nim-operator/latest/index.html)
- [SDK](https://github.com/NVIDIA/nim-deploy)
- [SDK](https://github.com/NVIDIA/k8s-nim-operator)
- [SDK](https://github.com/NVIDIA/GenerativeAIExamples)
- [SDK](https://github.com/NVIDIA/NeMo)
- [SDK](https://github.com/NVIDIA/NeMo-Guardrails)
- [SDK](https://github.com/NVIDIA/TensorRT-LLM)
- [SDK](https://github.com/triton-inference-server/server)
- [SDK](https://github.com/langchain-ai/langchain-nvidia)
- [SDK](https://pypi.org/project/openai/)
- [Code Examples](https://github.com/NVIDIA/GenerativeAIExamples)
- [Code Examples](https://github.com/NVIDIA-AI-Blueprints)
- [Models](https://build.nvidia.com/explore/discover)
- [Kubernetes C R D](https://github.com/NVIDIA/k8s-nim-operator/tree/main/api)
- [Rate Limits](https://docs.api.nvidia.com/nim/reference/limits)
- [Versioning](https://docs.nvidia.com/nim/large-language-models/latest/release-notes.html)
- [Plans](plans/nvidia-nim-plans-pricing.yml)
- [Rate Limits](rate-limits/nvidia-nim-rate-limits.yml)
- [Fin Ops](finops/nvidia-nim-finops.yml)
- [Features](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** info@apievangelist.com
**URL:** https://apievangelist.com
