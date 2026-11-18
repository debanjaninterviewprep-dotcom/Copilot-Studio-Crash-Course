# Module 16 — Analytics and Monitoring

> [!NOTE]
> **Status: 🔜 Planned.** This syllabus is published; the full lesson files are developed in Step 8 of the [course build plan](../COURSE-ROADMAP.md).

Publishing is the start of an agent's life, not the end. This module teaches you to read the **Monitor** page — conversation and session metrics, resolution and escalation rates, user feedback, and transcripts — and to turn those insights into a continuous improvement loop on both harnesses.

## At a glance

| Item | Details |
|---|---|
| **Level** | Advanced |
| **Estimated time** | 4 hours |
| **Prerequisites** | [Module 15 — Testing and Debugging](../15-Testing-and-Debugging/README.md) |
| **Harness focus** | Both, with per-harness differences — the standard harness **Monitor** page focuses on outcomes, satisfaction, and usage; the Microsoft Copilot harness **Monitor** tab focuses on sessions, success rate, reactions, and Copilot Credit consumption. |
| **Lab** | Analyze an agent and improve its performance |

## Why this module matters

**For beginners:** analytics answers the questions every agent owner gets asked — *Is anyone using it? Does it help? Where does it fail?* Learning where those answers live, and what each metric really means, keeps you from guessing.

**For the enterprise:** agents need operational ownership like any production service. Leaders want adoption and resolution trends, support teams want escalation insights, finance wants credit consumption, and compliance wants controlled access to transcripts. A professional builds an evidence-based improvement cycle — measure, diagnose, change, verify — and reports on it.

## Learning objectives

By the end of this module you will be able to:

1. **Navigate** the **Monitor** page in both experiences and **explain** what each section shows.
2. **Interpret** conversation and session metrics, including engaged versus unengaged sessions and how sessions time out.
3. **Calculate** and **explain** resolution, escalation, and abandonment outcomes, including their sub-types.
4. **Identify** unanswered or poorly answered questions using usage data, themes, and question lists.
5. **Analyze** user feedback — reactions, comments, satisfaction (CSAT), and sentiment.
6. **Monitor** performance and reliability, including tool and knowledge use, autonomous runs, and Copilot Credit consumption.
7. **Review** transcripts with the correct permissions and within documented retention windows.
8. **Prioritize**, **implement**, and **verify** improvements in a continuous optimization loop.

## Topics covered

- **Analytics dashboard** — the **Monitor** page (formerly labeled *Analytics*) in the classic experience: AI-generated summary, overview KPIs, savings, effectiveness, and use sections; and the **Monitor** tab in the new experience. Monitor data covers up to 360 days, timestamps are in UTC, and test-panel activity isn't included.
- **Conversation metrics** — conversations versus analytics sessions, the 30-minute inactivity timeout, engaged and unengaged sessions, and the hybrid view for agents with both conversations and event-triggered runs.
- **Session metrics** — total sessions, active users (daily and monthly, which require authentication), average duration, and success rate; on the Microsoft Copilot harness, sessions also show the credits they consumed.
- **Resolution rates** — *Resolved confirmed* versus *Resolved implied* outcomes, and how they're determined under classic and generative orchestration.
- **Escalation rates** — *System intended*, *System unintended*, and *User requested* escalations, and how the Escalate topic or a transfer node ends an analytics session.
- **Unanswered questions** — finding questions the agent couldn't answer well through the **Use** section, user question lists, drill-down data, and themes of user questions (🧪 **Preview**).
- **User feedback** — thumbs-up/down reactions and comments (on by default for most channels; the Microsoft Copilot channel requires admin consent to share feedback), CSAT scores, customer comments summary (🧪 **Preview**), and session sentiment (🧪 **Preview**).
- **Performance monitoring** — tool and knowledge-source usage, child and connected agent success rates, autonomous agent health, Copilot Credit consumption, and telemetry in Azure Application Insights at agent level or environment level (🧪 **Preview**).
- **Conversation transcripts** — downloading session data for the last 28 days, the **Bot Transcript Viewer** role, the **Analytics Viewer** sharing role for view-only access, admin transcript controls, and transcripts stored in Dataverse.
- **Agent improvement** — turning findings into concrete changes to knowledge, descriptions, instructions, topics, and tools, and verifying them with evaluations.
- **Continuous optimization** — a recurring review cadence, custom metrics for business-specific outcomes (🧪 **Preview**), time and cost savings, and reporting trends to stakeholders.

## Planned hands-on lab

**Lab: Analyze an agent and improve its performance**

After the lab you will have:

