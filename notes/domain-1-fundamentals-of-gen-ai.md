# Domain 1: Fundamentals of gen AI (30%)

This domain covers the vocabulary of generative AI, how data type and quality shape results, the five layers of the gen AI landscape, and which Google foundation model fits which job. Most questions hand you a description or a business scenario and ask for the matching term, layer, or model.

## 1.1 Describe core generative AI concepts and use cases

- **Nesting of terms:** AI (machines doing tasks that need human-like intelligence) contains machine learning (models learn from data instead of hand-coded rules), which contains generative AI (produces new text, images, code, audio, or video).
- **Quick test:** if the output is new content, it is generative AI. If the output is a label or a forecast, it is traditional (predictive) ML.
- **NLP:** the AI field for understanding and producing human language (translation, sentiment, chat). LLMs build on it.

| Term | Means | Exam cue |
|---|---|---|
| Foundation model | Large model pretrained on broad data, then adapted to many tasks | "one model reused for summarizing, drafting, classifying" |
| LLM | Foundation model specialized in language; predicts likely next words | "answer questions, draft, translate, write code" |
| Multimodal foundation model | One model that handles text, images, audio, and video together | "photo plus report", "recorded meeting to action items" |
| Diffusion model | Generates images by learning to turn random noise into a picture step by step | "create visuals from a written brief" |
| Prompt engineering | A person writes better instructions, context, examples, and format | "no training, immediate, anyone can do it" |
| Prompt tuning | The system learns an optimized prompt from examples; base weights stay frozen | "task-specific behavior, cheaper than fine-tuning" |

- **Customization order (cheapest first):** prompt engineering, then prompt tuning, then fine-tuning. Pick the least training effort that meets the quality bar.
- **ML approaches:**
  - Supervised = labeled examples with known answers (spam filters, fraud flags, sales forecasts).
  - Unsupervised = unlabeled data, the model finds structure (customer segments, anomalies, market-basket patterns).
  - Reinforcement = trial and error with rewards and penalties (recommendations, robotics). Human feedback as a reward signal also helps refine LLMs.
- **ML lifecycle (a loop, not a line):** data ingestion, data preparation, model training, model deployment, model management.
  - Ingestion: Cloud Storage (files), BigQuery (analytics data), Pub/Sub (event streams).
  - Preparation: Dataflow and BigQuery transform data at scale. Weak preparation is the usual reason projects underdeliver.
  - Management: monitor quality, track versions, watch for drift, retrain. This feeds back into new data.
- **Choosing a foundation model:** weigh modality, context window, security, availability and reliability, cost, performance, fine-tuning support, and customization. Simple high-volume work often favors a lighter, cheaper model. Complex reasoning over long or mixed inputs points to a frontier multimodal model with a long context window.
- **Trap:** "use the most capable model" is rarely the right answer. Match the deciding constraint (cost, security, modality) to the factor.
- **Four business value verbs:**
  - Create: marketing copy, campaign images, code, video.
  - Summarize: long reports to executive briefs, meeting recaps, ticket histories.
  - Discover: conversational search over internal documents, plain-language data analysis.
  - Automate: drafting replies, extracting invoice fields, classifying feedback, personalized experiences.

