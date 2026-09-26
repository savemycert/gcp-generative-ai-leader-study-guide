# GenAI Leader Study Guide: Google Cloud Generative AI Leader

A free, open study guide for the **Google Cloud Generative AI Leader (GenAI Leader)** exam: revision notes for every domain, side-by-side comparisons of commonly confused services, a glossary, 20 worked sample questions, and the official syllabus as a checklist with a full free lesson for every topic.

Maintained by [SaveMyCert](https://www.savemycert.com/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide), where you can read every lesson free, [practice with explained questions](https://www.savemycert.com/practice/gcp-generative-ai-leader/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide) and [take timed mock exams](https://www.savemycert.com/mocks/gcp-generative-ai-leader/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide).

## Contents

- [Exam at a glance](#exam-at-a-glance)
- [Exam domains](#exam-domains)
- [What is in this repo](#what-is-in-this-repo)
- [Syllabus checklist](#syllabus-checklist)
  - [Domain 1: Fundamentals of gen AI](#domain-1-fundamentals-of-gen-ai)
  - [Domain 2: Google Cloud's gen AI offerings](#domain-2-google-clouds-gen-ai-offerings)
  - [Domain 3: Techniques to improve gen AI model output](#domain-3-techniques-to-improve-gen-ai-model-output)
  - [Domain 4: Business strategies for a successful gen AI solution](#domain-4-business-strategies-for-a-successful-gen-ai-solution)
- [How to study for GenAI Leader](#how-to-study-for-genai-leader)
- [Sample questions](sample-questions.md)
- [Free resources](#free-resources)

## Exam at a glance

| | |
|---|---|
| Exam code | GenAI Leader |
| Level | Foundational |
| Questions | 50–60 |
| Time limit | 90 min |
| Passing score | Pass / fail |
| Format | Multiple choice |
| Exam fee | $99 |
| Valid for | 3 years |

Exam details change. Always confirm them in the official [Google Cloud Generative AI Leader exam guide](https://cloud.google.com/learn/certification/generative-ai-leader) from Google Cloud.

## Exam domains

| # | Domain | Weight | Topics |
|---|---|---|---|
| 1 | [Fundamentals of gen AI](#domain-1-fundamentals-of-gen-ai) | 30% | 4 |
| 2 | [Google Cloud's gen AI offerings](#domain-2-google-clouds-gen-ai-offerings) | 35% | 5 |
| 3 | [Techniques to improve gen AI model output](#domain-3-techniques-to-improve-gen-ai-model-output) | 20% | 3 |
| 4 | [Business strategies for a successful gen AI solution](#domain-4-business-strategies-for-a-successful-gen-ai-solution) | 15% | 3 |

That is 4 domains and 15 topics. Spend your time in proportion to the weights: the heaviest domain decides more of your score than the lightest.

Google publishes these weights as approximate figures (for example "~20%").

## What is in this repo

| File | What it gives you |
|---|---|
| [Domain 1 notes](notes/domain-1-fundamentals-of-gen-ai.md) | Fundamentals of gen AI: condensed revision notes per topic |
| [Domain 2 notes](notes/domain-2-google-clouds-gen-ai-offerings.md) | Google Cloud's gen AI offerings: condensed revision notes per topic |
| [Domain 3 notes](notes/domain-3-techniques-to-improve-gen-ai-model-output.md) | Techniques to improve gen AI model output: condensed revision notes per topic |
| [Domain 4 notes](notes/domain-4-business-strategies-for-a-successful-gen-ai-solution.md) | Business strategies for a successful gen AI solution: condensed revision notes per topic |
| [Commonly confused services](comparisons.md) | Side-by-side tables of the services questions set against each other |
| [Glossary](glossary.md) | Every in-scope term and service in one sentence |
| [Sample questions](sample-questions.md) | 20 worked questions with answers and reasoning |
| [Exam-day guide](exam-day-guide.md) | Booking, testing options, scoring, results and retakes |

## Syllabus checklist

Tick each topic off once you can explain it without notes. The "Must know" facts are the ones questions turn on. Each lesson link goes to the complete, free lesson.

### Domain 1: Fundamentals of gen AI

**Weight: 30%.** Core generative AI concepts and use cases, data types, the gen AI landscape layers, and Google’s foundation models. Official (approximate) weighting ~30%.

📝 Revision notes: [Domain 1: Fundamentals of gen AI](notes/domain-1-fundamentals-of-gen-ai.md)

- [ ] **Describe core generative AI concepts and use cases**
  <br>Defining core concepts (AI, NLP, machine learning, generative AI, foundation and multimodal foundation models, diffusion models, prompt tuning, prompt engineering, large language models); describing ML approaches (supervised, unsupervised, reinforcement); the ML lifecycle stages (data ingestion, preparation, training, deployment, management) and Google Cloud tools for each; choosing a foundation model for a use case (modality, context window, security, availability, cost, performance, fine-tuning); business use cases where gen AI can create, summarize, discover, and automate.
  - 📖 Lesson: [Generative AI Concepts: Foundation Models, LLMs, and Business Use Cases](https://www.savemycert.com/revision/gcp-generative-ai-leader/generative-ai-concepts-foundation-models-llms/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)
  - Must know: Generative AI is a branch of machine learning that creates new content; traditional ML classifies or predicts.
  - Must know: A foundation model is pretrained on broad data and adapted to many tasks; an LLM is a foundation model specialized in language.
- [ ] **Describe how various data types are used in gen AI and the business implications**
  <br>Explaining the characteristics and importance of data quality and data accessibility (completeness, consistency, relevance, availability, cost, format); differences between structured and unstructured data with real-world examples; differences between labeled and unlabeled data.
  - 📖 Lesson: [Data Types in Gen AI: Quality, Structured vs Unstructured, Labeled Data](https://www.savemycert.com/revision/gcp-generative-ai-leader/gen-ai-data-types-quality-structured-unstructured/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)
  - Must know: Gen AI output quality is bounded by data quality: incomplete, inconsistent, or irrelevant data produces confident but wrong answers.
  - Must know: Data quality and accessibility have six exam characteristics: completeness, consistency, relevance, availability, cost, and format.
- [ ] **Identify the core layers of the gen AI landscape and the business implications**
  <br>The core layers of the gen AI landscape and their business implications: infrastructure, models, platforms, agents, and applications.
  - 📖 Lesson: [The Five Layers of the Gen AI Landscape and What They Mean for Business](https://www.savemycert.com/revision/gcp-generative-ai-leader/gen-ai-landscape-layers-infrastructure-models-agents/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)
  - Must know: The gen AI landscape has five layers: infrastructure, models, platforms, agents, and applications, and each builds on the layer below.
  - Must know: Infrastructure (TPUs, GPUs, AI Hypercomputer, Google Cloud data centers) should be consumed from a cloud provider, not built.
- [ ] **Identify the use cases and strengths of Google's foundation models**
  <br>Use cases and strengths of Google's foundation models: Gemini, Gemma, Imagen, and Veo.
  - 📖 Lesson: [Google's Foundation Models: Gemini, Gemma, Imagen, and Veo Explained](https://www.savemycert.com/revision/gcp-generative-ai-leader/google-foundation-models-gemini-gemma-imagen-veo/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)
  - Must know: Google's four named foundation models are Gemini (multimodal reasoning), Gemma (lightweight open models), Imagen (image generation), and Veo (video generation).
  - Must know: Gemini is natively multimodal with a long context window, making it the choice for reasoning, conversation, document analysis, code, and mixed-input tasks.

### Domain 2: Google Cloud's gen AI offerings

**Weight: 35%.** Google Cloud's strengths in gen AI, its prebuilt offerings, customer-experience tools, developer platforms, and agent tooling. Official (approximate) weighting ~35%.

📝 Revision notes: [Domain 2: Google Cloud's gen AI offerings](notes/domain-2-google-clouds-gen-ai-offerings.md)

- [ ] **Describe Google Cloud's strengths in the field of gen AI**
  <br>Google's AI-first approach and innovation; the enterprise-ready AI platform (responsible, secure, private, reliable, scalable); the comprehensive AI ecosystem; the benefits of Google Cloud's open approach; AI-optimized infrastructure (hypercomputer, custom TPUs, GPUs, data centers); data control (security, privacy, governance, first-party models, customizable solutions, agents); democratizing AI development (low-code/no-code tools, pre-trained models, APIs).
  - 📖 Lesson: [Google Cloud's Gen AI Strengths: Platform, Infrastructure, and Openness](https://www.savemycert.com/revision/gcp-generative-ai-leader/google-cloud-gen-ai-strengths-platform/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)
  - Must know: Google's AI-first approach and research heritage — including the Transformer architecture — create a short path from breakthrough to product, so customers get state-of-the-art capability and a strong roadmap.
  - Must know: Enterprise-ready means five qualities: responsible, secure, private, reliable, and scalable — match the quality to the concern the exam scenario stresses.
- [ ] **Describe how Google Cloud's prebuilt gen AI offerings enable AI powered work**
  <br>Functionality, use cases, and business value of the Gemini app and Gemini Advanced (Gems); Gemini Enterprise (Gemini Notebook API, multimodal search, custom agent capabilities); and Gemini for Google Workspace.
  - 📖 Lesson: [Prebuilt Gen AI at Work: Gemini App, Gemini Enterprise, and Workspace](https://www.savemycert.com/revision/gcp-generative-ai-leader/gemini-app-enterprise-workspace-prebuilt-ai/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)
  - Must know: Prebuilt offerings are finished products — fastest time to value, no ML skills required — and the entry point of Google Cloud's gen AI spectrum.
  - Must know: The Gemini app is a standalone multimodal assistant for individuals; Gemini Advanced adds the most capable models and Gems.
- [ ] **Describe how Google Cloud's gen AI offerings improve the customer experience**
  <br>Google Cloud's external search offerings (Agent Search on Gemini Enterprise Agent Platform, Google Search); and the Customer Engagement Suite (Conversational Agents, Agent Assist, Conversational Insights, Contact Center as a Service).
  - 📖 Lesson: [Improving Customer Experience with Agent Search and Customer Engagement Suite](https://www.savemycert.com/revision/gcp-generative-ai-leader/google-cloud-customer-engagement-agent-search/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)
  - Must know: Google Cloud improves customer experience through two families: external search offerings (Agent Search, grounding with Google Search) and the Customer Engagement Suite.
  - Must know: Agent Search, on the Gemini Enterprise Agent Platform, embeds Google-quality generative search — with prebuilt RAG and grounded, cited answers — into a company's own sites and apps.
- [ ] **Describe how Google Cloud empowers developers to build with AI**
  <br>Agent Platform (Model Garden, Agent Search, Agent Platform AutoML); Google Cloud's RAG offerings (prebuilt RAG with Agent Search, RAG APIs); and using Agent Platform to build custom agents.
  - 📖 Lesson: [How Google Cloud Empowers Developers: Agent Platform and RAG](https://www.savemycert.com/revision/gcp-generative-ai-leader/google-cloud-agent-platform-rag-developers/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)
  - Must know: Agent Platform is Google Cloud's unified environment for discovering models, grounding them in company data, and building, deploying, and managing gen AI agents.
  - Must know: Model Garden is a curated library of Google, open, and partner foundation models — its value is informed model choice under one set of enterprise controls.
- [ ] **Define the purpose and types of tooling for gen AI agents**
  <br>How agents use tools (extensions, functions, data stores, plugins) to interact with the external environment; relevant Google Cloud services and pre-built AI APIs for agent tooling (Cloud Storage, databases, Cloud Functions, Cloud Run, Agent Platform, Speech-to-Text, Text-to-Speech, Translation, Document AI, Cloud Vision, Video Intelligence, Natural Language); when to use Agent Studio vs Google AI Studio.
  - 📖 Lesson: [Gen AI Agent Tooling: Extensions, Functions, Data Stores, and Plugins](https://www.savemycert.com/revision/gcp-generative-ai-leader/gen-ai-agent-tooling-extensions-functions/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)
  - Must know: Tools are the agent's connection to the external environment — without them a model can only generate text from frozen training data; with them an agent can retrieve live information and complete tasks.
  - Must know: Extensions are standardized bridges to external APIs, executed by the agent platform on the agent's behalf.

### Domain 3: Techniques to improve gen AI model output

**Weight: 20%.** Overcoming foundation-model limitations, prompt engineering, and grounding techniques. Official (approximate) weighting ~20%.

📝 Revision notes: [Domain 3: Techniques to improve gen AI model output](notes/domain-3-techniques-to-improve-gen-ai-model-output.md)

- [ ] **Describe how to proactively overcome foundation model limitations**
  <br>Common limitations of foundation models (data dependency, knowledge cutoff, bias, fairness, hallucinations, edge cases); recommended practices to address them (grounding, retrieval-augmented generation, prompt engineering, fine-tuning, human in the loop); continuous monitoring and evaluation (automatic upgrades, KPIs, security patches, versioning, performance tracking, drift monitoring, Agent Platform Feature Store).
  - 📖 Lesson: [Overcoming Foundation Model Limitations: Grounding, RAG, and HITL](https://www.savemycert.com/revision/gcp-generative-ai-leader/overcome-foundation-model-limitations-grounding-rag/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)
  - Must know: Foundation model limitations all stem from data dependency: the model only knows what its training data contained, up to its knowledge cutoff.
  - Must know: Grounding connects model output to verifiable sources; RAG implements it by retrieving relevant enterprise content and inserting it into the prompt before generation.
- [ ] **Describe prompt engineering techniques and how they drive better results**
  <br>Defining prompt engineering and its significance with LLMs; prompting techniques and use cases (zero-shot, one-shot, few-shot, role prompting, prompt chaining); advanced techniques and when to use them (chain-of-thought, ReAct).
  - 📖 Lesson: [Prompt Engineering Techniques: Few-Shot, Role, and Chain-of-Thought](https://www.savemycert.com/revision/gcp-generative-ai-leader/prompt-engineering-techniques-few-shot-chain-of-thought/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)
  - Must know: Prompt engineering is deliberately designing the model's input — instruction, context, format, examples — and is the fastest, cheapest way to improve gen AI output.
  - Must know: Zero-shot means no examples, one-shot means one, few-shot means several; add examples when output misses your format or standard, and use the fewest that work.
- [ ] **Identify grounding techniques and their use cases**
  <br>Grounding in LLMs and differentiating first-party enterprise data, third-party data, and world data; how retrieval-augmented generation (RAG) affects output; Google Cloud grounding offerings (pre-built RAG with Agent Search, RAG APIs, grounding with Google Search); sampling parameters (token count, temperature, top-p, safety settings, output length).
  - 📖 Lesson: [Grounding Techniques: RAG, Google Search, and Sampling Settings](https://www.savemycert.com/revision/gcp-generative-ai-leader/grounding-techniques-rag-google-search/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)
  - Must know: Grounding connects LLM responses to verifiable data sources, reducing hallucinations and keeping answers current without retraining the model.
  - Must know: First-party data is what your organization owns, third-party data is acquired from external providers, and world data is broad public knowledge such as Google Search results.

### Domain 4: Business strategies for a successful gen AI solution

**Weight: 15%.** Implementing a transformational gen AI solution, securing AI systems, and responsible AI in business. Official (approximate) weighting ~15%.

📝 Revision notes: [Domain 4: Business strategies for a successful gen AI solution](notes/domain-4-business-strategies-for-a-successful-gen-ai-solution.md)

- [ ] **Describe the Google Cloud-recommended steps to implement a transformational gen AI solution**
  <br>Types of gen AI solutions (text, image, code generation, personalized needs); key factors that influence gen AI needs (business requirements, technical constraints); choosing the right solution for a business need; steps to integrate gen AI into an organization; techniques to measure impact.
  - 📖 Lesson: [Implementing a Transformational Gen AI Solution: The Google Cloud Steps](https://www.savemycert.com/revision/gcp-generative-ai-leader/implement-gen-ai-solution-google-cloud-steps/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)
  - Must know: A transformational gen AI solution starts from a business need and works backward to the technology, never the reverse.
  - Must know: The main solution types are text generation, image generation, code generation, and personalized user experiences, and each maps to distinct business problems.
- [ ] **Define secure AI and its importance in protecting AI systems**
  <br>Security throughout the ML lifecycle; the purpose and benefits of Google's Secure AI Framework (SAIF); Google Cloud security tools (secure-by-design infrastructure, IAM, Security Command Center, workload monitoring).
  - 📖 Lesson: [Secure AI and SAIF: Protecting AI Systems on Google Cloud](https://www.savemycert.com/revision/gcp-generative-ai-leader/secure-ai-saif-framework-google-cloud/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)
  - Must know: Secure AI means protecting an AI system's data, models, infrastructure, and interactions from attacks and misuse across the entire ML lifecycle.
  - Must know: Know the core threats conceptually: data poisoning corrupts training data, prompt injection manipulates a deployed model through its inputs, model theft steals the model asset, and evasion and leakage round out the list.
- [ ] **Describe the importance of responsible AI in business**
  <br>The importance of responsible AI and transparency; privacy considerations (privacy risks, data anonymization and pseudonymization); implications of data quality, bias, and fairness; accountability and explainability in AI systems.
  - 📖 Lesson: [Responsible AI in Business: Transparency, Privacy, Bias, and Fairness](https://www.savemycert.com/revision/gcp-generative-ai-leader/responsible-ai-transparency-bias-fairness/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)
  - Must know: Responsible AI is a business requirement, not just an ethical ideal — it protects trust, brand reputation, and regulatory standing.
  - Must know: Google's AI Principles commit to socially beneficial AI that avoids unfair bias, is safe, accountable to people, and privacy-first — but the deploying business always retains accountability for its own use.

## How to study for GenAI Leader

1. **Read the lesson for each topic** in the checklist above, starting with the heaviest domain. Every lesson is free on the [GenAI Leader revision notes](https://www.savemycert.com/revision/gcp-generative-ai-leader/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide).
2. **Practice straight after reading.** Answer [GenAI Leader practice questions](https://www.savemycert.com/practice/gcp-generative-ai-leader/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide) on the topic you just read. Each option comes with an explanation of why it is right or wrong.
3. **Review what you got wrong**, re-read that lesson section, and tick the topic off only when you get its questions right.
4. **Take a full-length [GenAI Leader mock exam](https://www.savemycert.com/mocks/gcp-generative-ai-leader/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)** under the real time limit. Aim to pass mocks comfortably before you book.
5. **On the last day**, skim the [GenAI Leader cheat sheet](https://www.savemycert.com/cheat-sheet/gcp-generative-ai-leader/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide) instead of starting anything new.

## Sample questions

[sample-questions.md](sample-questions.md) has 20 worked GenAI Leader questions with the answer, why each option is right or wrong, and the reasoning steps.

## Free resources

- [Google Cloud Generative AI Leader exam guide](https://cloud.google.com/learn/certification/generative-ai-leader): the official source (Google Cloud)
- [GenAI Leader certification overview](https://www.savemycert.com/certifications/gcp-generative-ai-leader/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)
- [GenAI Leader revision notes](https://www.savemycert.com/revision/gcp-generative-ai-leader/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide): every lesson, free to read
- [GenAI Leader practice questions](https://www.savemycert.com/practice/gcp-generative-ai-leader/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide): with an explanation on every option
- [GenAI Leader mock exams](https://www.savemycert.com/mocks/gcp-generative-ai-leader/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide): full-length and timed
- [GenAI Leader cheat sheet](https://www.savemycert.com/cheat-sheet/gcp-generative-ai-leader/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide): the key facts on one page
- [All certification study guides](https://github.com/savemycert/certification-study-guides)

## Contributing

Spotted an error or an out-of-date fact? [Open an issue](../../issues) with the topic and a link to the official source. See [CONTRIBUTING.md](CONTRIBUTING.md).

## License and disclaimer

This guide is licensed under [CC BY 4.0](LICENSE). You can reuse and adapt it, including commercially, as long as you credit **SaveMyCert** with a link to https://www.savemycert.com/.

This is an independent study resource. It is not affiliated with or endorsed by Google Cloud. Google Cloud Generative AI Leader and GenAI Leader are trademarks of their respective owner. Exam domains and weights are taken from the official exam guide linked above.
