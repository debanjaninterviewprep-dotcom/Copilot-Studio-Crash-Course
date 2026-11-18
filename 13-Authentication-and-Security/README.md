# Module 13 — Authentication and Security

> [!NOTE]
> **Status: 🔜 Planned.** This syllabus is published; the full lesson files are developed in Step 7 of the [course build plan](../COURSE-ROADMAP.md).

An agent is only as trustworthy as its security configuration. This module covers who can talk to your agent, what it can see on their behalf, how Microsoft Entra ID and agent identities work, how data policies and environment controls protect data, and how responsible AI and governance fit into a secure design.

## At a glance

| Item | Details |
|---|---|
| **Level** | Intermediate–Advanced |
| **Estimated time** | 5 hours |
| **Prerequisites** | [Module 12 — Prompts and Generative Answers](../12-Prompts-and-Generative-Answers/README.md) |
| **Harness focus** | Both, with per-harness differences — for example, manual (custom) authentication is available on the standard harness but not on the Microsoft Copilot harness. |
| **Lab** | Configure an appropriately secured agent |

## Why this module matters

**For beginners:** a single setting — **No authentication** — lets anyone who has the link chat with your agent. Understanding authentication options, and what each one unlocks or exposes, prevents the most common and most serious mistakes new makers make.

**For the enterprise:** security reviews ask concrete questions: Which identity does the agent use? Does it respect each user's permissions? Which connectors and channels are allowed? Where is conversation data stored and for how long? This module gives you the vocabulary and the controls to answer those questions — and to design agents that pass review the first time.

## Learning objectives

By the end of this module you will be able to:

1. **Explain** authentication fundamentals — identity, sign-in, tokens, and consent — in the context of Copilot Studio agents.
2. **Compare** the authentication options (**No authentication**, **Authenticate with Microsoft**, **Authenticate manually**) and **state** which are available on each harness.
3. **Configure** Microsoft Entra ID authentication, including single sign-on for supported channels.
4. **Describe** agent identities — Microsoft Entra Agent IDs versus legacy app registrations — and when each harness provisions them.
5. **Apply** least privilege to agent sharing, user permissions, tool credentials, and knowledge access.
6. **Explain** how data policies can require authentication and block connectors, HTTP requests, channels, and triggers.
7. **Identify** data-privacy controls such as data residency, transcript retention and access, and privacy notices.
8. **Produce** a security checklist that combines environment security, responsible AI, and governance controls.

## Topics covered

- **Authentication fundamentals** — identities, sign-in, tokens, OAuth 2.0 flows, consent, and why changes to authentication take effect only after you publish.
- **User authentication** — signing users in so the agent can act on their behalf; the variables available after sign-in (such as `User.Id` and `User.DisplayName`) and which option provides an access token.
- **Microsoft Entra ID concepts** — tenants, users, groups, app registrations, service principals, and **Microsoft Entra Agent IDs**, which Copilot Studio provisions automatically for new agents (at creation on the standard harness; at first publish on the Microsoft Copilot harness). Conditional Access considerations.
- **Authentication configuration** — classic **Settings → Security → Authentication** versus the new **Agent settings → Safety & access** tab; manual providers on the standard harness (Microsoft Entra ID V2 with federated credentials, certificates, or client secrets; Microsoft Entra ID; generic OAuth 2); single sign-on for web and Teams.
- **Anonymous vs authenticated access** — when **No authentication** is acceptable (public FAQ content only), its risks, and what it rules out (for example, tools that use user credentials).
- **User permissions** — sharing agents for chat with individuals, security groups, or the whole organization; inviting collaborators; and the licensing prerequisites for sharing on the standard harness.
- **Knowledge permissions** — agent-user authentication for SharePoint, Dataverse, and connector knowledge so the agent only returns content each user can access.
- **Data privacy** — data locations and geographic residency, transcript retention and admin transcript controls, personal-data requests, sensitive data in test snapshots, data that leaves your boundary through some channels or external models, and a privacy statement link (🧪 **Preview**, *standard harness*).
- **Security roles** — environment and Dataverse roles that control authoring, plus Copilot Studio–specific roles such as **Bot Transcript Viewer** and the **Analytics Viewer** sharing role.
- **Environment security** — environment security groups, Managed Environments, network isolation options (Virtual Network support for outbound connections; IP firewall for inbound connections is 🧪 **Preview**), and customer-managed encryption keys. 💳 **Licensing/Region:** several of these controls depend on licensing.
- **DLP fundamentals** — Power Platform data policies (formerly *DLP policies*): Business, Non-business, and Blocked groups; Copilot Studio use cases such as requiring authentication, blocking connectors as tools, HTTP requests, Azure Bot Service skills, specific channels, and event triggers; and real-time enforcement messages.
- **Responsible AI** — content moderation settings, controls for image rendering and embedded URLs in responses, external threat detection, and safety evaluations as part of a secure design.
- **Governance** — the security and governance controls catalog: agent runtime protection status, automatic security scan, maker security warnings, audit logs in Microsoft Purview and Microsoft Sentinel, and Microsoft Agent 365 for centralized governance (deep dive in Module 17).

