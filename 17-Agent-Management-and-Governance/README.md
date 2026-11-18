# Module 17 — Agent Management and Governance

> [!NOTE]
> **Status: 🔜 Planned.** This syllabus is published; the full lesson files are developed in Step 8 of the [course build plan](../COURSE-ROADMAP.md).

One agent is a project; a hundred agents is an estate. This module teaches you how to manage agents across their lifecycle and govern them at scale — ownership, environments, sharing, permissions, data policies, responsible AI, data protection, capacity and licensing, and day-to-day operations — on both harnesses.

## At a glance

| Item | Details |
|---|---|
| **Level** | Advanced |
| **Estimated time** | 5 hours |
| **Prerequisites** | [Module 16 — Analytics and Monitoring](../16-Analytics-and-Monitoring/README.md) |
| **Harness focus** | Both, with per-harness differences — the Microsoft Copilot harness has no on/off switch and is governed through roles, data policies, sharing controls, and credit limits, alongside the established controls for standard-harness agents. |
| **Lab** | Design a governance plan and review environment-level controls |

## Why this module matters

**For beginners:** knowing *who owns* an agent, *who can use* it, and *what happens when its maker leaves* sounds administrative — until an unowned agent breaks in production. Good management habits keep your agents supportable long after you build them.

**For the enterprise:** governance is what lets an organization say "yes" to agents safely. Admins need to control who can build, what data and connectors agents can reach, who agents are shared with, how much they can spend, and how to find, quarantine, or delete non-compliant agents. Professionals who can design that operating model become trusted partners to IT, security, and finance.

## Learning objectives

By the end of this module you will be able to:

1. **Describe** the end-to-end agent lifecycle from idea to retirement and the controls that apply at each stage.
2. **Explain** agent ownership and **plan** for orphaned agents, including reassignment.
3. **Design** an environment strategy with development, test, and production environments and Managed Environments controls.
4. **Configure** — or **specify for an admin** — sharing limits using **Editor** and **Viewer** assignments.
5. **Apply** data policies and knowledge-source restrictions that match an organization's risk profile.
6. **Plan** Copilot Credit capacity, licensing, and spending controls for both harnesses.
7. **Use** the agent inventory, quarantine, and deletion capabilities to operate an agent estate.
8. **Produce** a governance plan with roles, responsibilities, policies, and review cadences, including responsible AI and data protection.

## Topics covered