📖 Full lesson: [Generative AI Concepts: Foundation Models, LLMs, and Business Use Cases](https://www.savemycert.com/revision/gcp-generative-ai-leader/generative-ai-concepts-foundation-models-llms/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)

## 1.2 Describe how various data types are used in gen AI and the business implications

- **Core rule:** model output is capped by data quality. Bad data does not make the model fail loudly; it makes it confidently wrong.
- **Leader's two questions before picking a model:** does the data this use case needs exist, and can the AI reach it?

| Characteristic | Group | Question it asks | Failure example |
|---|---|---|---|
| Completeness | Quality | Is all needed information present? | A third of catalog items lack size and material, so the assistant cannot answer |
| Consistency | Quality | Is data uniform across systems and time? | One customer stored three ways looks like three people |
| Relevance | Quality | Does the data fit the problem? | A support bot grounded on old policy answers confidently and wrongly |
| Availability | Accessibility | Can the AI reach it, on time? | Data stuck in team spreadsheets or silos; stale price lists |
| Cost | Accessibility | What does acquiring, storing, cleaning, labeling cost? | Paid labeling and licensed datasets blow the budget |
| Format | Accessibility | Can AI systems process it as-is? | Scanned forms and audio need conversion first |

- **Structured data:** fixed schema of rows, columns, typed fields. Examples: POS transactions, CRM records, inventory tables, ledgers, timestamped sensor values. Lives in databases and BigQuery. In gen AI it grounds factual answers (order status, stock level) and powers personalization.
- **Unstructured data:** no predefined model; meaning sits inside the content. Examples: emails, chats, contracts, reviews, call recordings, photos, video, slide decks. Usually in Cloud Storage and content systems. It is **most** enterprise data, and foundation models are what finally make it usable.
- **Semi-structured:** some tags but no rigid table (invoices with varying layouts).
- **Labeled vs unlabeled:**
  - Labeled = tagged with the correct answer or attributes (spam/not spam, "defective part"). Used for supervised learning and fine-tuning. Expensive, because people (often experts) must label it.
  - Unlabeled = raw, no tags. Used for unsupervised learning and foundation-model pretraining. Cheap to collect, still needs cleaning.
- **Why foundation models are economical:** they are pretrained mostly on unlabeled data, so a company can adapt one with prompts, grounding, or a small labeled set instead of labeling millions of examples.
- **Business impact of poor data:** lost trust from wrong answers, bias and unfair outputs, inflated cost and delays, misleading decisions delivered with confidence, and use cases that stay out of reach.
- **Exam cues:** "call recordings" = unstructured; "table of daily sales" = structured; "tagged with the correct answer" = labeled. Fix data quality **before** scaling, not after launch.

📖 Full lesson: [Data Types in Gen AI: Quality, Structured vs Unstructured, Labeled Data](https://www.savemycert.com/revision/gcp-generative-ai-leader/gen-ai-data-types-quality-structured-unstructured/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)

## 1.3 Identify the core layers of the gen AI landscape and the business implications

- **Five layers, bottom to top:** infrastructure, models, platforms, agents, applications. Each consumes the one beneath it.

| Layer | Provides | Google examples | Business stance |
|---|---|---|---|
| Infrastructure | Compute, networking, storage for training and serving | AI Hypercomputer, TPUs, GPUs, Google data centers | Rent from a cloud provider; almost never build |
| Models | Foundation models (raw capability, not a product) | Gemini, Gemma, Imagen, Veo | Choose, and tune if justified; do not train from scratch |
| Platforms | Model access, customization, grounding, deployment, governance | Agent Platform, Model Garden, Google AI Studio | Invest here for custom, data-grounded solutions; needs developers |
| Agents | Model plus reasoning, memory, and tools that take actions | Custom agents on Agent Platform, Agent Studio, Conversational Agents | Automates ambiguous, language-heavy work; needs more governance |
| Applications | Products with gen AI already inside them | Gemini Enterprise, Gemini app, Gemini for Google Workspace | Fastest value, no dev team; least differentiation |

- **Trade-off:** lower in the stack = more control and differentiation, more cost and expertise. Higher = faster and cheaper, less customization. This is build vs buy decided per layer.
- **Typical enterprise pattern:** two layers at once. Applications for broad workforce productivity, plus the platform or agent layer for a few differentiating processes.
- **Agents:** they plan multi-step tasks and act (look up an order, check policy, issue a refund). Because they act, begin with agents that help a person, and only later let agents act on their own.
- **Placement traps:**
  - Model Garden is a **platform** capability. The models it lists belong to the models layer.
  - Gemini for Google Workspace is an **application**, not a platform.
  - An agent is not just a model: it adds tools and reasoning.
- **Mismatch errors the exam probes:** commissioning a custom build for a need an off-the-shelf app already covers, or expecting a productivity app to deliver a differentiated, data-grounded customer experience.
- **No dev team?** Start at the applications layer.

📖 Full lesson: [The Five Layers of the Gen AI Landscape and What They Mean for Business](https://www.savemycert.com/revision/gcp-generative-ai-leader/gen-ai-landscape-layers-infrastructure-models-agents/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)

## 1.4 Identify the use cases and strengths of Google's foundation models

- **Two sorting axes:** modality (what it reads and produces) and openness (managed service vs downloadable open weights).

| Model | What it is | Strengths | Scenario cue |
|---|---|---|---|
| Gemini | Flagship, natively multimodal model family (managed) | Reasoning across text, images, audio, video, and code; long context; conversation; coding help; agent "brain" | "analyze mixed documents, photos, and a call recording", "customer assistant" |
| Gemma | Lightweight open model family that shares research roots with Gemini | Open weights, self-host or run on devices, deep fine-tuning, low running cost | "run on-premises", "keep data in our environment", "on-device", "open model" |
| Imagen | Text-to-image model, also edits images | Photorealism, follows the prompt closely, background changes and scene extension | "product photos in many settings", "campaign visuals without a shoot" |
| Veo | Video generation from text or a starting image | High-definition clips, control over camera movement and style | "short promo video", "storyboard in motion", "animate a concept" |

- **Selection order:** first ask what the output modality is (still image = Imagen, moving video = Veo, understanding/reasoning/language/code = Gemini or Gemma). Then ask how much control is needed (open weights, self-hosting, strict data locality = Gemma; strongest capability with no ops burden = Gemini).
- **Gemma trade-off:** you gain control, customization, and cost efficiency, but you take on the operational work a managed service would do.
- **Other factors still apply:** context window, cost and performance at expected volume, security, availability, and fine-tuning needs.
- **Access paths:** builders reach all four through **Model Garden on Agent Platform**. Gemini also reaches end users directly through Gemini Enterprise, Gemini for Google Workspace, and the Gemini app.
- **Complements, not rivals:** one campaign can use Gemini for messaging, Imagen for stills, and Veo for video, with Gemma where an on-device or self-hosted model is required.
- **Traps:**
  - Imagen vs Veo is simply still vs moving.
  - Gemini vs Gemma is managed flagship vs lightweight open.
  - Generated media still needs responsible-use review before publishing.

📖 Full lesson: [Google's Foundation Models: Gemini, Gemma, Imagen, and Veo Explained](https://www.savemycert.com/revision/gcp-generative-ai-leader/google-foundation-models-gemini-gemma-imagen-veo/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)

[← Back to the study guide](../README.md)
