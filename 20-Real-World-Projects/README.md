# Module 20 — Real-World Projects

> [!NOTE]
> **Status: 🔜 Planned.** This syllabus is published; the full lesson files are developed in Step 9 of the [course build plan](../COURSE-ROADMAP.md).

Ten complete, end-to-end Copilot Studio projects that mirror what organizations actually build. Every project starts from a business problem, names the recommended harness and why, and is delivered with the same eleven professional artifacts — from business requirements to troubleshooting.

## At a glance

| Item | Details |
|---|---|
| **Level** | Professional |
| **Estimated time** | 20 hours |
| **Prerequisites** | [Module 01](../01-Introduction-to-Copilot-Studio/README.md) through [Module 19](../19-Enterprise-Copilot-Architecture/README.md) |
| **Harness focus** | Each project specifies its harness and justifies it — most use the standard harness for predictable, GA-based delivery; reasoning- and file-heavy projects use the Microsoft Copilot harness. |
| **Lab** | Ten end-to-end projects (HR, IT helpdesk, customer support, company knowledge, employee policy, product FAQ, sales information, internal business, document Q&A, enterprise multi-agent) |

## Why this module matters

**For learners:** knowing features isn't the same as delivering solutions. These projects make you practice the full professional loop — clarify requirements, choose a harness, design, build, secure, test, publish, and support — until it becomes habit.

**For the enterprise and your portfolio:** each completed project produces artifacts a hiring manager or stakeholder can review: requirements, architecture, conversation design, test evidence, and a support runbook. Together they demonstrate that you can make sound harness decisions, manage preview risk, and ship agents that are secure and maintainable.

## Learning objectives

By the end of this module you will be able to:

1. **Translate** a business problem into documented requirements, use cases, and success criteria.
2. **Select** the right harness for each project and **defend** the choice with Learn's selection criteria.
3. **Design** agent architectures, conversation flows, knowledge configurations, and instructions for ten distinct scenarios.
4. **Build** and **configure** each agent, including tools where applicable, on the chosen harness.
5. **Validate** each agent with structured test sets and acceptance criteria.
6. **Secure** and **publish** each agent to an appropriate channel with matching authentication.
7. **Troubleshoot** project-specific failure modes and **document** fixes in a runbook.
8. **Compare** single-agent and multi-agent designs and **state** which multi-agent options are GA or preview on each harness.

## Topics covered

### The ten projects

- **1. HR Employee Assistant** — answers leave, benefits, and HR-process questions from HR content and guides employees through structured HR requests.
- **2. IT Helpdesk Agent** — resolves common IT questions, collects ticket details, and routes simple requests such as access or password help.
- **3. Customer Support Agent** — handles customer questions around the clock and escalates complex cases to a human with context.
- **4. Company Knowledge Assistant** — finds authoritative answers across SharePoint, files, and other company knowledge with citations.
- **5. Employee Policy Assistant** — gives consistent, cited answers about company policies with strict scope and refusal rules.
- **6. Product FAQ Agent** — answers public product questions on a website from approved product content.
- **7. Sales Information Assistant** — prepares account briefs from CRM data, documents, and Microsoft 365 context.
- **8. Internal Business Assistant** — automates a multistep back-office process, such as matching invoices to purchase orders and routing exceptions.
- **9. Document Question-Answering Agent** — answers questions about long documents (contracts, manuals) with traceable sources and structured outputs.
- **10. Enterprise Multi-Agent Solution (where supported)** — a front-door agent that routes employees to specialist agents owned by different teams.

### Project portfolio and harness recommendations

