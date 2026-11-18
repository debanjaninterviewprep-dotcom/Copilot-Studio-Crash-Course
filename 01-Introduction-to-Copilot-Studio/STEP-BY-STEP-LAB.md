# Lab 01 — Understand and Explore Copilot Studio

> [!NOTE]
> **Applies to:** the standard harness (classic experience) for all hands-on steps. There is an optional, look-only tour of the new experience (Microsoft Copilot harness).
> **UI snapshot:** November 2026. Copilot Studio releases roll out over several days, so labels can differ slightly in your tenant. When they do, follow the linked official article for that step.

## Lab overview

| Item | Detail |
|---|---|
| **Goal** | Orient yourself in Copilot Studio, create a first standard harness agent from a description, and map every concept from this module to something you can see |
| **Time** | 75–90 minutes |
| **Level** | Beginner |
| **You will produce** | A completed **exploration worksheet** (below), one working test agent named *Copilot Studio Learning Buddy*, and answers to the reflection questions |
| **Related lessons** | All lessons in [CONCEPTS.md](CONCEPTS.md) |

### Learning outcomes

By the end of this lab you will be able to:

1. Sign in to Copilot Studio and tell whether you are in the **new** or the **classic** experience.
2. Create a standard harness agent by **describing it in natural language**.
3. Add a **public website** as a knowledge source.
4. Find and explain the agent's main pages: **Overview, Knowledge, Tools, Agents, Topics, Activity, Evaluation, Monitor, Channels, Settings**.
5. Test the agent, read **citations**, and open the **activity map**.
6. Observe the difference between **generative** and **classic orchestration**.

### Prerequisites

- A **work or school** account. Personal email addresses can be rejected at sign-up.
- Access to Copilot Studio: a trial license is enough for this lab, because you won't publish. See [Get access to Copilot Studio](https://learn.microsoft.com/en-us/microsoft-copilot-studio/requirements-licensing-subscriptions).
- A supported browser: Edge or Chrome 122+, Firefox 127+, or Safari 17+.
- An environment where you're allowed to create agents. If your organization restricts this, ask your admin. Environment setup is covered in [Module 03](../03-Environment-and-Setup/README.md).

> [!IMPORTANT]
> **Cost and safety notes**
> - Testing a standard harness agent in the Copilot Studio test panel happens **before publishing**. Microsoft documents that standard harness billing starts after publish.
> - Building, testing, and evaluating agents on the **Microsoft Copilot harness** consumes **Copilot Credits from the moment you start building**. That's why Part 9 of this lab is **optional and look-only** unless your admin has approved credit use.
> - Don't add tools or triggers in this lab. Ignore or dismiss those suggestions.

---

## Exploration worksheet

Copy this table into your notes and fill it in as you go. You'll submit it as part of the [assessment](ASSESSMENT.md).

| # | Page or area | What is it for? (your words) | Which lesson concept does it show? | One thing you observed |
|---|---|---|---|---|
| 1 | Home (new experience) | | | |
| 2 | Classic experience Home | | | |
| 3 | Overview | | | |
| 4 | Knowledge | | | |
| 5 | Tools | | | |
| 6 | Agents | | | |
| 7 | Topics | | | |
| 8 | Activity | | | |
| 9 | Evaluation | | | |
| 10 | Monitor | | | |
| 11 | Channels | | | |
| 12 | Settings | | | |
| 13 | Test your agent panel | | | |

---

## Part 1 — Sign in and check your access (5 min)

1. Open your browser and go to `https://copilotstudio.microsoft.com`.
2. Sign in with your work or school account.
3. If you're asked to sign up, follow the trial sign-up. If you see *"sign-up couldn't be completed"*, your admin has disabled self-service sign-up. Ask them for access and pause the lab.
4. Note which **environment** you're in. Environments are covered in [Module 02](../02-Power-Platform-Fundamentals/README.md); for now, just record the name.

✅ **Checkpoint:** You see the Copilot Studio **Home** page.

## Part 2 — Tour the new experience Home page, look only (10 min)

The new experience is the default UI and builds **Microsoft Copilot harness** agents.

1. On **Home**, find the area where you can **describe** what you want to build. Microsoft calls building from natural language the *agentic builder* (🧪 Preview).
2. Find the **Agent** tile. Selecting it would open the agent designer on the **Build** tab. **Don't select it now.**
3. In the side pane, find **Agents** and **Workflows**. These list what has been built in this environment.
4. At the bottom of the side bar, find the **…** menu. You'll use it in Part 3.
5. Record your observations in worksheet row 1.

