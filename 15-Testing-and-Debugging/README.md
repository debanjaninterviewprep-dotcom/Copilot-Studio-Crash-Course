# Module 15 — Testing and Debugging

> [!NOTE]
> **Status: 🔜 Planned.** This syllabus is published; the full lesson files are developed in Step 7 of the [course build plan](../COURSE-ROADMAP.md).

Professional agents are tested systematically, not just "tried out". This module teaches you to test conversations, inspect topics and variables, debug generative orchestration, knowledge, tools, and authentication, read transcripts, and build repeatable regression and user acceptance testing — on both harnesses.

## At a glance

| Item | Details |
|---|---|
| **Level** | Advanced |
| **Estimated time** | 5 hours |
| **Prerequisites** | [Module 14 — Publishing and Channels](../14-Publishing-and-Channels/README.md) |
| **Harness focus** | Both, with per-harness differences — the standard harness uses the **Test your agent** panel, activity map, and Evaluation page; the Microsoft Copilot harness uses the **Preview** and **Evaluate** tabs, where testing consumes Copilot Credits. |
| **Lab** | Debug a deliberately misconfigured agent |

## Why this module matters

**For beginners:** most agent bugs fall into a handful of patterns — the wrong topic fires, a variable is empty, knowledge returns nothing, a tool fails, or sign-in breaks. Learning where to look for each pattern turns hours of guessing into minutes of diagnosis.

**For the enterprise:** generative behavior isn't fully deterministic, so a change that fixes one answer can break another. Repeatable test sets, regression runs after every change, transcript reviews, and formal user acceptance testing are what let organizations release agents with confidence and prove quality to stakeholders and auditors.

## Learning objectives

By the end of this module you will be able to:

1. **Use** the classic **Test your agent** panel and the new-experience **Preview** tab to run and reset test conversations.
2. **Debug** topics by tracking between topics, following responses back to nodes, and using the topic checker.
3. **Inspect** variable values during testing and **diagnose** type and scope problems.
4. **Analyze** generative orchestration plans with the activity map (standard harness) and the activity trace (Microsoft Copilot harness).
5. **Troubleshoot** knowledge, tool, and authentication failures using Learn's diagnostic steps and error codes.
6. **Interpret** conversation transcripts and conversation snapshots, and **handle** them as potentially sensitive data.
7. **Design** test scenarios and **build** single-response and conversational (multi-turn) evaluation test sets for regression testing.
8. **Plan** and **run** user acceptance testing with clear entry and exit criteria.

## Topics covered

- **Test panel** — the classic **Test your agent** panel (start, reset, **Track between topics**, activity map, save snapshot) and the new **Preview** tab (maker view, end-user preview, activity trace, conversation history, response feedback). 💳 Preview testing on the Microsoft Copilot harness consumes Copilot Credits.
- **Conversation testing** — scripted happy-path, edge-case, and adversarial conversations; testing in a fresh session versus a long-running one, because conversation history affects generative orchestration.
- **Topic debugging** — following a response to the node that sent it, nodes highlighted as they fire, and the **Topic checker** for errors and warnings. *Applies to: standard harness.*
- **Variable inspection** — the **Variables** panel's **Test** tab, variable properties, *unknown* values, and fixing type mismatches. *Applies to: standard harness.*
- **Generative orchestration debugging** — reading real-time activity maps (inputs, outputs, timings, errors), historical activity on the **Activity** page, chain-of-thought views for supported models, and the Microsoft Copilot harness activity trace.
- **Knowledge troubleshooting** — testing knowledge sources, checking authentication and permissions, grounding settings, and Learn's troubleshooting articles for SharePoint and enterprise data.
- **Tool troubleshooting** — missing or invalid inputs, failed connections and connector requests, tools blocked by data policies, and MCP server issues.
- **Authentication issues** — sign-in loops, missing user variables, channel and authentication mismatches, and Conditional Access–related failures.
- **Conversation transcripts** — downloading session transcripts from the **Monitor** page (within the 28-day window), the **Bot Transcript Viewer** role, transcripts in Dataverse, and redactions such as SharePoint-grounded answers; conversation snapshots and their sensitivity.
- **Test scenarios** — writing scenario-based test cases from requirements, including expected responses and expected tool or knowledge use.
- **Regression testing** — agent evaluation on the standard harness (🟢 **GA**): test sets of up to 100 single-response test cases, conversational test sets, test methods, safety evaluators, comparing versions, and automation through a connector or REST API (🧪 **Preview**). On the Microsoft Copilot harness, the **Evaluate** tab is 🧪 **Preview** (production-ready preview).
- **User acceptance testing** — stakeholder testing on the demo website, installing the published agent for yourself before wider release, pilot groups, and sign-off criteria.

