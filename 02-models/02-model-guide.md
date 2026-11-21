# Which model should a business use?

There is no single winner for every business job. The better question is, **which model performs this exact task well enough, at an acceptable speed, cost, and privacy level?** A strong research writer may be unnecessary for tagging routine email. A fast model that understands text may be unsuitable for inspecting a photographed form.

Model names and available versions change frequently. This guide emphasizes families and uses instead of treating a particular version number as permanently best. Check the linked official pages when choosing a subscription.

## General-purpose model families

| Family / provider | Useful starting jobs | What to check | Official information |
|---|---|---|---|
| **GPT / OpenAI** | Mixed office tasks, writing, reasoning, image questions, connected work | The model and app plan may differ in tools, speed, and media support | [ChatGPT models](https://learn.chatgpt.com/docs/models), [OpenAI developers](https://developers.openai.com/) |
| **Claude / Anthropic** | Reading and drafting long documents, analysis, structured business writing, tool-connected work | Available Opus, Sonnet, Haiku and other tiers; connection and plan permissions | [Claude model overview](https://platform.claude.com/docs/en/models/overview) |
| **Gemini / Google** | Work involving text, images, video and Google services; internal knowledge workflows | Different Pro, Flash and lighter variants; app versus cloud platform availability | [Google DeepMind model cards](https://deepmind.google/models/model-cards/) |
| **Command and Aya / Cohere** | Enterprise search, document-grounded answers, multilingual information work | Whether hosted services and required data controls fit your organization | [Cohere models](https://docs.cohere.com/docs/models) |
| **Mistral models** | General writing and analysis, document and voice-related workflows, hosted or open-weight choices | Which tasks need a hosted product and which would need technical hosting | [Mistral model catalog](https://docs.mistral.ai/models) |
| **Llama / Meta** | Organizations that want to explore open-weight models through a service provider | An open-weight model is not automatically a ready-made no-code business app | [Meta Llama repository](https://github.com/meta-llama/llama-models) |
| **DeepSeek** | Reasoning and general text work through supported services | Current model names, availability and data-handling terms | [DeepSeek official models and pricing](https://api-docs.deepseek.com/quick_start/pricing/) |
| **Qwen / Alibaba Cloud** | Multilingual, vision, document, and general model work through supported products | Regional availability, hosted interface, image/video abilities | [Alibaba Cloud models](https://www.alibabacloud.com/help/en/model-studio/models) |
| **Grok / xAI** | General reasoning and tool-enabled tasks in supported products | Model access, connected actions, data controls, performance on your tasks | [xAI model catalog](https://docs.x.ai/developers/models) |

This table describes **possible fit**, not independently measured rankings. A model provider's published capabilities should be tested against your own examples.

## Understand the tiers

Many providers offer variants that make different trade-offs:

- **Fast/light:** Appropriate for simple classification, short drafts, and repetitive tasks when accuracy is acceptable.
- **Balanced:** Often a good starting point for routine writing, documents, and general business reasoning.
- **High-reasoning:** Useful for difficult comparisons, tangled instructions, long analyses, and expensive decisions that still need human review.
- **Specialist:** Purpose-built for speech recognition, translation, image creation, document reading, embedding/search, or video.

For example, Anthropic describes its Claude family in tiers including Opus, Sonnet, Haiku, and Fable. Google's Gemini family uses several capability and speed tiers. The *labels* are less important than testing speed, cost, accuracy, and supported input types. [Anthropic explanation](https://claude.com/resources/articles/claude-models-explained-choosing-the-best-model-for-your-use-case) · [Google model cards](https://deepmind.google/models/model-cards/)

## Which model for which job? Start with a shortlist

| Job | First candidate type | Why |
|---|---|---|
| Categorize customer emails | Fast general-purpose model | High volume; short, well-defined decisions |
| Draft a carefully worded client proposal | Balanced or high-reasoning language model | Needs organization and detailed constraints |
| Explain differences between supplier offers | Strong reasoning model | Must compare conditions and exceptions |
| Answer questions over company manuals | Model plus trusted document retrieval | Accuracy depends on finding the right source |
| Read a photo of a product label | Vision-capable model | Requires visual input, not just text |
| Transcribe noisy voice notes | Speech-recognition service | Purpose-built for listening |
| Hold a real-time telephone conversation | Real-time voice service | Needs turn-taking and low delay |
| Produce marketing pictures | Image-generation service | Creative output is a different task |
| Extract many invoice fields | Document extraction service | Structured extraction and confidence checks |
| Check arithmetic in a financial report | Spreadsheet or calculation tool | Do not depend on plausible-sounding arithmetic |

## A caution about 'open' models

An **open-weight model** has downloadable model weights under a particular license. It does not necessarily mean anyone can use it for free, run it on a laptop, or operate it without technical staff. A no-code owner may access such a model through a hosted provider or another app. That provider becomes part of the privacy, reliability, and cost decision.

## Recommended starting approach

Choose one general-purpose model through a convenient business app and test it against real work. Add a second model only when it demonstrably improves one class of tasks, provides a needed modality, or reduces cost without lowering quality. The business should retain the same records and procedures when changing providers.

## Comparing a model's strength against an actual business risk

A company preparing quotations should first decide whether a model is allowed to choose prices. Usually it should not; prices come from the approved rate card or a live catalog. The model's job is to understand the inquiry, select relevant information and draft a clear explanation. This removes a large category of errors regardless of whether the model is fast or powerful.

For complex research, a stronger model may justify its cost if it finds contradictory evidence or handles nuanced instructions better. But a high-reasoning tier does not turn public websites into trusted facts. The final research note should identify sources, dates, unknowns and decisions that require human judgment.

### Specific workload choices

| Work | Try first | Add only if needed |
|---|---|---|
| Sort routine incoming inquiries | Fast text model in workflow platform | More capable fallback for ambiguous cases |
| Draft formal commercial proposal | Balanced model with approved template | Stronger reasoning for complex terms |
| Extract many invoice fields | Document extractor with validation | Language model to explain exceptions |
| Understand product label photograph | Vision-capable service | Human confirmation for similar items |
| Receive live phone calls | Real-time voice platform | Human transfer and calendar tools |
| Explain financial performance | Trusted calculations plus writing model | More complex analysis after verification |

### Model selection should be revisited

When your workflow changes, the model requirement can change too. A tool that worked for short English messages may struggle with noisy multilingual audio. A new connector may expose a dangerous write action, turning a previously harmless setup into a higher-risk one. Re-run the test pack after material changes.

[Deep model guide](../08-deep-dives/03-models-explained-for-owners.md) · [Testing workbook](../11-workbooks/03-model-bakeoff.md)
