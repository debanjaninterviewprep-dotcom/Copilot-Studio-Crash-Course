# Module 04 — Complete Copilot Studio Interface

> [!NOTE]
> **Status: 🔜 Planned.** This syllabus is published; the full lesson files are developed in Step 5 of the [course build plan](../COURSE-ROADMAP.md).

Copilot Studio now has two authoring experiences. The **new experience** (the default) builds agents on the Microsoft Copilot harness, and the **classic experience** builds agents on the standard harness. This module teaches you to find and explain every important section of both, with a practical example for each.

## At a glance

| Item | Details |
|---|---|
| **Level** | Beginner |
| **Estimated time** | 4 hours |
| **Prerequisites** | [Module 03 — Environment Setup](../03-Environment-and-Setup/README.md) |
| **Harness focus** | Both — the new experience (Home, Build tab, Agent settings, Monitor) and the classic experience (Overview, Knowledge, Tools, Agents, Topics, Activity, Monitor, Channels, Settings, test panel). |
| **Lab** | Guided interface tour: locate and explain every section in the new and classic experiences |

## Why this module matters

**For beginners:** most online tutorials and screenshots were made before 2026 and show only the classic layout. If you can't tell which experience you're in, you'll look for a **Topics** tab that doesn't exist in the new experience, or for a **Build** tab that doesn't exist in the classic one. A confident mental map of both interfaces makes every later module faster.

**For the enterprise:** teams will run both harnesses side by side for a long time — the standard harness remains fully supported and Microsoft states there's no forced switch. Professionals must support existing classic agents, build new ones in the new experience, and explain to stakeholders where settings, analytics, and publishing controls live in each.

## Learning objectives

By the end of this module you will be able to:

1. **Navigate** the new-experience Home page, the **Agents** and **Workflows** lists, and the route to the classic experience (**…** → **Open classic experience**).
2. **Identify** the four agent tabs in the new experience — **Build**, **Preview**, **Evaluate**, **Monitor** — and **explain** the purpose of each.
3. **Describe** the Build-tab components (instructions, knowledge, tools, skills, model, connected agents, memory) and the four **Agent settings** tabs.
4. **Locate** every classic-experience agent page — Overview, Knowledge, Tools, Agents, Topics, Activity, Evaluation, Monitor, Channels, Settings — plus the **Test your agent** panel and **Publish**.
5. **Compare** where the same task (for example, setting authentication or the greeting) lives in each experience.
6. **Explain** that the analytics area is now called **Monitor** in both experiences and what it shows.
7. **Use** the **Agents** page to find, open, sort, and safely delete agents, and **interpret** its *Powered by* and credit-usage columns.
8. **Apply** the right experience for a given scenario using a harness-aware checklist.

## Topics covered

Every curriculum topic below is taught in **both** experiences where it exists, with a practical example.

