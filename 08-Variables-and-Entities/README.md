# Module 08 — Variables and Entities

> [!NOTE]
> **Status: 🔜 Planned.** This syllabus is published; the full lesson files are developed in Step 6 of the [course build plan](../COURSE-ROADMAP.md).

Conversations need memory and structure. Variables let an agent remember what it has learned, and entities let it recognize structured information — dates, amounts, product names, account numbers — in what users type. This module teaches you to capture, validate, reuse, and pass that information between topics.

> [!IMPORTANT]
> **Applies to: standard harness.** Variables and entities as taught here are part of standard-harness topic authoring. Agents on the Microsoft Copilot harness don't support custom entities and don't use topics. The Customer Conversation harness (🧪 Preview) has its own variables and entities settings, which this module mentions for comparison only.

## At a glance

| Item | Details |
|---|---|
| **Level** | Intermediate |
| **Estimated time** | 6 hours |
| **Prerequisites** | [Module 07 — Topics and Conversation Design](../07-Topics-and-Conversation-Design/README.md) |
| **Harness focus** | Standard harness only — variables and entities live inside topics, which the Microsoft Copilot harness doesn't have. |
| **Lab** | Create an agent that collects customer information |

## Why this module matters

**For beginners:** without variables, an agent forgets your name the moment you give it. Without entities, it can't tell that "next Friday" is a date or that "1000 dollars" is an amount. Mastering both is what turns a scripted conversation into a useful one.

**For the enterprise:** customer data collection is where quality, privacy, and compliance meet. Correct data types, validation, and scoping prevent bad data from reaching downstream systems; disciplined use of global and environment variables keeps agents portable across development, test, and production; and avoiding unnecessary personal data in variables reduces privacy risk.

## Learning objectives

By the end of this module you will be able to:

1. **Differentiate** the four variable scopes — topic, global, system, and environment — and **choose** the right scope for a requirement.
2. **Identify** the base data types (String, Number, Boolean, Table, Record, DateTime, Choice, Blank) and **explain** why a variable's type is fixed after its first assignment.
3. **Create** and **use** string, number, and Boolean variables in Message, Question, and Condition nodes.
4. **Configure** Question nodes to recognize prebuilt (system) entities and **create** custom closed-list and regular-expression entities.
5. **Demonstrate** proactive slot filling, where the agent extracts several values from one user message.
6. **Implement** data validation with reprompts, conditions, and Power Fx expressions.
7. **Build** dynamic responses that insert variables and adapt to the values collected.
8. **Pass** information between topics with topic inputs and outputs and with global variables, and **inspect** values during testing.

## Topics covered

