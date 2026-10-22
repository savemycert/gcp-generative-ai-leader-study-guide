# Domain 3: Techniques to improve gen AI model output (20%)

This domain covers why foundation models go wrong and what fixes each failure, the named prompting techniques, and grounding sources, offerings, and sampling settings. Questions describe a symptom or a desired behavior and ask for the technique, offering, or parameter that addresses it.

## 3.1 Describe how to proactively overcome foundation model limitations

- **Root cause = data dependency:** a model only knows what its training data held, up to a point in time. Bigger models do not remove this. The leader's question is where the model's knowledge must be supplemented for this use case.
- **Limitations to recognize:**
  - Knowledge cutoff: no awareness of anything after training data was collected (new prices, rules, events).
  - Hallucination: fluent, confident, false output, because models predict likely tokens rather than look up facts. A fake citation looks as polished as a real one.
  - Edge cases: rare jargon, uncommon languages, odd formats. Test on your hardest realistic inputs, not just typical ones.
  - Bias and fairness: skew absorbed from human-generated training data. It is an ethical and a legal/reputational risk, so plan responsible AI review from the start.
- **The remedies:**
  - Grounding: tie output to authoritative sources. Options include Google Search grounding (current web) and Agent Search over your own content.
  - RAG: retrieve relevant passages, add them to the prompt, then generate. Answers stay current when the documents change and can cite sources.
  - Prompt engineering: instructions, role, format, examples. Cheapest, always first.
  - Fine-tuning: continue training on curated examples to learn vocabulary, style, or task patterns. Needs quality data and engineering effort.
  - Human in the loop (HITL): people review or approve before output takes effect. Required for medical, financial, legal, and fairness-sensitive decisions; corrections become evaluation and tuning data.

| Symptom                                  | Primary fix                                             |
| ---------------------------------------- | ------------------------------------------------------- |
| Model doesn't know our business          | Grounding / RAG on enterprise data                      |
| Stale facts, recent events               | Google Search grounding; RAG over current documents     |
| Invented answers                         | Grounding / RAG, plus HITL where stakes are high        |
| Skewed outcomes across groups            | HITL, curated data, safety settings, ongoing evaluation |
| Poor results on rare, specialized inputs | Fine-tuning on domain examples; few-shot prompting      |
| Wrong tone, structure, or role           | Prompt engineering; fine-tune only if it persists       |

- **Sequence:** prompt first, ground next, fine-tune last. HITL is a standing control, not a fallback.
- **Classic trap:** a chatbot invents details of a current promotion. The fix is grounding. Fine-tuning adds no current knowledge (it fixes knowledge at training time) and does not stop invention.
- **After launch (continuous monitoring and evaluation):**
  - KPIs: accuracy, quality, satisfaction, resolution rate, cost per interaction. Performance tracking watches them continuously.
  - Drift monitoring: flags when production inputs gradually diverge from the conditions the model was designed and evaluated for; triggers refreshed grounding, prompts, or tuning.
  - Versioning: track model, prompt, and dataset versions so changes can be tested and rolled back.
  - Automatic model upgrades: managed models improve without rebuilds, but validate each upgrade against your KPIs.
  - Security patches: Google applies them to the managed platform.
  - Agent Platform Feature Store: one governed source of feature data so models and agents get consistent inputs across environments.

