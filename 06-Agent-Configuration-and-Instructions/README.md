# Module 06 — Agent Configuration and Instructions

> [!NOTE]
> **Status: 🔜 Planned.** This syllabus is published; the full lesson files are developed in Step 6 of the [course build plan](../COURSE-ROADMAP.md).

Instructions are the single most powerful lever you have over an agent's behavior. This module teaches you to write, structure, test, and optimize instructions and descriptions — responsibly — on both the standard harness and the Microsoft Copilot harness.

## At a glance

| Item | Details |
|---|---|
| **Level** | Beginner–Intermediate |
| **Estimated time** | 4 hours |
| **Prerequisites** | [Module 05 — Creating Your First Agent](../05-Creating-Your-First-Agent/README.md) |
| **Harness focus** | Both — the standard harness uses instructions together with topic, tool, and knowledge descriptions; the Microsoft Copilot harness uses instructions as the primary mechanism for controlling behavior. |
| **Lab** | Create a professional customer-support agent |

## Why this module matters

**For beginners:** a vague instruction such as "be helpful" produces a vague agent. Learning to state a role, objectives, scope, restrictions, and tone turns a generic chatbot into a dependable assistant — and it's the fastest way to improve answer quality without adding any new features.

**For the enterprise:** instructions are part of your control surface. They encode brand voice, compliance boundaries, escalation rules, and what the agent must refuse. Poorly written instructions cause off-topic answers, missing citations, wrong tool calls, and reputational risk; well-written ones are reviewed, versioned, and tested like any other production artifact.

## Learning objectives

By the end of this module you will be able to:

1. **Explain** how the orchestrator uses instructions to choose resources, fill tool inputs, and generate responses.
2. **Write** a structured instruction set covering role, objectives, scope, restrictions, tone, and response guidelines.
3. **Distinguish** instructions from descriptions and **write** precise descriptions for agents, tools, topics, and knowledge sources.
4. **Use** `/` references in standard-harness instructions to point to specific tools, topics, agents, variables, or Power Fx expressions.
5. **Identify** instruction patterns that break agents — such as asking for tools or knowledge the agent doesn't have, or interfering with system-defined citations.
6. **Configure** behavior-related settings in each harness, such as the moderation level in the Microsoft Copilot harness and grounding controls on the standard harness.
7. **Evaluate** instructions with a test matrix (in-scope, out-of-scope, ambiguous, and adversarial prompts) and **optimize** them iteratively.
8. **Apply** responsible AI practices — transparency, human oversight, privacy notices, and safe refusals — to agent configuration.

## Topics covered

- **Agent instructions** — what instructions are, where you edit them (classic **Overview** page; new-experience **Build** tab), Learn's 8,000-character limit on the standard harness, and why instructions must be grounded in capabilities the agent actually has.
- **System behavior** — how system-level behavior is shaped: system topics and generative orchestration on the standard harness, and the **AI & behavior** settings tab (allow other agents to connect, moderation level) on the Microsoft Copilot harness.
- **Role definition** — giving the agent a clear identity and purpose ("You are the customer-support assistant for…"), and why a role alone isn't enough.
- **Objectives** — stating measurable goals for the agent (resolve, route, collect, inform) so behavior and testing align.
- **Scope** — declaring what the agent covers and what it redirects, so it stays on topic and hands off cleanly.
- **Restrictions** — writing explicit "do not" rules (for example, never promise refunds, never give legal advice) and pairing them with what to do instead.
- **Tone and communication style** — brand voice, formality, length, and accessibility, and testing tone across channels.
- **Response guidelines** — formatting, structure, follow-up questions, and how to handle unclear input — without overriding the system-defined citation format, which Learn warns can cause valid grounded answers to be discarded.
- **Context** — using conversation context, variables, and `/` references in instructions; how conversation history changes orchestration decisions; and, on the Microsoft Copilot harness, memory (🧪 **Preview**) as persistent context.
- **Agent descriptions** — writing descriptions that orchestration relies on: for the agent itself (used when other agents connect to it) and for each tool, topic, child or connected agent, and knowledge source.
- **Instruction optimization** — an iterate-and-test loop, recommended vocabulary for conditions and data retrieval, removing redundancy, and when to move logic out of instructions into topics, tools, or skills.
- **Responsible AI** — Microsoft's responsible AI principles, the Responsible AI FAQs for Copilot Studio features, moderation and grounding controls, human oversight, and a privacy statement link that a Power Platform admin configures per environment to appear at the start of conversations (🧪 **Preview**; *applies to: standard harness*).

