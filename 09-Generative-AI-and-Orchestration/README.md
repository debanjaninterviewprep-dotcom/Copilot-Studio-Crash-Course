# Module 09 — Generative AI and Orchestration

> [!NOTE]
> **Status: 🔜 Planned.** This syllabus is published; the full lesson files are developed in Step 6 of the [course build plan](../COURSE-ROADMAP.md).

Orchestration is how an agent decides *what to do next* — which topic, tool, knowledge source, or other agent to use, in what order, and how to answer. This module explains generative and classic orchestration on the standard harness, the reasoning runtime of the Microsoft Copilot harness, and how to keep generated answers grounded, safe, and debuggable.

## At a glance

| Item | Details |
|---|---|
| **Level** | Intermediate |
| **Estimated time** | 6 hours |
| **Prerequisites** | [Module 08 — Variables and Entities](../08-Variables-and-Entities/README.md) |
| **Harness focus** | Standard harness generative vs classic orchestration, plus the Microsoft Copilot harness's enhanced reasoning runtime, which every agent on that harness uses. |
| **Lab** | Create an agent that handles multiple user requests using available agent capabilities |

## Why this module matters

**For beginners:** with generative orchestration, you don't script every path — you describe your topics, tools, and knowledge well, and the agent plans how to combine them. Understanding *how* it plans is the difference between an agent that feels smart and one that feels random.

**For the enterprise:** orchestration choices drive accuracy, latency, cost, and risk. Architects must decide when predictable classic orchestration is required, when generative orchestration is appropriate, and when a workload justifies the Microsoft Copilot harness — and they must be able to prove, using activity maps and evaluations, why an agent did what it did.

## Learning objectives

By the end of this module you will be able to:

1. **Explain** core generative AI concepts — models, prompts, grounding, and generated responses — as they apply to Copilot Studio.
2. **Compare** generative and classic orchestration on the standard harness across topics, tools, knowledge, multi-intent requests, and response generation.
3. **Describe** how the Microsoft Copilot harness reasons through a goal, recovers from failures, and delegates work, and **contrast** it with the standard harness.
4. **Write** names and descriptions that help the orchestrator select the right tool, topic, knowledge source, or agent.
5. **Trace** an agent's plan for a multistep request using the activity map.
6. **Configure** grounding controls, such as **Allow ungrounded responses**, and **explain** how they reduce hallucinations.
7. **Design** a human-handoff path triggered by user request, business rule, or repeated failure.
8. **Troubleshoot** common orchestration problems such as wrong tool selection, duplicate messages, and missing answers.

## Topics covered

- **Generative AI fundamentals** — large language models, prompts, tokens, grounding, and non-deterministic output; choosing a primary AI model and why some external models may process data outside your geography (💳 **Licensing/Region**).
- **Generative orchestration** — the standard harness default: the agent selects and sequences topics, tools, knowledge, and other agents based on their names and descriptions, asks for missing inputs, and composes the final answer.
- **Classic orchestration** — topic selection by trigger phrases, one topic per turn with knowledge as fallback, tools only from inside topics, and when an admin setting or a prebuilt agent forces classic mode.
- **Agent planning** — how a plan is formed and executed, how conversation history affects planning, and plan-related topic triggers such as *A plan completes* and *An AI-generated response is about to be sent*.
- **Tool selection** — how names, descriptions, inputs, and outputs influence selection, the **Allow agent to decide dynamically when to use this tool** setting, and Learn's rule of thumb that selection can degrade beyond roughly 30–40 choices.
- **Agent instructions** — instructions as orchestration guidance: hints for when to use a resource, what to avoid, and how to respond (building on Module 06).
- **Natural language descriptions** — writing distinctive descriptions for topics, tools, agents, and knowledge, including what *not* to use them for.
- **Multi-step tasks** — multi-intent requests, chaining tools, returning topic outputs to the orchestrator, and the Microsoft Copilot harness's agentic loops for long-running work.
- **Context handling** — conversation history, variables, topic inputs filled from context, and the persistent memory available on the Microsoft Copilot harness (🧪 **Preview**).
- **Grounding** — grounding answers in knowledge and tool results, citations, and the **Allow ungrounded responses** setting.
- **Generative answers** — answers generated from knowledge sources, the **Conversational boosting** system topic, and generative answers nodes in topics (detailed in Modules 10 and 12).
- **Hallucinations** — why models invent content, how grounding settings and citation-friendly instructions reduce it, and how evaluations catch it.
- **Responsible AI** — the Responsible AI FAQ for generative orchestration, content moderation, safety evaluators, transparency, and human oversight.
- **Human handoff** — the Escalate system topic, the **Transfer conversation** node, live-agent engagement hubs, and the Customer Conversation harness's escalation to human representatives (🧪 **Preview**).
- **Orchestration troubleshooting** — reading the activity map, fixing overlapping descriptions, avoiding duplicate messages, and diagnosing missing or ungrounded answers.