## Planned hands-on lab

**Lab: Debug a deliberately misconfigured agent**

After the lab you will have:

- Built (from the lab guide) a standard-harness agent seeded with defects: a topic that never triggers, a variable with the wrong type, a knowledge source that returns nothing for some users, a tool with an invalid input, and an authentication mismatch.
- Located each defect with the test panel, **Track between topics**, the **Variables** panel, the activity map, and the topic checker.
- Fixed and verified every defect, with a written root-cause note for each.
- Created an evaluation test set that covers every fixed defect, and run it before and after the fixes to show the improvement.
- Saved a conversation snapshot and explained what it contains and why it must be handled as sensitive.
- Drafted a user acceptance testing plan with entry and exit criteria.

**What you need:**

- Your course environment and solution; a trial license is enough because the lab doesn't publish (the trial **can't publish**).
- A second test account if available, to reproduce permission-related knowledge failures.
- 💳 Optional: repeating the lab's checks with the **Preview** and **Evaluate** tabs on a **Microsoft Copilot harness** agent consumes Copilot Credits.

## Planned assessment

`ASSESSMENT.md` will follow the course-wide 24-item pattern, and `ANSWERS.md` will provide correct answers, detailed explanations (including why incorrect options are wrong), expected practical outcomes, and rubrics.

| Item type | Count | Planned focus for this module |
|---|---|---|
| Multiple-choice questions | 10 | Debugging tools per harness, evaluation features, transcript access, UAT practices |
| True/false questions | 5 | Statements such as "test-panel conversations appear in Monitor analytics" |
| Short-answer questions | 5 | Read an activity map excerpt; choose between single-response and conversational test sets |
| Practical implementation tasks | 2 | Find and fix a seeded defect; build and run a regression test set |
| Real-world scenario challenge | 1 | Design a release test strategy for a customer-facing agent with weekly content changes |
| Troubleshooting challenge | 1 | The agent doesn't respond in the test panel — work through Learn's diagnostic steps |
| **Total** | **24** | |

**Grading bands:** 0–59% Beginner · 60–74% Intermediate · 75–89% Advanced · 90–100% Professional Ready.

## Files in this module

| File | Purpose | Status |
|---|---|---|
| `README.md` | Syllabus: objectives, topics, lab outline, assessment plan (this file) | ✅ Syllabus |
| `CONCEPTS.md` | Full lessons for every topic using the course teaching sequence | 🔜 Planned |
| `STEP-BY-STEP-LAB.md` | Guided debugging lab with seeded defects and checkpoints | 🔜 Planned |
| `EXAMPLES.md` | Annotated debugging sessions and test-set examples | 🔜 Planned |
| `ASSESSMENT.md` | 24-item module assessment | 🔜 Planned |
| `ANSWERS.md` | Answers, explanations, and rubrics | 🔜 Planned |
| `INTERVIEW-QUESTIONS.md` | Interview questions with model answers | 🔜 Planned |
| `COMMON-MISTAKES.md` | Common mistakes, symptoms, and fixes | 🔜 Planned |

## Key official documentation

- [Test your agent (standard harness)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-test-bot)
- [Review agent activity](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-review-activity)
- [Preview and test an agent (Microsoft Copilot harness)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/preview-overview)
- [About agent evaluation](https://learn.microsoft.com/en-us/microsoft-copilot-studio/analytics-agent-evaluation-intro)
- [Create a single response test set](https://learn.microsoft.com/en-us/microsoft-copilot-studio/analytics-agent-evaluation-create)
- [Create a conversational test set](https://learn.microsoft.com/en-us/microsoft-copilot-studio/analytics-agent-evaluation-multi-turn)
- [Test your agent's knowledge sources](https://learn.microsoft.com/en-us/microsoft-copilot-studio/knowledge-test)
- [Understand error codes (Copilot Studio troubleshooting)](https://learn.microsoft.com/en-us/troubleshoot/power-platform/copilot-studio/authoring/error-codes)

## Navigation

⬅️ [Module 14 — Publishing and Channels](../14-Publishing-and-Channels/README.md) | 🗺️ [Course roadmap](../COURSE-ROADMAP.md) | 📈 [Learning progress](../LEARNING-PROGRESS.md) | ➡️ [Module 16 — Analytics and Monitoring](../16-Analytics-and-Monitoring/README.md)

## References

- https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-test-bot
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-review-activity
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/preview-overview
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/analytics-agent-evaluation-intro
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/analytics-agent-evaluation-create
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/analytics-agent-evaluation-multi-turn
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/knowledge-test
- https://learn.microsoft.com/en-us/troubleshoot/power-platform/copilot-studio/authoring/error-codes

_Last verified against Microsoft Learn: 18 November 2026._
