# GenAI Leader Sample Questions with Answers

20 worked practice questions for the **Google Cloud Generative AI Leader (GenAI Leader)** exam. Try each one before you open the answer.

For many more, with the same explanation on every option, use the [GenAI Leader practice questions](https://www.savemycert.com/practice/gcp-generative-ai-leader/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide) on SaveMyCert.

## Question 1

*Fundamentals of gen AI*

**A board member asks how artificial intelligence, machine learning, natural language processing and generative AI fit together. Which statement describes the relationship correctly?** Choose one.

- **a.** Generative AI and machine learning are sibling subsets of artificial intelligence that do not overlap.
- **b.** Generative AI is a subset of machine learning, and machine learning is a subset of artificial intelligence.
- **c.** Machine learning is a subset of generative AI, and generative AI is a subset of artificial intelligence.
- **d.** Natural language processing is the umbrella field, with machine learning and generative AI inside it.

<details>
<summary>Show answer and explanation</summary>

**Answer: b**

- **a** ❌ Gen AI is not a separate sibling of ML: generative models are trained with machine learning, so gen AI lies inside ML.
- **b** ✅ AI is the umbrella field, ML is the part of AI that learns from data, and generative AI is the part of ML that produces new content.
- **c** ❌ This inverts the nesting. Generative AI is built from machine learning techniques, so it sits inside ML, not around it.
- **d** ❌ NLP is the area of AI concerned with human language. It is not the umbrella; image and video generation are gen AI but are not NLP.

**The concept.** AI is the broad field of machines doing tasks that normally need human intelligence; machine learning is the subset that learns patterns from data; generative AI is the subset of ML that creates new content. Natural language processing is the area of AI focused on understanding and generating human language.

**Why this is correct.** Generative AI is a specialisation within machine learning, which is itself one approach within AI, so the circles nest AI > ML > gen AI. Inverting the order fails because gen AI depends on ML training. Treating gen AI and ML as non-overlapping siblings misses that every generative model is a machine learning model. Making NLP the umbrella confuses one application area (language) with the whole field; NLP overlaps gen AI where models generate text, but image generation is gen AI without being NLP.

**How to reason it out**

1. Start from the broadest term: AI covers any machine performing intelligent tasks.
2. Narrow to ML: AI systems that learn from data instead of hand-written rules.
3. Narrow again to gen AI: ML models whose output is new content.
4. Place NLP as the language-focused area of AI, not as the umbrella over the others.

> **Exam tip:** AI > machine learning > generative AI; NLP is the language area of AI, not the umbrella.

</details>

📖 Learn this topic: [Generative AI Concepts: Foundation Models, LLMs, and Business Use Cases](https://www.savemycert.com/revision/gcp-generative-ai-leader/generative-ai-concepts-foundation-models-llms/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)

---

## Question 2

*Fundamentals of gen AI*

**A product leader learns that one model could serve summarization, drafting and classification instead of three separately built models. Which description matches this kind of model?** Choose one.

- **a.** A large model trained on one domain's data that performs that domain's single task
- **b.** A small model trained from scratch on one team's labeled data for a single business task
- **c.** A large model pretrained on broad data that can be adapted to many downstream tasks
- **d.** A general pretrained model fine-tuned on one company's data to perform one specialised task

<details>
<summary>Show answer and explanation</summary>

**Answer: c**

- **a** ❌ Size alone does not make a model reusable. A model trained on one domain's data for one task is still task-specific; a foundation model's range comes from pretraining on broad, diverse data.
- **b** ❌ That is a conventional task-specific model, the approach a foundation model replaces; it cannot be reused across many tasks.
- **c** ✅ This is the definition of a foundation model: broad pretraining once, then adaptation to many tasks through prompting, tuning or fine-tuning.
- **d** ❌ That describes a model after it has been adapted for one task. The reusable starting point described in the stem is the foundation model itself.

**The concept.** A foundation model is a large model pretrained on vast, broad data so it can be adapted to many downstream tasks. Reusing one pretrained model cuts the time, data and cost of building a separate model per task.

**Why this is correct.** The stem's clue is reuse: one model serving several different tasks. Only a model pretrained on broad data has that generality. A small task-specific model trained on one team's labels is the old pattern foundation models replace. A large model trained on one domain's data for one task is big but still narrow. A fine-tuned model is a foundation model that has already been narrowed to one task, so it is the result of adaptation, not the reusable base.

**How to reason it out**

1. Spot the requirement: one model reused across several tasks.
2. Ask what gives a model that range: broad pretraining on large, diverse data.
3. Separate the base model (foundation model) from a version adapted to one task (fine-tuned model).

> **Exam tip:** Foundation model = pretrained once on broad data, adapted to many tasks.

</details>

📖 Learn this topic: [Generative AI Concepts: Foundation Models, LLMs, and Business Use Cases](https://www.savemycert.com/revision/gcp-generative-ai-leader/generative-ai-concepts-foundation-models-llms/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)

---

## Question 3

*Fundamentals of gen AI*

**A company evaluating gen AI for drafting replies and answering staff questions asks what a large language model (LLM) is. Which statement best describes it?** Choose one.

- **a.** A supervised classifier trained on labeled language data that sorts documents into fixed categories
- **b.** A diffusion model trained on image and caption pairs that generates pictures from a language prompt
- **c.** A foundation model trained on very large volumes of text that can understand and generate language
- **d.** A rules-based language system that parses sentences with grammar rules written by linguists

<details>
<summary>Show answer and explanation</summary>

**Answer: c**

- **a** ❌ That is traditional NLP classification: it labels text but cannot generate new language or answer open questions.
- **b** ❌ That describes an image model such as Imagen. It accepts a text prompt but its output is images, not language.
- **c** ✅ An LLM is a language-specialised foundation model: trained on huge text corpora, it predicts likely next tokens, which lets it answer, draft, translate and write code.
- **d** ❌ Rule-based NLP predates machine learning; it is not trained on data and is not a foundation model.

**The concept.** A large language model is a foundation model specialised in language. Trained on enormous text datasets, it predicts the most likely next words, which lets it understand and generate human language for tasks such as drafting, Q&A, translation and code. It builds on natural language processing (NLP), the field of AI concerned with language.

**Why this is correct.** Drafting replies and answering questions both need a model that both understands and generates language, which is what an LLM is. A text-to-image diffusion model takes language in but produces images. A supervised text classifier understands text only enough to assign a label. A rule-based parser is pre-ML NLP with no pretraining.

**How to reason it out**

1. Note the outputs needed: generated text and answers.
2. Recall that an LLM is a foundation model trained on large text corpora to understand and generate language.
3. Reject options that only classify text, only produce images, or are not trained at all.

> **Exam tip:** LLM = language-specialised foundation model that both understands and generates text.

</details>

📖 Learn this topic: [Generative AI Concepts: Foundation Models, LLMs, and Business Use Cases](https://www.savemycert.com/revision/gcp-generative-ai-leader/generative-ai-concepts-foundation-models-llms/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)

---

## Question 4

*Fundamentals of gen AI*

**Which description best defines structured data?** Choose one.

- **a.** Data in which each example carries a tag with its correct answer or category
- **b.** Free-form content with no predefined model, such as emails, contracts and call videos
- **c.** Data that has been cleaned so that no records have missing or duplicated values
- **d.** Data that fits a predefined schema, such as rows and columns in a database table

<details>
<summary>Show answer and explanation</summary>

**Answer: d**

- **a** ❌ This defines labeled data. Labeling is a separate axis from structure: a table can be unlabeled and a folder of photos can be labeled.
- **b** ❌ This defines unstructured data. Emails, contracts and video have no fixed fields; the meaning lives inside the content itself.
- **c** ❌ This describes data quality (completeness and consistency), not structure. Messy data can still be structured, and clean data can be unstructured.
- **d** ✅ Correct. Structured data follows a fixed schema of fields and data types, which is what makes it easy to query, aggregate and validate.

**The concept.** Structured data conforms to a predefined schema (rows, columns, defined fields and types); unstructured data is free-form content such as documents, images, audio and video. Whether data is labeled, and whether it is clean, are separate properties.

**Why this is correct.** The defining trait of structured data is its predefined schema: every value has a fixed place, like a column in a database table. The tempting alternatives describe other axes this topic also tests — tags carrying correct answers make data labeled, and the absence of gaps or duplicates is a quality property. Free-form content is the opposite category, unstructured data.

**How to reason it out**

1. Ask whether every value has a defined place in a fixed schema of fields.
2. If it does, the data is structured — sales transactions, CRM records, inventory tables.
3. Keep the other axes separate: labeled versus unlabeled is about tags; complete versus incomplete is about quality.

> **Exam tip:** Structure means a predefined schema; labels and quality are different questions about the same data.

</details>

📖 Learn this topic: [Data Types in Gen AI: Quality, Structured vs Unstructured, Labeled Data](https://www.savemycert.com/revision/gcp-generative-ai-leader/gen-ai-data-types-quality-structured-unstructured/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)

---

## Question 5

*Fundamentals of gen AI*

**Which layer of the gen AI landscape provides the physical compute, storage, and networking needed to train and serve foundation models?** Choose one.

- **a.** Agents
- **b.** Models
- **c.** Infrastructure
- **d.** Applications

<details>
<summary>Show answer and explanation</summary>

**Answer: c**

- **a** ❌ The agents layer contains software that reasons and takes actions toward goals; it runs on top of models and infrastructure rather than providing compute.
- **b** ❌ The models layer contains the foundation models themselves, such as Gemini. The models depend on the infrastructure layer for the compute used to train and run them.
- **c** ✅ Correct. The infrastructure layer is the foundation of the gen AI stack: the hardware and systems, such as TPUs, GPUs, storage, and networking, that make training and serving large models possible.
- **d** ❌ The applications layer is the top of the stack, where end users interact with gen AI through finished products, not where compute resources live.

**The concept.** The gen AI landscape is commonly described as a stack of layers: infrastructure at the bottom, then models, platforms, agents, and applications at the top. Each layer builds on the one below it.

**Why this is correct.** The infrastructure layer is the hardware foundation. It includes accelerators like TPUs and GPUs, plus the storage and networking required to train foundation models on massive datasets and serve them to users at scale. Google's AI Hypercomputer is an example of an integrated infrastructure offering. The other layers all consume this compute rather than provide it: models are trained on it, platforms manage it, and agents and applications run on top of it.

**How to reason it out**

1. Recall the five layers of the gen AI landscape: infrastructure, models, platforms, agents, and applications.
2. Identify what the question is asking about: raw compute, storage, and networking, which are hardware concerns.
3. Map hardware concerns to the bottom layer of the stack, which is infrastructure.

> **Exam tip:** Infrastructure is the bottom layer of the gen AI stack, supplying the compute (TPUs, GPUs), storage, and networking that every other layer depends on.

</details>

📖 Learn this topic: [The Five Layers of the Gen AI Landscape and What They Mean for Business](https://www.savemycert.com/revision/gcp-generative-ai-leader/gen-ai-landscape-layers-infrastructure-models-agents/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)

---

## Question 6

*Fundamentals of gen AI*

**Which characteristic most distinguishes Gemini from Google's other foundation models?** Choose one.

- **a.** A lightweight design with open weights for running on a developer's own laptop
- **b.** A focus on generating photorealistic still images from natural-language prompts
- **c.** A focus on generating short cinematic video clips from text or image prompts
- **d.** A native multimodal design that reasons over text, images, audio, video and code

<details>
<summary>Show answer and explanation</summary>

**Answer: d**

- **a** ❌ That is Gemma: a family of lightweight open models whose weights can be downloaded. Gemini is Google's flagship model, used as a managed service.
- **b** ❌ Generating still images from text is Imagen's specialty, not the trait that defines Gemini.
- **c** ❌ Generating video from a text or image prompt is Veo's role. Gemini understands video as an input; it is not Google's video generation model.
- **d** ✅ Correct. Gemini was built multimodal from the start, so a single model can take mixed inputs and reason across them together.

**The concept.** Google's four named foundation models split by modality and openness: Gemini (multimodal reasoning, managed), Gemma (lightweight open models), Imagen (images) and Veo (video).

**Why this is correct.** Gemini's defining trait is native multimodality: it was trained from the outset on several kinds of content, so one model can read a document, look at images, listen to audio and watch video in the same request and connect them. Each distractor is the headline strength of a sibling model: open, lightweight weights describe Gemma; photorealistic stills describe Imagen; cinematic clips describe Veo.

**How to reason it out**

1. List the four models and the single headline strength of each.
2. Match open, lightweight weights to Gemma, still images to Imagen and video clips to Veo.
3. The remaining trait, reasoning across many content types in one model, is Gemini's.

> **Exam tip:** Gemini = multimodal reasoning; Gemma = open and lightweight; Imagen = images; Veo = video.

</details>

📖 Learn this topic: [Google's Foundation Models: Gemini, Gemma, Imagen, and Veo Explained](https://www.savemycert.com/revision/gcp-generative-ai-leader/google-foundation-models-gemini-gemma-imagen-veo/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)

---

## Question 7

*Fundamentals of gen AI*

**An insurer wants one model that takes a photo of vehicle damage, the customer's recorded voice description and the typed claim form, and reasons across all three in a single request. Which model capability is the insurer relying on?** Choose one.

- **a.** Multimodality
- **b.** Multilingual support
- **c.** A large context window
- **d.** Prompt tuning

<details>
<summary>Show answer and explanation</summary>

**Answer: a**

- **a** ✅ A multimodal foundation model, such as Gemini, accepts and combines several data types (images, audio, text) in one model.
- **b** ❌ Multilingual support means handling several human languages. The requirement here is several data types, not several languages.
- **c** ❌ Context window is how much input fits in one request. It does not by itself let a model interpret images or audio.
- **d** ❌ Prompt tuning adapts a model's behaviour for a task; it does not add the ability to process new data types.

**The concept.** A multimodal foundation model understands and combines more than one data type, such as text, images, audio and video, in a single model. Gemini is natively multimodal.

**Why this is correct.** The deciding detail is that the inputs are of different types: an image, audio and text. Handling several modalities in one request is multimodality. Multilingual support is the tempting near-twin, but it concerns languages, not data types. A large context window helps with long inputs, and prompt tuning shapes behaviour; neither lets a text-only model see a photo or hear a recording.

**How to reason it out**

1. List the input types: photo, audio, typed text.
2. Recognise that multiple data types in one model means multimodality.
3. Separate it from multilingual (languages) and context window (input size).

> **Exam tip:** Several data types in one model = multimodal; several languages = multilingual.

</details>

📖 Learn this topic: [Generative AI Concepts: Foundation Models, LLMs, and Business Use Cases](https://www.savemycert.com/revision/gcp-generative-ai-leader/generative-ai-concepts-foundation-models-llms/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)

---

## Question 8

*Google Cloud's gen AI offerings*

**A business leader asks what Google means when it calls itself an "AI-first" company. Which statement best describes the idea?** Choose one.

- **a.** Google ships each new AI capability to cloud customers before using it in its own consumer products.
- **b.** Google gives AI workloads scheduling priority over other customer workloads running in its cloud data centers.
- **c.** Google aims to be first to market with each new category of AI model, ahead of its research rivals.
- **d.** Google has put AI at the center of its research and products for years, and its gen AI builds on that.

<details>
<summary>Show answer and explanation</summary>

**Answer: d**

- **a** ❌ The order runs the other way more often: capabilities are refined in products used by billions, such as Search and Photos, and that experience feeds the cloud offerings.
- **b** ❌ AI-first is a strategic posture about where Google invests and what its products are built around, not a rule for scheduling customer workloads.
- **c** ❌ AI-first is not a first-to-market claim; it describes AI being the organizing principle of Google's research and products.
- **d** ✅ Correct. AI-first means AI sits at the center of Google's research and products, and that long-term investment is what its current gen AI solutions draw on.

**The concept.** Google's AI-first approach means AI is the organizing principle of the company's research and products rather than a product line added later.

**Why this is correct.** Google has invested in AI research for many years (its researchers introduced the Transformer architecture behind today's large language models) and has refined AI inside products such as Search, Maps, Photos and Gmail. The exam guide links this heritage and a commitment to future innovation to cutting-edge gen AI solutions: customers get models that come out of a continuing research pipeline. The distractors misread "first" as workload priority, a customer-before-internal release order, or a race to be first to market.

**How to reason it out**

1. Recall that "AI-first" describes Google's own strategy, not a rule applied to workloads or release order.
2. Connect that strategy to years of research and product investment.
3. Link the investment to the depth and pace of today's gen AI offerings.
4. Discard readings that treat "first" as priority, sequence or market timing.

> **Exam tip:** AI-first = AI at the core of Google's research and products for years, which is why its gen AI offerings stay at the cutting edge.

</details>

📖 Learn this topic: [Google Cloud's Gen AI Strengths: Platform, Infrastructure, and Openness](https://www.savemycert.com/revision/gcp-generative-ai-leader/google-cloud-gen-ai-strengths-platform/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)

---

## Question 9

*Google Cloud's gen AI offerings*

**A board member asks which qualities Google Cloud uses to describe its AI platform as enterprise-ready. Which list matches Google Cloud's description?** Choose one.

- **a.** Responsible, secure, private, reliable, and scalable
- **b.** Responsible, open, portable, multimodal, and fast
- **c.** Secure, private, governed, sustainable, and affordable
- **d.** Open, multimodal, grounded, low-code, and scalable

<details>
<summary>Show answer and explanation</summary>

**Answer: a**

- **a** ✅ Correct. These five qualities are how the exam guide and Google Cloud describe an enterprise-ready AI platform.
- **b** ❌ This mixes one enterprise-ready quality (responsible) with the open approach and model capabilities; secure, private, reliable and scalable are missing.
- **c** ❌ Secure and private belong to the set, but governance, sustainability and cost are not among the five named qualities; responsible, reliable and scalable are missing.
- **d** ❌ Openness, multimodality, grounding and low-code tools are real Google Cloud strengths, but they are not the set Google uses to define enterprise readiness.

**The concept.** Google Cloud defines an enterprise-ready AI platform by five qualities: responsible, secure, private, reliable and scalable.

**Why this is correct.** Each quality answers a different objection a board or regulator raises: responsible (published AI principles and safety tooling), secure (secure-by-design infrastructure, the Secure AI Framework), private (customer data not used to train foundation models without permission), reliable (high availability) and scalable (growth from pilot to company-wide rollout). The distractor lists borrow real strengths from elsewhere in the topic, such as openness or low-code tools, so only knowing the five-quality set separates them.

**How to reason it out**

1. Recall the five enterprise-ready qualities named in the exam guide.
2. Check each list for all five and nothing else.
3. Recognise openness, multimodality and low-code as other strengths, not enterprise-ready qualities.

> **Exam tip:** Enterprise-ready = responsible, secure, private, reliable, scalable.

</details>

📖 Learn this topic: [Google Cloud's Gen AI Strengths: Platform, Infrastructure, and Openness](https://www.savemycert.com/revision/gcp-generative-ai-leader/google-cloud-gen-ai-strengths-platform/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)

---

## Question 10

*Google Cloud's gen AI offerings*

**Before approving a pilot, an HR director asks what employees would actually get from the Gemini app. Which description is accurate?** Choose one.

- **a.** A standalone chat assistant on web and mobile for drafting, summarizing, and Q&A
- **b.** An assistant built into Gmail, Docs, and Sheets that works on the file already open
- **c.** A cloud contact-center platform that routes customer calls and chats to agents
- **d.** An organization-wide search and agent hub grounded in connected company systems

<details>
<summary>Show answer and explanation</summary>

**Answer: a**

- **a** ✅ Correct. The Gemini app is Google's conversational, multimodal assistant used directly on the web or a phone for everyday individual tasks.
- **b** ❌ That is Gemini for Google Workspace, which lives inside the productivity apps; the Gemini app is a separate chat destination.
- **c** ❌ That is Google Cloud Contact Center as a Service in the Customer Engagement Suite, a customer-support platform rather than an employee assistant.
- **d** ❌ That describes Gemini Enterprise. The Gemini app is a standalone assistant for individual work, not an organization-wide layer over connected company systems.

**The concept.** The Gemini app is Google's conversational AI assistant, available on the web and on mobile, where individuals chat with Gemini models to brainstorm, draft, summarize, analyze uploaded files and get answers.

**Why this is correct.** All four options describe real Google offerings, so the question is about positioning. The Gemini app is the standalone chat destination for an individual. Gemini for Google Workspace is the same family of models embedded inside Gmail, Docs and Sheets; Gemini Enterprise is the organization-wide layer grounded in company systems; Contact Center as a Service serves customers, not employees.

**How to reason it out**

1. Identify what the stem asks about: the Gemini app itself, for employees.
2. Recall that the Gemini app is a standalone chat assistant on web and mobile.
3. Separate it from its siblings: Workspace is embedded in the apps, Gemini Enterprise is grounded in company systems.
4. Discard the customer-facing contact-center platform.

> **Exam tip:** Gemini app = standalone chat assistant for an individual; Workspace = inside the apps; Gemini Enterprise = across company data.

</details>

📖 Learn this topic: [Prebuilt Gen AI at Work: Gemini App, Gemini Enterprise, and Workspace](https://www.savemycert.com/revision/gcp-generative-ai-leader/gemini-app-enterprise-workspace-prebuilt-ai/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)

---

## Question 11

*Google Cloud's gen AI offerings*

**A bank wants customers to check balances, report a lost card and ask policy questions by chat or phone at any hour, with no employee involved in routine requests. Which Customer Engagement Suite component is designed for this?** Choose one.

- **a.** Agent Assist, which suggests replies to staff as they handle each request
- **b.** Contact Center as a Service, which routes each request to an available employee
- **c.** Conversational Agents, which handle each request end to end as virtual agents
- **d.** Conversational Insights, which reviews completed requests for common themes

<details>
<summary>Show answer and explanation</summary>

**Answer: c**

- **a** ❌ Agent Assist supports an employee who is already in the conversation. The bank wants routine requests handled with no employee involved.
- **b** ❌ Contact Center as a Service is the platform that routes contacts. Routing to an employee is the opposite of what the bank asked for.
- **c** ✅ Correct. Conversational Agents are the suite's self-service virtual agents: they talk with the customer over chat and voice and resolve routine requests without a person.
- **d** ❌ Conversational Insights analyzes conversations after they happen. It tells the bank what customers ask about but does not answer anyone.

**The concept.** Conversational Agents are the Customer Engagement Suite's customer-facing self-service component.

**Why this is correct.** The deciding detail is that routine requests must be resolved with no employee involved, at any hour. That is self-service, and in the Customer Engagement Suite self-service is Conversational Agents: virtual agents that understand natural language over chat and voice and complete tasks such as balance checks or card reports. Agent Assist helps an employee who is already on the contact, Conversational Insights analyzes conversations afterwards, and Contact Center as a Service routes contacts to people.

**How to reason it out**

1. Note who the AI must talk to: the customer, directly.
2. Note the constraint: no employee in routine requests.
3. Match customer-facing self-service to Conversational Agents.
4. Reject the components that help staff, analyze afterwards or route to staff.

> **Exam tip:** Customer talks to the AI with no person involved: Conversational Agents.

</details>

📖 Learn this topic: [Improving Customer Experience with Agent Search and Customer Engagement Suite](https://www.savemycert.com/revision/gcp-generative-ai-leader/google-cloud-customer-engagement-agent-search/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)

---

## Question 12

*Google Cloud's gen AI offerings*

**A developer wants to browse one curated catalog that lists Gemini, Gemma, Imagen and Veo alongside open and partner options such as Llama and Claude, read a card describing each one, and compare them before choosing one for a new project. Which Google Cloud offering provides this?** Choose one.

- **a.** Document AI API
- **b.** Model Garden
- **c.** Agent Search
- **d.** Agent Platform AutoML

<details>
<summary>Show answer and explanation</summary>

**Answer: b**

- **a** ❌ Document AI is a pre-trained API that extracts structured data from documents. It is a single-task service, not a catalog of foundation models.
- **b** ✅ Correct. Model Garden is Agent Platform's curated library of Google, open and partner models, each with a model card, so developers can compare them and start using the one they choose.
- **c** ❌ Agent Search delivers out-of-the-box search and grounded answers over an organization's own content. It does not list or compare foundation models.
- **d** ❌ AutoML trains a new custom model from your own labeled data. It does not offer a catalog of existing Google, open and partner models to compare.

**The concept.** Model Garden is the model discovery hub inside Agent Platform: one curated library of Google's models (Gemini, Gemma, Imagen, Veo), open models and partner models, each documented with a model card describing capabilities, intended uses and limits.

**Why this is correct.** The developer's need is to discover and compare many existing models before committing, which is exactly Model Garden's job. Agent Search and AutoML are also Agent Platform capabilities, but one searches company content and the other trains a new model from labeled data. Document AI is a task-specific pre-trained API.

**How to reason it out**

1. Identify the need: compare many existing models (Google, open and partner) before choosing one.
2. Recall which Agent Platform capability is a catalog with a card per model: Model Garden.
3. Rule out Agent Search (searches your content) and AutoML (trains a new model), then the single-task Document AI API.

> **Exam tip:** Need to discover and compare existing models from Google, open and partner sources? That is Model Garden.

</details>

📖 Learn this topic: [How Google Cloud Empowers Developers: Agent Platform and RAG](https://www.savemycert.com/revision/gcp-generative-ai-leader/google-cloud-agent-platform-rag-developers/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)

---

## Question 13

*Google Cloud's gen AI offerings*

**A retailer's assistant, built on a foundation model alone, explains the refund policy well but cannot look up a customer's order or issue the refund. What does giving it tools add?** Choose one.

- **a.** Access to systems outside the model, to read live data and to take actions
- **b.** A longer context window, so the whole order database fits inside each prompt
- **c.** A fine-tuned copy of the model that has learned the retailer's refund process
- **d.** A cached export of the order database, loaded into the prompt each morning

<details>
<summary>Show answer and explanation</summary>

**Answer: a**

- **a** ✅ Correct. Tools connect the agent to the external environment: it can retrieve the current order and perform the refund rather than only describe the policy.
- **b** ❌ A bigger prompt is not a connection to live systems, and it still gives the model no way to act.
- **c** ❌ Tuning changes how a model responds, but a tuned model still cannot reach the order system or carry out a refund.
- **d** ❌ A daily snapshot in the prompt goes stale as soon as a new order or refund happens, and reading a copy gives the assistant no way to issue the refund.

**The concept.** A gen AI agent pairs a reasoning model with tools. The model decides what needs to happen; tools are how the agent reaches outside itself to retrieve live or private information and to take actions in other systems.

**Why this is correct.** A foundation model alone generates text from what it learned in training: it has no view of today's orders and no way to change anything. Tools close both gaps. The distractors either change the model (tuning, a longer context window) or feed it a copy of the data (a morning export in the prompt); none connects the agent to the live order system or lets it act.

**How to reason it out**

1. Name what is missing: live order data and the ability to perform a refund.
2. Recall that a model alone has neither: its knowledge is frozen and it cannot act.
3. Pick the option that connects the agent to outside systems rather than changing the model.

> **Exam tip:** Tools give an agent what the model lacks: live data from outside systems and the ability to act.

</details>

📖 Learn this topic: [Gen AI Agent Tooling: Extensions, Functions, Data Stores, and Plugins](https://www.savemycert.com/revision/gcp-generative-ai-leader/gen-ai-agent-tooling-extensions-functions/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)

---

## Question 14

*Techniques to improve gen AI model output*

**A sales assistant built on a foundation model tells a prospect, without any hedging, that the company's flagship product launched in 2019. The launch was in 2021 and has been publicly documented for years. Which foundation model limitation does this illustrate?** Choose one.

- **a.** Bias, where outputs systematically favor certain groups or viewpoints
- **b.** Hallucination, where plausible-sounding output is factually incorrect
- **c.** Knowledge cutoff, where events after training data collection are unknown
- **d.** Edge case, where rare inputs fall outside the patterns seen in training

<details>
<summary>Show answer and explanation</summary>

**Answer: b**

- **a** ❌ Bias is a systematic skew for or against groups or viewpoints; a single wrong date about a product shows no such pattern.
- **b** ✅ Correct. The model produced a specific, confident-sounding date that contradicts the record, which is the defining pattern of a hallucination.
- **c** ❌ The launch happened years ago and is well documented, so it predates any realistic cutoff; a cutoff shows up as missing or stale knowledge of recent events, not an invented date for an old one.
- **d** ❌ A question about a well-documented product launch is an ordinary request, not a rare input outside the training distribution.

**The concept.** Hallucination is output that sounds plausible and confident but is factually wrong. It happens because a foundation model predicts likely text rather than looking facts up.

**Why this is correct.** The assistant asserted a precise but false date about an old, well-documented event. That rules out the knowledge cutoff (the event is not recent), bias (no systematic skew toward a group) and an edge case (the request is routine). What remains is a hallucination, which Google Cloud addresses mainly with grounding and RAG, plus human review where errors matter.

**How to reason it out**

1. Note what went wrong: a specific claim that contradicts a well-documented fact.
2. Check whether the event is recent (cutoff), a pattern against a group (bias) or a rare input (edge case); none applies.
3. Name the remaining limitation: a hallucination.
4. Link it to the remedy: grounding the model in verifiable sources.

> **Exam tip:** Wrong but plausible-sounding facts about things the model could have known are hallucinations; grounding is the main fix.

</details>

📖 Learn this topic: [Overcoming Foundation Model Limitations: Grounding, RAG, and HITL](https://www.savemycert.com/revision/gcp-generative-ai-leader/overcome-foundation-model-limitations-grounding-rag/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)

---

## Question 15

*Techniques to improve gen AI model output*

**A compliance officer asks an ungrounded foundation model about a data-privacy regulation that took effect last month. The model says it has no record of that regulation, yet it answers accurately about rules from earlier years. Which limitation explains this?** Choose one.

- **a.** An edge case, because privacy rules are rare in the training data
- **b.** A hallucination, because the model is inventing that the rule is absent
- **c.** Bias in the training data toward older, more widely discussed regulations
- **d.** The knowledge cutoff, because the rule postdates the training data

<details>
<summary>Show answer and explanation</summary>

**Answer: d**

- **a** ❌ The model handles earlier privacy rules accurately, so privacy questions are not rare inputs for it; only the new rule is missing.
- **b** ❌ A hallucination is fabricated content. Saying it has no information is an honest reflection of what the model was trained on, not an invention.
- **c** ❌ Bias is a systematic skew for or against groups or viewpoints. Older rules being better covered is a matter of timing, and the new rule is not covered at all.
- **d** ✅ Correct. The regulation took effect after the model's training data was collected, so the model cannot know about it unless it is connected to fresher sources.

**The concept.** The knowledge cutoff is the point in time when a foundation model's training data ends. Events after that date are unknown to the model unless it is grounded in fresher information.

**Why this is correct.** The model is accurate on older rules and blank only on a rule from last month, which points to timing rather than bias, rarity or fabrication. The fix is to ground the model in current sources, for example through retrieval-augmented generation (RAG) over the regulation text, rather than to wait for a newer model.

**How to reason it out**

1. Notice the split: older material answered well, recent material unknown.
2. Ask what changes with time: only the knowledge cutoff does.
3. Rule out hallucination (nothing was invented) and edge cases (the topic itself is familiar).
4. Recall the remedy: grounding or RAG over current sources.

> **Exam tip:** Accurate on the past and blank on recent events means a knowledge cutoff; ground the model in current data to close it.

</details>

📖 Learn this topic: [Overcoming Foundation Model Limitations: Grounding, RAG, and HITL](https://www.savemycert.com/revision/gcp-generative-ai-leader/overcome-foundation-model-limitations-grounding-rag/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)

---

## Question 16

*Techniques to improve gen AI model output*

**A manager who is new to generative AI asks what "prompt engineering" refers to when people talk about working with large language models (LLMs). Which description is accurate?** Choose one.

- **a.** Connecting a model to company databases so it can look up facts before it writes its response
- **b.** Adjusting a model's weights by training it further on labeled examples taken from your own business data
- **c.** Comparing several foundation models on cost and quality to pick the best fit for a project
- **d.** Designing and refining the instructions, context and examples a model receives so its output improves

<details>
<summary>Show answer and explanation</summary>

**Answer: d**

- **a** ❌ That describes grounding or retrieval-augmented generation, which supplies the model with external data. It is a separate technique from crafting the prompt.
- **b** ❌ That describes fine-tuning, which changes the model itself. Prompt engineering leaves the model untouched and changes what it is given.
- **c** ❌ Choosing a model is a separate, earlier decision. Prompt engineering is how you get the best output from whichever model you chose.
- **d** ✅ Correct. Prompt engineering is the deliberate crafting of the input (instruction, context, examples, format cues) to steer the model toward better output.

**The concept.** Prompt engineering is the practice of deliberately designing a model's input (instructions, background context, examples and format requirements) to steer a large language model toward the output you want, without changing the model.

**Why this is correct.** The defining feature is that only the input changes. Fine-tuning changes the model's weights, grounding connects the model to outside data sources, and model selection changes which model you use. Each of those is a real lever for better results, which is why they are tempting, but none of them is prompt engineering.

**How to reason it out**

1. Identify what each option changes: the weights, the data the model can reach, the model choice, or the input text.
2. Recall that prompt engineering works on the input text alone.
3. Pick the option describing instructions, context and examples written into the prompt.

> **Exam tip:** Prompt engineering changes what you ask the model, not the model itself or the data it can reach.

</details>

📖 Learn this topic: [Prompt Engineering Techniques: Few-Shot, Role, and Chain-of-Thought](https://www.savemycert.com/revision/gcp-generative-ai-leader/prompt-engineering-techniques-few-shot-chain-of-thought/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)

---

## Question 17

*Techniques to improve gen AI model output*

**A leader asks what it means to "ground" a large language model's responses. Which description is accurate?** Choose one.

- **a.** Applying content filters that block harmful categories from the response
- **b.** Supplying verifiable source data at request time for the model to answer from
- **c.** Retraining the model on company data so the facts are stored in its own weights
- **d.** Capping the number of tokens the model may generate in each response

<details>
<summary>Show answer and explanation</summary>

**Answer: b**

- **a** ❌ That is what safety settings do. Filtering harmful content does not make answers factually anchored to a source.
- **b** ✅ Correct. Grounding gives the model trusted reference material (enterprise documents, licensed data or web results) when it answers, so the response is anchored in that data rather than only in what it learned during training.
- **c** ❌ That describes training or fine-tuning, which changes the model's weights. Grounding leaves the model unchanged and supplies source data when it answers.
- **d** ❌ That is the output length (maximum output tokens) setting. It limits response size; it does not connect answers to a source of truth.

**The concept.** Grounding connects a model's output to verifiable sources of information supplied when it answers, rather than relying only on knowledge absorbed during training.

**Why this is correct.** Grounding changes what the model reads when it answers, not the model itself. Retraining is the tempting alternative, but it bakes knowledge into weights, goes stale and cannot point to a source. Output caps and content filters are sampling and safety controls: they shape how the model responds, not what facts it relies on.

**How to reason it out**

1. Ask whether the option changes the model's weights or what it reads at answer time.
2. Rule out generation controls (output length) and content controls (safety filters).
3. Pick the option that anchors the answer in a verifiable source supplied with the request.

> **Exam tip:** Grounding = give the model trusted source data when it answers; the model itself is not retrained.

</details>

📖 Learn this topic: [Grounding Techniques: RAG, Google Search, and Sampling Settings](https://www.savemycert.com/revision/gcp-generative-ai-leader/grounding-techniques-rag-google-search/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)

---

## Question 18

*Business strategies for a successful gen AI solution*

**A retailer wants thousands of catalog items to each get an original written description that matches its brand voice, without staff drafting them one by one. Which type of gen AI solution fits this need?** Choose one.

- **a.** Personalized user experiences
- **b.** Code generation
- **c.** Text generation
- **d.** Image generation

<details>
<summary>Show answer and explanation</summary>

**Answer: c**

- **a** ❌ Personalization tailors content to an individual visitor. Here every item needs one description for all shoppers, so the need is authoring text, not tailoring it per person.
- **b** ❌ Code generation helps developers write and explain software. It does not author customer-facing catalog copy.
- **c** ✅ Correct. The required output is written language, and drafting copy at scale is the core use of text generation.
- **d** ❌ Image generation produces visuals such as product shots or banners. The retailer needs written descriptions, not pictures.

**The concept.** The first step in choosing a gen AI solution is matching the output the business needs to a solution type: text, image, code, or personalized user experiences.

**Why this is correct.** The deciding detail is the output: written descriptions, produced at volume, in a consistent voice. That is text generation. Image generation would create the product visuals, code generation serves developers, and personalization would matter only if each shopper had to see different copy; here each item needs one description for everyone.

**How to reason it out**

1. Identify the output the business needs: written product descriptions.
2. Map written natural-language output to text generation.
3. Check whether the copy must differ per shopper; it does not, so personalization is not the core need.
4. Rule out the types whose output is visuals or software.

> **Exam tip:** Name the output first: words map to text generation, visuals to image generation, software to code generation.

</details>

📖 Learn this topic: [Implementing a Transformational Gen AI Solution: The Google Cloud Steps](https://www.savemycert.com/revision/gcp-generative-ai-leader/implement-gen-ai-solution-google-cloud-steps/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)

---

## Question 19

*Business strategies for a successful gen AI solution*

**A marketing team needs fresh campaign visuals and concept artwork for each product launch, and wants first drafts in minutes instead of waiting weeks for an agency. Which type of gen AI solution fits this need?** Choose one.

- **a.** Personalized user experiences
- **b.** Image generation
- **c.** Text generation
- **d.** Code generation

<details>
<summary>Show answer and explanation</summary>

**Answer: b**

- **a** ❌ Personalization tailors content to each individual. The team needs a set of campaign visuals, not a different experience per viewer.
- **b** ✅ Correct. Creating original visuals and concept art from a description is exactly what image generation solutions do.
- **c** ❌ Text generation could draft the slogans and copy for the campaign, but the stated need is the visuals themselves.
- **d** ❌ Code generation produces and explains software. It would not create the campaign artwork the team is asking for.

**The concept.** Image generation creates or edits visual content from a natural-language description, which suits creative teams producing concepts, mockups and design variations.

**Why this is correct.** The need is visual: campaign imagery and concept artwork, produced quickly. Image generation creates visuals from a text description, so the team can iterate on concepts in minutes. Text generation is the tempting near-miss because campaigns also need copy, but the stem asks for the visuals. Code generation serves developers, and personalization tailors content per person rather than producing it.

**How to reason it out**

1. Identify the output: campaign visuals and concept artwork.
2. Map visual output to image generation.
3. Notice that campaign copy would be text generation, but the stated need is the imagery.
4. Rule out code generation and personalization, which serve other needs.

> **Exam tip:** Visual output from a description is image generation, even when the project also needs copy.

</details>

📖 Learn this topic: [Implementing a Transformational Gen AI Solution: The Google Cloud Steps](https://www.savemycert.com/revision/gcp-generative-ai-leader/implement-gen-ai-solution-google-cloud-steps/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)

---

## Question 20

*Business strategies for a successful gen AI solution*

**A board member asks what the company's new "secure AI" program will actually cover. Which description defines secure AI?** Choose one.

- **a.** Protecting the AI system's data, models and interactions from attack and misuse
- **b.** Making sure AI outputs are fair, explainable and free of harmful bias toward users
- **c.** Hardening the network perimeter around the servers that host AI applications
- **d.** Using AI models to automate threat detection in the security operations center

<details>
<summary>Show answer and explanation</summary>

**Answer: a**

- **a** ✅ Correct. Secure AI covers every component of the AI system, training data, the model, the infrastructure and its inputs and outputs, at every lifecycle stage.
- **b** ❌ Fairness and explainability are responsible AI goals. They matter, but they do not protect the system from attackers or misuse.
- **c** ❌ Perimeter security is part of the picture but far too narrow: it misses poisoned training data, prompt injection through legitimate inputs and model theft through queries.
- **d** ❌ That is AI for security: applying AI as a defensive tool. Secure AI is the reverse, protecting the AI system itself.

**The concept.** Secure AI means protecting an AI system, its training data, models, infrastructure, and the inputs and outputs it handles, from malicious attacks and misuse across the whole ML lifecycle.

**Why this is correct.** Secure AI is about defending the AI system itself. The tempting alternatives are adjacent ideas: using AI to defend other systems (AI for security), making outputs fair and explainable (responsible AI), and classic perimeter hardening, which leaves AI-specific attack routes such as poisoned data or crafted prompts uncovered.

**How to reason it out**

1. Ask what is being protected: the AI system, or something else using AI.
2. Separate security (attacks and misuse) from responsible AI (fairness, transparency).
3. Check scope: secure AI covers data, model and interactions, not only the network.

> **Exam tip:** Secure AI = protecting the AI system itself (data, model, interactions) from attack and misuse across its lifecycle.

</details>

📖 Learn this topic: [Secure AI and SAIF: Protecting AI Systems on Google Cloud](https://www.savemycert.com/revision/gcp-generative-ai-leader/secure-ai-saif-framework-google-cloud/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)

---

[← Back to the GenAI Leader study guide](README.md)
