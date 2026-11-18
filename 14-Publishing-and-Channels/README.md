# Module 14 — Publishing and Channels

> [!NOTE]
> **Status: 🔜 Planned.** This syllabus is published; the full lesson files are developed in Step 7 of the [course build plan](../COURSE-ROADMAP.md).

An agent creates value only when people can reach it. This module covers publishing, the publishing lifecycle, and every major channel — the demo website, your own website, Teams and Microsoft Copilot, and other supported channels — along with per-channel authentication, deployment validation, and version management on both harnesses.

## At a glance

| Item | Details |
|---|---|
| **Level** | Intermediate–Advanced |
| **Estimated time** | 5 hours |
| **Prerequisites** | [Module 13 — Authentication and Security](../13-Authentication-and-Security/README.md) |
| **Harness focus** | Both, with per-harness differences — the standard harness supports the broadest channel list, while the Microsoft Copilot harness currently supports a smaller set. |
| **Lab** | Publish an agent to a supported channel |

## Why this module matters

**For beginners:** "it works in the test panel" isn't the finish line. Publishing makes your latest changes live on every connected channel, and each channel has its own rules for sign-in, formatting, and how quickly users see updates. Knowing those rules avoids confusing "but it worked for me" moments.

**For the enterprise:** channel choices determine reach, compliance boundaries, and support costs. Publishing to Teams and Microsoft Copilot involves admin approval and organization catalogs; external channels can move data outside your compliance boundary; and some channels change status over time — for example, the Azure Communication Services–based WhatsApp channel no longer accepts new connections. Professionals plan releases, validate deployments, and manage versions deliberately.

## Learning objectives

By the end of this module you will be able to:

1. **Publish** an agent and **explain** how publishing updates every connected channel.
2. **Describe** the publishing lifecycle — draft, publish, validate, release, update — and when users actually receive new content.
3. **Configure** the demo website for stakeholder testing and **explain** why it isn't for production use.
4. **Embed** an agent in a custom website and **secure** the web channel with Direct Line secrets.
5. **Connect** an agent to Teams and Microsoft Copilot and **plan** distribution from personal install to organization-wide availability.
6. **Compare** the channels available on the standard harness, the Microsoft Copilot harness, and the Customer Conversation harness.
7. **Match** authentication settings to channels and **predict** when a channel is blocked by policy or configuration.
8. **Validate** a deployment and **manage** versions across environments using solutions.

## Topics covered

- **Publishing agents** — the **Publish** action in both experiences, readiness checks before publishing, and why every change must be republished before users see it.
- **Publishing lifecycle** — draft → publish → validate → release → update; new content reaches users when a new session starts (most channels end a session after 30 minutes of inactivity), and Teams users can type `start over` to pick up the latest version immediately.
- **Demo website** — a prebuilt page for teammates and stakeholders, available when the agent uses **No authentication** or **Authenticate manually**; Learn advises not sharing it with customers.
- **Custom website** — embedding the agent in your own site or app, customizing the look and feel, and web and Direct Line channel security with secrets (Microsoft Copilot harness: **Web app** iframe embedding and **Web channel security** in **Safety & access**).
- **Microsoft Teams** — connecting the agent, installing it for yourself first, sharing the installation link, adding it to a team, single sign-on, and submitting it for admin approval to appear in your organization's app store.
- **Microsoft 365 Copilot channel where supported** — on the standard harness this is the combined **Teams and Microsoft Copilot** channel, which registers the agent in the Microsoft 365 Agent Store; on the Microsoft Copilot harness, **Microsoft Copilot** and **Microsoft Teams** are separate available channels. Suggested prompts appear on the agent's welcome page here.
- **Other supported channels** — standard harness: SharePoint, Power Pages, mobile and custom apps, Facebook, Azure Bot Service channels (for example Slack, Telegram, Twilio, Direct Line Speech, and email), WhatsApp, and contact-center handoff. Microsoft Copilot harness: MCP client and A2A client channels (🧪 **Preview**, early release cycle environments only). Customer Conversation harness (🧪 **Preview**): website chat or a phone number.
  - ⚠️ **WhatsApp (Azure Communication Services–based):** since 23 October 2026 you can't create new connections; agents connected before that date continue to work.
- **Authentication per channel** — **Authenticate with Microsoft** for Teams, SharePoint, Power Apps, and Microsoft Copilot; **Authenticate manually** for other authenticated channels; channels that require **No authentication** or manual authentication; and data policies that block publishing to specific channels.
- **Channel configuration** — per-channel setup steps, channel experience differences (Markdown, cards, welcome messages), the **Agent access channels** admin control in the Power Platform admin center (its configuration article is 🧪 **Preview**), and diagnosing a disabled channel from its information icon.
- **Deployment validation** — testing the published version yourself before releasing it widely, a channel validation checklist, agent readiness and issue status (🧪 **Preview**), and troubleshooting publishing errors.
- **Version management** — publish as the live version, promoting agents between environments with solutions (export and import), ALM practices, comparing agent versions with evaluations, and the display name suffix to tell environments apart in Teams and Microsoft 365 Copilot (🧪 **Preview**).

