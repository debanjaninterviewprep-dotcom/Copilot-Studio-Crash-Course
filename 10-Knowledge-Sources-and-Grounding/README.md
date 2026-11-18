# Module 10 — Knowledge Sources and Grounding

> [!NOTE]
> **Status: 🔜 Planned.** This syllabus is published; the full lesson files are developed in Step 6 of the [course build plan](../COURSE-ROADMAP.md).

Knowledge is what makes an agent *your* agent. This module teaches you how to connect websites, SharePoint, files, Dataverse, and Microsoft 365 content, how retrieval-augmented generation grounds answers with citations, how permissions flow through to users, and how to diagnose and fix wrong answers.

## At a glance

| Item | Details |
|---|---|
| **Level** | Intermediate |
| **Estimated time** | 6 hours |
| **Prerequisites** | [Module 09 — Generative AI and Orchestration](../09-Generative-AI-and-Orchestration/README.md) |
| **Harness focus** | Both, with per-harness differences — the standard harness and the Microsoft Copilot harness support different source types, limits, and settings. |
| **Lab** | Build a company knowledge assistant |

## Why this module matters

**For beginners:** an agent without knowledge can only answer from a model's general training. Adding the right knowledge sources — and configuring them well — is usually the biggest single improvement to answer quality, and it's achievable without writing any code.

**For the enterprise:** knowledge is where data governance meets AI. Architects must make sure agents only surface content each user is allowed to see, that answers carry citations users can verify, that admins can restrict which source types makers may add, and that stale or conflicting content doesn't quietly produce wrong answers at scale.

## Learning objectives

By the end of this module you will be able to:

1. **Explain** what knowledge sources are and how retrieval-augmented generation (RAG) grounds an agent's answers.
2. **Add** and **configure** public website, SharePoint, uploaded file, and Dataverse knowledge sources.
3. **Compare** the knowledge sources and limits available on the standard harness and on the Microsoft Copilot harness, including Microsoft 365 sources such as OneDrive and Work IQ.
4. **Configure** user authentication so permission-aware sources only return content the signed-in user can access.
5. **Interpret** citations and **configure** grounding behavior with **Allow ungrounded responses**.
6. **Describe** how knowledge search differs under generative and classic orchestration, including source limits and filtering.
7. **Improve** answer quality through source selection, descriptions, content structure, and metadata.
8. **Troubleshoot** incorrect, missing, or ungrounded answers with a repeatable diagnostic process.

## Topics covered

