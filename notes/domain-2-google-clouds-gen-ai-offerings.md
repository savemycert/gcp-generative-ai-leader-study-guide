# Domain 2: Google Cloud's gen AI offerings (35%)

This is the heaviest domain. It covers why organizations pick Google Cloud for gen AI, the prebuilt products for everyday work, the customer-experience portfolio, the developer platform and its RAG options, and the tools agents use to act. Nearly every question is a matching exercise: a stated need points to one named offering.

## 2.1 Describe Google Cloud's strengths in the field of gen AI

- **AI-first heritage:** Google researchers introduced the Transformer architecture behind today's LLMs, and Google DeepMind research flows into products. AI was hardened in Search, Maps, Photos, and Gmail before reaching customers. The pitch to a leader: you buy the roadmap, not only today's release.
- **Enterprise-ready platform = five qualities.** Match the quality to the concern in the scenario:

| Quality     | Meaning                                                                                               | Scenario cue                                           |
| ----------- | ----------------------------------------------------------------------------------------------------- | ------------------------------------------------------ |
| Responsible | Governed by published AI principles, with safety filters and tooling                                  | "public trust", "fairness", "brand risk"               |
| Secure      | Secure-by-design infrastructure plus guidance such as SAIF                                            | "attacks on models or data"                            |
| Private     | Google does not train its foundation models on customer prompts or data unless the customer allows it | "confidential data", "IP", "regulated industry"        |
| Reliable    | Global, highly available infrastructure with service commitments                                      | "customer-facing, cannot go down"                      |
| Scalable    | The infrastructure behind Google's own large services                                                 | "pilot to company-wide rollout without re-platforming" |

- **Comprehensive ecosystem:** the same Gemini models run in the Gemini app, Gemini for Google Workspace, Gemini Enterprise, and Google Cloud. Google also covers every landscape layer (infrastructure, models, Agent Platform, prebuilt agents and apps), so there is one vendor, one security model, and fewer integration seams.
- **Open approach:** Gemma open models; Model Garden lists Google, open, and partner models side by side; Google originated TensorFlow and Kubernetes and supports JAX and PyTorch. Benefits: choice, flexibility, less lock-in. Cue: "worried about depending on one model provider".
- **AI-optimized infrastructure:**
  - AI Hypercomputer = integrated architecture that ties together tuned AI hardware, open frameworks and software, and flexible ways to pay for capacity.
  - TPUs = Google's custom AI accelerator chips; Gemini is trained and served on them.
  - GPUs are also offered, so the accelerator follows the workload.
  - Efficient global data centers on a private fiber network, consumed on demand instead of bought.
- **Data control:** encryption and IAM (security), no training on your data without permission (privacy), policies, audit, and data residency (governance). You can use a ready-made agent, customize a prebuilt one, or build your own, and grounding data stays inside your boundary with existing permissions.
- **Democratizing AI:** low-code/no-code tools, pre-trained models (Gemini plus task APIs for speech, translation, vision, documents), and APIs. Cue: "no data scientists, need it fast" means a pre-trained model, API, or low-code tool, not hiring researchers.

