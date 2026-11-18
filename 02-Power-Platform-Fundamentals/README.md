# Module 02 — Power Platform Fundamentals

> [!NOTE]
> **Status: 🔜 Planned.** This syllabus is published; the full lesson files are developed in Step 5 of the [course build plan](../COURSE-ROADMAP.md).

Microsoft Copilot Studio runs on Microsoft Power Platform. This module teaches **only** the Power Platform fundamentals you need to build, secure, and ship Copilot Studio agents. It is not a Power Apps or Power Automate development track.

## At a glance

| Item | Details |
|---|---|
| **Level** | Beginner |
| **Estimated time** | 4 hours |
| **Prerequisites** | [Module 01 — Introduction to Microsoft Copilot Studio](../01-Introduction-to-Copilot-Studio/README.md) |
| **Harness focus** | Harness-independent — environments, Dataverse, connectors, solutions, and security roles sit underneath agents on every harness. |
| **Lab** | Map the Power Platform building blocks Copilot Studio uses (environments, Dataverse, connectors, solutions, security roles) |

## Why this module matters

**For beginners:** every agent you build lives in a Power Platform *environment*, relies on a *Dataverse* database, reaches other systems through *connectors*, and should be packaged in a *solution*. Once you understand these building blocks, common first-day errors such as "You don't have permissions to any environments" or "my environment isn't in the list" stop being mysterious.

**For the enterprise:** administrators govern Copilot Studio with the same Power Platform controls they already use for apps and flows — environment strategy, security roles, data policies, and managed environments. Makers who understand this vocabulary design agents that pass security review, move cleanly from development to production, and don't get blocked by policy at publish time.

## Learning objectives

By the end of this module you will be able to:

1. **Describe** the main Power Platform components and **explain** where Copilot Studio fits among them.
2. **Explain** what an environment is (tenant-scoped, bound to a geographic region, with zero or one Dataverse database) and **compare** the environment types: default, production, sandbox, trial, developer, and Dataverse for Teams.
3. **Identify** the Dataverse capabilities Copilot Studio depends on, such as agent storage, Dataverse knowledge sources, and conversation transcripts.
4. **Differentiate** standard, premium, and custom connectors and **explain** how a connector becomes an agent tool.
5. **Distinguish** unmanaged from managed solutions and **justify** building agents inside a solution from day one.
6. **Classify** tenant-level admin roles, environment roles (Environment Admin, Environment Maker), and Dataverse security roles (for example System Administrator, System Customizer, Basic User).
7. **Locate** environments, data policies, and Copilot Studio capacity information in the Power Platform admin center.
8. **Explain** how data policies group connectors into Business, Non-business, and Blocked, and **predict** how a policy affects an agent.

## Topics covered