- **What are knowledge sources?** — content a maker connects at design time so every user gets the same grounding (as opposed to a file a user attaches to one conversation); agent-level knowledge versus topic-level generative answers nodes.
- **Website knowledge** — public websites searched through Bing and filtered to the sites you provide (Learn lists up to 25 websites under generative orchestration and four under classic), URL considerations, and Bing Custom Search for curated web content.
- **SharePoint knowledge** — sites, libraries, and files searched with the signed-in user's Microsoft Entra ID permissions; metadata filters; and why SharePoint-grounded answers are redacted in downloaded transcripts.
- **Uploaded documents** — files uploaded to Dataverse as knowledge, supported formats, file groups, and why uploaded files don't count toward the generative-orchestration source limit.
- **Dataverse knowledge** — grounding in Dataverse tables, classic-mode limits (two sources with up to 15 tables each), and, on the Microsoft Copilot harness, unstructured reasoning over text and file columns (🧪 **Preview**).
- **Microsoft 365 knowledge sources where supported** — Copilot connectors (enterprise data indexed by Microsoft Search), OneDrive for Business (Microsoft Copilot harness), and **Work IQ** (🟢 **GA**; added by default to new Microsoft Copilot harness agents; some workloads are preview). 💳 **Licensing/Region:** availability varies by environment, licensing, and tenant enablement.
- **Knowledge configuration** — adding sources from the classic **Knowledge** page or the new Build tab's **Add knowledge** dialog, writing source descriptions, the **Generative AI** settings that affect knowledge, and the admin setting that limits which source types makers can add (documents, SharePoint and OneDrive, public websites).
- **Retrieval-Augmented Generation** — retrieve, rank, and generate: how the agent turns a user question into a search, selects passages, and composes an answer.
- **Grounding** — keeping answers tied to retrieved content, the **Allow ungrounded responses** setting, and why it doesn't guarantee zero general knowledge.
- **Citations** — reading and validating citations, why instructions must not alter the system citation format, and the current limitation that citations can't be passed as inputs to other tools.
- **Knowledge permissions** — agent-user authentication for SharePoint, Dataverse, and connector sources, so the agent surfaces only what each user can access; data policies that govern knowledge use.
- **Search behavior** — generative orchestration's filtering when an agent has more than 25 sources, classic-mode fallback through Conversational boosting, and source types (such as custom data) that need a generative answers node.
- **Knowledge source limitations** — documented per-source limits, unsupported combinations, and per-harness gaps (for example, Azure AI Search knowledge isn't supported on the Microsoft Copilot harness).
- **Improving answer quality** — curating and structuring content, removing duplicates, writing descriptions, using metadata filters, and measuring improvement with evaluations.
- **Troubleshooting incorrect answers** — a step-by-step method using the test panel, activity map, knowledge tests, and Learn's troubleshooting articles for SharePoint and enterprise data.

## Planned hands-on lab

**Lab: Build a company knowledge assistant**

After the lab you will have:

- A standard-harness agent grounded in at least three source types — a public website, a SharePoint site or library, and uploaded files — each with a clear description.
- Microsoft authentication configured so SharePoint answers respect each user's permissions, verified with a second test account if available.
- Ungrounded responses turned off and citations checked on every test answer.
- A 20-question test set run before and after quality improvements, with results compared.
- One incorrect answer diagnosed end to end and fixed, with the root cause documented.

**What you need:**

- Your course environment and solution, plus a SharePoint site with sample documents you're allowed to use.
- A trial license is enough to build and test (the trial **can't publish**); Microsoft authentication is needed for permission-aware sources.
- 💳 Optional comparison: rebuilding the assistant on the **Microsoft Copilot harness** (for example with OneDrive or Work IQ) consumes Copilot Credits while building and testing, and Work IQ requires tenant enablement.

## Planned assessment

`ASSESSMENT.md` will follow the course-wide 24-item pattern, and `ANSWERS.md` will provide correct answers, detailed explanations (including why incorrect options are wrong), expected practical outcomes, and rubrics.

| Item type | Count | Planned focus for this module |
|---|---|---|
| Multiple-choice questions | 10 | Source types and limits, RAG steps, permissions, grounding settings, harness differences |
| True/false questions | 5 | Statements such as "uploaded files count toward the 25-source limit" |
| Short-answer questions | 5 | Why citations matter; what agent-user authentication changes for SharePoint answers |
| Practical implementation tasks | 2 | Add and describe three source types; measure quality with a test set |
| Real-world scenario challenge | 1 | Design knowledge architecture for an HR policy assistant with confidential documents |
| Troubleshooting challenge | 1 | SharePoint knowledge returns no results for some users — diagnose authentication and permissions |
| **Total** | **24** | |

**Grading bands:** 0–59% Beginner · 60–74% Intermediate · 75–89% Advanced · 90–100% Professional Ready.

## Files in this module

| File | Purpose | Status |
|---|---|---|
| `README.md` | Syllabus: objectives, topics, lab outline, assessment plan (this file) | ✅ Syllabus |
| `CONCEPTS.md` | Full lessons for every topic using the course teaching sequence | 🔜 Planned |
| `STEP-BY-STEP-LAB.md` | Guided company knowledge assistant lab with checkpoints | 🔜 Planned |
| `EXAMPLES.md` | Knowledge architectures and before-and-after quality fixes | 🔜 Planned |
| `ASSESSMENT.md` | 24-item module assessment | 🔜 Planned |
| `ANSWERS.md` | Answers, explanations, and rubrics | 🔜 Planned |
| `INTERVIEW-QUESTIONS.md` | Interview questions with model answers | 🔜 Planned |
| `COMMON-MISTAKES.md` | Common mistakes, symptoms, and fixes | 🔜 Planned |

## Key official documentation

- [Knowledge sources summary](https://learn.microsoft.com/en-us/microsoft-copilot-studio/knowledge-copilot-studio)
- [Add a public website as a knowledge source](https://learn.microsoft.com/en-us/microsoft-copilot-studio/knowledge-add-public-website)
- [Add SharePoint as a knowledge source](https://learn.microsoft.com/en-us/microsoft-copilot-studio/knowledge-add-sharepoint)
- [Upload files as a knowledge source](https://learn.microsoft.com/en-us/microsoft-copilot-studio/knowledge-add-file-upload)
- [Add Dataverse tables as a knowledge source](https://learn.microsoft.com/en-us/microsoft-copilot-studio/knowledge-add-dataverse)
- [Available knowledge sources for agents (Microsoft Copilot harness)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/knowledge-sources-overview)
- [Choose knowledge sources for agents built in Copilot Studio](https://learn.microsoft.com/en-us/microsoft-copilot-studio/choose-knowledge-sources)
- [Test your agent's knowledge sources](https://learn.microsoft.com/en-us/microsoft-copilot-studio/knowledge-test)

## Navigation

⬅️ [Module 09 — Generative AI and Orchestration](../09-Generative-AI-and-Orchestration/README.md) | 🗺️ [Course roadmap](../COURSE-ROADMAP.md) | 📈 [Learning progress](../LEARNING-PROGRESS.md) | ➡️ [Module 11 — Agent Tools and Capabilities](../11-Agent-Tools-and-Capabilities/README.md)

## References

- https://learn.microsoft.com/en-us/microsoft-copilot-studio/knowledge-copilot-studio
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/knowledge-add-public-website
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/knowledge-add-sharepoint
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/knowledge-add-file-upload
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/knowledge-add-dataverse
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/knowledge-sources-overview
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/choose-knowledge-sources
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/knowledge-test

_Last verified against Microsoft Learn: 18 November 2026._