- Generated real analytics sessions by publishing an agent to a pilot channel and running a scripted set of conversations with colleagues (test-panel conversations don't appear on the **Monitor** page).
- Read and recorded the agent's overview KPIs, conversation outcomes, escalation types, and feedback for a defined period.
- Drilled into sessions and transcripts (with the required role) to diagnose the top three improvement opportunities.
- Implemented targeted fixes and verified them with an evaluation run and a follow-up review period.
- Optionally defined a custom metric (🧪 **Preview**) or reviewed telemetry in Application Insights.
- Written a one-page performance report with before-and-after evidence.

**What you need:**

- A license path that **can publish** (the trial license **can't publish**) and a pilot channel such as Teams or the demo website.
- The **Bot Transcript Viewer** security role, granted by an admin, to read transcripts; Microsoft authentication on the agent to see active-user metrics.
- 💳 If you monitor a **Microsoft Copilot harness** agent, its usage — including preview testing and evaluations — consumes Copilot Credits, which the **Monitor** tab reports.

## Planned assessment

`ASSESSMENT.md` will follow the course-wide 24-item pattern, and `ANSWERS.md` will provide correct answers, detailed explanations (including why incorrect options are wrong), expected practical outcomes, and rubrics.

| Item type | Count | Planned focus for this module |
|---|---|---|
| Multiple-choice questions | 10 | Session states, outcome types, retention windows, roles, per-harness Monitor content |
| True/false questions | 5 | Statements such as "active-user metrics work without authentication" |
| Short-answer questions | 5 | Resolved confirmed vs implied; why test-panel sessions aren't in analytics |
| Practical implementation tasks | 2 | Produce a KPI snapshot from Monitor; diagnose one escalation pattern from transcripts |
| Real-world scenario challenge | 1 | Build a monthly agent performance review for a service desk leadership team |
| Troubleshooting challenge | 1 | Monitor shows no data after go-live — check publishing, channel, period, authentication, and roles |
| **Total** | **24** | |

**Grading bands:** 0–59% Beginner · 60–74% Intermediate · 75–89% Advanced · 90–100% Professional Ready.

## Files in this module

| File | Purpose | Status |
|---|---|---|
| `README.md` | Syllabus: objectives, topics, lab outline, assessment plan (this file) | ✅ Syllabus |
| `CONCEPTS.md` | Full lessons for every topic using the course teaching sequence | 🔜 Planned |
| `STEP-BY-STEP-LAB.md` | Guided analysis-and-improvement lab with checkpoints | 🔜 Planned |
| `EXAMPLES.md` | Metric interpretation examples and improvement reports | 🔜 Planned |
| `ASSESSMENT.md` | 24-item module assessment | 🔜 Planned |
| `ANSWERS.md` | Answers, explanations, and rubrics | 🔜 Planned |
| `INTERVIEW-QUESTIONS.md` | Interview questions with model answers | 🔜 Planned |
| `COMMON-MISTAKES.md` | Common mistakes, symptoms, and fixes | 🔜 Planned |

## Key official documentation

- [Monitor agent performance in Copilot Studio](https://learn.microsoft.com/en-us/microsoft-copilot-studio/analytics-overview)
- [Monitor conversational agent effectiveness](https://learn.microsoft.com/en-us/microsoft-copilot-studio/analytics-improve-agent-effectiveness)
- [Monitor autonomous agent health](https://learn.microsoft.com/en-us/microsoft-copilot-studio/analytics-improve-agent-health)
- [Explore user questions, session, and feedback data](https://learn.microsoft.com/en-us/microsoft-copilot-studio/analytics-questions-sessions)
- [Monitor with custom metrics (preview)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/analytics-custom-metrics)
- [Understand downloaded session data from Copilot Studio](https://learn.microsoft.com/en-us/microsoft-copilot-studio/analytics-transcripts-studio)
- [Monitor agent performance overview (Microsoft Copilot harness)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/analytics-overview)
- [Telemetry with Application Insights overview](https://learn.microsoft.com/en-us/microsoft-copilot-studio/telemetry-overview)

## Navigation

⬅️ [Module 15 — Testing and Debugging](../15-Testing-and-Debugging/README.md) | 🗺️ [Course roadmap](../COURSE-ROADMAP.md) | 📈 [Learning progress](../LEARNING-PROGRESS.md) | ➡️ [Module 17 — Agent Management and Governance](../17-Agent-Management-and-Governance/README.md)

## References

- https://learn.microsoft.com/en-us/microsoft-copilot-studio/analytics-overview
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/analytics-improve-agent-effectiveness
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/analytics-improve-agent-health
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/analytics-questions-sessions
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/analytics-custom-metrics
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/analytics-transcripts-studio
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/analytics-overview
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/telemetry-overview

_Last verified against Microsoft Learn: 18 November 2026._