📖 Full lesson: [Overcoming Foundation Model Limitations: Grounding, RAG, and HITL](https://www.savemycert.com/revision/gcp-generative-ai-leader/overcome-foundation-model-limitations-grounding-rag/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)

## 3.2 Describe prompt engineering techniques and how they drive better results

- **Definition:** deliberately designing what the model sees before it answers (instruction, context, examples, format and tone cues). Same model, different prompt, very different output.
- **Why it matters:** highest leverage (no retraining or infrastructure), accessible to non-engineers in plain language, and good prompts become reusable team assets. Before deciding a model "can't do it", check whether it was asked well.
- **Effective prompt checklist:** instruction, context, format, examples. Weak output usually means one is missing and the model had to guess audience, length, or purpose. Prompting is iterative: review, add a constraint or example, retry.
- **Sampling settings** (temperature, top-p) tune creativity, but the prompt is still the main steering control.

| Technique        | What it is                                                             | Use when                                                 | Example cue                                                        |
| ---------------- | ---------------------------------------------------------------------- | -------------------------------------------------------- | ------------------------------------------------------------------ |
| Zero-shot        | Instruction only                                                       | Familiar tasks (summarize, translate)                    | "Summarize this transcript in five bullets"                        |
| One-shot         | One input/output example first                                         | A format easier to show than describe                    | "Here is a review and our one-line summary; do the next one"       |
| Few-shot         | Several examples (commonly two to five)                                | Nuanced classification, extraction, strict house style   | Three tickets labeled Billing / Technical / Account, then a fourth |
| Role prompting   | Give the model a persona                                               | Audience, tone, or viewpoint matters                     | "You are a financial analyst briefing non-financial executives"    |
| Prompt chaining  | Output of one prompt feeds the next                                    | Multi-stage work; inspect results between steps          | Summarize each interview, then themes, then recommendations        |
| Chain-of-thought | Ask for step-by-step reasoning before the answer                       | Calculations, multi-condition decisions, auditable logic | "Work through each year's cost, then compare"                      |
| ReAct            | Alternate reasoning with actions (search, tool calls) and observations | The task needs live or external information mid-task     | "Check current stock, then tell the customer when it ships"        |

- **Shot rule:** start zero-shot; add examples only when output misses your format. Examples cost tokens, so use the fewest that give consistency.
- **Role limit:** a persona changes **how** the model talks, not **what it knows**. Calling it a lawyer won't make its legal statements correct. Wrong facts need grounding.
- **Chaining benefit:** quality checks move into the middle of the process. It is also the basic shape of agent workflows on Agent Platform.
- **Chain-of-thought:** improves multi-step accuracy and exposes the reasoning for review. Skip it for simple factual or creative requests (extra tokens and latency, no gain).
- **ReAct vs chain-of-thought:** pure multi-step thinking = chain-of-thought. Thinking interleaved with information-gathering actions (thought, action, observation) = ReAct, the pattern underneath AI agents.
- **Techniques stack:** a production prompt may combine a role, few-shot examples, and a chain, with ReAct fetching order details.

📖 Full lesson: [Prompt Engineering Techniques: Few-Shot, Role, and Chain-of-Thought](https://www.savemycert.com/revision/gcp-generative-ai-leader/prompt-engineering-techniques-few-shot-chain-of-thought/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)

## 3.3 Identify grounding techniques and their use cases

- **Grounding:** supply reference material at answer time so the model reads, then responds, instead of recalling. The model turns into a language and reasoning engine on top of facts you own. Payoff: accuracy, freshness, traceability.

| Source                      | What it is                                 | Example                                           | Answers questions like               |
| --------------------------- | ------------------------------------------ | ------------------------------------------------- | ------------------------------------ |
| First-party enterprise data | Created and owned by your organization     | Policies, manuals, CRM records, tickets           | "What is our refund policy?"         |
| Third-party data            | Acquired from providers or partners        | Licensed research, market feeds, partner catalogs | "What are industry benchmark rates?" |
| World data                  | Public knowledge that changes all the time | Google Search results, news, public websites      | "What happened last week?"           |

- **How RAG changes output:** retrieval runs on every query, so answers are more specific, current, and attributable (citations), and hallucinations drop because the model is told to answer from the supplied context and can say it does not know.
- **RAG vs fine-tuning:** RAG for knowledge that changes, needs citations, or is large and access-controlled. Fine-tuning for stable knowledge, style, and behavior.
- **Google Cloud grounding offerings:**
  - Pre-built RAG with Agent Search: point it at your content; it ingests, indexes, retrieves, and cites. Fastest route; cue "enterprise documents, minimal build effort".
  - RAG APIs: components for document processing, embeddings, ranking, and grounded generation. Cue "custom pipeline control"; costs more engineering.
  - Grounding with Google Search: fresh public web results with source links. Cue "current, public, time-sensitive".
- **Combine them:** a regulated bank can ground fee and policy answers in first-party data via Agent Search, add licensed third-party rate data, and turn on Google Search grounding for public regulatory news.

| Setting                  | Controls                                                                     | Guidance                                                                                          |
| ------------------------ | ---------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| Token count              | Text processed and produced (tokens are small chunks of text)                | The unit of cost and capacity; longer prompts and retrieved context cost more                     |
| Temperature              | Randomness of each token choice                                              | Low = focused, repeatable (facts, grounded Q&A, summaries). High = varied (brainstorming, copy)   |
| Top-p (nucleus sampling) | Samples only from the smallest set of tokens whose probabilities add up to p | Low = few candidates, predictable. High = wider pool                                              |
| Safety settings          | Blocking thresholds per harm category                                        | Tune per audience: strict for a consumer brand bot, looser for an internal moderation review tool |
| Output length            | Max tokens per response                                                      | Caps size and cost; a chat widget needing short replies should not allow long ones                |

- **Division of labor:** grounding decides **what** the model knows; sampling settings decide **how** it writes. A typical grounded assistant pairs retrieval with low temperature, suitable safety settings, and an output length that fits the surface.
- **Vocabulary cues:** "verifiable sources" or "hallucination" = grounding; "last week's announcement" = Google Search grounding; "proprietary documents" = first-party data plus RAG; "less creative, more consistent" = lower temperature or top-p; "response size or cost" = token count and output length; "block harmful content" = safety settings.
- **None of these retrain the model**, which is their business appeal: the model stays fixed while the knowledge behind it is refreshed as often as needed.

📖 Full lesson: [Grounding Techniques: RAG, Google Search, and Sampling Settings](https://www.savemycert.com/revision/gcp-generative-ai-leader/grounding-techniques-rag-google-search/?utm_source=github&utm_medium=readme&utm_campaign=gcp-generative-ai-leader-study-guide)

[← Back to the study guide](../README.md)