> [!TIP]
> Can't find these items? Your tenant may still show an older layout with a **New experience** toggle. Record what you see. Both layouts are documented on Microsoft Learn.

## Part 3 — Open the classic experience (5 min)

1. Select **…** at the bottom of the side bar, then **Open classic experience**.
   - Alternative: on **Home**, select **Other ways to build**.
   - Older layout: turn off **New experience** and select **Submit** to dismiss the **Feedback** panel.
2. The **Home** page for standard harness agents appears.
3. Record the differences you notice in worksheet row 2.

> [!NOTE]
> The classic experience applies to **your current session only**, and there's no tenant-wide setting to make it the default. Next time, open it again the same way.

✅ **Checkpoint:** You're on the classic experience Home page.

## Part 4 — Create a standard harness agent from a description (10 min)

1. On the classic **Home** page (or the **Agents** page), find the box that asks you to describe what your agent should do.
2. Paste this description. It's well under the 1,024-character limit:

   ```text
   Help new makers learn Microsoft Copilot Studio concepts such as agents, harnesses,
   topics, knowledge sources, tools, orchestration, and licensing. Use the official
   Microsoft Learn documentation as the source. Explain clearly for beginners, cite
   your sources, and say when you are not sure instead of guessing.
   ```

3. Submit the description. The **Overview** page for your new agent appears.
4. Review what the AI generated: the **name**, **description**, and **instructions**.
5. Review the **suggestions** (knowledge sources, tools, triggers, channels). Suggestions don't persist beyond the current session. **Accept only the knowledge suggestion for Microsoft Learn** if one appears. Ignore or dismiss tool and trigger suggestions.
6. Wait for provisioning to finish. Then rename the agent **Copilot Studio Learning Buddy**: in the **Details** section, select **Edit**. Names can have up to 42 characters and can't include `<` or `>`.

> [!TIP]
> **No description box?** Your environment doesn't support agent creation from natural language. This happens, for example, in sovereign clouds or when your admin turned off cross-geo checks. Instead, select **Agent** under *Start building from scratch* on **Home**, or **Create blank agent** on the **Agents** page. Then paste the description text into the agent's **Instructions** yourself.

✅ **Checkpoint:** The **Overview** page shows *Copilot Studio Learning Buddy* with generated instructions.

## Part 5 — Add a public website as knowledge (5 min)

If you accepted the Microsoft Learn suggestion in Part 4, verify it appears under **Knowledge** and skip to Part 6. Otherwise:

1. On the **Overview** or **Knowledge** page, select **Add knowledge**.
2. Select **Public websites**.
3. In the **Public website link** field, enter `https://learn.microsoft.com/microsoft-copilot-studio`.
4. Review the name and add a clear **description**. Descriptions help generative orchestration choose the right source. Example: *"Official Microsoft Copilot Studio documentation on Microsoft Learn."*
5. Select **Add to agent**.

