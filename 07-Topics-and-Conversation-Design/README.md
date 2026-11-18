# Module 07 — Topics and Conversation Design

> [!NOTE]
> **Status: 🔜 Planned.** This syllabus is published; the full lesson files are developed in Step 6 of the [course build plan](../COURSE-ROADMAP.md).

Topics are how you design predictable, structured conversations in Copilot Studio. This module covers topics in depth — triggers, the authoring canvas, every core node type, branching, chaining, fallback, escalation, and error handling — so you can build conversations that behave the same way every time.

> [!IMPORTANT]
> **Applies to: standard harness.** Agents on the Microsoft Copilot harness don't have topics; during an upgrade, custom topics are rebuilt as skills or workflows. The Customer Conversation harness (🧪 Preview) reuses the same topic authoring canvas for its deterministic *Topic* skills, which this module notes for comparison only.

## At a glance

| Item | Details |
|---|---|
| **Level** | Intermediate |
| **Estimated time** | 7 hours |
| **Prerequisites** | [Module 06 — Agent Configuration and Instructions](../06-Agent-Configuration-and-Instructions/README.md) |
| **Harness focus** | Standard harness only — the Microsoft Copilot harness has no topics. |
| **Lab** | Build a complete customer-support conversation |

## Why this module matters

**For beginners:** generative AI is flexible, but some conversations must follow exact steps — collecting an order number, confirming a refund, or checking eligibility. Topics give you that control with a visual, no-code canvas, and they're the foundation for the variables, entities, and orchestration modules that follow.

**For the enterprise:** regulated processes, contact-center flows, and compliance-sensitive answers need deterministic paths that can be reviewed, tested, and audited. Well-designed topics — with clean triggers, explicit fallback and escalation paths, and reusable patterns — reduce risk, simplify testing, and make analytics meaningful, because conversation outcomes such as *resolved* and *escalated* are tied to topic behavior.

## Learning objectives

By the end of this module you will be able to:

1. **Explain** what a topic is and how topics are selected under generative orchestration (by description) and classic orchestration (by trigger phrases).
2. **Differentiate** system topics from custom topics and **customize** system topics such as Conversation Start, Fallback, Escalate, and On Error safely.
3. **Configure** topic triggers, including trigger phrases, trigger conditions written in Power Fx, and trigger priority.
4. **Build** topics on the authoring canvas using Message, Question, Condition, variable-management, and topic-management nodes.
5. **Design** branching and chained conversations using Redirect, topic inputs and outputs, and End of Conversation.
6. **Implement** fallback, escalation, and error-handling paths that keep users from getting stuck.
7. **Apply** reusable conversation patterns, copying topics and using the code editor where appropriate.
8. **Test** every branch of a topic with the test panel and the topic checker.

## Topics covered

