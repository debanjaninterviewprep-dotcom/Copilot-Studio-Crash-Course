# Module 03 — Environment Setup

> [!NOTE]
> **Status: 🔜 Planned.** This syllabus is published; the full lesson files are developed in Step 5 of the [course build plan](../COURSE-ROADMAP.md).

Before you build anything, you need the right access, the right license, and the right environment. This module walks you through getting into Copilot Studio and preparing a safe place to build — and explains how your choice of harness changes what you pay for and when.

## At a glance

| Item | Details |
|---|---|
| **Level** | Beginner |
| **Estimated time** | 3 hours |
| **Prerequisites** | [Module 02 — Power Platform Fundamentals](../02-Power-Platform-Fundamentals/README.md) |
| **Harness focus** | Both experiences — the new experience (Microsoft Copilot harness) and the classic experience (standard harness) — plus the licensing and Copilot Credit implications of each. |
| **Lab** | Prepare a development environment |

## Why this module matters

**For beginners:** most "it doesn't work" moments in the first week come from setup — signing in with a personal account, building in the wrong environment, an environment that has no Dataverse database, or a trial license that can't publish. Getting setup right once saves hours of confusion later.

**For the enterprise:** environment and licensing decisions are cost and compliance decisions. Agents on the standard harness start billing after they're published, while agents on the Microsoft Copilot harness consume Copilot Credits from the moment you start building, previewing, and evaluating. A professional maker knows which environment, license, and harness a project needs before writing the first instruction.

## Learning objectives

By the end of this module you will be able to:

1. **Sign in** to Copilot Studio with a supported browser and a work or school account, and **explain** why a trial sign-up with a personal email address can be rejected.
2. **Compare** the ways to get access — Copilot Studio user license, the Copilot Studio authors security-group setting (pay-as-you-go), a Microsoft 365 Copilot license, and the trial license — and **state** what each allows.
3. **Explain** how Copilot Credits are consumed on the standard harness (after publish) versus the Microsoft Copilot harness (from the start of building).
4. **Select** an appropriate environment for course work and **justify** why production agents belong in a non-default production environment.
5. **Verify** the Dataverse and regional prerequisites that make an environment visible in Copilot Studio.
6. **Check** your security permissions in an environment and **describe** how an admin grants access when you don't have it.
7. **Configure** the initial settings for your workspace: environment, experience (new or classic), solution and publisher, and primary language.
8. **Document** a development environment profile (type, region, release cycle, Dataverse, credit allocation) for your team.

## Topics covered

- **Copilot Studio access** — signing in to Copilot Studio in the browser (Edge or Chrome 122+, Firefox 127+, Safari 17+), signing up for a trial as an individual, and what to do if your admin has turned off self-service sign-up.
- **Licensing and prerequisites** — the access options on Learn: Copilot Studio user license (free, but the tenant needs a prepaid Copilot Credit pack subscription), the **Copilot Studio authors** security-group setting for pay-as-you-go, a Microsoft 365 Copilot license (lets users build agents for the Microsoft Copilot harness), and the trial license. 💳 **Licensing/Region:** Copilot Credits are the common currency (since 1 September 2025); Copilot Studio is also available in US Government Community Cloud (GCC) with its own considerations.
  - The **trial license** lets you create and test agents but **can't publish** them. When a trial expires you can extend it by 30 days, and agents keep working for up to 90 days after expiry.
  - **Microsoft Copilot harness** agents use usage-based billing: building with natural language, previewing, testing, and evaluating all consume Copilot Credits. **Standard harness** agents bill after publish.
- **Developer environment** — choosing a safe, non-production place to build: trial environments (expire after 30 days, one per user, convertible to production) and developer environments.
  - ⚠️ **Deprecated:** unmanaged developer environments created through the Power Apps Developer Plan. New ones can't be created from 15 November 2026 and existing ones are suspended from 15 December 2026; ask your admin for a *managed* developer environment (one per user) instead.
