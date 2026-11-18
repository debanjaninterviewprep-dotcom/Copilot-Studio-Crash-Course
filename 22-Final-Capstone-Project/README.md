# Module 22 — Final Capstone Project

> [!NOTE]
> **Status: 🔜 Planned.** This syllabus is published; the full lesson files are developed in Step 11 of the [course build plan](../COURSE-ROADMAP.md).

The capstone is where you prove you can work as a Copilot Studio professional. You'll design, build, secure, publish, test, monitor, and document a complete enterprise-grade agent for a realistic business scenario, and it will be scored against published, weighted criteria.

## At a glance

| Item | Details |
|---|---|
| **Level** | Professional |
| **Estimated time** | 15 hours |
| **Prerequisites** | [Module 01](../01-Introduction-to-Copilot-Studio/README.md) through [Module 21](../21-Interview-Preparation/README.md) |
| **Harness focus** | You specify and justify the harness. Because the capstone requires topics and variables, the core agent is built on the standard harness; a separately justified Microsoft Copilot harness component is an optional extension. |
| **Lab** | Enterprise-grade capstone agent with scored evaluation |

## Why this module matters

**For learners:** the capstone pulls every skill together under realistic constraints — incomplete requirements, security rules, budgets, and stakeholders — exactly the conditions you'll face on the job. Completing it end to end is the clearest evidence that you can take an agent from idea to production.

**For the enterprise and your career:** a scored capstone with a requirements document, architecture, test evidence, analytics plan, and handover documentation is a portfolio piece that demonstrates professional judgment, not just feature knowledge. The scoring model mirrors how organizations review agents before production.

## Learning objectives

By the end of this module you will be able to:

1. **Analyze** a business scenario and **write** a requirements document with measurable success criteria.
2. **Design** an agent architecture, **select** the harness, and **justify** every major decision, including preview-feature risks.
3. **Build** topics, variables, knowledge, generative orchestration, and tools that work together reliably.
4. **Secure** the agent with appropriate authentication, permissions, data policies, and responsible AI controls.
5. **Publish** the agent to a suitable channel and **validate** the deployment.
6. **Test** the agent with evaluation test sets, regression runs, and user acceptance criteria.
7. **Define** analytics KPIs and **use** monitoring data to drive an improvement.
8. **Document** and **present** the solution so another team could operate and extend it.

## Topics covered

Every capstone must address all thirteen curriculum requirements:

- **Business scenario** — choose an approved scenario (or propose one) with a real business problem, users, and constraints.
- **Requirements document** — scope, personas, use cases, non-functional requirements (security, privacy, availability, cost), and success criteria.
- **Agent architecture** — harness choice and justification, components, integrations, environments, and diagrams.
- **Knowledge configuration** — sources, descriptions, permissions, grounding settings, and content-maintenance plan.
- **Topics** — custom and system topics for deterministic paths, fallback, escalation, and error handling. *Applies to: standard harness.*
- **Variables** — topic, global, system, and environment variables plus entities and validation for the data the agent collects. *Applies to: standard harness.*
- **Generative orchestration** — instructions and descriptions that let the agent combine topics, knowledge, and tools for multi-intent requests.
- **Tools where appropriate** — connectors, agent flows, or other available tools with deliberate credentials and confirmation rules.
- **Security** — authentication, sharing, data policy impact, data privacy, and a responsible AI review.
- **Publishing** — channel selection and configuration, deployment validation, and a release plan.
- **Testing** — evaluation test sets, regression results, troubleshooting evidence, and user acceptance sign-off.
- **Analytics** — KPIs, a monitoring plan, transcript-review process, and at least one data-driven improvement.
- **Documentation** — architecture decision records, administrator runbook, user guide, and handover notes.

### Planned scoring outline

The capstone is scored out of 100%. Each criterion is rated **Exemplary** (100% of its weight), **Proficient** (75%), **Developing** (50%), or **Missing** (0%).

| # | Criterion | Weight | What earns full marks |
|---|---|---|---|
| 1 | Business scenario and requirements document | 10% | Clear problem, personas, scope, and measurable success criteria |
| 2 | Agent architecture | 10% | Justified harness choice, coherent components, diagrams, and preview risks identified |
| 3 | Knowledge configuration | 10% | Right sources, permission-aware retrieval, grounding settings, and citations verified |
| 4 | Topics | 10% | Deterministic paths, fallback, escalation, and error handling that are tested |
| 5 | Variables | 5% | Correct scopes and types, entities, validation, and data passed between topics |
| 6 | Generative orchestration | 10% | Precise instructions and descriptions; multi-intent requests handled and traced |
| 7 | Tools where appropriate | 5% | Appropriate tools, inputs and outputs, credentials, and confirmations |
| 8 | Security | 10% | Suitable authentication, least-privilege sharing, data policy fit, and responsible AI review |
| 9 | Publishing | 5% | Agent published to a suitable channel with deployment validation completed |
| 10 | Testing | 10% | Evaluation test sets, regression evidence, and user acceptance sign-off |
| 11 | Analytics | 5% | KPIs defined, monitoring plan in place, and one improvement driven by data |
| 12 | Documentation | 10% | Decision records, runbook, user guide, and handover that another team can use |
| | **Total** | **100%** | |

**Mapping to grading bands:**