- **What are topics?** — a topic as a portion of a conversation built from nodes on an authoring canvas; how topics coexist with knowledge and tools under generative orchestration.
- **System topics** — built-in topics (for example Conversation Start, Conversational boosting, End of Conversation, Escalate, Fallback, Multiple Topics Matched, On Error, Reset Conversation); you can't create or delete them, but you can turn them off and edit them carefully.
- **Custom topics** — the predefined custom topics every agent starts with, creating topics from blank or by describing them to Copilot, naming rules (avoid periods, which break solution export), and turning topics on or off.
- **Trigger phrases** — designing the 5–10 phrases Learn recommends for classic orchestration, uploading or downloading phrase lists, and writing topic descriptions for **The agent chooses** trigger under generative orchestration.
- **Trigger conditions** — the full list of trigger types (for example *A message is received*, *The conversation changes*, *It's redirected to*, *The user is inactive for a while*, *A plan completes*), plus trigger **Condition** expressions in Power Fx and trigger **Priority**.
- **Topic canvas** — adding, renaming, copying, pasting, and deleting nodes; undo; the **Topic checker** for errors and warnings; and the YAML code editor.
- **Message nodes** — sending text, variations, rich content, and Adaptive Cards; using condition groups (released June 2026) to vary a message without extra branches.
- **Question nodes** — asking for input, identifying the expected entity, saving the answer to a variable, reprompting, and escalating when no valid answer is given.
- **Condition nodes** — branching on variable values, *All other conditions*, condition groups, and Power Fx formulas.
- **Variable assignment** — setting, parsing, and clearing variables with variable-management nodes (including clearing conversation history); deeper coverage in Module 08.
- **Redirect nodes** — moving to another topic with **Go to another topic** and returning to the original topic afterward.
- **End conversation** — ending the topic versus ending the conversation, and redirecting to the **End of Conversation** system topic so satisfaction and outcomes are captured.
- **Topic chaining** — composing small topics into larger journeys with topic inputs and outputs that pass data between them.
- **Conversation branching** — designing decision trees that stay readable, ordering branches, and avoiding dead ends.
- **Fallback** — what happens when no topic matches: Conversational boosting (generative answers) first, then the Fallback system topic, and how to customize both.
- **Escalation** — the Escalate system topic, the **Transfer conversation** node, and handing off to a live agent or engagement hub with conversation context.
- **Error handling** — the On Error system topic (error code, conversation ID, timestamp), Question-node retry limits, and safe failure messages.
- **Conversation context** — carrying context across turns and topics, the **Multiple Topics Matched** ("did you mean") experience, and how conversation history influences generative orchestration.
- **Reusable conversation patterns** — patterns such as *collect-and-confirm*, *authenticate-then-act*, *menu with escape hatch*, and *escalate-after-N-failures*, implemented as copyable topics.

## Planned hands-on lab

**Lab: Build a complete customer-support conversation**

After the lab you will have:

- A conversation design (flowchart) for an order-status and returns support journey, reviewed before building.
- Custom topics with well-written triggers, Message, Question, and Condition nodes, plus variables that hold the customer's answers.
- Chained topics using **Go to another topic**, topic inputs and outputs, and a clean finish through **End of Conversation**.
- Customized Fallback, Escalate, and On Error topics so users never hit a dead end.
- A branch-coverage checklist proving every path was exercised in the test panel with **Track between topics** turned on.

**What you need:**

- A standard-harness agent in the classic experience, inside your course solution. A trial license is enough to build and test (the trial **can't publish**).
- No Copilot Credits are consumed while building and testing on the standard harness — billing starts after publish.

## Planned assessment

`ASSESSMENT.md` will follow the course-wide 24-item pattern, and `ANSWERS.md` will provide correct answers, detailed explanations (including why incorrect options are wrong), expected practical outcomes, and rubrics.

| Item type | Count | Planned focus for this module |
|---|---|---|
| Multiple-choice questions | 10 | Trigger types, node types, system topics, orchestration modes |
| True/false questions | 5 | Statements such as "system topics can be deleted" or "agents on the Microsoft Copilot harness have topics" |
| Short-answer questions | 5 | When to use Redirect vs End conversation; how fallback differs between orchestration modes |
| Practical implementation tasks | 2 | Build a three-branch topic with validation; chain two topics with inputs and outputs |
| Real-world scenario challenge | 1 | Design a refund-eligibility conversation with escalation rules for a retailer |
| Troubleshooting challenge | 1 | A topic never triggers and another triggers by mistake — fix descriptions, phrases, and priority |
| **Total** | **24** | |

**Grading bands:** 0–59% Beginner · 60–74% Intermediate · 75–89% Advanced · 90–100% Professional Ready.

## Files in this module

| File | Purpose | Status |
|---|---|---|
| `README.md` | Syllabus: objectives, topics, lab outline, assessment plan (this file) | ✅ Syllabus |
| `CONCEPTS.md` | Full lessons for every topic using the course teaching sequence | 🔜 Planned |
| `STEP-BY-STEP-LAB.md` | Guided customer-support conversation lab with checkpoints | 🔜 Planned |
| `EXAMPLES.md` | Reusable topic patterns and annotated topic designs | 🔜 Planned |
| `ASSESSMENT.md` | 24-item module assessment | 🔜 Planned |
| `ANSWERS.md` | Answers, explanations, and rubrics | 🔜 Planned |
| `INTERVIEW-QUESTIONS.md` | Interview questions with model answers | 🔜 Planned |
| `COMMON-MISTAKES.md` | Common mistakes, symptoms, and fixes | 🔜 Planned |

## Key official documentation

- [Create and edit topics](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-create-edit-topics)
- [Use system topics](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-system-topics)
- [Set topic triggers](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-triggers)
- [Design effective trigger phrases](https://learn.microsoft.com/en-us/microsoft-copilot-studio/guidance/trigger-phrases-best-practices)
- [Ask a question](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-ask-a-question)
- [Add conditions](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-using-conditions)
- [Manage topics](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-topic-management)
- [Hand off to a live agent](https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-hand-off)

## Navigation

⬅️ [Module 06 — Agent Configuration and Instructions](../06-Agent-Configuration-and-Instructions/README.md) | 🗺️ [Course roadmap](../COURSE-ROADMAP.md) | 📈 [Learning progress](../LEARNING-PROGRESS.md) | ➡️ [Module 08 — Variables and Entities](../08-Variables-and-Entities/README.md)

## References

- https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-create-edit-topics
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-system-topics
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-triggers
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/guidance/trigger-phrases-best-practices
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-ask-a-question
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-using-conditions
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-topic-management
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-hand-off

_Last verified against Microsoft Learn: 18 November 2026._