- **Environment selection** — using the environment picker (it lists environments where you can create agents or workflows), why the default environment suits experimentation but not production, and why the **Microsoft Copilot Chat** environment doesn't appear in Copilot Studio and shouldn't be used to build agents.
- **Dataverse prerequisites** — why an environment needs a Dataverse database (and a supported region) before Copilot Studio lists it, and how an admin adds a database.
- **Security permissions** — environment access, the roles that let you create agents (Learn's environment article walks through assigning the *agent author* security role), and how to read the "You don't have permissions to any environments" error.
- **Initial configuration** — switching between the new experience and the classic experience (Home → **…** at the bottom of the side bar → **Open classic experience**, which applies to the current session only), using **Other ways to build** for standard-harness agents, and setting primary language, solution, and schema name at creation time (some of these become read-only after the first save).
- **Understanding the development environment** — what lives in an environment (agents, flows, connections, Dataverse data), how development, test, and production environments relate, and how release-cycle settings matter: some 🧪 **Preview** capabilities (for example MCP and A2A client channels) are available only in early release cycle environments.

## Planned hands-on lab

**Lab: Prepare a development environment**

After the lab you will have:

- Signed in to Copilot Studio with a supported browser and confirmed which access path (trial, user license, pay-as-you-go, or Microsoft 365 Copilot) your account uses.
- Selected — or requested from your admin — a non-default environment that has a Dataverse database in a supported region.
- Confirmed your security permissions in that environment and resolved (or documented) any access errors.
- Created a solution and publisher for all course work so every later lab is ALM-ready.
- Opened both the new experience and the classic experience and located **Other ways to build**.
- Completed a one-page environment profile: type, region, release cycle, Dataverse status, and where Copilot Credit consumption is reported.

**What you need:**

- A work or school account (Learn notes that trial sign-ups with a personal email address can be rejected).
- A Copilot Studio trial or paid access. A trial lets you create and test agents, but it **can't publish**; any lab step that publishes needs a non-trial license path.
- An environment you're allowed to build in, or an admin who can create one or grant you access.
- Awareness of cost: this lab doesn't build or test agents, so it doesn't consume Copilot Credits. In later labs, anything you build or test on the **Microsoft Copilot harness** consumes credits even before publishing.

## Planned assessment

`ASSESSMENT.md` will follow the course-wide 24-item pattern, and `ANSWERS.md` will provide correct answers, detailed explanations (including why incorrect options are wrong), expected practical outcomes, and rubrics.

| Item type | Count | Planned focus for this module |
|---|---|---|
| Multiple-choice questions | 10 | Access options, trial limits, environment types, billing start points per harness |
| True/false questions | 5 | Statements such as "a trial license can publish to a demo website" |
| Short-answer questions | 5 | Why a production agent shouldn't live in the default environment; what happens when a trial environment expires |
| Practical implementation tasks | 2 | Prepare and document a development environment; create a course solution and publisher |
| Real-world scenario challenge | 1 | Recommend an access and environment setup for a five-person maker team with a fixed credit budget |
| Troubleshooting challenge | 1 | A maker sees "You don't have permissions to any environments" — diagnose and fix |
| **Total** | **24** | |

**Grading bands:** 0–59% Beginner · 60–74% Intermediate · 75–89% Advanced · 90–100% Professional Ready.

## Files in this module

| File | Purpose | Status |
|---|---|---|
| `README.md` | Syllabus: objectives, topics, lab outline, assessment plan (this file) | ✅ Syllabus |
| `CONCEPTS.md` | Full lessons for every topic using the course teaching sequence | 🔜 Planned |
| `STEP-BY-STEP-LAB.md` | Guided lab with numbered steps and checkpoints | 🔜 Planned |
| `EXAMPLES.md` | Worked examples and enterprise setup scenarios | 🔜 Planned |
| `ASSESSMENT.md` | 24-item module assessment | 🔜 Planned |
| `ANSWERS.md` | Answers, explanations, and rubrics | 🔜 Planned |
| `INTERVIEW-QUESTIONS.md` | Interview questions with model answers | 🔜 Planned |
| `COMMON-MISTAKES.md` | Common mistakes, symptoms, and fixes | 🔜 Planned |

## Key official documentation

- [Get access to Copilot Studio](https://learn.microsoft.com/en-us/microsoft-copilot-studio/requirements-licensing-subscriptions)
- [Standard harness licensing](https://learn.microsoft.com/en-us/microsoft-copilot-studio/billing-licensing)
- [Overview of usage-based billing (Microsoft Copilot harness)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/billing-credit-overview)
- [Assign licenses and manage access to Copilot Studio](https://learn.microsoft.com/en-us/microsoft-copilot-studio/requirements-licensing)
- [Work with Power Platform environments](https://learn.microsoft.com/en-us/microsoft-copilot-studio/environments-first-run-experience)
- [Create a developer environment with the Power Apps Developer Plan](https://learn.microsoft.com/en-us/power-platform/developer/create-developer-environment)
- [Access standard harness agents and agent flows](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/switch-experiences)
- [Start building in Copilot Studio](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/authoring-first-bot)

## Navigation

⬅️ [Module 02 — Power Platform Fundamentals](../02-Power-Platform-Fundamentals/README.md) | 🗺️ [Course roadmap](../COURSE-ROADMAP.md) | 📈 [Learning progress](../LEARNING-PROGRESS.md) | ➡️ [Module 04 — Complete Copilot Studio Interface](../04-Copilot-Studio-Interface/README.md)

## References

- https://learn.microsoft.com/en-us/microsoft-copilot-studio/requirements-licensing-subscriptions
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/billing-licensing
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/billing-credit-overview
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/requirements-licensing
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/environments-first-run-experience
- https://learn.microsoft.com/en-us/power-platform/developer/create-developer-environment
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/switch-experiences
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/authoring-first-bot

_Last verified against Microsoft Learn: 18 November 2026._