- **System variables** — variables Copilot Studio creates automatically to describe the conversation, user, and activity, available in all topics (for example `User.DisplayName` when Microsoft authentication is configured).
- **Topic variables** — the default scope: created in a topic and usable only there; naming conventions and lifecycle.
- **Global variables** — variables usable across all topics, changing a topic variable's scope to global, and when global state helps or hurts.
- **Variable scopes** — topic, global, system, and environment (Power Platform environment variables, read-only in Copilot Studio) and how environment variables keep configuration out of topics when solutions move between environments.
- **Data types** — String, Number, Boolean, Table, Record, DateTime, Choice, and Blank; type assignment on first use; and initializing variables correctly in looping topics.
- **String variables** — capturing free text, formatting, and concatenating strings in messages and Power Fx.
- **Number variables** — capturing amounts and quantities, comparisons such as *is greater than*, and arithmetic with Power Fx.
- **Boolean variables** — yes/no answers, flags that drive Condition nodes, and readable Boolean logic.
- **Entity recognition** — how natural language understanding extracts entities from user input and maps them to typed values.
- **System entities** — the prebuilt entities listed in **Settings → Entities** (Learn's examples include age, colors, numbers, names, money, and duration) and the typed values each one extracts.
- **Custom entities** — closed-list entities (with synonyms and optional smart matching) and regular-expression entities for domain terms such as product categories or account-number formats.
- **Slot filling** — placing extracted entity values into variables; proactive slot filling so a single message such as "I want hiking boots under $100" fills several variables at once; and the **Skip question** behavior that lets the agent skip a Question node when the value is already known.
- **Data validation** — validating input with entities, conditions, reprompts, and retry limits, and escalating when validation keeps failing.
- **Dynamic responses** — inserting variables into messages, message variations, and Power Fx formulas that adapt wording to collected values.
- **Passing information between topics** — topic input and output parameters, redirects that return values, global variables, and how generative orchestration can fill topic inputs from conversation context.

## Planned hands-on lab

**Lab: Create an agent that collects customer information**

After the lab you will have:

- A data-collection topic that asks for name, email, phone, account number, and preferred contact method using Question nodes and prebuilt entities.
- A custom closed-list entity (contact method) and a custom regular-expression entity (account-number format).
- Validation with reprompts and conditions, plus a confirmation message that plays the collected details back dynamically.
- A demonstration of proactive slot filling from a single user message.
- Collected values passed to a second topic through topic outputs and inputs, and a global variable reused in a later topic.
- Screenshots or notes from the **Variables** panel's **Test** tab showing each value during testing.

**What you need:**

- A standard-harness agent in your course solution; a trial license is enough to build and test (the trial **can't publish**).
- Synthetic test data only — never real customer personal data in a learning environment.
- No Copilot Credits are consumed while building and testing on the standard harness — billing starts after publish.

## Planned assessment

`ASSESSMENT.md` will follow the course-wide 24-item pattern, and `ANSWERS.md` will provide correct answers, detailed explanations (including why incorrect options are wrong), expected practical outcomes, and rubrics.

| Item type | Count | Planned focus for this module |
|---|---|---|
| Multiple-choice questions | 10 | Variable scopes, data types, entity types, slot filling |
| True/false questions | 5 | Statements such as "environment variables can be changed from inside a topic" |
| Short-answer questions | 5 | When to use a global variable; closed-list vs regex entity |
| Practical implementation tasks | 2 | Build a validated data-collection topic; pass values between two topics |
| Real-world scenario challenge | 1 | Design data capture for a warranty-claim conversation with privacy constraints |
| Troubleshooting challenge | 1 | A variable shows *unknown* or the wrong type during testing — diagnose and fix |
| **Total** | **24** | |

**Grading bands:** 0–59% Beginner · 60–74% Intermediate · 75–89% Advanced · 90–100% Professional Ready.

## Files in this module

| File | Purpose | Status |
|---|---|---|
| `README.md` | Syllabus: objectives, topics, lab outline, assessment plan (this file) | ✅ Syllabus |
| `CONCEPTS.md` | Full lessons for every topic using the course teaching sequence | 🔜 Planned |
| `STEP-BY-STEP-LAB.md` | Guided customer-information lab with checkpoints | 🔜 Planned |
| `EXAMPLES.md` | Variable, entity, validation, and Power Fx examples | 🔜 Planned |
| `ASSESSMENT.md` | 24-item module assessment | 🔜 Planned |
| `ANSWERS.md` | Answers, explanations, and rubrics | 🔜 Planned |
| `INTERVIEW-QUESTIONS.md` | Interview questions with model answers | 🔜 Planned |
| `COMMON-MISTAKES.md` | Common mistakes, symptoms, and fixes | 🔜 Planned |

## Key official documentation

- [Variables overview](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-variables-about)
- [Work with variables](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-variables)
- [Work with global variables](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-variables-bot)
- [Use entities and slot filling in agents](https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-entities-slot-filling)
- [Manage topic inputs and outputs](https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-managing-topic-inputs-outputs)
- [Create expressions with Power Fx](https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-power-fx)
- [Ask a question](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-ask-a-question)
- [Test your agent (variable inspection)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-test-bot)

## Navigation

⬅️ [Module 07 — Topics and Conversation Design](../07-Topics-and-Conversation-Design/README.md) | 🗺️ [Course roadmap](../COURSE-ROADMAP.md) | 📈 [Learning progress](../LEARNING-PROGRESS.md) | ➡️ [Module 09 — Generative AI and Orchestration](../09-Generative-AI-and-Orchestration/README.md)

## References

- https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-variables-about
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-variables
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-variables-bot
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-entities-slot-filling
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-managing-topic-inputs-outputs
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-power-fx
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-ask-a-question
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-test-bot

_Last verified against Microsoft Learn: 18 November 2026._
