# Research record and feature verification

**Reference date:** 21 November 2026. This book uses official standards documentation, product help centers, and product documentation. It is not a commissioned ranking or a performance test of the named vendors.

## How the research was done

The research pass used current web retrieval and Firecrawl search and page reading to examine official MCP, Relevance AI, Make, Zapier and other first-party documentation. Product statements were checked against documentation where feasible. The pages most closely tied to real setup decisions are linked below, so a reader can repeat the verification before subscribing.

The evidence has different strengths:

1. **Official specification:** Establishes what MCP defines, not what one product necessarily supports.
2. **First-party help documentation:** Establishes a documented capability, subject to plan, region, account configuration, and date.
3. **Product overview or marketing page:** Useful for understanding positioning, weaker evidence of actual restrictions.
4. **Illustrative walkthrough in this handbook:** A proposed design, not confirmation that every tool is available in the reader's subscription.
5. **Business judgment:** Recommendations about priorities, security and economics. These are not a vendor benchmark.

The comparison deliberately avoids a fixed “best model” ranking or price table. Models, availability, interface labels, credits and bundled integrations change too quickly for a static book to guarantee them.

## MCP: verified fundamentals

| Claim checked | What the primary documentation supports | Link |
|---|---|---|
| MCP purpose | Standardized connections for tools and information | [Official introduction](https://modelcontextprotocol.io/docs/2026-07-28/getting-started/intro) |
| Three server features | Tools, resources and prompts are distinct building blocks | [Server concepts](https://modelcontextprotocol.io/docs/2026-07-28/learn/server-concepts) |
| Architecture | Host, client, server and protocol boundaries | [Architecture](https://modelcontextprotocol.io/docs/2026-07-28/learn/architecture) |
| Security | MCP connection and authorization introduce real attack surfaces | [Security best practices](https://modelcontextprotocol.io/docs/2026-07-28/tutorials/security/security_best_practices) |
| Authorization | Access is mediated through authorization policies and established flows | [Authorization guidance](https://modelcontextprotocol.io/docs/2026-07-28/tutorials/security/authorization) |

For owners, the central implication is that an MCP connection does not automatically deliver a trusted business process. The provider, authentication, permission boundaries, business records, staff oversight and action verification remain separate concerns.

## No-code visual builders: details worth confirming

| Product | Official reading | Concrete point to confirm in a trial |
|---|---|---|
| Relevance AI | [Workforces](https://relevanceai.com/docs/get-started/core-concepts/workforces) | Visual canvas supports specialist handoffs, next-step routes and conditional logic; check limits and connected tools |
| Make | [Current AI Agent application](https://help.make.com/meet-the-new-make-ai-agents-app) · [Create first agent](https://help.make.com/create-your-first-ai-agent) | A scenario can connect triggers and app actions; review current agent app, billing and error handling |
| Zapier | [Human in the Loop](https://help.zapier.com/hc/en-us/articles/38731463206029-Request-approval-to-keep-your-workflow-running-with-Human-in-the-Loop) | Approval feature has plan requirements; test what happens after rejection |
| Microsoft Copilot Studio | [Generative orchestration](https://learn.microsoft.com/en-us/microsoft-copilot-studio/guidance/generative-orchestration) | Confirm licensing, data access, agent authorizations and supported channels |
| Google Workspace Studio | [Product overview](https://workspace.google.com/studio/) | Confirm administrator settings, available workflow actions, Workspace edition and limits |
| n8n | [Agent node](https://docs.n8n.io/integrations/builtin/cluster-nodes/root-nodes/n8n-nodes-langchain.agent/) · [Human approval for tools](https://docs.n8n.io/build/integrate-ai/ai-examples/human-in-the-loop-for-tools/) | Confirm available tool types and exact human-review setup; visually built does not mean zero operational responsibility |
| Voiceflow | [Official product](https://www.voiceflow.com/) | Test live voice and chat separately with the actual channels and languages |
| ElevenLabs | [ElevenAgents](https://elevenlabs.io/docs/eleven-agents/overview) · [WhatsApp](https://elevenlabs.io/docs/eleven-agents/whatsapp) | **Do not assume** telephone handoff and WhatsApp handoff have equivalent support; WhatsApp documentation noted a human-handoff limitation during review |
| Botpress | [Product site](https://botpress.com/) | Ask for supported messaging channels, test escalation and per-channel features |

## Model comparisons: official catalogs, not winner announcements

| Family | Official source | What must be tested yourself |
|---|---|---|
| OpenAI | [Models](https://developers.openai.com/api/docs/models) · [Selection](https://developers.openai.com/api/docs/guides/model-selection) | Current availability through your *app* versus API, language accuracy, media support and tool behavior |
| Claude | [Model overview](https://platform.claude.com/docs/en/models/overview) | Which tiers your product offers, long-document handling and approved connections |
| Gemini | [Google model cards](https://deepmind.google/models/model-cards/) | Workspace features versus separate Gemini models, modalities and data terms |
| Cohere | [Cohere model documentation](https://docs.cohere.com/v2/docs/models) | Whether search, embedding and reranking tools are needed separately |
| Mistral | [Model directory](https://docs.mistral.ai/models) | Hosted product or model host, documents, languages and pricing |
| Meta Llama | [Llama information](https://dev.meta.ai/llama) | Hosting, licensing, maintenance and no-code availability |
| Qwen | [Model Studio catalog](https://www.alibabacloud.com/help/en/model-studio/models) | Supported region, vision/audio offerings, terms |
| DeepSeek | [Official API documentation](https://api-docs.deepseek.com/quick_start/pricing/) | Current hosted models, data handling, reliability |
| xAI | [Model documentation](https://docs.x.ai/developers/models) | Current model selection and source verification |

## Governance references

- [NIST AI Risk Management Framework](https://airc.nist.gov/airmf-resources/airmf/): a structured way to map and manage risk.
- [OWASP GenAI Security](https://genai.owasp.org/): prompt injection and related application risks.
- [WhatsApp Business Messaging Policy](https://business.whatsapp.com/policy): platform messaging rules, which must be checked before live deployment.

## Important unresolved or variable points

Plan availability, regional phone support, exact tariffs, custom MCP support, approval mechanics, permitted data storage, channel handoff, and tool permission granularity vary. These should be demonstrated using the reader's own intended subscription. Do not infer capability from a feature in a different product tier or from a video published in a previous year.

## Updating a factual claim

When editing the handbook, locate the official product page, record the date checked, identify the exact claim, and note whether it was **documented** or **personally tested**. For claims about actual performance, record the test cases and limitations. Avoid replacing one unsupported superlative with another.