| # | Project | Business problem | Recommended harness | Why this harness |
|---|---|---|---|---|
| 1 | HR Employee Assistant | Employees wait for answers about leave and benefits, and HR answers the same questions repeatedly. | Standard harness | Predictable, policy-bound answers plus deterministic HR request topics; permission-aware SharePoint knowledge; Teams publishing. |
| 2 | IT Helpdesk Agent | Service desks are flooded with repetitive requests. | Standard harness | Learn describes an internal help desk that answers common questions and routes simple requests through a workflow as a standard-harness fit; an IT Helpdesk template exists. |
| 3 | Customer Support Agent | Customers need 24/7 help and a smooth path to a person. | Standard harness for production; Customer Conversation harness (🧪 Preview) as an optional pilot | GA channels and live-agent handoff to engagement hubs today; the Customer Conversation harness is purpose-built for voice and chat with human escalation but is in preview. |
| 4 | Company Knowledge Assistant | Knowledge is scattered and employees can't find authoritative answers. | Standard harness (Microsoft Copilot harness variant optional) | Bounded, cited Q&A over SharePoint, files, and Dataverse; a Copilot-harness variant with Work IQ is justified only if cross-Microsoft 365 reasoning is required. |
| 5 | Employee Policy Assistant | Inconsistent policy answers create compliance risk. | Standard harness | Explicit control: ungrounded responses off, citation-backed answers, and deterministic topics for sensitive policies. |
| 6 | Product FAQ Agent | Prospects ask the same product questions on the public site. | Standard harness | Public-website knowledge, anonymous web chat, the broadest channel support, and predictable FAQ behavior. |
| 7 | Sales Information Assistant | Sellers spend hours compiling account information before meetings. | Microsoft Copilot harness (🧪 production-ready preview) | Reasons across several sources, natively creates Word, Excel, and PowerPoint briefs, uses Work IQ grounding, and publishes to Teams and Microsoft Copilot. 💳 Consumes credits from build time. |
| 8 | Internal Business Assistant | Multistep back-office processes are slow and manual. | Microsoft Copilot harness (🧪 production-ready preview) | Matches Learn's accounts-payable example: breaks goals into steps, recovers from failures, handles files, and calls workflows (🧪 Preview as tools). 💳 Usage-based billing. |
| 9 | Document Question-Answering Agent | Teams need fast, accurate, traceable answers from long documents. | Standard harness | Uploaded documents, generative answers nodes, and prompts with JSON output give controlled, cited answers; use the Microsoft Copilot harness only when whole-file reasoning or user-attached files are central. |
| 10 | Enterprise Multi-Agent Solution | Employees need one entry point to services owned by many teams. | Standard harness for the production path; optional Microsoft Copilot harness pilot | The standard harness offers GA multi-agent options (child agents, connected Copilot Studio agents, A2A); most external-agent options and the Copilot harness itself are preview. |

> [!IMPORTANT]
> **Project 10 — multi-agent options by harness (verified 18 November 2026)**
>
> - **Standard harness:** 🟢 GA — child agents, connected Copilot Studio agents in the same environment, and Agent2Agent (A2A) protocol agents. 🧪 Preview — Microsoft Foundry agents, Microsoft Fabric data agents, and Microsoft 365 Agents SDK agents.
> - **Microsoft Copilot harness** (🧪 production-ready preview): connected agents — other Microsoft Copilot harness agents, Microsoft Foundry agents, and Microsoft 365 Agents SDK agents; A2A connected agents are 🧪 Preview. Delegation is one level deep, and there are no child agents (use skills, connected agents, or task agents where available).
> - **Customer Conversation harness** (🧪 Preview): a primary agent with sub-agents, plus Microsoft Foundry agents as connected agents.
> - **Across harnesses:** standard-harness and Microsoft Copilot harness agents can't invoke each other directly.

### Deliverables for every project

Each project is delivered with the same eleven artifacts:

- **Business requirements** — problem statement, stakeholders, scope, constraints, and measurable success criteria.
- **Use cases** — prioritized user stories and example conversations, including out-of-scope requests.
- **Agent architecture** — harness choice and justification, components (topics or skills, knowledge, tools, other agents), and a diagram.
- **Conversation design** — greeting, key flows, clarification, fallback, escalation, and closing behavior.
- **Knowledge configuration** — sources, descriptions, permissions, and grounding settings.
- **Instructions** — the final instruction set and agent and component descriptions, with rationale.
- **Tools where applicable** — tool choices, inputs and outputs, credentials, and confirmation rules.
- **Testing** — test sets, evaluation results, and acceptance criteria.
- **Security** — authentication, sharing, data policy impact, and responsible AI review.
- **Publishing** — target channels, channel configuration, and deployment validation.
- **Troubleshooting** — known issues, diagnostics, fixes, and a support runbook.

## Planned hands-on lab

**Lab: Ten end-to-end projects (HR, IT helpdesk, customer support, company knowledge, employee policy, product FAQ, sales information, internal business, document Q&A, enterprise multi-agent)**

After the lab you will have:

- Ten working agents (or documented designs where licensing prevents a build), each on its recommended harness.
- A complete set of eleven deliverables per project, ready for a portfolio.
- Evaluation evidence for every project, with before-and-after improvements.
- At least one published agent per channel type you have access to, validated end to end.
- A cross-project lessons-learned note comparing harness choices, costs, and preview risks.

**What you need:**

- A license path that **can publish** — the trial license **can't publish** — plus development and test environments, a SharePoint site with sample content, and Teams.
- 💳 Projects 7 and 8 (and any Microsoft Copilot harness or Customer Conversation harness variants) consume Copilot Credits from the moment you start building, previewing, and evaluating; agree a credit budget first.
- Admin support for data policies, sharing, and organization-wide publishing where required.

## Planned assessment

`ASSESSMENT.md` will follow the course-wide 24-item pattern, and `ANSWERS.md` will provide correct answers, detailed explanations (including why incorrect options are wrong), expected practical outcomes, and rubrics. Each project's deliverables are also scored against a project rubric.

| Item type | Count | Planned focus for this module |
|---|---|---|
| Multiple-choice questions | 10 | Harness selection per project, multi-agent status, deliverable quality criteria |
| True/false questions | 5 | Statements such as "child agents are available on the Microsoft Copilot harness" |
| Short-answer questions | 5 | Justify a harness for a given project; outline a project's test strategy |
| Practical implementation tasks | 2 | Complete two projects' deliverables end to end |
| Real-world scenario challenge | 1 | Adapt one project to a new industry with stricter compliance rules |
| Troubleshooting challenge | 1 | A deployed project agent fails after a content update — diagnose and fix using the runbook |
| **Total** | **24** | |

**Grading bands:** 0–59% Beginner · 60–74% Intermediate · 75–89% Advanced · 90–100% Professional Ready.

## Files in this module

| File | Purpose | Status |
|---|---|---|
| `README.md` | Syllabus: project portfolio, harness choices, deliverables, assessment plan (this file) | ✅ Syllabus |
| `CONCEPTS.md` | Project delivery method, harness-selection approach, and deliverable templates | 🔜 Planned |
| `STEP-BY-STEP-LAB.md` | Step-by-step build guides for all ten projects | 🔜 Planned |
| `EXAMPLES.md` | Completed example deliverables for each project | 🔜 Planned |
| `ASSESSMENT.md` | 24-item module assessment plus project rubric | 🔜 Planned |
| `ANSWERS.md` | Answers, explanations, and rubrics | 🔜 Planned |
| `INTERVIEW-QUESTIONS.md` | Project-based interview questions with model answers | 🔜 Planned |
| `COMMON-MISTAKES.md` | Common project mistakes, symptoms, and fixes | 🔜 Planned |

## Key official documentation

- [Compare Copilot Studio agent harnesses](https://learn.microsoft.com/en-us/microsoft-copilot-studio/guidance/choose-harness)
- [Harnesses in Copilot Studio](https://learn.microsoft.com/en-us/microsoft-copilot-studio/harnesses-overview)
- [Define project objectives and success criteria](https://learn.microsoft.com/en-us/microsoft-copilot-studio/guidance/project-best-practices)
- [Create a custom agent from a template](https://learn.microsoft.com/en-us/microsoft-copilot-studio/template-fundamentals)
- [Agents powered by the Customer Conversation harness overview](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/overview-customer-conversation)
- [Add other agents overview (standard harness)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-add-other-agents)
- [Connected agents overview (Microsoft Copilot harness)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/authoring-add-other-agents)
- [About agent evaluation](https://learn.microsoft.com/en-us/microsoft-copilot-studio/analytics-agent-evaluation-intro)

## Navigation

⬅️ [Module 19 — Enterprise Copilot Studio Architecture](../19-Enterprise-Copilot-Architecture/README.md) | 🗺️ [Course roadmap](../COURSE-ROADMAP.md) | 📈 [Learning progress](../LEARNING-PROGRESS.md) | ➡️ [Module 21 — Interview Preparation](../21-Interview-Preparation/README.md)

## References

- https://learn.microsoft.com/en-us/microsoft-copilot-studio/guidance/choose-harness
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/harnesses-overview
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/guidance/project-best-practices
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/template-fundamentals
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/overview-customer-conversation
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-add-other-agents
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/authoring-add-other-agents
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/analytics-agent-evaluation-intro

_Last verified against Microsoft Learn: 18 November 2026._