Official steps: [Add a public website as a knowledge source](https://learn.microsoft.com/en-us/microsoft-copilot-studio/knowledge-add-public-website).

✅ **Checkpoint:** The Microsoft Learn site is listed as a knowledge source.

## Part 6 — Explore every page of the agent (20 min)

Open each page and fill in worksheet rows 3–12. Use these hints, and connect each page to a lesson.

| Page | Look for | Lesson link |
|---|---|---|
| **Overview** | **Details** (name, description), **Instructions** (up to 8,000 characters), **Model** section (the default model and its tags), **Triggers** section, **Knowledge**, **Suggested prompts** | Lessons [9](CONCEPTS.md#lesson-9-large-language-models-llms), [11](CONCEPTS.md#lesson-11-agent-architecture), [7](CONCEPTS.md#lesson-7-ai-agents-and-autonomous-agents) |
| **Knowledge** | Your Microsoft Learn source and its status | [Lesson 8](CONCEPTS.md#lesson-8-generative-ai-fundamentals) |
| **Tools** | Empty for now. This is where connectors, agent flows, prompts, and more are added. | [Lesson 11](CONCEPTS.md#lesson-11-agent-architecture) |
| **Agents** | Where child and connected agents are added | [Lesson 11](CONCEPTS.md#lesson-11-agent-architecture) |
| **Topics** | The **system topics**: **Conversation Start**, **Conversational boosting**, **End of Conversation**, **Escalate**, **Fallback**, **Multiple Topics Matched**, **On Error**, **Reset Conversation**, **Sign in** | Lessons [6](CONCEPTS.md#lesson-6-copilot-studio-vs-traditional-chatbots), [10](CONCEPTS.md#lesson-10-natural-language-processing-nlp) |
| **Activity** | Records every activity in real time, including your tests | [Lesson 11](CONCEPTS.md#lesson-11-agent-architecture) |
| **Evaluation** | Where test sets and agent evaluations are created (**New evaluation**). Look only; evaluations are covered in [Module 15](../15-Testing-and-Debugging/README.md). | [Lesson 8](CONCEPTS.md#lesson-8-generative-ai-fundamentals) |
| **Monitor** | The analytics page. It's empty for now: Monitor doesn't show activity from test-panel sessions. | [Lesson 12](CONCEPTS.md#lesson-12-enterprise-use-cases) |
| **Channels** | Publishing targets such as **Teams and Microsoft Copilot** and websites. Look only; trial licenses can't publish. | Lessons [4](CONCEPTS.md#lesson-4-copilot-studio-vs-microsoft-copilot), [13](CONCEPTS.md#lesson-13-licensing-fundamentals) |
| **Settings** | The **Generative AI** section > **Orchestration** setting | [Lesson 6](CONCEPTS.md#lesson-6-copilot-studio-vs-traditional-chatbots) |

> [!NOTE]
> Page names reflect Microsoft Learn in November 2026. Older material and screenshots may call the **Monitor** page "Analytics". If a page is missing or named differently, record what you see. That observation is valuable too.

## Part 7 — Test the agent and read the activity map (15 min)

1. If the **Test your agent** panel is hidden, select **Test** at the top of any page.
2. In the test panel, select **…** at the top and turn on **Show activity map when testing**.
3. Ask these three questions one at a time, and record the answers and citations:
   1. *What is a harness in Copilot Studio?*
   2. *What is the difference between generative and classic orchestration?*
   3. *How do I add a public website as a knowledge source?*
4. For each answer, check: Is there a **citation**? Does the **activity map** show a knowledge search?
5. Start a **new test session** using the restart icon at the top of the panel, then ask question 1 again. Compare the wording; generative answers aren't deterministic.
6. Go to **Overview** > **Instructions**, select **Edit**, and add this line at the end: *"Explain every answer in no more than three short bullet points."* Save, start a new test session, and ask question 2 again. Note how the format changed.
7. Remove the line you added and save. This restores the original behavior.
8. Open the **Activity** page and find your test sessions.

✅ **Checkpoint:** You have three cited answers, one before-and-after instruction comparison, and you've seen your tests on the **Activity** page.

## Part 8 — Compare generative and classic orchestration (10 min)

1. Go to **Settings** > **Generative AI**. Under **Orchestration**, note the current value of **Use generative AI orchestration for your agent's responses?**. It should be **Yes**, the default.
2. Start a new test session and ask a **two-part** question:
   *"What is Copilot Studio, and how is it licensed?"*
   Record how the agent handles both parts.
3. Change the setting to **No** (classic orchestration) and save.
4. Start a new test session and ask the same question. Record the difference. Classic orchestration matches topics by trigger phrases and falls back to knowledge, if that's configured.
5. **Set the setting back to Yes** and save.

> [!WARNING]
> If the **Orchestration** option is unavailable, an admin may have turned off generative orchestration in your environment. Agents there can only use classic orchestration. Record this and skip steps 3–5.

## Part 9 (optional) — Look at the new experience without testing (5 min)

Do this only if your organization allows it. Microsoft Copilot harness building and testing consume Copilot Credits.

1. Return to the new experience (start a new session, or go back to **Home**).
2. Select the **Agent** tile. The agent designer opens on the **Build** tab.
3. Without testing, identify these areas:
   - The **Instructions** section.
   - The components area: knowledge, tools, skills, connected agents, and channels.
   - The **Agent settings** dialog tabs: **Agent details**, **AI & behavior**, **Safety & access**, **Greeting & prompts**.
4. Notice what's **missing** compared with the classic experience: there's no **Topics** page.
5. Leave without saving, or delete the agent if you saved it. Official reference: [Create a new agent (Microsoft Copilot harness)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/build-new-agent).

## Part 10 — Reflect (5 min)

Answer in 2–4 sentences each:

1. Which harness did your *Learning Buddy* agent use, and how can you tell?
2. Which page would you use to change the agent's model, and which tags did you see?
3. What did the activity map show for question 1?
4. How did the instruction change in Part 7 affect the answers?
5. What happened to the two-part question under classic orchestration?
6. Name one enterprise use case where you would choose the standard harness, and one where you would choose the Microsoft Copilot harness. Explain why.

---

## Clean-up

- **Recommended:** keep *Copilot Studio Learning Buddy* as a reference agent for later modules.
- **To delete it:** go to the **Agents** page and select the agent. Choose **Delete**, enter the agent's name to confirm, and select **Delete agent**. All data associated with the agent is permanently deleted after a few minutes. See [Create and delete agents](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-first-bot).

## Expected results

| Check | Expected |
|---|---|
| Agent exists | *Copilot Studio Learning Buddy* on the standard harness, in your chosen environment |
| Knowledge | Microsoft Learn Copilot Studio docs listed as a public website source |
| Answers | Cited answers to the three questions; wording varies across sessions |
| Instructions experiment | The format followed the added instruction, then reverted |
| Orchestration comparison | Generative orchestration addressed both parts more completely; classic relied on topic matching and knowledge fallback |
| Worksheet | All 13 rows completed |

## Troubleshooting

| Symptom | Likely cause | Fix |
|---|---|---|
| Personal email rejected at sign-up | Trial requires a work or school account | Use your organization account |
| "Sign-up couldn't be completed" | Self-service sign-up disabled by admin | Ask the admin to enable sign-up or assign a license |
| No description box in Part 4 | Natural-language creation isn't supported in this environment | Create a blank agent and paste the text into Instructions |
| Can't find **Open classic experience** | Different rollout layout | Use **Other ways to build**, or turn off the **New experience** toggle |
| Answers don't cite Microsoft Learn | Knowledge not added, still processing, or a weak description | Check the **Knowledge** page; add a clear description; retest in a new session |
| Test panel shows old behavior after edits | The session started before your change | Start a new test session |
| The **Monitor** page is empty | Test-panel activity isn't shown on Monitor | Expected; Monitor shows published-agent usage |
| The **Orchestration** setting is locked | Generative orchestration turned off by an admin | Record it; the agent uses classic orchestration |
| The agent answers general questions not in the docs | Ungrounded responses allowed | Review **Allow ungrounded responses** (covered in Module 10) |

## Lab deliverables and scoring

| Deliverable | Points |
|---|---|
| Worksheet complete and accurate (13 rows) | 40 |
| Three cited answers recorded, with activity-map observations | 20 |
| Instruction experiment and orchestration comparison recorded | 20 |
| Reflection answers (6) | 20 |
| **Total** | **100** |

Score bands: 0–59 Beginner · 60–74 Intermediate · 75–89 Advanced · 90–100 Professional Ready. Record your score in [LEARNING-PROGRESS.md](../LEARNING-PROGRESS.md).

## References

- [Quickstart: Create and deploy an agent with the standard harness](https://learn.microsoft.com/en-us/microsoft-copilot-studio/fundamentals-get-started)
- [Create and delete agents](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-first-bot)
- [Access standard harness agents and agent flows](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/switch-experiences)
- [Create a new agent (Microsoft Copilot harness)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/build-new-agent)
- [Add a public website as a knowledge source](https://learn.microsoft.com/en-us/microsoft-copilot-studio/knowledge-add-public-website)
- [Use system topics](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-system-topics)
- [Test your agent](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-test-bot)
- [Review agent activity](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-review-activity)
- [Monitor agent performance](https://learn.microsoft.com/en-us/microsoft-copilot-studio/analytics-overview)
- [Orchestrate agent behavior with generative AI](https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-generative-actions)
- [Select a primary AI model for your agent](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-select-agent-model)
- [Get access to Copilot Studio](https://learn.microsoft.com/en-us/microsoft-copilot-studio/requirements-licensing-subscriptions)
- [Overview of usage-based billing](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/billing-credit-overview)

_Last verified against Microsoft Learn: 18 November 2026._