- **Agent overview** — the classic **Overview** page (details, instructions, knowledge, suggested prompts) versus the new experience's **Build** tab, which consolidates identity, knowledge, tools, skills, model, connected agents, and memory on one surface.
- **Create agent** — creating from the Home page (agent tile or natural-language description) or from the **Agents** page (**New agent** / **Create blank agent**); **Other ways to build** for standard-harness agents. 🧪 **Preview:** creating agents and workflows with natural language from the new Home page.
- **Agent details** — name, description, icon, primary language, solution, and schema name: on the classic Overview page and agent settings, and in the new experience's **Agent settings → Agent details** tab (read-only after the first save).
- **Instructions** — the classic Overview **Instructions** section (with `/` references to tools, topics, agents, variables, and Power Fx) versus the **Instructions** section of the new Build tab.
- **Knowledge** — the classic **Knowledge** page versus the **Knowledge** component in the Build tab; which source types each harness supports (covered in depth in Module 10).
- **Tools** — the classic **Tools** page (**Add a tool**) versus the **Tools** component in the Build tab; per-harness tool types (covered in depth in Module 11).
- **Topics** — the classic **Topics** page and topic canvas. *Applies to: standard harness.* The Microsoft Copilot harness has no topics; reusable behavior uses skills, workflows, and hooks instead.
- **Activity** — the classic **Activity** page (activity maps and transcripts for agents with generative orchestration) versus the new experience's **Preview** activity trace and **Monitor** session list.
- **Analytics** — now the **Monitor** page in both experiences: conversation outcomes, reactions, and topic/tool usage in classic; sessions, users, success rate, reactions, and Copilot Credit usage in the new experience.
- **Channels** — the classic **Channels** page versus channels configured as Build-tab components and in the **Publish agent** dialog; the Microsoft Copilot harness supports a smaller channel set.
- **Settings** — the classic **Settings** page (for example **Generative AI**, **Security**, and **Entities**) versus the new **Agent settings** dialog with four tabs: **Agent details**, **AI & behavior**, **Safety & access**, and **Greeting & prompts**.
- **Test panel** — the classic **Test your agent** panel (track between topics, variables, activity map, snapshots) versus the new **Preview** tab (maker view, end-user preview, activity trace, conversation history). 💳 Previewing a Microsoft Copilot harness agent consumes Copilot Credits.
- **Publishing** — the **Publish** button in both experiences, readiness checks, channel selection, and what "publish again after every change" means for users.
- **Agent management** — the **Agents** page (status, owner, last modified, *Powered by*, credit usage for the last 30 days), opening agents in the correct experience, sharing, and permanent deletion.

### Sections explained in the new experience (Microsoft Copilot harness)

| Section | What it's for |
|---|---|
| **Home** | Choose what to build (agent or workflow card), describe a solution in natural language (🧪 Preview), pick an environment, and reach **Other ways to build** for standard-harness agents. |
| **Agents / Workflows** (side pane) | Lists of everything you can access in the environment, across harnesses. |
| **Build** tab | Instructions (plus name and icon), Knowledge, Tools, Skills, Model, Connected agents, Memory (🧪 Preview), and channel components. |
| **Agent settings** dialog | **Agent details** (schema name, solution, primary language) · **AI & behavior** (allow other agents to connect, moderation level) · **Safety & access** (authentication, web channel security, user feedback) · **Greeting & prompts** (greeting message, suggested prompts). |
| **Preview** tab | Interactive testing with an activity trace; switch between maker view and end-user preview. |
| **Evaluate** tab | 🧪 **Preview** (production-ready preview): repeatable test conversations scored by a test method. |
| **Monitor** tab | Sessions, users, success rate, reactions, and total estimated Copilot Credits used. |
| **Publish** | Publish dialog: readiness checks, channel selection and configuration, then share or add to the organization catalog. |

### Sections explained in the classic experience (standard harness)

| Section | What it's for |
|---|---|
| **Home** (classic) | Describe an agent in your own words or start from scratch. |
| **Overview** | Details, instructions, knowledge, and suggested prompts at a glance. |
| **Knowledge** | Add and manage knowledge sources. |
| **Tools** | Add connectors, agent flows, prompts, REST APIs, MCP servers, and computer use. |
| **Agents** | Child agents and connected agents. |
| **Topics** | System and custom topics on the authoring canvas. |
| **Activity** | Historical activity maps and transcripts. |
| **Evaluation** | Test sets and agent evaluations (🟢 GA on the standard harness). |
| **Monitor** | Analytics (formerly labeled *Analytics*): outcomes, reactions, satisfaction, topic and tool usage. |
| **Channels** | Connect the agent to Teams and Microsoft Copilot, websites, and other channels. |
| **Settings** | Agent-level configuration such as generative AI behavior, security and authentication, and entities. |
| **Test your agent** panel | Live testing with topic tracking, variables, and the activity map. |
| **Publish** | Push the latest content to every connected channel. |

## Planned hands-on lab

**Lab: Guided interface tour: locate and explain every section in the new and classic experiences**

After the lab you will have:

- Navigated Home, **Agents**, and **Workflows** in the new experience, switched to the classic experience, and returned.
- Opened a sample agent in each experience and recorded the purpose of every tab and section on a "where is it?" worksheet.
- Explored each **Agent settings** tab and the classic **Settings** page, noting which settings take effect only after publishing.
- Opened the classic **Test your agent** panel and the **Publish** dialog in both experiences without publishing.
- Produced a side-by-side map of equivalent locations (for example, greeting, authentication, analytics) across the two experiences.

**What you need:**

- The environment you prepared in [Module 03](../03-Environment-and-Setup/README.md). A trial license is fine — the trial can create and test agents but **can't publish**, and this lab doesn't publish.
- 💳 Cost awareness: browsing isn't one of the credit-consuming activities Learn lists, but natural-language creation, previewing and testing, and evaluations on the **Microsoft Copilot harness** consume Copilot Credits. Hands-on testing in this lab uses the classic experience; Copilot-harness testing is optional.

## Planned assessment

`ASSESSMENT.md` will follow the course-wide 24-item pattern, and `ANSWERS.md` will provide correct answers, detailed explanations (including why incorrect options are wrong), expected practical outcomes, and rubrics.

| Item type | Count | Planned focus for this module |
|---|---|---|
| Multiple-choice questions | 10 | Which tab or dialog owns a given setting in each experience |
| True/false questions | 5 | Statements such as "agents on the Microsoft Copilot harness have a Topics page" |
| Short-answer questions | 5 | Purpose of Build, Preview, Evaluate, Monitor; how to open the classic experience |
| Practical implementation tasks | 2 | Complete the "where is it?" worksheet; change a greeting in both experiences |
| Real-world scenario challenge | 1 | Guide a stakeholder who only knows the classic layout through a new-experience agent |
| Troubleshooting challenge | 1 | "I can't find the Topics tab" — identify the harness and recommend the equivalent feature |
| **Total** | **24** | |

**Grading bands:** 0–59% Beginner · 60–74% Intermediate · 75–89% Advanced · 90–100% Professional Ready.

## Files in this module

| File | Purpose | Status |
|---|---|---|
| `README.md` | Syllabus: objectives, topics, lab outline, assessment plan (this file) | ✅ Syllabus |
| `CONCEPTS.md` | Full lessons for every section of both experiences using the course teaching sequence | 🔜 Planned |
| `STEP-BY-STEP-LAB.md` | Guided interface tour with numbered steps and checkpoints | 🔜 Planned |
| `EXAMPLES.md` | Practical examples for each section | 🔜 Planned |
| `ASSESSMENT.md` | 24-item module assessment | 🔜 Planned |
| `ANSWERS.md` | Answers, explanations, and rubrics | 🔜 Planned |
| `INTERVIEW-QUESTIONS.md` | Interview questions with model answers | 🔜 Planned |
| `COMMON-MISTAKES.md` | Common mistakes, symptoms, and fixes | 🔜 Planned |

## Key official documentation

- [Start building in Copilot Studio](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/authoring-first-bot)
- [About agents powered by the Microsoft Copilot harness](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/overview)
- [Configure settings for agents powered by the Microsoft Copilot harness](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/settings-overview)
- [Manage agents from the Agents page](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/agents-page)
- [Access standard harness agents and agent flows](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/switch-experiences)
- [Create and delete agents (standard harness)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-first-bot)
- [Test your agent (standard harness)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-test-bot)
- [Monitor agent performance in Copilot Studio](https://learn.microsoft.com/en-us/microsoft-copilot-studio/analytics-overview)

## Navigation

⬅️ [Module 03 — Environment Setup](../03-Environment-and-Setup/README.md) | 🗺️ [Course roadmap](../COURSE-ROADMAP.md) | 📈 [Learning progress](../LEARNING-PROGRESS.md) | ➡️ [Module 05 — Creating Your First Agent](../05-Creating-Your-First-Agent/README.md)

## References

- https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/authoring-first-bot
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/overview
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/settings-overview
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/agents-page
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/switch-experiences
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-first-bot
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-test-bot
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/analytics-overview

_Last verified against Microsoft Learn: 18 November 2026._