📖 Full lesson: [Google Cloud's Gen AI Strengths: Platform, Infrastructure, and Openness](https://www.savemycert.com/revision/gcp-generative-ai-leader/google-cloud-gen-ai-strengths-platform/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)

## 2.2 Describe how Google Cloud's prebuilt gen AI offerings enable AI powered work

- **Prebuilt** = a finished product you switch on. No model training, no app to build, per-user cost, value in days. It is the entry point of a spectrum that runs through customizable solutions to fully custom builds on Agent Platform.
- **Sort by scope and grounding:**

| Offering                    | Where it runs                                  | Grounded in                                                    | Named capabilities                                                                        | Cue                                                                        |
| --------------------------- | ---------------------------------------------- | -------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| Gemini app                  | Standalone chat, web and mobile                | General knowledge plus what the user uploads                   | Multimodal chat                                                                           | "one person brainstorming or drafting"                                     |
| Gemini Advanced             | Premium tier of the Gemini app                 | Same, with most capable models and larger context              | **Gems**                                                                                  | "reusable assistant set up once for a recurring task"                      |
| Gemini for Google Workspace | Inside Gmail, Docs, Sheets, Meet, Slides, Chat | The user's own mail, files, and meetings                       | Drafting, thread summaries, sheet organization, slide and image generation, meeting notes | "summarize this thread", "notes from the Meet call"                        |
| Gemini Enterprise           | Organization-wide AI destination               | Company data across repositories and systems, permission-aware | **Multimodal search, custom agent capabilities, Gemini Notebook API**                     | "employees can't find institutional knowledge", "shared HR or sales agent" |

- **Gems:** write instructions (role, tone, rules) once and the Gem applies them in every chat. Value: consistency, and one good prompt writer can standardize a team's output.
- **Gemini Enterprise capabilities:**
  - Multimodal search spans documents, decks, images, and other media, not only text.
  - Custom agents are built and shared without application code, grounded in chosen company sources.
  - Gemini Notebook API exposes notebook-style, source-grounded research (briefings and summaries drawn from a trusted source set the team picks) to developers' internal tools.
  - Answers respect each user's existing access rights.
- **Workspace advantage:** context without copy-paste, and Workspace's existing security and compliance controls carry over.
- **Value ladder:** personal productivity (Gemini app), workforce-wide time savings (Workspace), unlocked institutional knowledge (Gemini Enterprise).
- **Traps:** a custom-built option offered when a prebuilt product already covers the need is usually wrong. The Gemini app is also the cheapest way to build AI literacy, since skills carry over to the other two.

📖 Full lesson: [Prebuilt Gen AI at Work: Gemini App, Gemini Enterprise, and Workspace](https://www.savemycert.com/revision/gcp-generative-ai-leader/gemini-app-enterprise-workspace-prebuilt-ai/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)

## 2.3 Describe how Google Cloud's gen AI offerings improve the customer experience

- **Two families:** first place the scenario as a findability problem (external search) or a support problem (Customer Engagement Suite).
- **Agent Search** runs on the Gemini Enterprise Agent Platform and embeds Google-quality search in your own site or app. It understands intent, not just keywords, handles multimodal content, and returns generated answers grounded in your content with source references (prebuilt RAG). Value: better product discovery and conversion, higher order value through recommendations, and support contacts deflected before they start.
- **Grounding with Google Search:** ties answers to fresh public web information, past the model's knowledge cutoff.
- **Key split:** Agent Search grounds in **your enterprise content**; Google Search grounding uses **world knowledge**. One assistant can use both (your change-fee policy plus current destination news).

| Component                           | Job                                                                                   | Serves                              | Benefit                                                         |
| ----------------------------------- | ------------------------------------------------------------------------------------- | ----------------------------------- | --------------------------------------------------------------- |
| Conversational Agents               | Virtual agents over chat and voice that resolve requests, grounded in company content | Customers (self-service)            | 24/7 answers, deflection, lower cost per resolution             |
| Agent Assist                        | Live transcription, suggested replies, surfaced knowledge, auto-summaries             | Human agents during calls and chats | Shorter handle time, consistency, faster new-hire ramp-up       |
| Conversational Insights             | Analyzes all conversations for topics, sentiment, contact drivers                     | Supervisors and CX leaders          | Root-cause fixes, coaching, quality monitoring without sampling |
| Contact Center as a Service (CCaaS) | Cloud contact-center platform: telephony, omnichannel routing, interaction management | The whole operation                 | No on-prem phone systems, elastic scale, native AI integration  |

- **Conversational Agents mix** deterministic, rule-based flows (identity checks, refund rules) with generative answers for unscripted questions. That hybrid is the answer to "gen AI is too unpredictable for regulated processes".
- **Memory aid:** Conversational Agents speak to the customer; Agent Assist coaches the employee; Conversational Insights reviews everything afterward; CCaaS is the platform under all three.
- **Most common trap:** Conversational Agents vs Agent Assist. Decide by who the AI is talking to.
- **Full loop:** search deflects, virtual agents resolve routine requests, CCaaS routes complex ones to people helped by Agent Assist, and Insights finds the root cause (for example, a confusing charge) so volume falls.

📖 Full lesson: [Improving Customer Experience with Agent Search and Customer Engagement Suite](https://www.savemycert.com/revision/gcp-generative-ai-leader/google-cloud-customer-engagement-agent-search/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)

## 2.4 Describe how Google Cloud empowers developers to build with AI

- **Agent Platform:** one governed environment to discover models, ground them in company data, and build, deploy, and manage agents. Value: speed (start from pretrained parts), accessibility (AutoML, low-code agent building), and consistent governance.

| Offering                        | Does                                                                                                   | Cue                                                                      |
| ------------------------------- | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------ |
| Model Garden                    | Curated catalog of Google (Gemini, Imagen, Veo, Gemma), open, and partner models, with docs to compare | "compare models on quality, latency, cost", "avoid betting on one model" |
| Agent Search                    | Managed search and grounded Q&A over your content with source references                               | "trusted answers over our documents, fast, no search engineers"          |
| Agent Platform AutoML           | Trains a custom model from your labeled data through a guided flow, no training code                   | "defects unique to our line", "our own category labels", "no ML team"    |
| Prebuilt RAG with Agent Search  | Whole retrieval pipeline managed: ingest, index, retrieve, cite                                        | "grounded answers with minimal engineering"                              |
| RAG APIs                        | Component services (parsing and chunking, embeddings, retrieval, ranking) you assemble                 | "custom retrieval strategy", "unusual formats", "control over each step" |
| Custom agents on Agent Platform | Goals, instructions, data stores, and tools for multi-step work                                        | "takes actions", "completes the workflow"                                |

- **Why RAG:** models have a knowledge cutoff, know nothing about private data, and can hallucinate. Retrieval at question time fixes all three without retraining.
- **AutoML vs foundation model:** if a general model already handles the task via prompting or grounding, that is cheaper. AutoML fits when the knowledge lives only in your labeled data.
- **Selection rule:** prefer the most prepackaged option that satisfies the requirement. Each step toward custom (Agent Search, then RAG APIs, then fully custom agents) adds engineering cost that a real requirement must justify.
- **Agents vs Q&A:** a scenario that only needs answers points to Agent Search. One that needs actions (check status, request documents, draft a letter) points to a custom agent.

📖 Full lesson: [How Google Cloud Empowers Developers: Agent Platform and RAG](https://www.savemycert.com/revision/gcp-generative-ai-leader/google-cloud-agent-platform-rag-developers/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)

## 2.5 Define the purpose and types of tooling for gen AI agents

- **Why tools:** a bare model has frozen knowledge, no access to your systems, and cannot act. Tools connect the agent to the outside world. Agent loop: goal, reason, pick a tool, use it, observe, repeat until done. Which systems an agent may touch is a governance decision.

| Tool type   | Connects to                                                | Who executes                                                                     | Cue                                                                            |
| ----------- | ---------------------------------------------------------- | -------------------------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| Extensions  | External APIs through standardized, often prebuilt bridges | The agent platform, on the agent's behalf                                        | "live fares", low-risk lookups                                                 |
| Functions   | Actions you define (name, purpose, parameters)             | **Your application**, client side; the model only outputs the call and arguments | "must validate or approve before it happens", orders, payments, record changes |
| Data stores | Your documents, sites, and structured data                 | Platform retrieves content at question time                                      | "answer from current policy with citations"                                    |
| Plugins     | Outside applications and services                          | The connected application                                                        | "act inside our storefront or scheduling system"                               |

- **Shorthand:** extensions and plugins reach out; functions keep control; data stores know your business.
- **Data stores = RAG as a tool:** update the document and answers change immediately, with no retraining.
- **Backing services:** Cloud Storage (files that feed data stores), databases (live records), Cloud Functions (small event-driven logic behind a function call), Cloud Run (containerized services such as a pricing engine), Agent Platform (where the agent is built and governed).
- **Pre-built AI APIs (senses for agents):**
  - Speech-to-Text: callers speak. Text-to-Speech: agent answers aloud.
  - Translation: many languages, full documents.
  - Document AI: pull fields from invoices, claims, IDs.
  - Cloud Vision: understand an uploaded photo.
  - Video Intelligence: detect scenes, objects, and text in video.
  - Natural Language: sentiment and entities, e.g., spot frustration and route urgent cases.
- **Agent Studio vs Google AI Studio:** Google AI Studio is a light web tool to prototype prompts and try Gemini. Agent Studio (part of Agent Platform) builds grounded, governed, production agents. Cues: "experiment, prototype" vs "production, company data, at scale". They are stages of one journey.

📖 Full lesson: [Gen AI Agent Tooling: Extensions, Functions, Data Stores, and Plugins](https://www.savemycert.com/revision/gcp-generative-ai-leader/gen-ai-agent-tooling-extensions-functions/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)

[← Back to the study guide](../README.md)