| Score | Band | Meaning for the capstone |
|---|---|---|
| 0–59% | Beginner | Not yet ready — address the gaps and resubmit |
| 60–74% | Intermediate | Working agent, but significant gaps in design, security, or evidence |
| 75–89% | Advanced | Production-capable with minor gaps |
| 90–100% | Professional Ready | Enterprise-grade and ready for real deployment |

> [!IMPORTANT]
> To be rated **Professional Ready**, a capstone also needs **no criterion rated Missing** and **no unresolved security finding**, regardless of the total score.

## Planned hands-on lab

**Lab: Enterprise-grade capstone agent with scored evaluation**

After the lab you will have:

- A complete requirements document and architecture for your chosen scenario, including a harness decision record.
- A working standard-harness agent with topics, variables, knowledge, generative orchestration, and tools where appropriate.
- A secured agent published to at least one suitable channel, with deployment validation evidence.
- Evaluation results, regression evidence, and a user acceptance sign-off.
- An analytics plan and at least one documented, data-driven improvement.
- A full documentation pack and a recorded or live presentation, scored against the outline above.

**What you need:**

- A license path that **can publish** — the trial license **can't publish** — plus development and test environments, sample knowledge content, and Teams or another supported channel.
- Admin support for data policies, sharing, and transcript access (the **Bot Transcript Viewer** role).
- 💳 Any optional Microsoft Copilot harness component consumes Copilot Credits from the moment you start building, previewing, and evaluating, and it can't be invoked directly by the standard-harness agent.

## Planned assessment

`ASSESSMENT.md` will follow the course-wide 24-item pattern (used as a capstone defense), and `ANSWERS.md` will provide correct answers, detailed explanations (including why incorrect options are wrong), expected practical outcomes, and rubrics. The capstone itself is scored with the outline above.

| Item type | Count | Planned focus for this module |
|---|---|---|
| Multiple-choice questions | 10 | Cross-course decisions applied to your capstone |
| True/false questions | 5 | Feature-status and harness-applicability statements relevant to capstone designs |
| Short-answer questions | 5 | Defend key architecture, security, and testing decisions |
| Practical implementation tasks | 2 | Live change to the capstone agent; add a test case and rerun the evaluation |
| Real-world scenario challenge | 1 | A stakeholder changes a requirement late — re-plan scope, design, and release |
| Troubleshooting challenge | 1 | Diagnose a seeded production issue in your capstone agent |
| **Total** | **24** | |

**Grading bands:** 0–59% Beginner · 60–74% Intermediate · 75–89% Advanced · 90–100% Professional Ready.

## Files in this module

| File | Purpose | Status |
|---|---|---|
| `README.md` | Syllabus: requirements, scoring outline, lab outline, assessment plan (this file) | ✅ Syllabus |
| `CONCEPTS.md` | Capstone delivery method, templates, and scenario options | 🔜 Planned |
| `STEP-BY-STEP-LAB.md` | Milestone-by-milestone capstone guide with checkpoints | 🔜 Planned |
| `EXAMPLES.md` | Example requirements, architecture records, and documentation | 🔜 Planned |
| `ASSESSMENT.md` | 24-item capstone defense plus the detailed scoring rubric | 🔜 Planned |
| `ANSWERS.md` | Answers, explanations, and rubric guidance | 🔜 Planned |
| `INTERVIEW-QUESTIONS.md` | Capstone-based interview questions with model answers | 🔜 Planned |
| `COMMON-MISTAKES.md` | Common capstone mistakes, symptoms, and fixes | 🔜 Planned |

## Key official documentation

- [Define project objectives and success criteria](https://learn.microsoft.com/en-us/microsoft-copilot-studio/guidance/project-best-practices)
- [Design effective agents using a structured design framework](https://learn.microsoft.com/en-us/microsoft-copilot-studio/guidance/agent-design-canvas-overview)
- [Orchestrate agent behavior with generative AI](https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-generative-actions)
- [Knowledge sources summary](https://learn.microsoft.com/en-us/microsoft-copilot-studio/knowledge-copilot-studio)
- [Security and governance](https://learn.microsoft.com/en-us/microsoft-copilot-studio/security-and-governance)
- [Key concepts - Publish and deploy your agent](https://learn.microsoft.com/en-us/microsoft-copilot-studio/publication-fundamentals-publish-channels)
- [About agent evaluation](https://learn.microsoft.com/en-us/microsoft-copilot-studio/analytics-agent-evaluation-intro)
- [Monitor agent performance in Copilot Studio](https://learn.microsoft.com/en-us/microsoft-copilot-studio/analytics-overview)

## Navigation

⬅️ [Module 21 — Interview Preparation](../21-Interview-Preparation/README.md) | 🗺️ [Course roadmap](../COURSE-ROADMAP.md) | 📈 [Learning progress](../LEARNING-PROGRESS.md) | ➡️ [Course README](../README.md)

## References

- https://learn.microsoft.com/en-us/microsoft-copilot-studio/guidance/project-best-practices
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/guidance/agent-design-canvas-overview
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-generative-actions
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/knowledge-copilot-studio
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/security-and-governance
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/publication-fundamentals-publish-channels
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/analytics-agent-evaluation-intro
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/analytics-overview

_Last verified against Microsoft Learn: 18 November 2026._