## Planned hands-on lab

**Lab: Create a professional customer-support agent**

After the lab you will have:

- Written a structured instruction set (role, objectives, scope, restrictions, tone, response guidelines, escalation) for a fictional company's customer-support agent.
- Written precise descriptions for the agent and its knowledge sources so orchestration chooses them correctly.
- Configured grounding and safety-related settings and documented why each value was chosen.
- Run a 20-prompt test matrix covering in-scope, out-of-scope, ambiguous, and adversarial requests, and recorded pass/fail results.
- Revised the instructions at least twice and shown measurable improvement on the same test matrix.

**What you need:**

- Your course environment and solution from [Module 03](../03-Environment-and-Setup/README.md); a trial license is enough because this lab doesn't publish (the trial **can't publish**).
- A short, fictional support-policy document to use as knowledge.
- 💳 Optional comparison: repeating the test matrix on a **Microsoft Copilot harness** agent consumes Copilot Credits during preview and testing.

## Planned assessment

`ASSESSMENT.md` will follow the course-wide 24-item pattern, and `ANSWERS.md` will provide correct answers, detailed explanations (including why incorrect options are wrong), expected practical outcomes, and rubrics.

| Item type | Count | Planned focus for this module |
|---|---|---|
| Multiple-choice questions | 10 | Instruction components, descriptions vs instructions, harness differences, responsible AI controls |
| True/false questions | 5 | Statements such as "instructions can make an agent use a tool it hasn't been given" |
| Short-answer questions | 5 | Rewrite a weak instruction; explain why citation-altering instructions are risky |
| Practical implementation tasks | 2 | Author the support agent's instruction set; write descriptions for three tools or knowledge sources |
| Real-world scenario challenge | 1 | Adapt one agent's instructions for a regulated industry with strict refusal rules |
| Troubleshooting challenge | 1 | The agent answers off-topic questions and skips citations — diagnose the instruction problems |
| **Total** | **24** | |

**Grading bands:** 0–59% Beginner · 60–74% Intermediate · 75–89% Advanced · 90–100% Professional Ready.

## Files in this module

| File | Purpose | Status |
|---|---|---|
| `README.md` | Syllabus: objectives, topics, lab outline, assessment plan (this file) | ✅ Syllabus |
| `CONCEPTS.md` | Full lessons for every topic using the course teaching sequence | 🔜 Planned |
| `STEP-BY-STEP-LAB.md` | Guided customer-support agent lab with checkpoints | 🔜 Planned |
| `EXAMPLES.md` | Before-and-after instruction examples and description patterns | 🔜 Planned |
| `ASSESSMENT.md` | 24-item module assessment | 🔜 Planned |
| `ANSWERS.md` | Answers, explanations, and rubrics | 🔜 Planned |
| `INTERVIEW-QUESTIONS.md` | Interview questions with model answers | 🔜 Planned |
| `COMMON-MISTAKES.md` | Common mistakes, symptoms, and fixes | 🔜 Planned |

## Key official documentation

- [Write agent instructions (standard harness)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-instructions)
- [Configure agent details and instructions (Microsoft Copilot harness)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/authoring-instructions)
- [Configure high-quality instructions for generative orchestration](https://learn.microsoft.com/en-us/microsoft-copilot-studio/guidance/generative-mode-guidance)
- [Orchestrate agent behavior with generative AI (authoring descriptions)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-generative-actions)
- [Configure settings for agents powered by the Microsoft Copilot harness](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/settings-overview)
- [Responsible AI FAQs for Copilot Studio](https://learn.microsoft.com/en-us/microsoft-copilot-studio/responsible-ai-overview)
- [FAQ for generative orchestration](https://learn.microsoft.com/en-us/microsoft-copilot-studio/faqs-generative-orchestration)
- [Configure a privacy statement link (preview)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/configure-privacy-statement-link)

## Navigation

⬅️ [Module 05 — Creating Your First Agent](../05-Creating-Your-First-Agent/README.md) | 🗺️ [Course roadmap](../COURSE-ROADMAP.md) | 📈 [Learning progress](../LEARNING-PROGRESS.md) | ➡️ [Module 07 — Topics and Conversation Design](../07-Topics-and-Conversation-Design/README.md)

## References

- https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-instructions
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/authoring-instructions
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/guidance/generative-mode-guidance
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-generative-actions
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/settings-overview
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/responsible-ai-overview
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/faqs-generative-orchestration
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/configure-privacy-statement-link

_Last verified against Microsoft Learn: 18 November 2026._
