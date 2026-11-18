# Module 01 — Assessment: Introduction to Microsoft Copilot Studio

> [!NOTE]
> Answer every question **before** opening [ANSWERS.md](ANSWERS.md). Sections A–C are closed-book (30 minutes). Sections D–F are open-book and hands-on (60–90 minutes). Record your score in [LEARNING-PROGRESS.md](../LEARNING-PROGRESS.md).

## Scoring overview

| Section | Items | Points each | Total |
|---|---|---|---|
| A. Multiple choice | 10 | 2 | 20 |
| B. True / false | 5 | 1 | 5 |
| C. Short answer | 5 | 3 | 15 |
| D. Practical implementation tasks | 2 | 15 | 30 |
| E. Real-world scenario challenge | 1 | 15 | 15 |
| F. Troubleshooting challenge | 1 | 15 | 15 |
| **Total** | **24** | | **100** |

**Grading levels:** 0–59% **Beginner** · 60–74% **Intermediate** · 75–89% **Advanced** · 90–100% **Professional Ready**

---

## Section A — Multiple choice (choose one)

**A1.** Which statement best describes Microsoft Copilot Studio?
- a) A large language model trained by Microsoft
- b) A graphical, low-code studio for building and managing AI-powered agents and workflows
- c) A consumer chat app for personal Microsoft accounts
- d) A Microsoft Teams administration tool

**A2.** Which harness powers the default **new experience** in Copilot Studio (November 2026)?
- a) Standard harness
- b) Microsoft Copilot harness
- c) Customer Conversation harness
- d) Bot Framework harness

**A3.** Which capability is **not** available on the Microsoft Copilot harness?
- a) Skills
- b) Memory
- c) Topics
- d) Connected agents

**A4.** When did Power Virtual Agents' capabilities become part of Microsoft Copilot Studio?
- a) December 2019
- b) November 2023
- c) November 2024
- d) September 2025

**A5.** With **generative orchestration**, what is the most important factor the agent uses to select a topic, tool, agent, or knowledge source?
- a) The trigger phrases
- b) The component's description
- c) The order in which components were added
- d) The component's icon

**A6.** On the standard harness, event triggers are available only when:
- a) Classic orchestration is turned on
- b) Generative orchestration is turned on
- c) The agent is published to the demo website
- d) The agent uses a custom connector

**A7.** According to Microsoft's comparison guide, which is a limitation of **Agent Builder** compared with Copilot Studio?
- a) It can't use Microsoft 365 knowledge sources
- b) It doesn't support authoring actions that integrate external services
- c) It can't share agents within the organization
- d) It can't be configured with natural language

**A8.** On the standard harness, how many Copilot Credits does a **generative answer** consume for a user **without** a Microsoft 365 Copilot license?
- a) 1
- b) 2
- c) 5
- d) 10

**A9.** In the model list, what does the **cross-geo** tag indicate?
- a) The model is experimental
- b) Data might be processed outside your region
- c) The model is available only in GCC
- d) The model doesn't consume Copilot Credits

**A10.** What does a Copilot Studio **trial license** allow?
- a) Publishing to Microsoft Teams
- b) Creating and testing agents, but not publishing them
- c) Viewing agents only
- d) Publishing to the demo website only

## Section B — True or false

**B1.** An admin can set the classic experience as the tenant-wide default.

**B2.** Microsoft trains its foundation models using customer data from Copilot Studio agents.

**B3.** Unused prepaid Copilot Credits carry over to the next month.

**B4.** Building and testing agents on the Microsoft Copilot harness can consume Copilot Credits before the agent is published.

**B5.** Since July 2026, Copilot Studio automatically creates a Microsoft Entra Agent ID for every new agent.

## Section C — Short answer (3–5 sentences each)

**C1.** Define a **harness** in Copilot Studio and name the three harnesses with one ideal use for each.

**C2.** Explain **grounding** and **retrieval-augmented generation (RAG)** in your own words, and say why they reduce hallucinations.

**C3.** Give **two** differences between **Copilot Studio** and **Microsoft Copilot Chat**, and explain how the two can work together.

**C4.** List **four** components of a Copilot Studio agent and describe what each contributes.

**C5.** Name the **three** ways to acquire Copilot Credits and one characteristic of each.

## Section D — Practical implementation tasks

**D1. Build and evidence a first agent (15 points).**
Complete Parts 3–7 of the [lab](STEP-BY-STEP-LAB.md) and submit evidence (screenshots or detailed notes) that shows:
1. *Copilot Studio Learning Buddy* on the **standard harness**, with its name, description, instructions, and the model shown on the **Overview** page.
2. The Microsoft Learn website as a **knowledge source**, with a description.
3. Three answers **with citations**, plus your activity-map observation for each.
4. A before-and-after comparison of the instruction change in Part 7.

**D2. Orchestration comparison and recommendation (15 points).**
1. Run Part 8 of the lab (generative vs. classic orchestration) and document the differences you observed for the two-part question.
2. Write a 150–200-word recommendation: which **harness** and which **orchestration mode** should Contoso use for an *Employee Policy Assistant* in Teams? Justify it using at least three concepts from this module, such as predictability, citations, licensing, channel support, and preview status.

## Section E — Real-world scenario challenge (15 points)

**Fabrikam Retail** has 12,000 employees (3,000 have Microsoft 365 Copilot licenses) and 2 million customers. Leadership wants three agents:

1. **HR Policy Agent:** answers employee questions about policies in Teams and Microsoft Copilot.
2. **Order Help Agent:** customers check order status on the website and can reach a human representative. A phone line is planned for next year.
3. **Invoice Agent:** finance staff want an agent that reads supplier invoices (PDF), matches them to purchase orders, and routes exceptions for approval.

For **each** agent, provide:

- a) The recommended harness, with justification.
- b) The channel(s).
- c) The key knowledge and tools.
- d) Licensing and billing considerations.
- e) One key risk and its mitigation.

Finally, explain how Fabrikam should handle any **preview** capabilities in your design.

## Section F — Troubleshooting challenge (15 points)

A colleague sends you this message:

> "Yesterday I created an agent in the new Copilot Studio. Today I followed a 2024 YouTube tutorial to add a topic with trigger phrases, but there's no **Topics** page. Yesterday I also switched to the classic experience, but today it's gone again. My manager says we've used a lot of Copilot Credits even though nothing is published. Finally, I tried to publish my classic agent to Teams, but my trial account won't let me."

Identify **each** problem, its **root cause**, and the **fix or recommendation**. Add one general recommendation that would prevent this kind of confusion.

---

When you're done, check your work in [ANSWERS.md](ANSWERS.md) and record your score in [LEARNING-PROGRESS.md](../LEARNING-PROGRESS.md).

_Last verified against Microsoft Learn: 18 November 2026._
