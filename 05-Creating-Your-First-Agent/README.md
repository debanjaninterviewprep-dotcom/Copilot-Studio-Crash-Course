# Module 05 — Creating Your First Agent

> [!NOTE]
> **Status: 🔜 Planned.** This syllabus is published; the full lesson files are developed in Step 5 of the [course build plan](../COURSE-ROADMAP.md).

Time to build. In this module you create, configure, test, and publish a complete FAQ assistant — first on the standard harness, then compared with the same agent built on the Microsoft Copilot harness so you see how the two experiences differ.

## At a glance

| Item | Details |
|---|---|
| **Level** | Beginner |
| **Estimated time** | 4 hours |
| **Prerequisites** | [Module 04 — Complete Copilot Studio Interface](../04-Copilot-Studio-Interface/README.md) |
| **Harness focus** | Standard-harness lab, because building and testing there doesn't consume credits before publish, with a side-by-side comparison of the Microsoft Copilot harness. |
| **Lab** | Create a complete FAQ assistant |

## Why this module matters

**For beginners:** your first agent teaches the core loop you'll repeat in every project — *create → configure → test → fix → publish*. Seeing an agent answer real questions from your own content within an hour builds the confidence you need for the deeper modules that follow.

**For the enterprise:** first agents often become the template for everything that follows. Habits formed here — meaningful names and descriptions, scoped instructions, building inside a solution, choosing the primary language deliberately (it can't be changed later on the standard harness), and testing before publishing — decide whether an organization's agent estate is maintainable or chaotic.

## Learning objectives

By the end of this module you will be able to:

1. **Create** an agent from scratch and from a natural-language description, and **compare** what Copilot Studio generates in each case.
2. **Create** an agent from a built-in template and **assess** the template's suitability, safety, and legal implications for your scenario.
3. **Write** an agent name, description, and instructions that respect Learn's documented limits (for example 42 characters for a name, 1,024 for a description, and 8,000 for instructions on the standard harness).
4. **Configure** basic agent behavior, including the greeting message and orchestration defaults.
5. **Choose** a primary language at creation time and **explain** how secondary languages are added.
6. **Configure** up to 10 suggested prompts (conversation starters) for Teams and Microsoft Copilot.
7. **Test** the agent in the test panel with a planned set of questions and **fix** at least one incorrect response.
8. **Publish** the agent to the demo website — or **describe** each publish step when using a trial license — and **explain** why changes need republishing.

## Topics covered

- **Creating agents from scratch** — starting a blank agent from the classic Home page or the **Agents** page (**Create blank agent**), with advanced settings for primary language, solution, and schema name. Compared with the new experience's **Agent** tile and **New agent** button.
- **Creating agents using descriptions** — describing your agent in up to 1,024 characters so Copilot Studio generates a name, description, and instructions and suggests knowledge, tools, triggers, and channels. Not available in sovereign clouds or when an admin turns off cross-geo checks.
- **Agent templates** — templates offered on the **Agents** page (Benefits, IT Helpdesk, Safe Travels, Sustainability Insights, Weather, Website Q&A), how to customize them, and your responsibility to assess their safety and legal fit. *Applies to: standard harness.*
- **Agent name and description** — naming conventions, Learn's limits (name up to 42 characters without angle brackets; description up to 1,024 characters), and why descriptions matter to orchestration and to other agents that connect to yours.
- **Agent instructions** — writing a first set of instructions (up to 8,000 characters on the standard harness) and editing them on the Overview page; previewing the deeper treatment in Module 06.
- **Agent behavior** — generative orchestration as the default on the standard harness, the **Conversation Start** greeting, and the enhanced orchestration runtime that the Microsoft Copilot harness uses for every agent.
- **Language settings** — choosing a primary language and region at creation (the primary language can't be changed afterward on the standard harness), adding secondary languages, and how the Microsoft Copilot harness controls response language through instructions instead.
- **Conversation starters** — configuring up to 10 **suggested prompts** that appear on the agent's welcome page in Teams and Microsoft Copilot (they aren't visible in the Copilot Studio test panel), and the Microsoft Copilot harness equivalent in **Agent settings → Greeting & prompts**.
- **Initial testing** — using the **Test your agent** panel, starting a new test session, following responses back to topics, and turning a test conversation into a short regression list.
- **Saving and publishing** — saving, publishing, opening the demo website, and remembering that every change must be published again before users see it. The trial license **can't publish**; the demo website also depends on the authentication option you choose (covered in Modules 13 and 14).

## Planned hands-on lab

**Lab: Create a complete FAQ assistant**

After the lab you will have:

- Created an FAQ agent on the standard harness from a natural-language description, and compared it with a blank-agent start.
- Set a clear name, description, and instructions within Learn's limits, inside the solution you created in Module 03.
- Grounded the agent in a public FAQ web page or an uploaded FAQ document (a preview of Module 10).
- Customized the greeting and added suggested prompts for Teams and Microsoft Copilot.
- Tested the agent against a list of at least 10 FAQ questions, recorded the results, and fixed at least one weak answer.
- Published the agent to the demo website (non-trial license) — or documented every publish step if you're on a trial.

**What you need:**

- The environment, solution, and access you prepared in [Module 03](../03-Environment-and-Setup/README.md).
- A trial license is enough to build and test; publishing needs a non-trial license path because the trial license **can't publish**.
- A short FAQ source: a public web page you're allowed to use, or a document you own.
- 💳 Optional comparison: rebuilding the FAQ agent in the new experience runs on the **Microsoft Copilot harness**, where building, previewing, and testing consume Copilot Credits. Keep that comparison short or do it as a guided walkthrough.

## Planned assessment

`ASSESSMENT.md` will follow the course-wide 24-item pattern, and `ANSWERS.md` will provide correct answers, detailed explanations (including why incorrect options are wrong), expected practical outcomes, and rubrics.

| Item type | Count | Planned focus for this module |
|---|---|---|
| Multiple-choice questions | 10 | Creation paths, templates, documented limits, suggested prompts, publishing behavior |
| True/false questions | 5 | Statements such as "you can change the primary language after creating an agent" |
| Short-answer questions | 5 | Why descriptions matter; what happens to users until you republish |
| Practical implementation tasks | 2 | Build the FAQ assistant; add suggested prompts and a custom greeting |
| Real-world scenario challenge | 1 | Turn a messy customer FAQ page into a well-scoped first agent with a test list |
| Troubleshooting challenge | 1 | "Users still see the old answer after I changed the agent" — find the missing step |
| **Total** | **24** | |

**Grading bands:** 0–59% Beginner · 60–74% Intermediate · 75–89% Advanced · 90–100% Professional Ready.

## Files in this module

| File | Purpose | Status |
|---|---|---|
| `README.md` | Syllabus: objectives, topics, lab outline, assessment plan (this file) | ✅ Syllabus |
| `CONCEPTS.md` | Full lessons for every topic using the course teaching sequence | 🔜 Planned |
| `STEP-BY-STEP-LAB.md` | Guided FAQ-assistant lab with numbered steps and checkpoints | 🔜 Planned |
| `EXAMPLES.md` | Example descriptions, instructions, and test lists | 🔜 Planned |
| `ASSESSMENT.md` | 24-item module assessment | 🔜 Planned |
| `ANSWERS.md` | Answers, explanations, and rubrics | 🔜 Planned |
| `INTERVIEW-QUESTIONS.md` | Interview questions with model answers | 🔜 Planned |
| `COMMON-MISTAKES.md` | Common mistakes, symptoms, and fixes | 🔜 Planned |

## Key official documentation

- [Quickstart: Create and deploy an agent with the standard harness](https://learn.microsoft.com/en-us/microsoft-copilot-studio/fundamentals-get-started)
- [Create and delete agents](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-first-bot)
- [Create a custom agent from a template](https://learn.microsoft.com/en-us/microsoft-copilot-studio/template-fundamentals)
- [Write agent instructions](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-instructions)
- [Configure and create multilingual agents](https://learn.microsoft.com/en-us/microsoft-copilot-studio/multilingual)
- [Configure suggested prompts for Teams and Copilot](https://learn.microsoft.com/en-us/microsoft-copilot-studio/configure-starter-prompts)
- [Key concepts - Publish and deploy your agent](https://learn.microsoft.com/en-us/microsoft-copilot-studio/publication-fundamentals-publish-channels)
- [Create a new agent (Microsoft Copilot harness)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/build-new-agent)

## Navigation

⬅️ [Module 04 — Complete Copilot Studio Interface](../04-Copilot-Studio-Interface/README.md) | 🗺️ [Course roadmap](../COURSE-ROADMAP.md) | 📈 [Learning progress](../LEARNING-PROGRESS.md) | ➡️ [Module 06 — Agent Configuration and Instructions](../06-Agent-Configuration-and-Instructions/README.md)

## References

- https://learn.microsoft.com/en-us/microsoft-copilot-studio/fundamentals-get-started
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-first-bot
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/template-fundamentals
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-instructions
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/multilingual
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/configure-starter-prompts
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/publication-fundamentals-publish-channels
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/build-new-agent

_Last verified against Microsoft Learn: 18 November 2026._