## Planned hands-on lab

**Lab: Create an agent that handles multiple user requests using available agent capabilities**

After the lab you will have:

- A standard-harness agent with two or three topics, at least one tool, and a knowledge source, each with a precise description.
- Multi-intent requests (for example, "check my order status and tell me the return policy") handled in one turn, with the plan traced in the activity map.
- A copy of the agent switched to classic orchestration and a written comparison of the two behaviors.
- Grounding tightened (ungrounded responses turned off, citation-friendly instructions) and the effect on unsupported questions recorded.
- A working human-handoff path through the Escalate topic, tested with user-requested and rule-based escalation.

**What you need:**

- Your course environment and solution; a trial license is enough to build and test (the trial **can't publish**).
- A tool you're allowed to use under your organization's data policies, such as a prebuilt connector or a simple agent flow.
- 💳 Optional comparison: running the same requests on a **Microsoft Copilot harness** agent consumes Copilot Credits during preview and testing.

## Planned assessment

`ASSESSMENT.md` will follow the course-wide 24-item pattern, and `ANSWERS.md` will provide correct answers, detailed explanations (including why incorrect options are wrong), expected practical outcomes, and rubrics.

| Item type | Count | Planned focus for this module |
|---|---|---|
| Multiple-choice questions | 10 | Generative vs classic behavior, planning, tool selection, grounding settings, harness runtimes |
| True/false questions | 5 | Statements such as "in classic orchestration, the agent can call tools without a topic" |
| Short-answer questions | 5 | Why descriptions matter; when to choose classic orchestration |
| Practical implementation tasks | 2 | Make a multi-intent request succeed; add a rule-based escalation |
| Real-world scenario challenge | 1 | Choose an orchestration approach (and harness) for a regulated banking assistant and justify it |
| Troubleshooting challenge | 1 | The agent keeps calling the wrong tool and repeats its answer — diagnose from an activity map |
| **Total** | **24** | |

**Grading bands:** 0–59% Beginner · 60–74% Intermediate · 75–89% Advanced · 90–100% Professional Ready.

## Files in this module

| File | Purpose | Status |
|---|---|---|
| `README.md` | Syllabus: objectives, topics, lab outline, assessment plan (this file) | ✅ Syllabus |
| `CONCEPTS.md` | Full lessons for every topic using the course teaching sequence | 🔜 Planned |
| `STEP-BY-STEP-LAB.md` | Guided multi-request agent lab with checkpoints | 🔜 Planned |
| `EXAMPLES.md` | Annotated activity maps and description patterns | 🔜 Planned |
| `ASSESSMENT.md` | 24-item module assessment | 🔜 Planned |
| `ANSWERS.md` | Answers, explanations, and rubrics | 🔜 Planned |
| `INTERVIEW-QUESTIONS.md` | Interview questions with model answers | 🔜 Planned |
| `COMMON-MISTAKES.md` | Common mistakes, symptoms, and fixes | 🔜 Planned |

## Key official documentation

- [Orchestrate agent behavior with generative AI](https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-generative-actions)
- [AI-based agent authoring overview](https://learn.microsoft.com/en-us/microsoft-copilot-studio/nlu-gpt-overview)
- [About agents powered by the Microsoft Copilot harness](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/overview)
- [Harnesses in Copilot Studio](https://learn.microsoft.com/en-us/microsoft-copilot-studio/harnesses-overview)
- [Knowledge sources summary (grounding settings)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/knowledge-copilot-studio)
- [FAQ for generative orchestration](https://learn.microsoft.com/en-us/microsoft-copilot-studio/faqs-generative-orchestration)
- [Review agent activity](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-review-activity)
- [Hand off to a live agent](https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-hand-off)

## Navigation

⬅️ [Module 08 — Variables and Entities](../08-Variables-and-Entities/README.md) | 🗺️ [Course roadmap](../COURSE-ROADMAP.md) | 📈 [Learning progress](../LEARNING-PROGRESS.md) | ➡️ [Module 10 — Knowledge Sources and Grounding](../10-Knowledge-Sources-and-Grounding/README.md)

## References

- https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-generative-actions
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/nlu-gpt-overview
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/overview
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/harnesses-overview
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/knowledge-copilot-studio
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/faqs-generative-orchestration
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-review-activity
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-hand-off

_Last verified against Microsoft Learn: 18 November 2026._