## Planned hands-on lab

**Lab: Publish an agent to a supported channel**

After the lab you will have:

- Published a standard-harness agent and validated it on the demo website with a stakeholder test script.
- Connected the agent to **Teams and Microsoft Copilot** with **Authenticate with Microsoft**, installed it for yourself, and validated the published version before sharing it with a pilot group.
- Optionally embedded the agent in a test web page with web channel security turned on.
- Completed a deployment validation checklist covering sign-in, formatting, greeting and suggested prompts, and tool and knowledge behavior per channel.
- Made a change, republished, and confirmed when and how users received the update.
- Exported the agent in a solution ready for promotion to a test or production environment.

**What you need:**

- A license path that **can publish** — the trial license **can't publish** — plus access to Teams.
- Admin cooperation for organization-wide Teams availability and for any channels blocked by data policies.
- 💳 If you publish a **Microsoft Copilot harness** agent instead, remember that its usage consumes Copilot Credits and that its Microsoft Entra Agent ID is provisioned at first publish.

## Planned assessment

`ASSESSMENT.md` will follow the course-wide 24-item pattern, and `ANSWERS.md` will provide correct answers, detailed explanations (including why incorrect options are wrong), expected practical outcomes, and rubrics.

| Item type | Count | Planned focus for this module |
|---|---|---|
| Multiple-choice questions | 10 | Channel availability per harness, authentication per channel, publishing behavior |
| True/false questions | 5 | Statements such as "you can still create new WhatsApp connections through the ACS-based channel" |
| Short-answer questions | 5 | Demo website vs production website; how users get the latest version |
| Practical implementation tasks | 2 | Publish to Teams and Microsoft Copilot and validate; export the agent in a solution |
| Real-world scenario challenge | 1 | Plan a phased rollout of an HR agent from pilot group to the whole organization |
| Troubleshooting challenge | 1 | A channel is greyed out and users still see old answers — diagnose policy, authentication, and session causes |
| **Total** | **24** | |

**Grading bands:** 0–59% Beginner · 60–74% Intermediate · 75–89% Advanced · 90–100% Professional Ready.

## Files in this module

| File | Purpose | Status |
|---|---|---|
| `README.md` | Syllabus: objectives, topics, lab outline, assessment plan (this file) | ✅ Syllabus |
| `CONCEPTS.md` | Full lessons for every topic using the course teaching sequence | 🔜 Planned |
| `STEP-BY-STEP-LAB.md` | Guided publishing lab with checkpoints | 🔜 Planned |
| `EXAMPLES.md` | Channel selection examples and validation checklists | 🔜 Planned |
| `ASSESSMENT.md` | 24-item module assessment | 🔜 Planned |
| `ANSWERS.md` | Answers, explanations, and rubrics | 🔜 Planned |
| `INTERVIEW-QUESTIONS.md` | Interview questions with model answers | 🔜 Planned |
| `COMMON-MISTAKES.md` | Common mistakes, symptoms, and fixes | 🔜 Planned |

## Key official documentation

- [Key concepts - Publish and deploy your agent](https://learn.microsoft.com/en-us/microsoft-copilot-studio/publication-fundamentals-publish-channels)
- [Publish an agent to a live or demo website](https://learn.microsoft.com/en-us/microsoft-copilot-studio/publication-connect-bot-to-web-channels)
- [Connect and configure an agent for Teams and Microsoft Copilot](https://learn.microsoft.com/en-us/microsoft-copilot-studio/publication-add-bot-to-microsoft-teams)
- [Available channels for agents (Microsoft Copilot harness)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/publication-channels-overview)
- [Publish an agent (Microsoft Copilot harness)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/publication-publish-agent)
- [Publish an agent to WhatsApp](https://learn.microsoft.com/en-us/microsoft-copilot-studio/publication-add-bot-to-whatsapp)
- [Configure web and Direct Line channel security](https://learn.microsoft.com/en-us/microsoft-copilot-studio/configure-web-security)
- [Export and import agents using solutions](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-solutions-import-export)

## Navigation

⬅️ [Module 13 — Authentication and Security](../13-Authentication-and-Security/README.md) | 🗺️ [Course roadmap](../COURSE-ROADMAP.md) | 📈 [Learning progress](../LEARNING-PROGRESS.md) | ➡️ [Module 15 — Testing and Debugging](../15-Testing-and-Debugging/README.md)

## References

- https://learn.microsoft.com/en-us/microsoft-copilot-studio/publication-fundamentals-publish-channels
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/publication-connect-bot-to-web-channels
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/publication-add-bot-to-microsoft-teams
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/publication-channels-overview
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/publication-publish-agent
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/publication-add-bot-to-whatsapp
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/configure-web-security
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-solutions-import-export

_Last verified against Microsoft Learn: 18 November 2026._