- **Agent lifecycle** — idea and intake, build in development, test, publish, monitor, update, and retire; ALM with solutions; and source-control and deploy-from-Git options listed in Learn's security and governance controls.
- **Agent ownership** — owners and co-authors, what happens when an owner leaves, and reassigning ownership of orphaned agents with the Power Platform API.
- **Environment management** — environment strategy, the default environment's limits, Managed Environments, environment groups and rules, and environment routing.
- **Agent sharing** — sharing for chat versus collaboration, **Editor** and **Viewer** assignments, and sharing limits enforced as a Managed Environments control (they apply only to agents that require authentication).
- **Permissions** — who can build (environment and Dataverse security roles), who can view analytics (**Analytics Viewer**) and transcripts (**Bot Transcript Viewer**), and least-privilege patterns.
- **Governance** — the security and governance controls catalog, Microsoft Agent 365 as a central control plane, agent runtime protection status, maker audit logs in Microsoft Purview, and how the Microsoft Copilot harness is governed without a dedicated on/off setting.
- **DLP policies** — data policies for Copilot Studio connectors (require authentication; block connectors as tools, HTTP requests, Azure Bot Service skills, channels, and event triggers), advanced connector policies, and admin control over which knowledge-source types makers can add.
- **Responsible AI** — governance for responsible AI: review checkpoints, evaluation and safety-test requirements before release, content moderation standards, transparency to users, and incident response.
- **Data protection** — data residency and data locations, transcript access and retention controls, customer-managed keys, network isolation, sensitivity labels, and data movement across geographies for external models.
- **Capacity and licensing** — Copilot Credits as the common currency; prepaid packs, pay-as-you-go, and prepurchase plans; monthly enforcement (unused credits don't carry over); usage-based billing for the Microsoft Copilot harness, which isn't included in a Microsoft 365 Copilot license; environment credit allocations, agent limits, and disabling draw from the tenant pool. 💳 **Licensing/Region:** confirm terms in the Microsoft Copilot Studio Licensing Guide.
- **Operational management** — agent inventory in the Power Platform admin center, API, or Azure Resource Graph; quarantining non-compliant agents; deleting agents; usage reports; and run books for incidents.
- **Enterprise administration** — the Power Platform admin center and Copilot Hub, the Microsoft 365 admin center for agent and plugin availability, tenant settings such as the Copilot Studio authors group, and a center-of-excellence operating model.

## Planned hands-on lab

**Lab: Design a governance plan and review environment-level controls**

After the lab you will have:

- An environment strategy for a fictional organization's agent estate, including a policy for the default environment and Managed Environments.
- A guided review — with an admin, or observe-only — of the Power Platform admin center controls that affect agents: data policies, sharing limits, knowledge-source restrictions, Copilot Credit allocations and agent limits, and transcript controls.
- An agent inventory review that identifies owners, harnesses, and candidates for quarantine or reassignment.
- A capacity and licensing plan with access paths per persona and credit budgets per environment.
- A governance plan with a RACI matrix, policies, responsible AI checkpoints, and a review cadence.

**What you need:**

- Access to the Power Platform admin center, or a partner admin who can walk through the controls with you (Environment Admin or tenant admin roles are needed for many settings).
- No agent is published and no Copilot Credits are consumed in this lab — it's a design-and-review exercise.

## Planned assessment

`ASSESSMENT.md` will follow the course-wide 24-item pattern, and `ANSWERS.md` will provide correct answers, detailed explanations (including why incorrect options are wrong), expected practical outcomes, and rubrics.

| Item type | Count | Planned focus for this module |
|---|---|---|
| Multiple-choice questions | 10 | Sharing controls, data policy use cases, credit controls, inventory and quarantine |
| True/false questions | 5 | Statements such as "there's a tenant setting that turns off the Microsoft Copilot harness" |
| Short-answer questions | 5 | How to handle an orphaned agent; why Editor rights can't be granted to security groups |
| Practical implementation tasks | 2 | Draft a data policy for agents; define credit allocations and agent limits for three environments |
| Real-world scenario challenge | 1 | Govern a sudden spread of maker-built agents across a 20,000-person company |
| Troubleshooting challenge | 1 | An agent consumed far more credits than expected — trace the cause and recommend controls |
| **Total** | **24** | |

**Grading bands:** 0–59% Beginner · 60–74% Intermediate · 75–89% Advanced · 90–100% Professional Ready.

## Files in this module

| File | Purpose | Status |
|---|---|---|
| `README.md` | Syllabus: objectives, topics, lab outline, assessment plan (this file) | ✅ Syllabus |
| `CONCEPTS.md` | Full lessons for every topic using the course teaching sequence | 🔜 Planned |
| `STEP-BY-STEP-LAB.md` | Guided governance-plan lab with checkpoints | 🔜 Planned |
| `EXAMPLES.md` | Sample governance plans, RACI matrices, and policies | 🔜 Planned |
| `ASSESSMENT.md` | 24-item module assessment | 🔜 Planned |
| `ANSWERS.md` | Answers, explanations, and rubrics | 🔜 Planned |
| `INTERVIEW-QUESTIONS.md` | Interview questions with model answers | 🔜 Planned |
| `COMMON-MISTAKES.md` | Common mistakes, symptoms, and fixes | 🔜 Planned |

## Key official documentation

- [Security and governance](https://learn.microsoft.com/en-us/microsoft-copilot-studio/security-and-governance)
- [View agent inventory](https://learn.microsoft.com/en-us/microsoft-copilot-studio/admin-agent-inventory)
- [Control how agents are shared](https://learn.microsoft.com/en-us/microsoft-copilot-studio/admin-sharing-controls-limits)
- [Configure data policies for agents](https://learn.microsoft.com/en-us/microsoft-copilot-studio/admin-data-loss-prevention)
- [Quarantine noncompliant agents](https://learn.microsoft.com/en-us/microsoft-copilot-studio/admin-api-quarantine)
- [Standard harness licensing](https://learn.microsoft.com/en-us/microsoft-copilot-studio/billing-licensing)
- [Manage costs for agents powered by the Microsoft Copilot harness](https://learn.microsoft.com/en-us/power-platform/admin/manage-usage-microsoft-copilot-harness)
- [Govern Copilot Credit consumption for the Microsoft Copilot harness](https://learn.microsoft.com/en-us/microsoft-copilot-studio/guidance/govern-credit-consumption)

## Navigation

⬅️ [Module 16 — Analytics and Monitoring](../16-Analytics-and-Monitoring/README.md) | 🗺️ [Course roadmap](../COURSE-ROADMAP.md) | 📈 [Learning progress](../LEARNING-PROGRESS.md) | ➡️ [Module 18 — Advanced Agent Development](../18-Advanced-Agent-Development/README.md)

## References

- https://learn.microsoft.com/en-us/microsoft-copilot-studio/security-and-governance
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/admin-agent-inventory
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/admin-sharing-controls-limits
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/admin-data-loss-prevention
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/admin-api-quarantine
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/billing-licensing
- https://learn.microsoft.com/en-us/power-platform/admin/manage-usage-microsoft-copilot-harness
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/guidance/govern-credit-consumption

_Last verified against Microsoft Learn: 18 November 2026._
