# Module 12 — Prompts and Generative Answers

> [!NOTE]
> **Status: 🔜 Planned.** This syllabus is published; the full lesson files are developed in Step 7 of the [course build plan](../COURSE-ROADMAP.md).

Prompts and generative answers are where you shape exactly *what* the model produces. This module teaches prompt engineering with the prompt builder, generative answers grounded in your documents, structured outputs, and response formatting on the standard harness — and shows how the Microsoft Copilot harness packages the same reusable behavior as **skills**.

## At a glance

| Item | Details |
|---|---|
| **Level** | Intermediate |
| **Estimated time** | 5 hours |
| **Prerequisites** | [Module 11 — Agent Tools and Capabilities](../11-Agent-Tools-and-Capabilities/README.md) |
| **Harness focus** | Standard harness prompts and generative answers; on the Microsoft Copilot harness, which has no separate prompts feature, skills are the equivalent. |
| **Lab** | Build a document-based question-answering agent |

## Why this module matters

**For beginners:** a prompt is just well-written instructions for a model — but small changes in wording, inputs, and output format can change results dramatically. Learning a repeatable way to design and test prompts gives you reliable summaries, extractions, and answers instead of lucky ones.

**For the enterprise:** document question-answering is one of the most requested agent scenarios, and also one of the riskiest. Professionals ground answers in approved sources, return structured outputs that downstream steps can trust, measure accuracy before release, keep humans in the loop for sensitive outputs, and document known limitations.

## Learning objectives

By the end of this module you will be able to:

1. **Explain** prompt engineering principles and **apply** them to business tasks such as summarizing, classifying, and extracting.
2. **Create** a reusable prompt in the prompt builder with clear instructions, input variables, and optional knowledge.
3. **Configure** prompt outputs — including JSON output — and **use** them in topics, tools, and responses.
4. **Configure** generative answers at agent level and in a topic-level generative answers node, choosing appropriate sources.
5. **Format** responses for the target channel while preserving system-defined citations.
6. **Measure** answer accuracy with a test set and **document** limitations and refusal cases.
7. **Compare** standard-harness prompts with Microsoft Copilot harness skills and **decide** which fits a scenario.
8. **Apply** responsible AI practices, including human oversight, content moderation settings, and transparency notes.

## Topics covered

- **Prompt engineering** — what a prompt is, the build–test–refine cycle, and the prompt builder experience for creating, testing, saving, and sharing reusable prompts. *Applies to: standard harness* (prompts can also be used as workflow nodes).
- **Generative answers** — answers generated from knowledge: the **Conversational boosting** system topic as fallback, and generative answers nodes that target specific sources inside a topic.
- **Prompt design** — structuring a prompt (role, task, context, constraints, output format), using the prompt assistant and prompt library, and choosing a model and settings per prompt.
- **Prompt instructions** — writing precise task instructions, and using prompt modification to give generative answers custom instructions.
- **Input variables** — adding inputs to a prompt and passing values from topics, tools, or conversation context at runtime.
- **Output handling** — text versus JSON output, document output (🧪 **Preview**), validating and using outputs downstream, and human review of AI output before it's acted on.
- **Grounded responses** — adding knowledge to prompts, choosing sources for generative answers nodes, and keeping answers tied to approved content.
- **Response formatting** — channel-appropriate formatting (Markdown support varies by channel), concise structures, and why instructions must not alter the system citation format.
- **Context** — what context a prompt or generative answer receives, how conversation history and variables are used, and how skills receive context on the Microsoft Copilot harness.
- **Accuracy** — building test sets, evaluating answers, batch testing prompts (🧪 **Preview**), and tracking accuracy as content changes.
- **Limitations** — region and model availability, Copilot Credit consumption, usage limits and throttling, unsupported source combinations, and cases the agent should refuse.
- **Responsible AI** — the Responsible AI FAQs for generative answers and prompts, per-prompt content moderation sensitivity, human oversight, and transparency with users.
- **Microsoft Copilot harness equivalent: skills** — packaging reusable, task-specific behavior as a skill (name, description, Markdown instructions), created from blank, generated with AI, or uploaded; sharing skills from the marketplace is 🧪 **Preview**.

## Planned hands-on lab

**Lab: Build a document-based question-answering agent**

After the lab you will have:

- A standard-harness agent that answers questions from a set of uploaded policy or product documents, with citations.
- A topic-level generative answers node scoped to one document set, alongside agent-level knowledge.
- A prompt tool with input variables that returns structured JSON (for example, a summary plus key fields) used in a topic response.
- A 20-question accuracy test with results, plus a documented list of limitations and refusal cases.
- A short responsible-AI checklist applied to the agent: moderation settings, human-review points, and user-facing transparency.

**What you need:**

- Your course environment and solution, with sample documents you're allowed to use.
- Prompt builder prerequisites from Learn: an environment in a supported region, Dataverse, and available Copilot Credits — check these before you start.
- A trial license is enough to build and test (the trial **can't publish**).
- 💳 Optional comparison: rebuilding the prompt as a **skill** on the Microsoft Copilot harness consumes Copilot Credits while building and testing.

## Planned assessment

`ASSESSMENT.md` will follow the course-wide 24-item pattern, and `ANSWERS.md` will provide correct answers, detailed explanations (including why incorrect options are wrong), expected practical outcomes, and rubrics.

| Item type | Count | Planned focus for this module |
|---|---|---|
| Multiple-choice questions | 10 | Prompt components, generative answers placement, outputs, skills vs prompts |
| True/false questions | 5 | Statements such as "the Microsoft Copilot harness has a separate prompts feature" |
| Short-answer questions | 5 | Rewrite a weak prompt; explain when JSON output is preferable |
| Practical implementation tasks | 2 | Build a prompt with inputs and JSON output; add a scoped generative answers node |
| Real-world scenario challenge | 1 | Design a contract-summary assistant with human review and refusal rules |
| Troubleshooting challenge | 1 | Answers are long, unformatted, and missing citations — find the prompt and instruction causes |
| **Total** | **24** | |

**Grading bands:** 0–59% Beginner · 60–74% Intermediate · 75–89% Advanced · 90–100% Professional Ready.

## Files in this module

| File | Purpose | Status |
|---|---|---|
| `README.md` | Syllabus: objectives, topics, lab outline, assessment plan (this file) | ✅ Syllabus |
| `CONCEPTS.md` | Full lessons for every topic using the course teaching sequence | 🔜 Planned |
| `STEP-BY-STEP-LAB.md` | Guided document Q&A lab with checkpoints | 🔜 Planned |
| `EXAMPLES.md` | Prompt patterns, JSON output examples, and skill equivalents | 🔜 Planned |
| `ASSESSMENT.md` | 24-item module assessment | 🔜 Planned |
| `ANSWERS.md` | Answers, explanations, and rubrics | 🔜 Planned |
| `INTERVIEW-QUESTIONS.md` | Interview questions with model answers | 🔜 Planned |
| `COMMON-MISTAKES.md` | Common mistakes, symptoms, and fixes | 🔜 Planned |

## Key official documentation

- [Prompts overview](https://learn.microsoft.com/en-us/microsoft-copilot-studio/prompts-overview)
- [Create a prompt](https://learn.microsoft.com/en-us/microsoft-copilot-studio/create-custom-prompt)
- [Add inputs to your prompt](https://learn.microsoft.com/en-us/microsoft-copilot-studio/add-inputs-prompt)
- [JSON output for prompts](https://learn.microsoft.com/en-us/microsoft-copilot-studio/process-responses-json-output)
- [Add a generative answers node](https://learn.microsoft.com/en-us/microsoft-copilot-studio/nlu-boost-node)
- [Use prompt modification to provide custom instructions](https://learn.microsoft.com/en-us/microsoft-copilot-studio/nlu-generative-answers-prompt-modification)
- [Skills overview for agents (Microsoft Copilot harness)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/skills-overview)
- [FAQ for generative answers](https://learn.microsoft.com/en-us/microsoft-copilot-studio/faqs-generative-answers)

## Navigation

⬅️ [Module 11 — Agent Tools and Capabilities](../11-Agent-Tools-and-Capabilities/README.md) | 🗺️ [Course roadmap](../COURSE-ROADMAP.md) | 📈 [Learning progress](../LEARNING-PROGRESS.md) | ➡️ [Module 13 — Authentication and Security](../13-Authentication-and-Security/README.md)

## References

- https://learn.microsoft.com/en-us/microsoft-copilot-studio/prompts-overview
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/create-custom-prompt
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/add-inputs-prompt
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/process-responses-json-output
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/nlu-boost-node
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/nlu-generative-answers-prompt-modification
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/skills-overview
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/faqs-generative-answers

_Last verified against Microsoft Learn: 18 November 2026._