- **Power Platform overview** — the low-code family (Power Apps, Power Automate, Power Pages, Power BI, Copilot Studio) and the shared layers underneath it (environments, Dataverse, connectors, administration), with a focus on the parts Copilot Studio uses.
- **Environments** — what an environment contains, why it is bound to a tenant and region, the environment types and their intended use, and why Learn recommends a *non-default production environment* for production agents.
  - ⚠️ **Deprecated:** unmanaged developer environments (new ones can't be created from 15 November 2026; existing ones are suspended from 15 December 2026) and Dataverse for Teams environments (no new ones from 15 November 2026). The developer environment type continues only as a *managed* developer environment, one per user.
- **Dataverse fundamentals** — tables, rows, and columns; role-based security; the "zero or one database per environment" rule; and why an environment without a Dataverse database doesn't appear in the Copilot Studio environment list.
- **Connectors** — prebuilt connectors (standard and premium tiers), custom connectors, connections and credentials, and how connectors surface in Copilot Studio as agent tools (both harnesses) or, as Copilot connectors, as knowledge sources.
- **Solutions** — unmanaged solutions (develop) versus managed solutions (deploy), solution publishers and dependencies, and how Copilot Studio agents and their components travel between environments.
- **Security roles** — the difference between tenant-level admin roles, environment roles, and Dataverse security roles, and the important rule that tenant admin roles don't automatically grant Dataverse data access. Includes a first look at Copilot Studio–specific roles such as **Bot Transcript Viewer**.
- **Environment management** — creating environments, environment routing, trial-environment expiry (30 days) and conversion to production, and the lifecycle operations Copilot Studio supports (back up and restore, copy, reset, delete, recover; *move* isn't supported).
- **Power Platform administration basics** — a guided tour of the Power Platform admin center: environments, tenant settings (for example the Copilot Studio authors security-group setting), data policies, managed environments, and Copilot Credit capacity views. 💳 **Licensing/Region:** several controls depend on licensing and Managed Environments.

> [!TIP]
> Keep the [Glossary](../GLOSSARY.md) open while you study — terms such as *environment*, *Dataverse*, *connector*, and *solution* are defined there.

## Planned hands-on lab

**Lab: Map the Power Platform building blocks Copilot Studio uses (environments, Dataverse, connectors, solutions, security roles)**

After the lab you will have:

- An inventory of the environments you can access, recording each one's type, region, and whether it has a Dataverse database.
- A record of your own security roles in a chosen environment, with a note on what each role allows.
- A short list of connectors you'd expect an agent to use, classified as standard, premium, or custom, with a prediction of how a data policy might treat them.
- An unmanaged solution created (or an existing one inspected) to show where Copilot Studio agents and components are stored for application lifecycle management.
- A one-page "platform map" that links each building block to the Copilot Studio feature that depends on it.

**What you need:**

- A work or school account and access to at least one Power Platform environment. A trial environment is fine; read-only access to the Power Platform admin center helps, and admin-only steps are marked "observe only".
- A Copilot Studio trial license is sufficient. The trial license lets you create and test agents but **can't publish** them — this lab doesn't publish anything.
- No Copilot Credits are consumed: the lab inspects the platform and doesn't build or test an agent.
- If you planned to use a Power Apps Developer Plan environment, read the deprecation note above and ask your admin for a managed developer environment or use a trial environment instead.

## Planned assessment

`ASSESSMENT.md` will follow the course-wide 24-item pattern, and `ANSWERS.md` will provide correct answers, detailed explanations (including why incorrect options are wrong), expected practical outcomes, and rubrics.

| Item type | Count | Planned focus for this module |
|---|---|---|
| Multiple-choice questions | 10 | Environment types, Dataverse basics, connector tiers, solution types, role scopes |
| True/false questions | 5 | Rules such as "an environment can have more than one Dataverse database" |
| Short-answer questions | 5 | Why production agents belong in a non-default production environment, managed vs unmanaged |
| Practical implementation tasks | 2 | Build an environment inventory; create an unmanaged solution and explain the managed export path |
| Real-world scenario challenge | 1 | Propose development, test, and production environments, roles, and a solution flow for an HR agent |
| Troubleshooting challenge | 1 | "My environment doesn't appear in Copilot Studio" — diagnose missing database, unsupported region, or permissions |
| **Total** | **24** | |

**Grading bands:** 0–59% Beginner · 60–74% Intermediate · 75–89% Advanced · 90–100% Professional Ready.

## Files in this module

| File | Purpose | Status |
|---|---|---|
| `README.md` | Syllabus: objectives, topics, lab outline, assessment plan (this file) | ✅ Syllabus |
| `CONCEPTS.md` | Full lessons for every topic using the course teaching sequence (what, why, how, when, configuration, example, enterprise scenario, mistakes, troubleshooting) | 🔜 Planned |
| `STEP-BY-STEP-LAB.md` | Guided lab with numbered steps and checkpoints | 🔜 Planned |
| `EXAMPLES.md` | Worked examples and enterprise scenarios | 🔜 Planned |
| `ASSESSMENT.md` | 24-item module assessment | 🔜 Planned |
| `ANSWERS.md` | Answers, explanations, and rubrics | 🔜 Planned |
| `INTERVIEW-QUESTIONS.md` | Interview questions with model answers | 🔜 Planned |
| `COMMON-MISTAKES.md` | Common mistakes, symptoms, and fixes | 🔜 Planned |

## Key official documentation

- [Power Platform environments overview](https://learn.microsoft.com/en-us/power-platform/admin/environments-overview)
- [Work with Power Platform environments in Copilot Studio](https://learn.microsoft.com/en-us/microsoft-copilot-studio/environments-first-run-experience)
- [What is Microsoft Dataverse?](https://learn.microsoft.com/en-us/power-apps/maker/data-platform/data-platform-intro)
- [Connectors overview](https://learn.microsoft.com/en-us/connectors/overview)
- [Solution concepts with Power Platform](https://learn.microsoft.com/en-us/power-platform/alm/solution-concepts-alm)
- [Role-based security roles for Dataverse](https://learn.microsoft.com/en-us/power-platform/admin/database-security)
- [Power Platform administration documentation](https://learn.microsoft.com/en-us/power-platform/admin/admin-documentation)
- [Data policies (Power Platform)](https://learn.microsoft.com/en-us/power-platform/admin/wp-data-loss-prevention)

## Navigation

⬅️ [Module 01 — Introduction to Microsoft Copilot Studio](../01-Introduction-to-Copilot-Studio/README.md) | 🗺️ [Course roadmap](../COURSE-ROADMAP.md) | 📈 [Learning progress](../LEARNING-PROGRESS.md) | ➡️ [Module 03 — Environment Setup](../03-Environment-and-Setup/README.md)

## References

- https://learn.microsoft.com/en-us/power-platform/admin/environments-overview
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/environments-first-run-experience
- https://learn.microsoft.com/en-us/power-apps/maker/data-platform/data-platform-intro
- https://learn.microsoft.com/en-us/connectors/overview
- https://learn.microsoft.com/en-us/power-platform/alm/solution-concepts-alm
- https://learn.microsoft.com/en-us/power-platform/admin/database-security
- https://learn.microsoft.com/en-us/power-platform/admin/admin-documentation
- https://learn.microsoft.com/en-us/power-platform/admin/wp-data-loss-prevention

_Last verified against Microsoft Learn: 18 November 2026._