## Planned hands-on lab

**Lab: Configure an appropriately secured agent**

After the lab you will have:

- An internal agent configured with **Authenticate with Microsoft**, with sign-in variables verified in testing, and a written comparison against **No authentication**.
- SharePoint knowledge whose answers respect each user's permissions, verified with a second test account if available.
- Tool credentials set deliberately (end-user versus maker-provided) and confirmation required for consequential actions.
- A review — with your admin if needed — of the data policies that apply to your environment and their predicted effect on the agent.
- The agent shared for chat with a security group following least privilege, and its agent identity located.
- A one-page security sign-off checklist for the agent.

**What you need:**

- Your course environment and solution, a Microsoft Entra ID tenant, and ideally a second test user.
- Admin collaboration for steps that need a tenant admin or the Environment Admin role (for example, reviewing data policies).
- A trial license is enough to build and test (the trial **can't publish**); some sharing scenarios require licensed users.
- 💳 Optional comparison: configuring **Safety & access** on a **Microsoft Copilot harness** agent and testing it consumes Copilot Credits.

## Planned assessment

`ASSESSMENT.md` will follow the course-wide 24-item pattern, and `ANSWERS.md` will provide correct answers, detailed explanations (including why incorrect options are wrong), expected practical outcomes, and rubrics.

| Item type | Count | Planned focus for this module |
|---|---|---|
| Multiple-choice questions | 10 | Authentication options per harness, agent identities, data policy use cases, sharing |
| True/false questions | 5 | Statements such as "authentication changes take effect immediately without publishing" |
| Short-answer questions | 5 | When anonymous access is acceptable; how knowledge permissions are enforced |
| Practical implementation tasks | 2 | Configure Microsoft authentication and verify user variables; share an agent with a security group |
| Real-world scenario challenge | 1 | Secure an HR agent that answers from confidential SharePoint content |
| Troubleshooting challenge | 1 | Users can't sign in on a channel and the agent can't call a tool — diagnose authentication and policy causes |
| **Total** | **24** | |

**Grading bands:** 0–59% Beginner · 60–74% Intermediate · 75–89% Advanced · 90–100% Professional Ready.

## Files in this module

| File | Purpose | Status |
|---|---|---|
| `README.md` | Syllabus: objectives, topics, lab outline, assessment plan (this file) | ✅ Syllabus |
| `CONCEPTS.md` | Full lessons for every topic using the course teaching sequence | 🔜 Planned |
| `STEP-BY-STEP-LAB.md` | Guided security configuration lab with checkpoints | 🔜 Planned |
| `EXAMPLES.md` | Security configurations for common agent types | 🔜 Planned |
| `ASSESSMENT.md` | 24-item module assessment | 🔜 Planned |
| `ANSWERS.md` | Answers, explanations, and rubrics | 🔜 Planned |
| `INTERVIEW-QUESTIONS.md` | Interview questions with model answers | 🔜 Planned |
| `COMMON-MISTAKES.md` | Common mistakes, symptoms, and fixes | 🔜 Planned |

## Key official documentation

- [Configure user authentication in Copilot Studio](https://learn.microsoft.com/en-us/microsoft-copilot-studio/configuration-end-user-authentication)
- [Configure user authentication with Microsoft Entra ID](https://learn.microsoft.com/en-us/microsoft-copilot-studio/configuration-authentication-azure-ad)
- [Configure single sign-on for web](https://learn.microsoft.com/en-us/microsoft-copilot-studio/configure-sso)
- [App registration, agent identities, and authentication](https://learn.microsoft.com/en-us/microsoft-copilot-studio/govern-agents-identities-overview)
- [Share agents with other users](https://learn.microsoft.com/en-us/microsoft-copilot-studio/admin-share-bots)
- [Configure data policies for agents](https://learn.microsoft.com/en-us/microsoft-copilot-studio/admin-data-loss-prevention)
- [Security and governance](https://learn.microsoft.com/en-us/microsoft-copilot-studio/security-and-governance)
- [Geographic data residency](https://learn.microsoft.com/en-us/microsoft-copilot-studio/geo-data-residency)

## Navigation

⬅️ [Module 12 — Prompts and Generative Answers](../12-Prompts-and-Generative-Answers/README.md) | 🗺️ [Course roadmap](../COURSE-ROADMAP.md) | 📈 [Learning progress](../LEARNING-PROGRESS.md) | ➡️ [Module 14 — Publishing and Channels](../14-Publishing-and-Channels/README.md)

## References

- https://learn.microsoft.com/en-us/microsoft-copilot-studio/configuration-end-user-authentication
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/configuration-authentication-azure-ad
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/configure-sso
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/govern-agents-identities-overview
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/admin-share-bots
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/admin-data-loss-prevention
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/security-and-governance
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/geo-data-residency

_Last verified against Microsoft Learn: 18 November 2026._
