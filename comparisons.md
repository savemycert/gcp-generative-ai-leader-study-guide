# GenAI Leader Commonly Confused Services and Concepts

Side-by-side comparisons of the GenAI Leader services and ideas that exam questions most often set against each other. Each table ends with the one thing to remember.

- [Domain 1: Fundamentals of gen AI](#domain-1-fundamentals-of-gen-ai)
- [Domain 2: Google Cloud's gen AI offerings](#domain-2-google-clouds-gen-ai-offerings)
- [Domain 3: Techniques to improve gen AI model output](#domain-3-techniques-to-improve-gen-ai-model-output)
- [Domain 4: Business strategies for a successful gen AI solution](#domain-4-business-strategies-for-a-successful-gen-ai-solution)

## Domain 1: Fundamentals of gen AI

### Gemini vs Gemma vs Imagen vs Veo

| | Gemini | Gemma | Imagen | Veo |
|---|---|---|---|---|
| What it is | Flagship multimodal model family | Family of lightweight open models | Text-to-image model | Video generation model |
| Output | Text and more, from mixed text, image, audio, video, and code input | Language output from a model you host | Still images, plus edits to existing images | Moving video clips from text or a starting image |
| How you get it | Managed service (Model Garden, Gemini apps) | Download the weights and run or fine-tune them yourself | Managed service (Model Garden) | Managed service (Model Garden) |
| Main strength | Reasoning over long, mixed inputs | Control, customization, low running cost | Photorealistic visuals from a description | Cinematic control of camera and style |
| Exam cue | "Analyze documents, photos, and a call together" | "Run on-premises or on-device", "open weights" | "Product shots in a dozen settings" | "Short promo clip", "storyboard in motion" |

**Remember:** pick by output modality first (still = Imagen, moving = Veo), then by control (self-hosted or open = Gemma, managed = Gemini).

### Structured vs Unstructured data

| | Structured | Unstructured |
|---|---|---|
| What it is | Data in a fixed schema of rows, columns, and typed fields | Free-form content whose meaning sits inside it |
| Examples | Sales transactions, CRM records, inventory tables, sensor readings | Emails, contracts, reviews, call recordings, photos, video |
| Typical home | Relational databases, BigQuery | Cloud Storage, content and email systems |
| Share of enterprise data | The smaller part | The large majority |
| Role in gen AI | Grounds exact facts; feeds personalization | Main fuel for summarization, conversational search, content understanding |
| Exam cue | "A spreadsheet of quarterly sales" | "Support-call recordings", "customer reviews" |

**Remember:** gen AI's distinctive value over older analytics is that it can finally use unstructured data.

### Supervised vs Unsupervised vs Reinforcement learning

| | Supervised | Unsupervised | Reinforcement |
|---|---|---|---|
| Data | Labeled examples with known answers | Unlabeled data | Feedback from an environment |
| How it learns | Maps inputs to correct outputs | Finds groupings and patterns on its own | Trial and error, maximizing reward |
| Business examples | Spam filtering, fraud detection, sales forecasting | Customer segmentation, anomaly detection | Recommendations, robotics, resource optimization |
| Exam cue | "Labeled", "tagged with the correct answer" | "Discover segments nobody defined" | "Rewards and penalties over repeated attempts" |

**Remember:** read the data description. Labels mean supervised, no labels mean unsupervised, rewards mean reinforcement.

### Platforms layer vs Applications layer

| | Platforms | Applications |
|---|---|---|
| What it is | Tools to access, customize, ground, deploy, and govern models | Finished products with gen AI already built in |
| Who uses it | Developers and builders | End users |
| Google examples | Agent Platform, Model Garden, Google AI Studio | Gemini app, Gemini for Google Workspace, Gemini Enterprise |
| Trade-off | Custom, data-grounded, differentiating, but needs a dev team | Fastest value and no engineering, but little differentiation |
| Exam cue | "Build a claims tool grounded in our own policies" | "Help all staff draft and summarize, starting this week" |

**Remember:** buy applications for common needs, build on the platform for needs unique to your data and workflows.

## Domain 2: Google Cloud's gen AI offerings

### Gemini app vs Gemini for Google Workspace vs Gemini Enterprise

| | Gemini app (and Gemini Advanced) | Gemini for Google Workspace | Gemini Enterprise |
|---|---|---|---|
| What it is | Standalone conversational assistant | Gemini built into Gmail, Docs, Sheets, Slides, Meet, and Chat | Organization-wide AI front door over company data |
| Scope | One person | One person, inside their own work | The whole organization |
| Grounded in | General knowledge plus uploads | The user's own mail, files, and meetings | Company repositories and systems, permission-aware |
| Named capabilities | Gems (in Gemini Advanced) | Drafting, thread and meeting summaries, slide and image generation | Multimodal search, custom agents, Gemini Notebook API |
| Exam cue | "Reusable assistant for a recurring task" | "Summarize this email thread", "meeting action items" | "Staff can't find what the firm already knows" |

**Remember:** decide by scope and grounding: one person with general knowledge, one person in their own files, or the whole company's data.

### Conversational Agents vs Agent Assist vs Conversational Insights

| | Conversational Agents | Agent Assist | Conversational Insights |
|---|---|---|---|
| What it is | Virtual agents that resolve requests over chat and voice | Real-time copilot for human agents | Analytics across all conversations |
| Who it talks to | The customer | The employee, never the customer | Supervisors and CX leaders, after the fact |
| What it does | Self-service with rule-based flows plus grounded generative answers | Transcribes, surfaces knowledge, suggests replies, summarizes | Surfaces topics, sentiment, and drivers of contact volume |
| Business benefit | Deflection, 24/7 service, lower cost per contact | Shorter handle time, consistency, faster ramp-up | Root-cause fixes, evidence-based coaching |
| Exam cue | "Customers solve it themselves" | "Make human agents faster and more consistent" | "Why are customers calling so much?" |

**Remember:** ask who the AI is serving. Contact Center as a Service is the platform all three run on.

### Prebuilt RAG with Agent Search vs RAG APIs

| | Prebuilt RAG with Agent Search | RAG APIs |
|---|---|---|
| What it is | A fully managed retrieval pipeline | Component services you assemble into your own pipeline |
| Covers | Ingest, index, retrieve, ground with citations, all in one | Parsing and chunking, embeddings, retrieval, ranking |
| Effort | Lowest; nothing to maintain | Higher; you own the pipeline |
| Use it when | Standard enterprise content needs grounding quickly | You need a custom retrieval strategy, unusual formats, or tight app integration |
| Exam cue | "Minimal engineering", "fastest time to value" | "Control over each retrieval step" |

**Remember:** take the packaged option unless a stated requirement forces you to build.

### Extensions vs Functions (agent tools)

| | Extensions | Functions |
|---|---|---|
| What it is | Standardized, often prebuilt bridges to external APIs | Action definitions the model can choose from |
| Who executes the call | The agent platform, on the agent's behalf | Your application, on the client side |
| What the model does | Triggers the call; the result flows back into its reasoning | Outputs only the function name and arguments |
| Control | Convenience, less engineering | You validate, approve, and keep credentials away from the model |
| Exam cue | "Look up live public information" | "Must review before placing the order or changing the record" |

**Remember:** if the business must control what actually runs, the answer is functions.

### Google AI Studio vs Agent Studio

| | Google AI Studio | Agent Studio |
|---|---|---|
| What it is | Lightweight web tool for trying Gemini and prototyping prompts | Environment for building production agents within Agent Platform |
| Typical user | A developer testing an idea | Enterprise teams shipping agents to staff or customers |
| Company data | Not the focus | Connects to data stores and enterprise tools |
| Governance | Minimal, for individual exploration | Enterprise security, access control, production management |
| Exam cue | "Experiment", "prototype", "try a model" | "Production", "grounded in our data", "at scale" |

**Remember:** prototype in Google AI Studio, productionize in Agent Studio.

## Domain 3: Techniques to improve gen AI model output

### Prompt engineering vs Grounding/RAG vs Fine-tuning

| | Prompt engineering | Grounding / RAG | Fine-tuning |
|---|---|---|---|
| What it is | Better instructions, context, format, and examples | Supplying retrieved, authoritative content at answer time | Further training the model on curated examples |
| Changes the model? | No | No | Yes |
| Fixes | Tone, format, role, instruction-following | Stale facts, missing company knowledge, hallucination | Persistent domain vocabulary, style, or task-pattern gaps |
| Keeps knowledge current? | No | Yes; update the documents and answers follow | No; knowledge is fixed at training time |
| Cost and effort | Lowest | Moderate | Highest (quality data plus engineering) |
| Exam cue | "Output ignores our format" | "Bot invents details of the current promotion" | "Specialist clinical terms prompting can't capture" |

**Remember:** prompt first, ground next, fine-tune last, and keep a human in the loop wherever the stakes are high.

### Chain-of-thought vs ReAct

| | Chain-of-thought | ReAct |
|---|---|---|
| What it is | Asking the model to reason step by step before answering | Alternating reasoning with actions and observations |
| Information used | Only the prompt and trained knowledge | Also fetches what is missing (search, tool calls, lookups) |
| Best for | Calculations, multi-condition decisions, auditable logic | Tasks that need live or external data mid-task |
| Link to agents | Reasoning only | The core pattern behind tool-using agents |
| Exam cue | "Show the reasoning behind the cost comparison" | "Check current stock, then draft the reply" |

**Remember:** thinking alone is chain-of-thought; thinking plus fetching is ReAct.

### Zero-shot vs One-shot vs Few-shot prompting

| | Zero-shot | One-shot | Few-shot |
|---|---|---|---|
| Examples in the prompt | None | One | Several |
| Relies on | The model's general training | One demonstration of the target format | A pattern inferred from multiple examples |
| Use it for | Familiar tasks such as summarizing or translating | A format easier to show than describe | Nuanced classification, extraction, strict style |
| Exam cue | "Just summarize this transcript" | "Follow this one sample summary" | "Label tickets using our three categories" |

**Remember:** start with zero examples and add only as many as it takes to get consistent output.

### Temperature vs Top-p

| | Temperature | Top-p (nucleus sampling) |
|---|---|---|
| What it controls | How random each token choice is | How big the pool of candidate tokens is |
| Mechanism | Sharpens or flattens the probability differences between tokens | Keeps only the smallest set of tokens whose probabilities sum to p |
| Low setting | Focused, repeatable output | Only a few high-probability tokens considered |
| High setting | Varied, creative output | A wider candidate pool |
| Exam cue | "Make the legal assistant less creative" | "Cut off unlikely word choices" |

**Remember:** both steer consistency vs variety; low values suit factual and grounded tasks.

### First-party vs Third-party vs World data

| | First-party | Third-party | World |
|---|---|---|---|
| What it is | Data your organization creates and owns | External data you acquire from providers or partners | Broad public knowledge that keeps changing |
| Examples | Policies, manuals, CRM records | Licensed research, market feeds, partner catalogs | Google Search results, news, public websites |
| Google Cloud route | Agent Search / RAG | RAG over the acquired data | Grounding with Google Search |
| Exam cue | "Our refund policy" | "Industry benchmark rates" | "Last week's announcement" |

**Remember:** start from the question, then pick the source that authoritatively holds the answer.

## Domain 4: Business strategies for a successful gen AI solution

### Anonymization vs Pseudonymization

| | Anonymization | Pseudonymization |
|---|---|---|
| What it is | Irreversibly removing or transforming identifying information | Replacing identifiers with artificial tokens |
| Re-identification | Not possible, even for the data holder | Possible through a mapping stored separately and securely |
| Legal status | Generally outside most privacy regulation | Still personal data under most privacy laws |
| Use it when | You never need to link data back to a person | You must be able to re-link, e.g., to honor a deletion request |
| Exam cue | "Dataset for training that can never identify anyone" | "Customer IDs swapped for tokens, key held elsewhere" |

**Remember:** if the data can be re-linked to a person, it is pseudonymized, not anonymized.

### Secure AI vs Responsible AI

| | Secure AI | Responsible AI |
|---|---|---|
| What it is | Protecting AI systems from attack, unauthorized access, and misuse | Building and running AI to be fair, transparent, private, accountable, explainable |
| Main risk | Poisoning, prompt injection, model theft, evasion, data leakage | Bias, undisclosed AI use, privacy harm, unexplainable decisions |
| Google anchor | SAIF plus secure-by-design infrastructure, IAM, Security Command Center, monitoring | AI Principles plus safety filters, evaluation tooling, grounding with citations |
| Who is accountable | Shared: Google secures the platform, the customer governs access and data | Always the deploying business |
| Exam cue | "Crafted prompt made the bot reveal another customer's data" | "Screening summaries favor one group of applicants" |

**Remember:** an attacker or an access failure points to secure AI; unfair, hidden, or unexplainable outcomes point to responsible AI.

### Security Command Center vs IAM vs Workload monitoring

| | Security Command Center | IAM | Workload monitoring |
|---|---|---|---|
| What it is | Central security posture management | Access control for resources | Observation of running systems |
| Job | Finds misconfigurations, vulnerabilities, and threats across the organization | Decides who can do what on which resource, with least privilege | Logs activity, tracks performance, alerts on anomalies |
| Lifecycle fit | The organization-wide view | Data, training, and deployment access | Post-launch monitoring |
| Exam cue | "One view of security weaknesses across all projects" | "Too many people can modify the training data" | "Unusual query pattern suggests probing" |

**Remember:** posture = Security Command Center, access = IAM, runtime behavior = monitoring.

### Transparency vs Explainability vs Accountability

| | Transparency | Explainability | Accountability |
|---|---|---|---|
| What it is | Disclosing that AI is used, what data it relies on, and its limits | Being able to say why the system produced a given output | Named people and processes answer for AI outcomes |
| Question it answers | "Is AI involved here, and what can it do?" | "Why this result?" | "Who owns this, and how do I appeal?" |
| Typical practice | Label AI agents and AI content; publish AI use policies | Model documentation, cited sources, human verification | Owners per use case, usage policies, human oversight, appeal channels |
| Exam cue | "Customers weren't told a bot was answering" | "No one can justify why the loan was declined" | "Nobody was responsible when the tool went wrong" |

**Remember:** transparency is about disclosure, explainability is about reasons, accountability is about ownership.

[← Back to the study guide](README.md)
