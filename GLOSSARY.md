# Microsoft Copilot Studio Glossary

A plain-language reference for every important term used in this course — from generative-AI basics to Copilot Studio features, Power Platform administration, and the wider Microsoft agent ecosystem. Each entry starts with a beginner-friendly definition and then adds a professional note about how the term is used or configured in Copilot Studio.

> [!IMPORTANT]
> Copilot Studio changed significantly in 2026. It now has **three harnesses** (runtimes): the **Microsoft Copilot harness** (default "new experience"), the **Customer Conversation harness**, and the **standard harness** (the "classic experience" with topics, nodes, and entities). Many terms apply to only one harness, so always check the **Applies to** line.

## How to use this glossary

- Terms are listed **alphabetically** under A–Z headings. Use the [index](#index) to jump to a letter, or your browser's find (Ctrl+F / Cmd+F).
- Every entry has the same compact shape:
  - **Term** — a 1–2 sentence plain-language definition.
  - **Professional note** — how practitioners use or configure it in Copilot Studio.
  - A metadata line with, where relevant: a **status badge**, **Applies to** (harness), a **Learn more** link to Microsoft Learn, and **Covered in** links to the course module(s).
- No status badge means the item is an established concept or Microsoft Learn doesn't label it as preview, deprecated, or retired. Statuses change often — always confirm on the linked Learn page before production use.
- Old names (Power Virtual Agents, messages, Azure AI Foundry, and others) are mapped to current names in [Renamed and legacy terms](#renamed-and-legacy-terms).

> [!TIP]
> New to the subject? Read these first: [Agent](#a), [Harness](#h), [Large language model (LLM)](#l), [Knowledge source](#k), [Tool](#t), [Topic](#t), and [Copilot Credits](#c).

## Status legend

| Badge | Meaning |
|---|---|
| 🟢 **GA** | Generally available. |
| 🧪 **Preview** | Public preview (includes Microsoft's "production-ready preview"); behavior can change — check the preview terms before production use. |
| ⚠️ **Deprecated** | Still works, but it's being phased out. |
| ⛔ **Retired** | No longer available. |
| 💳 **Licensing/Region** | Subject to licensing, billing, cloud (for example GCC), or regional limitations. |

**Harness labels used in "Applies to":** Microsoft Copilot harness (new experience, default) · Customer Conversation harness · standard harness (classic experience). "All harnesses" means the concept applies everywhere, even if the UI differs.

## Index

[A](#a) · [B](#b) · [C](#c) · [D](#d) · [E](#e) · [F](#f) · [G](#g) · [H](#h) · [I](#i) · [K](#k) · [L](#l) · [M](#m) · [N](#n) · [O](#o) · [P](#p) · [Q](#q) · [R](#r) · [S](#s) · [T](#t) · [U](#u) · [V](#v) · [W](#w) · [Renamed and legacy terms](#renamed-and-legacy-terms) · [References](#references)

## A

- **A2A (Agent2Agent) protocol** — An open standard that lets AI agents send tasks to each other and receive structured responses, even when they're built on different platforms.
  - **Professional note:** Add an A2A-compatible external agent as a connected agent so your agent can delegate work to it; on the Microsoft Copilot harness you can also expose your own agent to A2A clients through the A2A channel.
  - 🟢 **GA** (standard harness connected agents, April 2026) · 🧪 **Preview** (Microsoft Copilot harness connected agent and A2A channel) · **Applies to:** standard and Microsoft Copilot harnesses · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/add-agent-agent-to-agent) · **Covered in:** [Module 18](18-Advanced-Agent-Development/README.md)
- **Activity map** — A visual, step-by-step map of what a standard-harness agent did for a message or event: which topics, tools, knowledge, or agents it used, any errors, and how long each step took.
  - **Professional note:** Turn on **Show activity map when testing** in the test panel to watch the generative orchestration plan live, and review historical maps for past activity; evaluation results also show the activity map for each test case.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-review-activity) · **Covered in:** [Module 04](04-Copilot-Studio-Interface/README.md), [Module 15](15-Testing-and-Debugging/README.md)
- **Activity trace** — The Microsoft Copilot harness equivalent of the activity map: a chain-of-thought trace showing which knowledge sources, tools, and reasoning steps the agent used for each message.
  - **Professional note:** It appears next to the chat on the **Preview** tab when the **End user preview** toggle is off; use it to confirm tool execution and source attribution while troubleshooting.
  - **Applies to:** Microsoft Copilot harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/authoring-activity-trace) · **Covered in:** [Module 15](15-Testing-and-Debugging/README.md)
- **Adaptive Card** — Interactive UI content (text, images, buttons, input fields) described in JSON and rendered by the host app, such as Microsoft Teams, in its own style.
  - **Professional note:** Use the Adaptive Card node or a card-based question to collect structured input. Copilot Studio supports schema version 1.6 and earlier, but each channel supports different versions and features, so design for the lowest version among your channels.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/adaptive-cards-overview) · **Covered in:** [Module 07](07-Topics-and-Conversation-Design/README.md), [Module 14](14-Publishing-and-Channels/README.md)
- **Agent** — In Copilot Studio, an AI assistant that handles conversations and completes tasks: it follows your instructions, draws on the knowledge you connect, and uses tools to act.
  - **Professional note:** Every agent runs on one of three harnesses, which decides its features, channels, and billing. "Agent" replaces older terms such as bot, chatbot, and copilot.
  - **Applies to:** all harnesses · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-overview) · **Covered in:** [Module 01](01-Introduction-to-Copilot-Studio/README.md), [Module 05](05-Creating-Your-First-Agent/README.md)
- **Agent account** — An identity of the agent's own in Microsoft 365 — its own Microsoft Entra ID, mailbox, and presence in Teams and the directory — so it can take part in business processes by email, Teams messages, and Office comments.
  - **Professional note:** Part of the Frontier preview program. It needs an early release cycle environment, admin enablement in both the Microsoft 365 admin center and the Power Platform admin center, and specific licenses (for example Microsoft 365 E5 with the Microsoft Agent 365 add-on, or Microsoft 365 E7). Agents with an account can't read label-protected documents.
  - 🧪 **Preview** (Frontier) · 💳 **Licensing/Region** · **Applies to:** Microsoft Copilot harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/authoring-agent-account) · **Covered in:** [Module 18](18-Advanced-Agent-Development/README.md)
- **Agent Builder** — The guided, natural-language builder in Microsoft 365 Copilot (for example at microsoft365.com/chat or in Teams) for creating declarative agents grounded in instructions and Microsoft 365 knowledge.
  - **Professional note:** Agent Builder can't author actions that integrate external services. When you need connectors, workflows, external channels, or ALM, copy the agent to Copilot Studio — the copy is a one-time snapshot, not a synchronized upgrade. The admin agent inventory labels these as *Microsoft Copilot Agent Builder* agents.
  - 💳 **Licensing/Region** · [Learn more](https://learn.microsoft.com/en-us/plugins/agent-builder) · **Covered in:** [Module 01](01-Introduction-to-Copilot-Studio/README.md), [Module 19](19-Enterprise-Copilot-Architecture/README.md)
- **Agent flow** — A deterministic automation (a trigger plus one or more actions) built natively in Copilot Studio with a designer similar to Power Automate; the same input always follows the same path.
  - **Professional note:** Run it on its own or attach it to a standard-harness agent as a tool that returns results. Agent flows can run prompts, call agents, and include human review steps; they consume Copilot Studio capacity for each action and are managed in the classic experience.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/flows-overview) · **Covered in:** [Module 11](11-Agent-Tools-and-Capabilities/README.md)
- **Agent inventory** — A tenant-wide, automatically refreshed list of every agent created with Copilot Studio or Agent Builder (drafts and published), with metadata such as creator, last publish date, channels, authentication method, and capabilities.
  - **Professional note:** Admins read it in the Power Platform admin center, through the Power Platform API, or with Azure Resource Graph. Classic chatbots (Power Virtual Agents V1) aren't included.
  - [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/admin-agent-inventory) · **Covered in:** [Module 17](17-Agent-Management-and-Governance/README.md)
- **Agent settings** — The settings dialog for Microsoft Copilot harness agents, organized into four tabs: **Agent details**, **AI & behavior**, **Safety & access**, and **Greeting & prompts**.
  - **Professional note:** Agent details (schema name, solution, primary language) become read-only after the first save, and setting changes take effect after you save and publish. Standard-harness agents use the **Settings** page instead.
  - **Applies to:** Microsoft Copilot harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/settings-overview) · **Covered in:** [Module 04](04-Copilot-Studio-Interface/README.md), [Module 06](06-Agent-Configuration-and-Instructions/README.md)
- **Agent status (readiness)** — A consolidated page that lists an agent's publishing errors, runtime issues, and configuration blocks, sorted by severity.
  - **Professional note:** For blocking issues it names the admin policy causing the block and whether the draft, the published agent, or both are affected — review it before every publish.
  - 🧪 **Preview** (standard harness) · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-agent-status) · **Covered in:** [Module 15](15-Testing-and-Debugging/README.md)
- **Agent usage estimator** — A Microsoft tool that forecasts an agent's Copilot Credit consumption from choices such as agent type, traffic, orchestration, knowledge, and tools.
  - **Professional note:** Use it during solution design and capacity planning, then compare the estimate with real consumption after launch. The authoritative source for licensing terms remains the Microsoft Copilot Studio Licensing Guide.
  - 💳 **Licensing/Region** · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agent-usage-estimator) · **Covered in:** [Module 17](17-Agent-Management-and-Governance/README.md), [Module 19](19-Enterprise-Copilot-Architecture/README.md)
- **AI agent** — Software that uses AI, usually a large language model, to understand a goal, decide what to do, and act — answering, calling tools, or completing tasks — rather than only following a fixed script.
  - **Professional note:** Distinguish *conversational* agents (respond to people) from *autonomous* agents (start from events). Copilot Studio builds both.
  - [Learn more](https://learn.microsoft.com/en-us/agents/) · **Covered in:** [Module 01](01-Introduction-to-Copilot-Studio/README.md), [Module 09](09-Generative-AI-and-Orchestration/README.md)
- **Allow ungrounded responses** — A standard-harness setting that decides whether the agent may answer from the model's general knowledge in a turn where it used no knowledge source or tool.
  - **Professional note:** When it's off, such responses are blocked (the Fallback topic triggers) and knowledge answers need an in-text citation — but it doesn't guarantee the model never mixes in general knowledge. Requires generative orchestration.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/knowledge-copilot-studio#allow-ungrounded-responses) · **Covered in:** [Module 10](10-Knowledge-Sources-and-Grounding/README.md), [Module 12](12-Prompts-and-Generative-Answers/README.md)
- **ALM (application lifecycle management)** — The disciplined way of moving an agent from development to test to production with controlled, repeatable deployments.
  - **Professional note:** In Copilot Studio, ALM is built on Power Platform solutions: build in unmanaged solutions in development, then import managed solutions downstream, using environment variables for values that change per environment.
  - [Learn more](https://learn.microsoft.com/en-us/power-platform/alm/solution-concepts-alm) · **Covered in:** [Module 17](17-Agent-Management-and-Governance/README.md), [Module 19](19-Enterprise-Copilot-Architecture/README.md)
- **Analytics** — Measurements of how an agent is used and how well it performs: sessions, outcomes, satisfaction, and knowledge and tool usage.
  - **Professional note:** Analytics live on the agent's **Monitor** page. On the standard harness, monitor data is kept for up to 360 days, session details and transcripts for the last 28 days, and test-panel activity isn't counted.
  - **Applies to:** all harnesses · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/analytics-overview) · **Covered in:** [Module 16](16-Analytics-and-Monitoring/README.md)
- **Analytics Viewer** — A sharing role that gives someone view-only access to an agent's Monitor page without broader maker permissions.
  - **Professional note:** It can be shared only with individuals, not groups. To read transcripts, the person also needs the Bot Transcript Viewer security role.
  - [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/analytics-overview#grant-limited-view-only-access-to-analytics) · **Covered in:** [Module 16](16-Analytics-and-Monitoring/README.md), [Module 17](17-Agent-Management-and-Governance/README.md)
- **Application Insights (telemetry)** — An Azure monitoring service that can receive detailed agent telemetry for custom dashboards, queries, and alerts.
  - **Professional note:** Configure agent-level telemetry per agent, or export environment-level agent telemetry from the Power Platform admin center (preview) for fleet monitoring.
  - 🧪 **Preview** (environment-level export) · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/telemetry-overview) · **Covered in:** [Module 16](16-Analytics-and-Monitoring/README.md)
- **Apps (Copilot Studio)** — A newer Copilot Studio building block for creating apps alongside agents and workflows.
  - **Professional note:** App creation is in preview and is outside this course's core scope; mention it when explaining what the studio can build.
  - 🧪 **Preview** · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/apps-experience/apps-overview) · **Covered in:** [Module 01](01-Introduction-to-Copilot-Studio/README.md)
- **Authentication options (user authentication)** — How users prove who they are to an agent: **No authentication**, **Authenticate with Microsoft** (Microsoft Entra ID, on by default), or **Authenticate manually** (Microsoft Entra ID or another OAuth 2.0 provider).
  - **Professional note:** **No authentication** lets anyone with the link chat and stops tools from using user credentials. Use **Authenticate with Microsoft** for Teams, Power Apps, and Microsoft Copilot; use manual authentication for other channels that still need sign-in.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/configuration-end-user-authentication) · **Covered in:** [Module 13](13-Authentication-and-Security/README.md), [Module 14](14-Publishing-and-Channels/README.md)
- **Autonomous agent** — An agent that starts work by itself when something happens — a new SharePoint item, an incoming email, a schedule — instead of waiting for a user's message.
  - **Professional note:** Built from event triggers plus clear instructions and tools. Each trigger payload is billed like a user message, so plan trigger frequency; monitor these agents with the autonomous-agent views on the Monitor page.
  - 🧪 **Preview** (Microsoft Copilot harness triggers) · 💳 **Licensing/Region** · **Applies to:** standard and Microsoft Copilot harnesses · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-triggers-about) · **Covered in:** [Module 01](01-Introduction-to-Copilot-Studio/README.md), [Module 18](18-Advanced-Agent-Development/README.md)
- **Azure AI Search (knowledge source)** — Azure's enterprise search service over your own indexed content, usable as a knowledge source for standard-harness agents.
  - **Professional note:** Microsoft Copilot harness agents don't support it as a knowledge source; reach the same content through Foundry IQ or a connector tool (the harness upgrade doesn't carry it over).
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/knowledge-azure-ai-search) · **Covered in:** [Module 10](10-Knowledge-Sources-and-Grounding/README.md)
- **Azure Bot Service / Bot Framework** — Microsoft's code-first platform (SDK plus Azure hosting service) for building and connecting bots; Azure documentation now calls the service *Azure AI Bot Service*.
  - **Professional note:** Mainly legacy context in this course: standard-harness agents can publish to Azure Bot Service channels (for example Slack, Telegram, Twilio) and use the Bot Framework Direct Line API for custom apps.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/publication-connect-bot-to-azure-bot-service-channels) · **Covered in:** [Module 01](01-Introduction-to-Copilot-Studio/README.md), [Module 14](14-Publishing-and-Channels/README.md)
- **Azure Bot Service skills** — Code-based Bot Framework bots that a standard-harness agent can call to reuse a set of related actions.
  - **Professional note:** Microsoft Learn separates three different "skills": Azure Bot Service skills (standard harness), *agent skills* (Microsoft Copilot and Customer Conversation harnesses), and *plugin skills* (Microsoft 365 Copilot plugins). Don't mix them up in designs or interviews.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/configuration-add-skills) · **Covered in:** [Module 18](18-Advanced-Agent-Development/README.md)
- **Azure SQL (knowledge source)** — Structured tables and views from an Azure SQL database or SQL Server that an agent can query to answer questions from business data.
  - **Professional note:** Added from the **Add knowledge** dialog in the new experience (tables and views); use it when answers depend on current structured data rather than documents.
  - **Applies to:** Microsoft Copilot harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/knowledge-add-azure-sql-tables) · **Covered in:** [Module 10](10-Knowledge-Sources-and-Grounding/README.md)

## B

- **Bing Custom Search** — A curated, scoped web index you define in Bing Custom Search and reference by its Custom Configuration ID.
  - **Professional note:** On the standard harness, generative orchestration doesn't support it as agent-level knowledge, so embed it in a generative answers node; in the new experience it's an Advanced knowledge source, limited to one per agent.
  - **Applies to:** standard and Microsoft Copilot harnesses · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/knowledge-bing-custom-search) · **Covered in:** [Module 10](10-Knowledge-Sources-and-Grounding/README.md)
- **Bot Transcript Viewer** — A Dataverse security role that lets a person view and download conversation transcripts and session-level data.
  - **Professional note:** Admins assign it per environment. Pair it with the Analytics Viewer role for analysts who need transcripts but no edit rights.
  - [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/admin-share-bots) · **Covered in:** [Module 16](16-Analytics-and-Monitoring/README.md), [Module 17](17-Agent-Management-and-Governance/README.md)
- **Build tab** — The main authoring surface in the new experience, where knowledge, tools, channels, connected agents, and other components such as Memory appear in a components panel.
  - **Professional note:** Customer Conversation harness agents use a tab set of **Build**, **Preview**, **Evaluate**, **Deploy**, and **Monitor**; Microsoft Copilot harness agents keep agent-level options in the Agent settings dialog.
  - **Applies to:** Microsoft Copilot and Customer Conversation harnesses · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/faqs-copilot-harness) · **Covered in:** [Module 04](04-Copilot-Studio-Interface/README.md)
- **Build with natural language** — Describe a business goal and Copilot Studio proposes and creates the right mix of agents and workflows in one conversation, which you refine with follow-up requests.
  - **Professional note:** It runs on the Microsoft Copilot harness, so creating solutions this way consumes Copilot Credits.
  - 🧪 **Preview** · 💳 **Licensing/Region** · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/create-automation-natural-language) · **Covered in:** [Module 05](05-Creating-Your-First-Agent/README.md)

## C

- **Capacity enforcement** — How Copilot Studio enforces the Copilot Credit capacity you've purchased or allocated.
  - **Professional note:** Standard harness: capacity is enforced monthly, unused credits don't carry over, and overage can trigger technical enforcement, including service denial. Usage-based harnesses: when an environment has no credits left (after limited overage), agents stop responding and makers can't author with natural language, preview, or evaluate until capacity is reallocated, purchased, or covered by pay-as-you-go.
  - 💳 **Licensing/Region** · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/billing-licensing#capacity-enforcement) · **Covered in:** [Module 17](17-Agent-Management-and-Governance/README.md)
- **Channel** — A place where people reach a published agent, such as Microsoft Teams, Microsoft Copilot, a website, a mobile app, or a phone line.
  - **Professional note:** Channels differ by harness: the standard harness supports many (Teams and Microsoft Copilot, SharePoint, websites, mobile apps, Facebook, WhatsApp, Azure Bot Service channels), while the Microsoft Copilot harness currently supports fewer (Microsoft Copilot, Teams, demo website, web app, and preview MCP/A2A clients). Admins can restrict channels in the Power Platform admin center.
  - **Applies to:** all harnesses · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/publication-fundamentals-publish-channels#configure-channels) · **Covered in:** [Module 14](14-Publishing-and-Channels/README.md)
- **Chatbot (traditional)** — A program that follows scripted, rule-based conversation paths and keyword matching to respond to users.
  - **Professional note:** Use "chatbot" only for history or comparison. Modern Copilot Studio agents add generative AI, knowledge grounding, tools, and planning on top of (or instead of) scripted paths.
  - [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/nlu-gpt-overview) · **Covered in:** [Module 01](01-Introduction-to-Copilot-Studio/README.md)
- **Child agent** — A lightweight agent built inside a standard-harness agent to group a focused set of instructions, tools, and knowledge, such as "create a ticket."
  - **Professional note:** Choose child agents when one team owns the solution and the sub-agent doesn't need its own settings, publishing, or ALM. The Microsoft Copilot harness has no child agents (use skills, connected agents, or task agents), and the harness upgrade doesn't migrate them.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/add-agent-child-agent) · **Covered in:** [Module 18](18-Advanced-Agent-Development/README.md)
- **Citations** — References in an answer that point to the knowledge passages used to produce it, so users can verify the source.
  - **Professional note:** Rendering varies by channel — Teams shows at most 20 citations and shortens long titles and snippets. If you customize the answer (for example, render it in an Adaptive Card), you must render citations yourself.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/knowledge-copilot-studio#how-citations-appear-on-different-channels) · **Covered in:** [Module 10](10-Knowledge-Sources-and-Grounding/README.md), [Module 12](12-Prompts-and-Generative-Answers/README.md)
- **Classic agent** — Microsoft Learn's everyday name for agents (and agent flows) built on the standard harness in the classic experience.
  - **Professional note:** Don't confuse it with *classic chatbot*: a classic agent is current and fully supported; a classic chatbot is a Power Virtual Agents–era bot.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/switch-experiences) · **Covered in:** [Module 04](04-Copilot-Studio-Interface/README.md)
- **Classic chatbot** — A bot created with Power Virtual Agents or an early version of the Copilot Studio app for Teams; it's marked "classic" and doesn't support generative AI features.
  - **Professional note:** Clone and convert it into a standard-harness agent, then retest before moving users over.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/unified-authoring-conversion) · **Covered in:** [Module 01](01-Introduction-to-Copilot-Studio/README.md)
- **Classic experience** — The Copilot Studio interface for standard-harness agents and agent flows, built around pages such as Overview, Knowledge, Tools, Agents, Topics, Channels, Monitor, and Settings, plus the **Test your agent** panel.
  - **Professional note:** From Home, select **…** at the bottom of the side bar → **Open classic experience**. It applies to the current session only, and there's no tenant-wide default; **Other ways to build** on Home also creates standard-harness assets.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/switch-experiences) · **Covered in:** [Module 03](03-Environment-and-Setup/README.md), [Module 04](04-Copilot-Studio-Interface/README.md)
- **Classic orchestration** — A standard-harness routing mode that triggers the single topic whose trigger phrases best match the user's message, falling back to knowledge if configured.
  - **Professional note:** Tools run only when a topic calls them, and you author every question and message. Choose it for highly predictable flows; it uses NLU, NLU+, or CLU. Admins can force it by turning off generative orchestration for an environment.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-generative-actions) · **Covered in:** [Module 09](09-Generative-AI-and-Orchestration/README.md)
- **Closed list entity** — A custom entity defined by a list of values, each with optional synonyms (for example *hiking* = *trekking*).
  - **Professional note:** Best for small, stable lists; turn on smart matching to tolerate misspellings and related words.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-entities-slot-filling#closed-list-entities) · **Covered in:** [Module 08](08-Variables-and-Entities/README.md)
- **CLU (Conversational Language Understanding)** — An Azure language service where you train your own intents and entities, which you can link to an agent as its classic understanding model.
  - **Professional note:** Requires an Azure subscription and ongoing work to keep the CLU model and agent in sync; it's one of three classic options alongside NLU and NLU+.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/nlu-overview) · **Covered in:** [Module 09](09-Generative-AI-and-Orchestration/README.md)
- **Component collection** — A reusable, shareable set of agent components that several agents can use.
  - **Professional note:** Collections export as versioned managed solutions and can be restricted to control who edits them — useful for shared enterprise building blocks.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-export-import-copilot-components) · **Covered in:** [Module 17](17-Agent-Management-and-Governance/README.md), [Module 18](18-Advanced-Agent-Development/README.md)
- **Computer use** — A tool that lets an agent operate websites and Windows desktop apps through their user interface — selecting buttons, choosing menus, typing — when no API exists.
  - **Professional note:** It's powered by a vision-capable Computer-Using Agent model and requires generative orchestration. Plan where it runs (for example a Cloud PC pool), human supervision, monitoring, and credentials; standalone computer-use tools are a separate preview.
  - 🟢 **GA** (May 2026) · **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/computer-use) · **Covered in:** [Module 11](11-Agent-Tools-and-Capabilities/README.md)
- **Condition node** — A topic node that branches the conversation based on variable values or Power Fx expressions.
  - **Professional note:** Branches are considered left to right. *Condition groups* let you manage several conditions inside a single Message, Question, or prompt node to reduce branching.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-using-conditions) · **Covered in:** [Module 07](07-Topics-and-Conversation-Design/README.md)
- **Connected agent** — A separately owned and managed agent that your agent can delegate work to, such as a specialist HR agent behind a front-door agent.
  - **Professional note:** Supported types differ by harness. Standard harness: other Copilot Studio agents and A2A agents, plus Microsoft Foundry, Fabric data, and Microsoft 365 Agents SDK agents (preview). Microsoft Copilot harness: Copilot-harness agents, Foundry, Microsoft 365 Agents SDK, and A2A (preview) agents. Customer Conversation harness: currently Foundry agents. Standard and Copilot-harness agents can't invoke each other directly.
  - **Applies to:** all harnesses · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-add-other-agents) · **Covered in:** [Module 18](18-Advanced-Agent-Development/README.md), [Module 19](19-Enterprise-Copilot-Architecture/README.md)
- **Connection** — The stored, authenticated link between a connector and an account that a tool, trigger, or knowledge source uses at runtime.
  - **Professional note:** Decide early whether each tool runs with the end user's credentials or with credentials the maker provides, because that choice affects security, sharing, and auditing.
  - [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-connections) · **Covered in:** [Module 11](11-Agent-Tools-and-Capabilities/README.md), [Module 13](13-Authentication-and-Security/README.md)
- **Connector** — A Power Platform "wrapper" around an API that lets agents, flows, and apps work with a service (for example Outlook, SharePoint, or Salesforce) through prebuilt actions and triggers.
  - **Professional note:** Use connectors as agent tools, inside topics, in agent flows, and (preview) as real-time knowledge. Standard connectors are included in all Copilot Studio plans, premium connectors only in select plans, and data policies control which connectors makers can use.
  - [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-connectors) · **Covered in:** [Module 02](02-Power-Platform-Fundamentals/README.md), [Module 11](11-Agent-Tools-and-Capabilities/README.md)
- **Content moderation (content safety)** — Filtering that blocks potentially harmful generated content — such as hate, sexual, violent, or self-harm content — at a chosen strictness level.
  - **Professional note:** Standard harness: set it per agent (Generative AI settings), per topic (generative answers node, which takes precedence), or per prompt, from Lowest to Highest (default High). Microsoft Copilot harness: **Moderation level** (Minimum to Maximum) under **AI & behavior**. Evaluations can add a content-safety test method.
  - **Applies to:** all harnesses · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/knowledge-copilot-studio#moderation) · **Covered in:** [Module 06](06-Agent-Configuration-and-Instructions/README.md), [Module 12](12-Prompts-and-Generative-Answers/README.md)
- **Context window** — The maximum amount of text, measured in tokens, that a model can consider at once — instructions, conversation history, retrieved content, tool results, and its own output.
  - **Professional note:** In Copilot Studio, a message plus tool responses and conversation history must fit in the selected model's context window; long instructions, large retrievals, and long conversations also increase Copilot Credit consumption.
  - [Learn more](https://learn.microsoft.com/en-us/dotnet/ai/conceptual/understanding-tokens) · **Covered in:** [Module 09](09-Generative-AI-and-Orchestration/README.md)
- **Conversation Start (system topic)** — The system topic that greets users and introduces the agent when a conversation begins.
  - **Professional note:** In Teams it runs only the first time a user adds the agent, because Teams reuses the conversation ID. If you publish only to Teams, consider turning it off so the welcome page with suggested prompts appears.
  - **Applies to:** standard harness (a built-in *event* in the Customer Conversation harness) · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-system-topics) · **Covered in:** [Module 07](07-Topics-and-Conversation-Design/README.md)
- **Conversation transcript** — A saved record of a conversation: the messages plus metadata such as start and end time and the topics that triggered.
  - **Professional note:** Transcripts are saved to Dataverse (the ConversationTranscript table; Power Apps downloads default to the last 30 days), and Copilot Studio keeps session data for 28 days. Admins can stop makers from viewing or downloading transcripts. Transcripts aren't written in Dataverse for Teams environments.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/admin-transcript-controls) · **Covered in:** [Module 15](15-Testing-and-Debugging/README.md), [Module 16](16-Analytics-and-Monitoring/README.md)
- **Conversational boosting (system topic)** — The standard-harness system topic that generates answers from your knowledge sources when no topic matches the user's message.
  - **Professional note:** It's created automatically with a generative answers node, and all agent-level knowledge sources are added to it.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-system-topics) · **Covered in:** [Module 07](07-Topics-and-Conversation-Design/README.md), [Module 10](10-Knowledge-Sources-and-Grounding/README.md)
- **Copilot connectors** — Connectors that index non-Microsoft content (for example ServiceNow or Jira) into Microsoft Graph so Microsoft 365 Copilot and agents can ground answers in it. Formerly *Microsoft Graph connectors*.
  - **Professional note:** Use Copilot connectors for broad, searchable knowledge reused across Microsoft experiences with semantic indexing and citations; use Power Platform connectors for real-time reads and writes against live systems.
  - **Applies to:** standard and Microsoft Copilot harnesses · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/knowledge-graph-vs-power-platform-connectors) · **Covered in:** [Module 10](10-Knowledge-Sources-and-Grounding/README.md)
- **Copilot Credits** — The common currency for Copilot Studio usage; agent responses, tools, and other capabilities consume credits at published rates. They replaced "messages" on 1 September 2025.
  - **Professional note:** The standard harness bills after you publish; the Microsoft Copilot harness bills from the moment you start building (natural-language creation, previews, and evaluations), and Customer Conversation harness building and testing can also consume credits. Get credits through prepaid packs, pay-as-you-go, or a prepurchase plan.
  - 💳 **Licensing/Region** · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/requirements-messages-management) · **Covered in:** [Module 01](01-Introduction-to-Copilot-Studio/README.md), [Module 03](03-Environment-and-Setup/README.md), [Module 17](17-Agent-Management-and-Governance/README.md)
- **Copilot Studio authors (setting)** — A Power Platform admin center setting that grants Copilot Studio authoring access, for pay-as-you-go scenarios, to members of a chosen Microsoft Entra security group.
  - **Professional note:** It doesn't revoke access that other licenses grant. To block a user, remove them from the group *and* remove any Copilot Studio, trial, and Microsoft 365 Copilot licenses.
  - 💳 **Licensing/Region** · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/billing-licensing) · **Covered in:** [Module 03](03-Environment-and-Setup/README.md), [Module 17](17-Agent-Management-and-Governance/README.md)
- **Copilot Studio MCP** — A Microsoft-published MCP server (the `@microsoft/copilot-studio-mcp` npm package) that brings Copilot Studio tools into MCP clients such as Visual Studio Code and GitHub Copilot CLI to create, test, deploy, and monitor agents and workflows.
  - **Professional note:** Don't confuse it with adding an MCP server *to* your agent (a tool) or with the MCP channel (exposing your agent *to* MCP clients). Access stays tied to your identity, environment permissions, and policies.
  - [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/copilot-studio-mcp) · **Covered in:** [Module 18](18-Advanced-Agent-Development/README.md)
- **Copilot Studio user license** — A free per-user license that an admin assigns in the Microsoft 365 admin center so a maker can use Copilot Studio.
  - **Professional note:** The tenant needs a prepaid Copilot Credit pack subscription before this license can be assigned.
  - 💳 **Licensing/Region** · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/requirements-licensing) · **Covered in:** [Module 03](03-Environment-and-Setup/README.md)
- **CSAT (customer satisfaction score)** — A satisfaction rating collected from users, for example through the end-of-conversation survey, and shown on the Monitor page.
  - **Professional note:** Downloaded session transcripts include session-level CSAT values for users with Bot Transcript Viewer privileges. In Teams, the survey is text-only rather than an Adaptive Card.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/analytics-improve-agent-effectiveness) · **Covered in:** [Module 16](16-Analytics-and-Monitoring/README.md)
- **Custom connector** — A connector you define, typically from an OpenAPI definition, to call your own API or any publicly available API that prebuilt connectors don't cover.
  - **Professional note:** For an agent to use it as a tool, the custom connector must be viewable and shared across the organization; data policies govern it like any other connector.
  - [Learn more](https://learn.microsoft.com/en-us/connectors/custom-connectors/) · **Covered in:** [Module 11](11-Agent-Tools-and-Capabilities/README.md)
- **Custom engine agent** — A Microsoft 365 Copilot agent whose orchestration, models, and integrations you control, built low-code with Copilot Studio or pro-code with the Microsoft 365 Agents SDK, Teams SDK, or Microsoft Foundry.
  - **Professional note:** Contrast with declarative agents, which use Microsoft 365 Copilot's own orchestration. Pick custom engine agents when you need your own models, workflows, or proactive automation.
  - [Learn more](https://learn.microsoft.com/en-us/microsoft-365/copilot/extensibility/overview-custom-engine-agent) · **Covered in:** [Module 19](19-Enterprise-Copilot-Architecture/README.md)
- **Custom entity** — An entity you define for domain-specific information: a closed list or a regular expression (regex).
  - **Professional note:** Create it under **Settings** → **Entities**. NLU and CLU use .NET regular-expression syntax; NLU+ uses JavaScript syntax.
  - **Applies to:** standard and Customer Conversation harnesses · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-entities-slot-filling#custom-entities) · **Covered in:** [Module 08](08-Variables-and-Entities/README.md)
- **Custom topic** — Any topic you create, plus the predefined non-system topics (such as greetings) that you can edit or delete.
  - **Professional note:** All business logic you author lives in custom topics; avoid periods in topic names because they block solution export.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-create-edit-topics) · **Covered in:** [Module 07](07-Topics-and-Conversation-Design/README.md)
- **Custom website (live website)** — Your organization's production website where the agent is embedded for real users, as opposed to the demo website.
  - **Professional note:** Configure web and Direct Line channel security before going live. On the Microsoft Copilot harness, the equivalent is the **Web app** channel (embedding with an iframe).
  - **Applies to:** standard and Microsoft Copilot harnesses · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/publication-connect-bot-to-web-channels) · **Covered in:** [Module 14](14-Publishing-and-Channels/README.md)
- **Customer Assist Agent** — The name Microsoft Learn uses for an agent built on the Customer Conversation harness (also the Self-Service/Customer Assist Agent in Microsoft Contact Center Intelligence).
  - **Professional note:** Its credit consumption varies by conversation complexity and modality (digital, voice), so estimate costs per scenario.
  - 🧪 **Preview** · 💳 **Licensing/Region** · **Applies to:** Customer Conversation harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/overview-customer-conversation) · **Covered in:** [Module 18](18-Advanced-Agent-Development/README.md), [Module 19](19-Enterprise-Copilot-Architecture/README.md)
- **Customer Conversation harness** — The harness for customer-facing agents over voice and chat: a primary agent with specialized sub-agents, each of which can escalate to a human representative.
  - **Professional note:** Build from Copilot Studio or the Microsoft Contact Center Intelligence portal — the authoring is the same, but only the portal connects the agent to a live contact center. It supports topics (as topic skills), knowledge, tools, MCP, connected agents, skills, and memory, with usage-based Copilot Credits.
  - 🧪 **Preview** (October 2026) · 💳 **Licensing/Region** · **Applies to:** Customer Conversation harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/overview-customer-conversation) · **Covered in:** [Module 01](01-Introduction-to-Copilot-Studio/README.md), [Module 19](19-Enterprise-Copilot-Architecture/README.md)
- **Customer-managed key (CMK)** — An encryption key that your organization owns and controls, used instead of a Microsoft-managed key to encrypt Copilot Studio data.
  - **Professional note:** After CMK is turned on, new data and changes are encrypted with your key; previously stored data keeps using Microsoft-managed keys.
  - [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/admin-customer-managed-keys) · **Covered in:** [Module 13](13-Authentication-and-Security/README.md), [Module 19](19-Enterprise-Copilot-Architecture/README.md)

## D

- **Data location (data residency)** — Where Copilot Studio stores and processes your agents' data, based on the environment's geography.
  - **Professional note:** Environments are bound to a geography, but some external models may process and store data outside your organization's geographic boundaries, so review data-location and data-movement settings for regulated workloads.
  - [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/data-location) · **Covered in:** [Module 13](13-Authentication-and-Security/README.md), [Module 19](19-Enterprise-Copilot-Architecture/README.md)
- **Data policies (DLP)** — Admin-defined guardrails in the Power Platform admin center that control which connectors — and therefore which tools, triggers, and channels — agents may use and combine.
  - **Professional note:** Enforcement is on for all tenants, and agent exemptions are no longer supported. Combine with advanced connector policies; blocked items appear disabled to makers, and the policies still apply when an agent is packaged in a plugin.
  - **Applies to:** all harnesses · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/admin-data-loss-prevention) · **Covered in:** [Module 13](13-Authentication-and-Security/README.md), [Module 17](17-Agent-Management-and-Governance/README.md)
- **Dataverse** — Microsoft's secure cloud data platform for Power Platform; it stores data in tables made of rows and columns.
  - **Professional note:** Copilot Studio agents, their components, and conversation transcripts are stored in Dataverse inside an environment, and Dataverse security roles control who can do what.
  - [Learn more](https://learn.microsoft.com/en-us/power-apps/maker/data-platform/data-platform-intro) · **Covered in:** [Module 02](02-Power-Platform-Fundamentals/README.md)
- **Dataverse for Teams** — A lightweight Dataverse environment that's provisioned for a Microsoft Teams team, for example when you build a classic agent with the Copilot Studio Teams plan.
  - **Professional note:** New Dataverse for Teams environments can't be created from 15 November 2026; environments that aren't upgraded are suspended on 15 September 2027 and decommissioned on 30 October 2027.
  - ⚠️ **Deprecated** · [Learn more](https://learn.microsoft.com/en-us/power-platform/admin/about-teams-environment) · **Covered in:** [Module 02](02-Power-Platform-Fundamentals/README.md)
- **Dataverse tables (knowledge source)** — Dataverse tables connected as knowledge so an agent can answer from structured business records.
  - **Professional note:** Answers respect the user's own permissions (Microsoft Entra ID authentication). Reasoning over unstructured columns (multiline text and file columns) is in preview.
  - 🧪 **Preview** (unstructured columns) · **Applies to:** standard and Microsoft Copilot harnesses · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/knowledge-add-dataverse) · **Covered in:** [Module 10](10-Knowledge-Sources-and-Grounding/README.md)
- **Declarative agent** — An agent for Microsoft 365 Copilot defined by its purpose, instructions, knowledge, and supported actions, and powered by Microsoft 365 Copilot's own orchestration.
  - **Professional note:** Build one in Agent Builder or with pro-code tools; it can be one component of a Microsoft 365 Copilot plugin. Move to Copilot Studio when you need external integrations, workflows, or broader channels.
  - [Learn more](https://learn.microsoft.com/en-us/plugins/overview-declarative-agent) · **Covered in:** [Module 19](19-Enterprise-Copilot-Architecture/README.md)
- **Default environment** — The environment every tenant gets automatically and that all users share; new Power Apps users are added to its Maker role.
  - **Professional note:** It's meant for experimentation and has no backup guarantees, so don't host production agents there.
  - [Learn more](https://learn.microsoft.com/en-us/power-platform/admin/environments-overview#default-environment) · **Covered in:** [Module 02](02-Power-Platform-Fundamentals/README.md), [Module 03](03-Environment-and-Setup/README.md)
- **Demo website** — A prebuilt test website that Copilot Studio creates when you publish, so teammates and stakeholders can try the agent.
  - **Professional note:** It's not for production — don't share its URL with customers.
  - **Applies to:** standard and Microsoft Copilot harnesses · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/publication-connect-bot-to-web-channels) · **Covered in:** [Module 14](14-Publishing-and-Channels/README.md)
- **Description (agent, topic, tool)** — Natural-language text that explains what an agent, topic, tool, or connected agent is for and when to use it.
  - **Professional note:** Generative orchestration and the newer harnesses choose topics, tools, and agents largely from their names and descriptions, so write distinct, specific descriptions; overlapping descriptions degrade routing as the number of choices grows.
  - **Applies to:** all harnesses · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-generative-actions) · **Covered in:** [Module 06](06-Agent-Configuration-and-Instructions/README.md), [Module 09](09-Generative-AI-and-Orchestration/README.md)
- **Developer environment** — A personal, single-owner Power Platform environment for building and testing.
  - **Professional note:** *Unmanaged* developer environments are deprecated: none can be created from 15 November 2026, and existing ones are suspended from 15 December 2026. Only managed developer environments remain (one per user) — ask your admin for one, or use a sandbox or trial environment for labs.
  - ⚠️ **Deprecated** (unmanaged developer environments) · [Learn more](https://learn.microsoft.com/en-us/power-platform/developer/create-developer-environment) · **Covered in:** [Module 02](02-Power-Platform-Fundamentals/README.md), [Module 03](03-Environment-and-Setup/README.md)
- **Direct Line** — The Bot Framework API for sending and receiving messages programmatically, used to connect an agent to native apps, custom web interfaces, or other services.
  - **Professional note:** Your app first gets a Direct Line token from the Copilot Studio token endpoint (not Direct Line's own token-generation endpoint), then uses it for later requests. The native-app channel isn't yet available on the Microsoft Copilot harness.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/publication-connect-bot-to-custom-application) · **Covered in:** [Module 14](14-Publishing-and-Channels/README.md)
- **Dynamics 365 Contact Center** — Microsoft's Copilot-first contact center product, working with the CRM of your choice, with voice and digital channels, unified routing, interactive voice response (IVR), and AI agents.
  - **Professional note:** Standard-harness agents integrate with it for voice and live-agent handoff; the NLU+ option requires a Dynamics 365 Contact Center license.
  - 💳 **Licensing/Region** · [Learn more](https://learn.microsoft.com/en-us/dynamics365/contact-center/implement/overview-contact-center) · **Covered in:** [Module 14](14-Publishing-and-Channels/README.md), [Module 18](18-Advanced-Agent-Development/README.md)

## E

- **Early release cycle environment** — An environment set to receive Copilot Studio and Power Platform updates earlier than standard environments, so you can validate changes before they reach business-critical environments.
  - **Professional note:** Several 2026 features are available only in early release cycle environments — for example task agents, the MCP and A2A channels, and agent accounts — so check an environment's **Release cycle** in the Power Platform admin center before a lab or pilot.
  - [Learn more](https://learn.microsoft.com/en-us/power-platform/admin/environments-overview) · **Covered in:** [Module 03](03-Environment-and-Setup/README.md), [Module 18](18-Advanced-Agent-Development/README.md)
- **Embeddings** — Lists of numbers (vectors) that represent the meaning of text, so text with similar meaning gets similar vectors.
  - **Professional note:** Embeddings are the foundation of vector (semantic) search in retrieval-augmented generation — useful background when you design knowledge with Azure AI Search or Foundry IQ.
  - [Learn more](https://learn.microsoft.com/en-us/dotnet/ai/conceptual/embeddings) · **Covered in:** [Module 10](10-Knowledge-Sources-and-Grounding/README.md)
- **End conversation node** — A topic management node that ends the conversation at the bottom of a conversation path.
  - **Professional note:** Before ending, consider redirecting to the End of Conversation system topic so users can confirm their issue was resolved and give satisfaction feedback.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-create-edit-topics#node-types) · **Covered in:** [Module 07](07-Topics-and-Conversation-Design/README.md)
- **End of Conversation (system topic)** — A system topic that confirms with the user whether their question was answered; it runs only when another topic redirects to it.
  - **Professional note:** Call it from your custom topics when a task is complete; it feeds satisfaction (CSAT) data into analytics.
  - **Applies to:** standard harness (a built-in *event* in the Customer Conversation harness) · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-system-topics) · **Covered in:** [Module 07](07-Topics-and-Conversation-Design/README.md), [Module 16](16-Analytics-and-Monitoring/README.md)
- **Entity** — A type of real-world information — such as age, date, city, money, or email — that an agent can recognize in a user's message and extract.
  - **Professional note:** The extracted value is saved to a variable of a matching type (for example, Money is saved as a Number). Start with prebuilt entities and add custom ones for domain terms.
  - **Applies to:** standard and Customer Conversation harnesses · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-entities-slot-filling) · **Covered in:** [Module 08](08-Variables-and-Entities/README.md)
- **Environment** — A Power Platform container for agents, apps, flows, and data, with its own security, geography, and (usually) a Dataverse database.
  - **Professional note:** Each environment belongs to one Microsoft Entra tenant and is bound to a geographic location. Use separate development, test, and production environments and move agents between them with solutions.
  - [Learn more](https://learn.microsoft.com/en-us/power-platform/admin/environments-overview) · **Covered in:** [Module 02](02-Power-Platform-Fundamentals/README.md), [Module 03](03-Environment-and-Setup/README.md), [Module 19](19-Enterprise-Copilot-Architecture/README.md)
- **Environment variable** — A named setting, such as a URL or ID, stored in a solution so components read it instead of hard-coding the value.
  - **Professional note:** Environment variables are read-only in Copilot Studio. Set different values per environment as you deploy solutions from development to test to production.
  - [Learn more](https://learn.microsoft.com/en-us/power-apps/maker/data-platform/environmentvariables) · **Covered in:** [Module 08](08-Variables-and-Entities/README.md), [Module 17](17-Agent-Management-and-Governance/README.md)
- **Escalate (system topic)** — The system topic that tells users they'll be connected with a person; it triggers on phrases such as "talk to agent" or when the Escalate event is called.
  - **Professional note:** By itself it only informs the user. To actually transfer the chat, add a **Transfer conversation** node and configure handoff to an engagement hub.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-hand-off) · **Covered in:** [Module 07](07-Topics-and-Conversation-Design/README.md), [Module 18](18-Advanced-Agent-Development/README.md)
- **Evaluation (agent evaluation)** — Automated testing that runs a test set against your agent, compares the responses with expected answers or quality criteria, and scores each test case.
  - **Professional note:** Standard harness evaluations support single-response and multi-turn tests and safety evaluators, and can be automated with a connector or (preview) the Power Platform REST API. On the Microsoft Copilot harness, evaluation is a production-ready preview and consumes credits.
  - 🟢 **GA** (standard harness, March 2026) · 🧪 **Preview** (Microsoft Copilot harness) · **Applies to:** all harnesses · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/analytics-agent-evaluation-intro) · **Covered in:** [Module 15](15-Testing-and-Debugging/README.md)
- **Event trigger** — A trigger that starts an agent when something happens in a connected service — for example a new SharePoint item, a new OneDrive file, a completed Planner task, or a recurrence schedule.
  - **Professional note:** On the standard harness it requires generative orchestration, each trigger payload is billed like a user message, and the triggers available depend on data policies. On the Microsoft Copilot harness, triggers are in preview.
  - 🧪 **Preview** (Microsoft Copilot harness) · 💳 **Licensing/Region** · **Applies to:** standard and Microsoft Copilot harnesses · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-triggers-about) · **Covered in:** [Module 18](18-Advanced-Agent-Development/README.md)
- **Events (Customer Conversation)** — Built-in responses for common conversation moments — such as Conversation Start, End of Conversation, and On Error — that you turn on or off in a Customer Conversation harness agent.
  - **Professional note:** They play the role that system topics play on the standard harness.
  - **Applies to:** Customer Conversation harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/events-overview-customer-conversation) · **Covered in:** [Module 18](18-Advanced-Agent-Development/README.md)

## F

- **Fabric IQ** — A connection that grounds an agent's responses in business data and analytics from Microsoft Fabric, using your organization's semantic model.
  - **Professional note:** Add it from the Tools section of the Build page; the picker shows only the Fabric workspaces and semantic models you can access.
  - 🧪 **Preview** · **Applies to:** Microsoft Copilot harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/fabric-iq-connect) · **Covered in:** [Module 10](10-Knowledge-Sources-and-Grounding/README.md), [Module 18](18-Advanced-Agent-Development/README.md)
- **Fallback (system topic)** — The system topic that tells users their message couldn't be matched to a topic and asks them to try again.
  - **Professional note:** It triggers when nothing matches (including when a blocked ungrounded response leaves no answer). Customize it so repeated misses lead somewhere useful, such as escalation.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-system-fallback-topic) · **Covered in:** [Module 07](07-Topics-and-Conversation-Design/README.md)
- **File attachments** — Files a user attaches to a conversation (for example Word, Excel, or PowerPoint) so the agent can read, summarize, or reason over them.
  - **Professional note:** An attachment is per-conversation input, not a knowledge source that every user shares. Files the *agent* creates during a conversation are a separate preview feature.
  - 🟢 **GA** (September 2026) · **Applies to:** Microsoft Copilot harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/attachments-overview) · **Covered in:** [Module 10](10-Knowledge-Sources-and-Grounding/README.md)
- **Foundry IQ** — A managed knowledge layer in Microsoft Foundry: a Foundry IQ knowledge base bundles enterprise data sources with retrieval and relevance settings so agents get permission-aware, cited answers.
  - **Professional note:** Connect an existing, already-tuned knowledge base as a tool instead of rebuilding retrieval in Copilot Studio; only knowledge bases you have access to appear in the picker.
  - 🧪 **Preview** · **Applies to:** Microsoft Copilot and Customer Conversation harnesses · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/foundry-iq-connect) · **Covered in:** [Module 10](10-Knowledge-Sources-and-Grounding/README.md), [Module 19](19-Enterprise-Copilot-Architecture/README.md)
- **Frontier program** — Microsoft's early-access program for its latest AI capabilities; Frontier previews are subject to the preview terms of your agreements.
  - **Professional note:** Agent accounts are a Frontier feature; tenant enrollment and specific licenses are prerequisites, and capabilities can change.
  - 🧪 **Preview** · 💳 **Licensing/Region** · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/authoring-agent-account) · **Covered in:** [Module 18](18-Advanced-Agent-Development/README.md)

## G

- **GCC (Government Community Cloud)** — Microsoft's US government cloud offering, in which Copilot Studio is available with some differences.
  - **Professional note:** Some features behave differently in GCC — for example, several external models are generally available "excluding GCC," and agent evaluations have GCC limitations — so check the US Government article before planning.
  - 💳 **Licensing/Region** · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/requirements-licensing-gcc) · **Covered in:** [Module 03](03-Environment-and-Setup/README.md), [Module 19](19-Enterprise-Copilot-Architecture/README.md)
- **Generative AI** — AI that creates new content — text, images, code — based on patterns learned in training, typically using large language models.
  - **Professional note:** In Copilot Studio it powers natural-language agent creation, generative orchestration, generative answers, prompts, and AI-assisted topic authoring.
  - [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/nlu-gpt-overview) · **Covered in:** [Module 01](01-Introduction-to-Copilot-Studio/README.md), [Module 09](09-Generative-AI-and-Orchestration/README.md)
- **Generative answers** — Answers an agent composes at runtime from your knowledge sources, without you authoring a topic for each question.
  - **Professional note:** They're used automatically by generative orchestration, as a fallback (Conversational boosting) in classic orchestration, or explicitly through a generative answers node. Responses can contain mistakes, and the system doesn't fact-check your sources.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/faqs-generative-answers) · **Covered in:** [Module 10](10-Knowledge-Sources-and-Grounding/README.md), [Module 12](12-Prompts-and-Generative-Answers/README.md)
- **Generative answers node** — A topic node that searches specified knowledge sources and generates an answer at that point in the conversation.
  - **Professional note:** Sources set on the node override agent-level knowledge. Use it for sources that generative orchestration doesn't support at agent level, such as Bing Custom Search, Azure OpenAI, or custom data.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/nlu-boost-node) · **Covered in:** [Module 07](07-Topics-and-Conversation-Design/README.md), [Module 12](12-Prompts-and-Generative-Answers/README.md)
- **Generative orchestration** — The standard harness's default mode: the AI plans a response by choosing the best combination of topics, tools, knowledge, and other agents from their descriptions, asks for missing inputs, and composes the reply.
  - **Professional note:** It's required for MCP, computer use, event triggers, web search, and the Allow ungrounded responses setting. Follow its plan on the activity map; admins can turn it off for an environment.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-generative-actions) · **Covered in:** [Module 09](09-Generative-AI-and-Orchestration/README.md)
- **Global variable** — A variable available in every topic for the length of a user session; external sources can also set it.
  - **Professional note:** Reference it in Power Fx with the `Global.` prefix. For data that only a few topics need, prefer topic inputs and outputs.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-variables-bot) · **Covered in:** [Module 08](08-Variables-and-Entities/README.md)
- **Grounding** — Giving a model trusted, relevant information at runtime — documents, data, search results — so its answer is based on that information rather than only on its training.
  - **Professional note:** In Copilot Studio, grounding comes from knowledge sources, tools, Work IQ, Foundry IQ, and Fabric IQ; citations and the Allow ungrounded responses setting help you control it.
  - [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/knowledge-copilot-studio) · **Covered in:** [Module 09](09-Generative-AI-and-Orchestration/README.md), [Module 10](10-Knowledge-Sources-and-Grounding/README.md)

## H

- **Hallucination** — When an AI model produces information that sounds plausible but is false or isn't supported by its sources; Microsoft documentation also calls this *ungrounded* output.
  - **Professional note:** Reduce it with high-quality knowledge, instructions that require citations, turning off Allow ungrounded responses, evaluations, and human review for high-stakes answers.
  - [Learn more](https://learn.microsoft.com/en-us/azure/ai-services/content-safety/concepts/groundedness) · **Covered in:** [Module 09](09-Generative-AI-and-Orchestration/README.md), [Module 12](12-Prompts-and-Generative-Answers/README.md)
- **Handoff (escalation to a live agent)** — Transferring a conversation from the agent to a human representative, together with the conversation history and relevant variables.
  - **Professional note:** Standard harness: use the Escalate topic with a **Transfer conversation** node and an engagement hub such as Dynamics 365 Customer Service, Genesys, LivePerson, Salesforce, ServiceNow, or a generic hub. Customer Conversation harness: each sub-agent can have its own escalation path.
  - **Applies to:** standard and Customer Conversation harnesses · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-hand-off) · **Covered in:** [Module 09](09-Generative-AI-and-Orchestration/README.md), [Module 18](18-Advanced-Agent-Development/README.md)
- **Harness** — The runtime that sits between your agent design and the AI model: it decides when to call the model, what to send it, interprets what comes back, and calls the right tools.
  - **Professional note:** Copilot Studio has three — the Microsoft Copilot harness, the Customer Conversation harness, and the standard harness. The choice affects features, channels, and billing, so make it deliberately at design time.
  - **Applies to:** all harnesses · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/harnesses-overview) · **Covered in:** [Module 01](01-Introduction-to-Copilot-Studio/README.md), [Module 19](19-Enterprise-Copilot-Architecture/README.md)
- **Hooks** — Workflows that run automatically at points in an agent's lifecycle — for example when a session starts, before a tool runs, or when an error occurs.
  - **Professional note:** Use a hook when something must happen *every* time (such as logging or a policy check); a tool runs only when the agent decides it's relevant.
  - 🧪 **Preview** · **Applies to:** Microsoft Copilot harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/hooks-overview) · **Covered in:** [Module 18](18-Advanced-Agent-Development/README.md)
- **HTTP request node** — An advanced topic node that calls a web API directly from a topic and stores the response in variables.
  - **Professional note:** You can configure error handling to store the HTTP status code and error body in variables instead of triggering the On Error system topic. Prefer an existing connector or tool when one covers the API, because it's easier to reuse across agents.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-http-node) · **Covered in:** [Module 11](11-Agent-Tools-and-Capabilities/README.md)

## I

- **Instructions** — Natural-language guidance that defines an agent's role, scope, tone, rules, and how it should use its knowledge and tools.
  - **Professional note:** Keep instructions specific and testable, and ask for citations when grounding matters — instructions that force rigid output formats can suppress citations. The harness upgrade carries instructions over.
  - **Applies to:** all harnesses · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-instructions) · **Covered in:** [Module 05](05-Creating-Your-First-Agent/README.md), [Module 06](06-Agent-Configuration-and-Instructions/README.md)
- **Intent** — What a user is trying to achieve with a message (for example, "reset my password"), regardless of the exact words used.
  - **Professional note:** Classic orchestration maps intents to topics through trigger phrases; generative orchestration infers intent and picks components from their names and descriptions.
  - [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-triggers) · **Covered in:** [Module 07](07-Topics-and-Conversation-Design/README.md), [Module 09](09-Generative-AI-and-Orchestration/README.md)

## K

- **Knowledge source** — Content you connect to an agent at design time — websites, SharePoint, OneDrive, files, Dataverse, Copilot connectors, and more — so every user's answers are grounded in it.
  - **Professional note:** Supported types and limits differ by harness and orchestration mode. Sources that use the agent user's authentication return only what each user can access, and admins can restrict which source types makers may add.
  - **Applies to:** all harnesses · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/knowledge-copilot-studio) · **Covered in:** [Module 10](10-Knowledge-Sources-and-Grounding/README.md)

## L

- **Large language model (LLM)** — An AI model trained on huge amounts of text that generates language by predicting the next token, enabling it to understand and produce natural language.
  - **Professional note:** Copilot Studio lets you choose the model an agent uses, including external and preview or experimental models with their own region and data-processing considerations. Default models change over time, with an option to stay on the current model for up to 30 days after a default upgrade.
  - [Learn more](https://learn.microsoft.com/en-us/dotnet/ai/conceptual/how-genai-and-llms-work) · **Covered in:** [Module 01](01-Introduction-to-Copilot-Studio/README.md), [Module 09](09-Generative-AI-and-Orchestration/README.md)

## M

- **Managed environment** — A suite of premium Power Platform capabilities that helps admins manage environments at scale with more control, less effort, and more insight.
  - **Professional note:** It's included as an entitlement with standalone Copilot Studio licenses. Managed environment sharing controls and environment security groups govern who agents can be shared with.
  - 💳 **Licensing/Region** · [Learn more](https://learn.microsoft.com/en-us/power-platform/admin/managed-environment-overview) · **Covered in:** [Module 02](02-Power-Platform-Fundamentals/README.md), [Module 17](17-Agent-Management-and-Governance/README.md)
- **Managed solution** — A locked solution package imported into downstream environments, such as test and production, where its components aren't edited directly.
  - **Professional note:** Export managed solutions from development to deploy; component collections are also packaged as versioned managed solutions.
  - [Learn more](https://learn.microsoft.com/en-us/power-platform/alm/solution-concepts-alm) · **Covered in:** [Module 02](02-Power-Platform-Fundamentals/README.md), [Module 17](17-Agent-Management-and-Governance/README.md)
- **MCP (Model Context Protocol)** — An open standard for connecting AI applications to tools and context. An MCP server publishes tools, resources, and prompts that agents can discover and call.
  - **Professional note:** Copilot Studio supports MCP tools and resources, and changes on the server flow through automatically. It requires generative orchestration on the standard harness; on the Microsoft Copilot harness, MCP tools are in preview, and MCP servers count against an agent's tool limits.
  - 🧪 **Preview** (Microsoft Copilot harness) · **Applies to:** all harnesses · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agent-extend-action-mcp) · **Covered in:** [Module 11](11-Agent-Tools-and-Capabilities/README.md)
- **MCP and A2A channels** — Publishing options that expose your agent as a remote MCP server or as an A2A agent, so external tools, IDEs, and orchestrators can call it with Microsoft Entra ID authentication.
  - **Professional note:** Available only in early release cycle environments.
  - 🧪 **Preview** · **Applies to:** Microsoft Copilot harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/publication-channels-mcp-agent-to-agent) · **Covered in:** [Module 14](14-Publishing-and-Channels/README.md), [Module 18](18-Advanced-Agent-Development/README.md)
- **Memory** — Lets an agent remember user preferences and useful context across interactions, kept separately for each user.
  - **Professional note:** On the Microsoft Copilot harness, makers turn Memory on in the Build tab. Memories are private to each user, deleted after 28 days of inactivity, disabled in group chats and Teams channels, and kept (not deleted) if you turn Memory off. The Customer Conversation harness has its own structured memory.
  - 🧪 **Preview** (production-ready) · **Applies to:** Microsoft Copilot and Customer Conversation harnesses · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/memory-overview) · **Covered in:** [Module 18](18-Advanced-Agent-Development/README.md)
- **Message node** — A topic node that sends a message to the user: plain text, or richer content such as variables, images, videos, quick replies, and cards.
  - **Professional note:** Use variations and channel-aware formatting, because channels render Markdown and cards differently.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-send-message) · **Covered in:** [Module 07](07-Topics-and-Conversation-Design/README.md)
- **Microsoft 365 Agents SDK** — A pro-code framework (C#, JavaScript, Python) for building conversational agents that work across channels such as Teams, Microsoft Copilot, websites, and non-Microsoft apps.
  - **Professional note:** Agents built with it can be connected agents in Copilot Studio (preview on the standard harness), and the SDK can embed Copilot Studio agents in web or native apps.
  - [Learn more](https://learn.microsoft.com/en-us/microsoft-365/agents-sdk/agents-sdk-overview) · **Covered in:** [Module 18](18-Advanced-Agent-Development/README.md), [Module 19](19-Enterprise-Copilot-Architecture/README.md)
- **Microsoft 365 Copilot** — Microsoft's AI assistant for work, integrated into Microsoft 365 apps. Licensing tiers are Copilot Chat (Basic), Microsoft 365 Copilot (Basic), and Microsoft 365 Copilot (Premium, the add-on license grounded in work data through Microsoft Graph and Work IQ).
  - **Professional note:** The Microsoft 365 Copilot *app* is now called Microsoft Copilot. A Microsoft 365 Copilot license lets users build Microsoft Copilot harness agents in Copilot Studio, and some standard-harness agent usage in Copilot Chat, Teams, and SharePoint isn't charged when it runs with a licensed user's identity.
  - 💳 **Licensing/Region** · [Learn more](https://learn.microsoft.com/en-us/copilot/plan/copilot-overview) · **Covered in:** [Module 01](01-Introduction-to-Copilot-Studio/README.md), [Module 03](03-Environment-and-Setup/README.md)
- **Microsoft 365 Copilot plugin** — A package that bundles skills, tools such as MCP servers, and agents so people can find, install, and use them directly in supported Copilot experiences; admins manage plugins in the Microsoft 365 admin center.
  - **Professional note:** Tools inside your Copilot Studio agent are different — your agent decides when to use them. Agents you make available in Teams and Microsoft Copilot are added to the Microsoft plugin registry. Older Copilot Studio material also used "plugin" for what are now tools.
  - [Learn more](https://learn.microsoft.com/en-us/microsoft-365/copilot/extensibility/) · **Covered in:** [Module 11](11-Agent-Tools-and-Capabilities/README.md), [Module 19](19-Enterprise-Copilot-Architecture/README.md)
- **Microsoft Agent 365** — Microsoft's observability and control platform for AI agents across an organization, built on four pillars: management, governance, security, and business value (agent registry, agent map, policy templates, Purview audit).
  - **Professional note:** Onboard Copilot Studio agents for centralized identity representation in Microsoft Entra, Conditional Access, access governance, and observability. Some features, such as agent accounts, need Agent 365 licensing.
  - 💳 **Licensing/Region** · [Learn more](https://learn.microsoft.com/en-us/microsoft-agent-365/overview) · **Covered in:** [Module 17](17-Agent-Management-and-Governance/README.md), [Module 19](19-Enterprise-Copilot-Architecture/README.md)
- **Microsoft Contact Center Intelligence** — Microsoft's contact center intelligence product and portal, with connectors (for example Genesys Cloud), real-time and historical dashboards, and quality assurance.
  - **Professional note:** You can build Customer Conversation harness agents in its portal, and only the portal connects an agent to a live contact center; its customer conversations are billed in Copilot Credits.
  - 💳 **Licensing/Region** · [Learn more](https://learn.microsoft.com/en-us/contact-center-intelligence/) · **Covered in:** [Module 18](18-Advanced-Agent-Development/README.md), [Module 19](19-Enterprise-Copilot-Architecture/README.md)
- **Microsoft Copilot (app, including consumer use)** — Microsoft's Copilot app on web, desktop, and mobile (copilot.cloud.microsoft). It's the new name of the Microsoft 365 Copilot app and serves both work (Microsoft Entra) accounts and personal Microsoft accounts.
  - **Professional note:** "Consumer" Copilot means using Microsoft Copilot with a personal Microsoft account; it isn't where you build Copilot Studio agents. *Teams and Microsoft Copilot* is a Copilot Studio publishing channel for work users.
  - [Learn more](https://learn.microsoft.com/en-us/copilot/plan/copilot-overview) · **Covered in:** [Module 01](01-Introduction-to-Copilot-Studio/README.md), [Module 14](14-Publishing-and-Channels/README.md)
- **Microsoft Copilot Chat (formerly Microsoft 365 Copilot Chat)** — Secure, enterprise AI chat included with eligible Microsoft 365 licenses (Copilot Chat (Basic)); it's grounded mainly in web data unless users provide work content or use agents.
  - **Professional note:** Declarative agents grounded in instructions and public websites are included; access to custom or other agents is pay-as-you-go.
  - 💳 **Licensing/Region** · [Learn more](https://learn.microsoft.com/en-us/copilot/plan/copilot-overview) · **Covered in:** [Module 01](01-Introduction-to-Copilot-Studio/README.md)
- **Microsoft Copilot harness** — The default harness behind Copilot Studio's new experience, built for reasoning-heavy, multistep work: it breaks goals into steps, calls tools across connectors, knowledge, MCP, and connected agents, recovers from failures, and natively creates and edits Word, Excel, PowerPoint, and PDF files.
  - **Professional note:** It has no topics, no separate prompts feature, and no child agents — use skills, workflows, connected agents, and task agents. Tasks run in a secure sandbox, and usage-based billing starts when you start building.
  - 🧪 **Preview** (production-ready, June 2026) · 💳 **Licensing/Region** · **Applies to:** Microsoft Copilot harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/overview) · **Covered in:** [Module 01](01-Introduction-to-Copilot-Studio/README.md), [Module 09](09-Generative-AI-and-Orchestration/README.md), [Module 19](19-Enterprise-Copilot-Architecture/README.md)
- **Microsoft Copilot Studio** — Microsoft's graphical, low-code studio for building and managing AI-powered agents and workflows, connecting them to organizational data and systems, and publishing them where users work. The web app is at copilotstudio.microsoft.com.
  - **Professional note:** The overview page lists three building blocks (agents, workflows, and agent flows), plus a separate app creation experience in preview. Everything you build runs on a harness. It was formerly Power Virtual Agents.
  - [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/fundamentals-what-is-copilot-studio) · **Covered in:** [Module 01](01-Introduction-to-Copilot-Studio/README.md)
- **Microsoft Entra Agent ID** — An identity type for AI agents in Microsoft Entra (a service principal with an "Agent" subtype) that gives each agent its own identity for governance.
  - **Professional note:** Copilot Studio automatically provisions Entra Agent IDs for new agents, and you can't opt out; older agents keep legacy app registrations. Use agent identities to scope connector permissions, Conditional Access, and DLP governance per agent.
  - [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/govern-agents-identities-overview) · **Covered in:** [Module 13](13-Authentication-and-Security/README.md), [Module 17](17-Agent-Management-and-Governance/README.md)
- **Microsoft Entra ID** — Microsoft's cloud identity and access management service (formerly Azure Active Directory) that signs users in and secures access to apps and data.
  - **Professional note:** **Authenticate with Microsoft** uses Entra ID automatically for Teams, Power Apps, and Microsoft Copilot. SharePoint, Dataverse, and Copilot connector knowledge use the user's Entra identity, so users see only content they can access.
  - [Learn more](https://learn.microsoft.com/en-us/entra/fundamentals/what-is-entra) · **Covered in:** [Module 13](13-Authentication-and-Security/README.md)
- **Microsoft Foundry** — Microsoft's Azure platform that brings agents, models (more than 10,000 from Microsoft, OpenAI, Anthropic, Meta, and others), and tools together with tracing, evaluation, and governance. Formerly Azure AI Studio / Azure AI Foundry.
  - **Professional note:** Foundry agents can be connected agents in Copilot Studio, Foundry IQ knowledge bases can ground Copilot Studio agents, and Copilot Studio prompts use models hosted in Foundry.
  - [Learn more](https://learn.microsoft.com/en-us/azure/foundry/what-is-foundry) · **Covered in:** [Module 18](18-Advanced-Agent-Development/README.md), [Module 19](19-Enterprise-Copilot-Architecture/README.md)
- **Microsoft Graph** — The data and API layer behind Microsoft 365 that represents a user's work context — emails, files, meetings, calendars, chats, and organizational relationships.
  - **Professional note:** Microsoft 365 Copilot (Premium) grounds answers in Microsoft Graph and Work IQ, and Copilot connectors bring non-Microsoft data into Graph for agents to use.
  - [Learn more](https://learn.microsoft.com/en-us/copilot/plan/copilot-overview) · **Covered in:** [Module 10](10-Knowledge-Sources-and-Grounding/README.md)
- **Microsoft Purview** — Microsoft's family of data security, governance, and compliance solutions, including classification, sensitivity labels, data loss prevention, and audit.
  - **Professional note:** Copilot Studio maker audit logs and runtime security audit telemetry flow into Purview, and Purview helps you manage data security and compliance for Copilot Studio agents.
  - [Learn more](https://learn.microsoft.com/en-us/purview/ai-copilot-studio) · **Covered in:** [Module 13](13-Authentication-and-Security/README.md), [Module 17](17-Agent-Management-and-Governance/README.md)
- **Mobile app (channel)** — Connecting an agent to a native mobile or custom app through Direct Line, using the token endpoint shown on the channel's Mobile app page.
  - **Professional note:** Secure the channel and handle authentication in your app; see Direct Line.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/publication-connect-bot-to-custom-application) · **Covered in:** [Module 14](14-Publishing-and-Channels/README.md)
- **Monitor page / Monitor tab** — Where you see an agent's usage and health. In the new experience it shows sessions, users, autonomous runs, success and failure rates, reactions, and estimated Copilot Credits; in the classic experience it holds the analytics dashboards.
  - **Professional note:** You can open Monitor before publishing, but production data appears only after people use the published agent. Use admin tools for fleet-wide monitoring across agents and environments.
  - **Applies to:** all harnesses · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/analytics-overview) · **Covered in:** [Module 04](04-Copilot-Studio-Interface/README.md), [Module 16](16-Analytics-and-Monitoring/README.md)
- **Multilingual agent** — An agent configured to converse with users in more than one language.
  - **Professional note:** Plan languages at design time and test each one; check the language support article for what's available per feature.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/multilingual) · **Covered in:** [Module 05](05-Creating-Your-First-Agent/README.md)
- **Multiple Topics Matched (system topic)** — Also called "did you mean": it asks the user to choose when a message closely matches several topics, and records the choice in a system variable.
  - **Professional note:** Frequent triggering is a sign of overlapping trigger phrases or descriptions — refine them.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-system-topics) · **Covered in:** [Module 07](07-Topics-and-Conversation-Design/README.md)

## N

- **Natural language processing (NLP)** — The branch of AI that lets computers process and analyze human language, for example to detect language, sentiment, key phrases, or named entities.
  - **Professional note:** Copilot Studio uses NLP throughout — to understand user messages, extract entities, and decide which topic, tool, or knowledge source to use.
  - [Learn more](https://learn.microsoft.com/en-us/azure/ai-services/language-service/overview) · **Covered in:** [Module 01](01-Introduction-to-Copilot-Studio/README.md)
- **Natural language understanding (NLU)** — The part of NLP focused on working out the meaning and intent behind a user's words.
  - **Professional note:** The standard harness offers generative AI (default) or three classic options: **NLU** (5–20 short phrases per topic), **NLU+** (higher accuracy for large enterprise agents; needs a Dynamics 365 Contact Center license), and **CLU** (your own Azure model).
  - 💳 **Licensing/Region** (NLU+) · **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/nlu-overview) · **Covered in:** [Module 07](07-Topics-and-Conversation-Design/README.md), [Module 09](09-Generative-AI-and-Orchestration/README.md)
- **New experience** — Copilot Studio's default interface for creating Microsoft Copilot harness agents (and Customer Conversation harness agents), with the Build tab, Agent settings dialog, Preview tab, and Monitor.
  - **Professional note:** You can't configure Copilot Studio to always create agents in the classic experience; existing standard-harness agents still open from the **Agents** or **Workflows** lists.
  - 🧪 **Preview** (Microsoft Copilot harness, production-ready) · **Applies to:** Microsoft Copilot and Customer Conversation harnesses · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/switch-experiences) · **Covered in:** [Module 04](04-Copilot-Studio-Interface/README.md)
- **Node** — One step on a topic's authoring canvas, such as sending a message, asking a question, branching, setting a variable, calling a tool, or redirecting.
  - **Professional note:** Node families are Message, Question, Adaptive Card, Condition, Variable management, Topic management (redirect, transfer, end), Tool, and Advanced (generative answers, HTTP requests, events, and more). Rename nodes so complex topics stay readable.
  - **Applies to:** standard and Customer Conversation harnesses · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-create-edit-topics#node-types) · **Covered in:** [Module 07](07-Topics-and-Conversation-Design/README.md)

## O

- **OAuth 2.0** — An industry-standard authorization protocol that lets an app obtain a token to access a protected resource on a user's behalf, without handling the user's password.
  - **Professional note:** Manual authentication in Copilot Studio can use Microsoft Entra ID or another OAuth 2.0 identity provider, such as Google or Facebook; Entra Agent IDs still use OAuth-based authentication flows.
  - [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/configuration-end-user-authentication) · **Covered in:** [Module 13](13-Authentication-and-Security/README.md)
- **Official source** — A standard-harness knowledge source you mark as highly trusted, so the agent can use it directly without verification and flags such answers distinctively.
  - **Professional note:** It isn't compatible with generative orchestration — it only works when generative orchestration is off.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/knowledge-copilot-studio#official-sources) · **Covered in:** [Module 10](10-Knowledge-Sources-and-Grounding/README.md)
- **On Error (system topic)** — The system topic that tells users an error occurred, showing an error code, the conversation ID, and a timestamp (with more detail in the test panel).
  - **Professional note:** It handles user-facing errors, not system errors. Record the error code and conversation ID when troubleshooting; HTTP request nodes can be set to store errors in variables instead of triggering it.
  - **Applies to:** standard harness (a built-in *event* in the Customer Conversation harness) · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-system-topics) · **Covered in:** [Module 07](07-Topics-and-Conversation-Design/README.md), [Module 15](15-Testing-and-Debugging/README.md)
- **OneDrive for Business (knowledge source)** — Files in personal or shared OneDrive that an agent can reference as knowledge, with support for Microsoft Purview sensitivity labels.
  - **Professional note:** Admins control SharePoint and OneDrive knowledge together in the Power Platform admin center's knowledge-source settings.
  - **Applies to:** standard and Microsoft Copilot harnesses · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/knowledge-sources-overview) · **Covered in:** [Module 10](10-Knowledge-Sources-and-Grounding/README.md)
- **OpenAPI specification** — A standard, machine-readable description of a REST API's operations, inputs, outputs, and authentication (formerly known as a Swagger file).
  - **Professional note:** REST API tools in Copilot Studio must be created from an OpenAPI v2 specification, and custom connectors are also defined from OpenAPI definitions.
  - [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agent-extend-action-rest-api) · **Covered in:** [Module 11](11-Agent-Tools-and-Capabilities/README.md)

## P

- **Pay-as-you-go (PAYG)** — Paying monthly through an Azure subscription for the Copilot Credits your agents actually use, with no upfront commitment.
  - **Professional note:** Link environments to an Azure subscription with a billing policy in the Power Platform admin center; a pay-as-you-go meter can also absorb overage when allocated capacity runs out.
  - 💳 **Licensing/Region** · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/billing-licensing#copilot-studio-pay-as-you-go) · **Covered in:** [Module 03](03-Environment-and-Setup/README.md), [Module 17](17-Agent-Management-and-Governance/README.md)
- **Power Fx** — Microsoft's low-code, Excel-like formula language used across Power Platform.
  - **Professional note:** In topics, use Power Fx to set variables, parse text, and write conditions, with scope prefixes `Topic.`, `Global.`, and `System.`. Formulas use US-style numbers (period as the decimal separator, comma between parameters). Power Fx expressions aren't migrated by the harness upgrade.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-power-fx) · **Covered in:** [Module 08](08-Variables-and-Entities/README.md)
- **Power Platform** — Microsoft's low-code platform family — including Power Apps, Power Automate, Power Pages, and Copilot Studio — that shares environments, Dataverse, connectors, and governance.
  - **Professional note:** You need only its fundamentals for Copilot Studio: environments, Dataverse, connectors, solutions, security roles, and admin controls.
  - [Learn more](https://learn.microsoft.com/en-us/power-platform/) · **Covered in:** [Module 02](02-Power-Platform-Fundamentals/README.md)
- **Power Platform admin center** — The web portal where admins manage environments, capacity and billing, data policies, security, and Copilot Studio settings.
  - **Professional note:** Copilot Studio controls here include the Copilot Studio authors setting, allowed knowledge sources, channel access, credit allocations and agent spending limits, billing policies, and the agent inventory.
  - [Learn more](https://learn.microsoft.com/en-us/power-platform/admin/admin-documentation) · **Covered in:** [Module 02](02-Power-Platform-Fundamentals/README.md), [Module 17](17-Agent-Management-and-Governance/README.md)
- **Power Platform connector (real-time knowledge)** — Using a Power Platform connector as a knowledge source that's queried live at runtime; Microsoft indexes only metadata, such as table and column names, not the data itself.
  - **Professional note:** Use it when answers depend on current data in systems such as CRM or ITSM, and you don't want to replicate that data.
  - 🧪 **Preview** · **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/knowledge-real-time-connectors) · **Covered in:** [Module 10](10-Knowledge-Sources-and-Grounding/README.md)
- **Power Virtual Agents (PVA)** — Microsoft's former low-code chatbot product; it became part of Microsoft Copilot Studio, announced in November 2023.
  - **Professional note:** Bots built with PVA are now *classic chatbots* that don't support generative AI features until you clone and convert them. The legacy PVA license is no longer sold — use "Copilot Studio" and "agent" for anything current.
  - ⛔ **Retired** (product name and legacy license) · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/unified-authoring-conversion) · **Covered in:** [Module 01](01-Introduction-to-Copilot-Studio/README.md)
- **Prebuilt entity** — A ready-made entity — such as Age, City, Date and time, Email, Money, Number, Person name, or Phone number — that Copilot Studio recognizes without setup.
  - **Professional note:** Each prebuilt entity maps to a variable base type (for example, Date and time maps to DateTime), which determines how you can use the value later.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-entities-slot-filling#prebuilt-entities) · **Covered in:** [Module 08](08-Variables-and-Entities/README.md)
- **Premium connector** — A connector category available only in select Copilot Studio plans, unlike standard connectors, which are included in all plans.
  - **Professional note:** The standalone Copilot Studio subscription lets agents connect to any data with premium connectors; confirm licensing before you design around one.
  - 💳 **Licensing/Region** · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-connectors) · **Covered in:** [Module 11](11-Agent-Tools-and-Capabilities/README.md)
- **Prepaid Copilot Credit pack** — A subscription that provides a fixed quantity of Copilot Credits for the tenant.
  - **Professional note:** Purchased capacity is enforced monthly and unused credits don't carry over; a tenant prepaid pack is also a prerequisite for assigning the free Copilot Studio user license.
  - 💳 **Licensing/Region** · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/billing-licensing#copilot-studio-prepaid-copilot-credits-subscription) · **Covered in:** [Module 03](03-Environment-and-Setup/README.md), [Module 17](17-Agent-Management-and-Governance/README.md)
- **Prepurchase plan (Copilot Credits)** — A one-year prepaid option, bought in the Azure portal, that provides a pool of Copilot Credit Commit Units (CCCUs) usable across eligible Microsoft products.
  - **Professional note:** It requires a billing policy linked to your Azure subscription in the Power Platform admin center.
  - 💳 **Licensing/Region** · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/billing-licensing#copilot-credits-prepurchase-plan) · **Covered in:** [Module 17](17-Agent-Management-and-Governance/README.md), [Module 19](19-Enterprise-Copilot-Architecture/README.md)
- **Preview tab** — The testing area for Microsoft Copilot harness agents: interactive chat, prompt suggestions, the activity trace, conversation history, and response feedback, all before publishing.
  - **Professional note:** Previewing consumes Copilot Credits on this harness, so plan test sessions and reuse evaluations.
  - 💳 **Licensing/Region** · **Applies to:** Microsoft Copilot harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/preview-overview) · **Covered in:** [Module 04](04-Copilot-Studio-Interface/README.md), [Module 15](15-Testing-and-Debugging/README.md)
- **Primary AI model** — The language model an agent uses for orchestration and responses.
  - **Professional note:** Options include generally available, preview, and experimental models, including external providers; some may process data outside your geography or be unavailable in GCC. Defaults change over time, and you can stay on the current model for up to 30 days after a default upgrade.
  - 💳 **Licensing/Region** · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-select-agent-model) · **Covered in:** [Module 09](09-Generative-AI-and-Orchestration/README.md)
- **Production environment** — An environment intended for permanent, business-critical work, where published agents serve real users.
  - **Professional note:** Deploy to production with managed solutions from your development pipeline rather than building directly in production.
  - [Learn more](https://learn.microsoft.com/en-us/power-platform/admin/environments-overview) · **Covered in:** [Module 02](02-Power-Platform-Fundamentals/README.md), [Module 19](19-Enterprise-Copilot-Architecture/README.md)
- **Prompt** — The natural-language instruction, plus any context, that you give a generative AI model to perform a task.
  - **Professional note:** In Copilot Studio, a *prompt* is also a reusable asset — built in the prompt builder with inputs, knowledge, and a model — that you can use as an agent tool, in topics, or in agent flows and workflows.
  - **Applies to:** standard harness (prompt assets) · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/prompts-overview) · **Covered in:** [Module 12](12-Prompts-and-Generative-Answers/README.md)
- **Prompt builder** — Copilot Studio's experience for building, testing, and saving reusable prompts with input variables, knowledge, model settings, JSON output, and content-moderation sensitivity.
  - **Professional note:** Prompts need Copilot Credits and a Dataverse-enabled environment in a supported region. The Microsoft Copilot harness has no separate prompts feature — use skills there.
  - 💳 **Licensing/Region** · **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/create-custom-prompt) · **Covered in:** [Module 12](12-Prompts-and-Generative-Answers/README.md)
- **Prompt engineering** — The practice of designing and refining prompts — clear instructions, context, examples, and output format — to get reliable results from a model.
  - **Professional note:** Apply it to agent instructions, descriptions, and prompt tools; for example, asking the model to cite its sources makes statements more likely to be grounded.
  - [Learn more](https://learn.microsoft.com/en-us/azure/foundry/openai/concepts/prompt-engineering) · **Covered in:** [Module 06](06-Agent-Configuration-and-Instructions/README.md), [Module 12](12-Prompts-and-Generative-Answers/README.md)
- **Public website (knowledge source)** — Public web pages an agent searches (through Bing, limited to the sites you list) to answer questions.
  - **Professional note:** Standard-harness limits are 25 websites with generative orchestration and 4 URLs with classic orchestration. Confirm which sites your organization owns, and note that admins can block public website knowledge.
  - **Applies to:** standard and Microsoft Copilot harnesses · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/knowledge-add-public-website) · **Covered in:** [Module 10](10-Knowledge-Sources-and-Grounding/README.md)
- **Publishing** — Making the latest saved version of an agent available on its connected channels.
  - **Professional note:** On the standard harness, publishing updates all channels at once, and users get new content in their next session (most channels end a session after 30 minutes of inactivity; type "start over" in Teams to test right away). Trial licenses can't publish.
  - **Applies to:** all harnesses · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/publication-fundamentals-publish-channels) · **Covered in:** [Module 05](05-Creating-Your-First-Agent/README.md), [Module 14](14-Publishing-and-Channels/README.md)

## Q

- **Quarantine (agent)** — An admin action, through the Power Platform API, that isolates a noncompliant agent while it's investigated.
  - **Professional note:** Makers can still test a quarantined agent in Copilot Studio, but no one can use it in any other channel while it's quarantined.
  - [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/admin-api-quarantine) · **Covered in:** [Module 17](17-Agent-Management-and-Governance/README.md)
- **Question node** — A topic node that asks the user a question and saves the answer, recognized through an entity, to a variable.
  - **Professional note:** Configure validation, reprompts (up to two by default), and what happens when no valid answer arrives — for example, escalate.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-ask-a-question) · **Covered in:** [Module 07](07-Topics-and-Conversation-Design/README.md), [Module 08](08-Variables-and-Entities/README.md)

## R

- **RAG (retrieval-augmented generation)** — A pattern in which a system first retrieves relevant content (from search or a database) and then gives it to a model to generate an answer grounded in that content.
  - **Professional note:** Copilot Studio's knowledge features apply this pattern for you — for example, Dataverse knowledge uses a retrieval-augmented technique — so your job is choosing, curating, and securing the sources.
  - [Learn more](https://learn.microsoft.com/en-us/azure/search/retrieval-augmented-generation-overview) · **Covered in:** [Module 10](10-Knowledge-Sources-and-Grounding/README.md)
- **Redirect node** — A topic management node that sends the conversation to another topic, optionally passing inputs and receiving outputs.
  - **Professional note:** Use redirects to reuse common sub-dialogs; system topics such as End of Conversation and Reset Conversation run when another topic redirects to them.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-managing-topic-inputs-outputs) · **Covered in:** [Module 07](07-Topics-and-Conversation-Design/README.md)
- **Regex entity** — A custom entity that matches a pattern, such as an order-number format, with a regular expression.
  - **Professional note:** Matching is case-sensitive by default (add `(?i)` for case-insensitive). NLU and CLU use .NET syntax; NLU+ uses JavaScript syntax.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-entities-slot-filling#regular-expression-regex-entities) · **Covered in:** [Module 08](08-Variables-and-Entities/README.md)
- **Reset Conversation (system topic)** — The system topic that clears variable values and makes the agent use its latest published version; it runs when another topic redirects to it.
  - **Professional note:** It doesn't clear conversation history by default — add a **Clear variable values** node with the conversation-history option if you need that.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-system-topics) · **Covered in:** [Module 07](07-Topics-and-Conversation-Design/README.md)
- **Responsible AI** — Developing and using AI with care for the whole system — the technology, the people who use it, the people affected by it, and the environment where it's deployed — guided by Microsoft's AI principles.
  - **Professional note:** Copilot Studio publishes a Platform Card and Responsible AI FAQs for its AI features. Combine content moderation, grounding, evaluations (including safety evaluators), transparency with users, and human review.
  - [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/responsible-ai-overview) · **Covered in:** [Module 06](06-Agent-Configuration-and-Instructions/README.md), [Module 09](09-Generative-AI-and-Orchestration/README.md), [Module 13](13-Authentication-and-Security/README.md)
- **REST API tool** — A tool that calls selected endpoints of a REST API described by an OpenAPI specification, with authentication details and descriptions that tell the model when to call it.
  - **Professional note:** It must be created from an OpenAPI v2 specification. The Customer Conversation harness also offers REST API tools.
  - 🧪 **Preview** (standard harness) · **Applies to:** standard and Customer Conversation harnesses · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agent-extend-action-rest-api) · **Covered in:** [Module 11](11-Agent-Tools-and-Capabilities/README.md)

## S

- **Sandbox environment** — A non-production environment for development and testing that supports operations such as copy and reset.
  - **Professional note:** Use sandboxes for development and test stages of your ALM pipeline; admins can restrict who creates them.
  - [Learn more](https://learn.microsoft.com/en-us/power-platform/admin/sandbox-environments) · **Covered in:** [Module 02](02-Power-Platform-Fundamentals/README.md), [Module 03](03-Environment-and-Setup/README.md)
- **Security role** — A Dataverse role that grants a set of privileges in an environment — for example Environment Maker, System Administrator, or Bot Transcript Viewer.
  - **Professional note:** Coauthors need Environment Maker; users need the ChatBotReaders privilege (included in Environment Maker) to chat with agents in an environment; transcript access needs Bot Transcript Viewer. Security roles are also the main control over who can build Microsoft Copilot harness agents.
  - [Learn more](https://learn.microsoft.com/en-us/power-platform/admin/security-roles-privileges) · **Covered in:** [Module 02](02-Power-Platform-Fundamentals/README.md), [Module 13](13-Authentication-and-Security/README.md), [Module 17](17-Agent-Management-and-Governance/README.md)
- **Semantic search** — Search that finds results by meaning rather than exact keywords, typically using embeddings (vectors).
  - **Professional note:** The standard-harness setting **Tenant graph grounding with semantic search** uses the Microsoft 365 semantic index to improve SharePoint and connector retrieval. It requires **Authenticate with Microsoft** and a Microsoft 365 Copilot license in the tenant, and it costs extra.
  - 💳 **Licensing/Region** · **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/knowledge-copilot-studio#tenant-graph-grounding-with-semantic-search) · **Covered in:** [Module 10](10-Knowledge-Sources-and-Grounding/README.md)
- **Sensitivity label** — A Microsoft Purview classification (for example *Confidential*) applied to documents and data that can encrypt content and control how it's shared.
  - **Professional note:** Copilot Studio supports sensitivity labels to help prevent oversharing, but uploaded files that are encrypted, password-protected, or labeled confidential or highly confidential can't be indexed as knowledge.
  - [Learn more](https://learn.microsoft.com/en-us/purview/sensitivity-labels) · **Covered in:** [Module 13](13-Authentication-and-Security/README.md)
- **Session** — One continuous interaction between a user (or an event) and an agent; analytics classify each session's outcome as resolved, escalated, abandoned, or unengaged.
  - **Professional note:** In most channels, a session ends after 30 minutes of inactivity, and newly published content applies from the next session.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/analytics-improve-agent-effectiveness) · **Covered in:** [Module 16](16-Analytics-and-Monitoring/README.md)
- **SharePoint (knowledge source)** — SharePoint sites, libraries, files, and (in the new experience) lists that an agent searches to answer questions, using each user's own permissions.
  - **Professional note:** Standard-harness limits are 25 URLs with generative orchestration and 4 per generative answers node with classic orchestration. Give documents clear, descriptive titles — titles help the agent pick the right content.
  - **Applies to:** standard and Microsoft Copilot harnesses · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/knowledge-add-sharepoint) · **Covered in:** [Module 10](10-Knowledge-Sources-and-Grounding/README.md)
- **Sign in (system topic)** — The system topic that prompts users to sign in when user authentication is turned on; it runs at the start of the conversation or when a node needs authentication variables.
  - **Professional note:** Test sign-in on every channel you publish to, because authentication behavior differs by channel.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-system-topics) · **Covered in:** [Module 07](07-Topics-and-Conversation-Design/README.md), [Module 13](13-Authentication-and-Security/README.md)
- **Single sign-on (SSO)** — Signing users in automatically with an identity they're already signed in with, so they don't have to authenticate again.
  - **Professional note:** Copilot Studio supports SSO with Microsoft Entra ID for websites, SSO in Teams, and SSO with generic OAuth providers; each has its own app registration and configuration steps.
  - [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/configure-sso) · **Covered in:** [Module 13](13-Authentication-and-Security/README.md)
- **Skill (agent skill)** — A reusable package of Markdown instructions (and optionally scripts and resources) with a name and description, which an agent activates when a request matches its purpose.
  - **Professional note:** On the Microsoft Copilot harness, skills replace standard-harness prompts and topics; create them from blank, generate them with AI, or upload them, then share or export them. The Customer Conversation harness has generative skills and topic skills. Marketplace-shared skills are in preview.
  - 🧪 **Preview** (shared skills) · **Applies to:** Microsoft Copilot and Customer Conversation harnesses · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/skills-overview) · **Covered in:** [Module 12](12-Prompts-and-Generative-Answers/README.md), [Module 18](18-Advanced-Agent-Development/README.md)
- **Slot filling** — Saving an entity value extracted from the user's message into a variable; *proactive slot filling* captures several values from a single message.
  - **Professional note:** Watch variable values in the test panel to confirm that slot filling works, and design questions so users can answer naturally.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-entities-slot-filling#slot-filling) · **Covered in:** [Module 08](08-Variables-and-Entities/README.md)
- **Solution** — A Power Platform package that holds agents and their related components so you can move them between environments.
  - **Professional note:** Every Copilot Studio agent is created in a solution. Use custom solutions and pipelines for development → test → production, and avoid periods in topic names because they block export.
  - [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-solutions-overview) · **Covered in:** [Module 02](02-Power-Platform-Fundamentals/README.md), [Module 17](17-Agent-Management-and-Governance/README.md), [Module 19](19-Enterprise-Copilot-Architecture/README.md)
- **Standard harness** — Copilot Studio's rule-based harness, used in the classic experience: you define topics, prompts, and paths for predictable behavior, and it can also use generative orchestration and generative answers from knowledge.
  - **Professional note:** It's fully supported with no forced switch, and it's billed after publishing under the standard licensing model. Choose it for well-defined, consistent conversations.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/harnesses-overview) · **Covered in:** [Module 01](01-Introduction-to-Copilot-Studio/README.md), [Module 07](07-Topics-and-Conversation-Design/README.md), [Module 19](19-Enterprise-Copilot-Architecture/README.md)
- **Sub-agent** — A specialist agent built inside a Customer Conversation harness primary agent (for example billing or technical support) that shares the primary agent's configuration, deployment, and ALM.
  - **Professional note:** Use a connected agent instead when the specialist needs its own owner, ALM, or reuse across several primary agents.
  - 🧪 **Preview** · **Applies to:** Customer Conversation harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/sub-agents-overview-customer-conversation) · **Covered in:** [Module 18](18-Advanced-Agent-Development/README.md)
- **Suggested prompts (conversation starters)** — Up to 10 example prompts shown on an agent's welcome page in Teams and Microsoft Copilot to help users start a conversation.
  - **Professional note:** Copilot Studio can generate them from your description and instructions; they don't appear in the Copilot Studio test panel. In the new experience, configure them on the **Greeting & prompts** tab.
  - **Applies to:** standard and Microsoft Copilot harnesses · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/configure-starter-prompts) · **Covered in:** [Module 05](05-Creating-Your-First-Agent/README.md)
- **System topic** — A built-in standard-harness topic for common events: Conversation Start, Conversational boosting, End of Conversation, Escalate, Fallback, Multiple Topics Matched, On Error, Reset Conversation, and Sign in.
  - **Professional note:** You can't create or delete system topics, but you can turn them off or customize them — wait until you can build complete conversations first.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-system-topics) · **Covered in:** [Module 07](07-Topics-and-Conversation-Design/README.md)
- **System variable** — A variable Copilot Studio creates automatically with context about the conversation, user, or channel (for example `Activity.Channel` or `User.DisplayName`).
  - **Professional note:** In Power Fx, add the `System.` prefix — for example `System.User.DisplayName`.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-variables-about) · **Covered in:** [Module 08](08-Variables-and-Entities/README.md)

## T

- **Task agent** — A helper that a parent agent uses for a focused assignment — research, analysis, or review — with its own context window, returning its findings to the parent.
  - **Professional note:** Guide task agents through instructions or skills; you don't create or publish a separate agent. Task agents are available only in early release cycle environments.
  - **Applies to:** Microsoft Copilot harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/task-agents-overview) · **Covered in:** [Module 18](18-Advanced-Agent-Development/README.md)
- **Teams and Microsoft Copilot (channel)** — The Copilot Studio channel that makes an agent available in Microsoft Teams and Microsoft Copilot (older material says "Teams and Microsoft 365 Copilot").
  - **Professional note:** Use **Authenticate with Microsoft**. The agent is added to the Microsoft plugin registry (Agent Store, organization catalog, Microsoft 365 admin center); install it for yourself and test before making it available to others.
  - **Applies to:** standard and Microsoft Copilot harnesses · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/publication-add-bot-to-microsoft-teams) · **Covered in:** [Module 14](14-Publishing-and-Channels/README.md)
- **Telephony / voice-enabled agent (IVR)** — An agent that customers can call on the phone; Copilot Studio supports basic voice agents and real-time voice agents for interactive voice response.
  - **Professional note:** You need a phone number through Azure Communication Services, typically with Dynamics 365 Contact Center. Voice options include DTMF, hold and resume, consent-based recording, and post-call actions; real-time voice agents arrived in preview in April 2026, so check their current status.
  - 💳 **Licensing/Region** · **Applies to:** standard and Customer Conversation harnesses · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/voice-overview) · **Covered in:** [Module 14](14-Publishing-and-Channels/README.md)
- **Template (agent template)** — A prebuilt agent (for example IT Helpdesk, Benefits, Safe Travels, Sustainability Insights, Weather, or Website Q&A) that you create and then customize.
  - **Professional note:** The template's configuration decides the new agent's orchestration method, so review its settings before you extend it.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/template-fundamentals) · **Covered in:** [Module 05](05-Creating-Your-First-Agent/README.md)
- **Test pane (Test your agent)** — The standard-harness chat panel where makers try the agent as a user while building, with topic tracking, variable values, and the activity map.
  - **Professional note:** Test activity isn't counted in analytics. The Microsoft Copilot harness equivalent is the Preview tab, which consumes credits.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-test-bot) · **Covered in:** [Module 04](04-Copilot-Studio-Interface/README.md), [Module 15](15-Testing-and-Debugging/README.md)
- **Test set** — A collection of test cases — questions or multi-turn conversations with expected responses or quality criteria — used by agent evaluations.
  - **Professional note:** Build test sets from a validated CSV template, from real user questions, or manually, and rerun them after every significant change as regression tests.
  - [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/analytics-agent-evaluation-create) · **Covered in:** [Module 15](15-Testing-and-Debugging/README.md)
- **Token** — A small chunk of text — a word, part of a word, or punctuation — that a language model reads and writes; models count input and output in tokens.
  - **Professional note:** Tokens drive context-window limits and, on the Microsoft Copilot harness, Copilot Credit charges, because LLM tokens are billed there.
  - [Learn more](https://learn.microsoft.com/en-us/dotnet/ai/conceptual/understanding-tokens) · **Covered in:** [Module 01](01-Introduction-to-Copilot-Studio/README.md), [Module 09](09-Generative-AI-and-Orchestration/README.md)
- **Tool** — A capability an agent can call to take action or fetch live data: connectors, custom connectors, agent flows, workflows, prompts, REST APIs, MCP servers, computer use, and more.
  - **Professional note:** With generative orchestration, the agent picks tools by name and description and asks users for missing inputs; in classic orchestration, tools run only from topics. Available tool types differ by harness, and data policies govern them.
  - **Applies to:** all harnesses · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/add-tools-custom-agent) · **Covered in:** [Module 11](11-Agent-Tools-and-Capabilities/README.md)
- **Topic** — A defined part of a conversation, built from nodes on an authoring canvas, that determines how an agent handles a particular need.
  - **Professional note:** Standard harness: system and custom topics, selected by description (generative orchestration) or trigger phrases (classic). Customer Conversation harness: deterministic topic skills. Microsoft Copilot harness: no topics — rebuild them as skills or workflows.
  - **Applies to:** standard and Customer Conversation harnesses · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-create-edit-topics) · **Covered in:** [Module 07](07-Topics-and-Conversation-Design/README.md)
- **Topic inputs and outputs** — Parameters a topic receives from, or returns to, the orchestrator or another topic.
  - **Professional note:** Generative orchestration can fill topic inputs from the conversation automatically; inputs and outputs are a cleaner way to pass data than global variables.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-managing-topic-inputs-outputs) · **Covered in:** [Module 08](08-Variables-and-Entities/README.md), [Module 09](09-Generative-AI-and-Orchestration/README.md)
- **Topic variable** — A variable usable only in the topic where it's created; this is the default scope.
  - **Professional note:** Reference it in Power Fx with the `Topic.` prefix; make it global or pass it through topic inputs and outputs when other topics need it.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-variables) · **Covered in:** [Module 08](08-Variables-and-Entities/README.md)
- **Transfer conversation node** — A topic management node that hands the conversation to a human through a connected engagement hub.
  - **Professional note:** Agents created in Copilot Studio don't include it in the Escalate topic by default; add it when you configure live-agent handoff.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-hand-off) · **Covered in:** [Module 07](07-Topics-and-Conversation-Design/README.md), [Module 18](18-Advanced-Agent-Development/README.md)
- **Trial license** — A Copilot Studio trial that lets individuals sign up to create and test agents.
  - **Professional note:** You can test in the test panel, but you can't publish; admins can assign trial licenses and block self-service sign-up.
  - 💳 **Licensing/Region** · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/billing-licensing#copilot-studio-trial-license) · **Covered in:** [Module 03](03-Environment-and-Setup/README.md)
- **Trigger (topic trigger)** — What starts a topic: **The agent chooses** (generative orchestration, based on name and description), **User says a phrase** (classic orchestration), or other types such as a received message, event, or activity, a redirect, or a completed plan.
  - **Professional note:** Don't confuse topic triggers with *event triggers*, which start the whole agent from an external event.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-triggers) · **Covered in:** [Module 07](07-Topics-and-Conversation-Design/README.md)
- **Trigger phrase** — An example phrase, keyword, or question that tells classic orchestration when to start a topic; users don't have to match it exactly.
  - **Professional note:** Learn recommends 5–10 short, varied trigger phrases per topic. With generative orchestration, the topic's description matters more.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-triggers) · **Covered in:** [Module 07](07-Topics-and-Conversation-Design/README.md)

## U

- **Unmanaged solution** — An editable solution used in development environments, where you build and change components.
  - **Professional note:** Export from development as managed for downstream environments, and keep the unmanaged solution as your source of truth.
  - [Learn more](https://learn.microsoft.com/en-us/power-platform/alm/solution-concepts-alm) · **Covered in:** [Module 02](02-Power-Platform-Fundamentals/README.md), [Module 17](17-Agent-Management-and-Governance/README.md)
- **Upgrade to the Microsoft Copilot harness** — A feature that copies a standard-harness agent onto the Microsoft Copilot harness, carrying over instructions, tools, and suggested prompts, rebuilding custom topics as skills or workflows, and producing a migration report.
  - **Professional note:** Knowledge sources, Power Fx expressions, and child agents aren't migrated, and the upgrade consumes credits — plan to reconnect knowledge and retest.
  - 🧪 **Preview** · 💳 **Licensing/Region** · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/upgrade-to-microsoft-copilot-from-standard-harness) · **Covered in:** [Module 19](19-Enterprise-Copilot-Architecture/README.md)
- **Uploaded files (knowledge source)** — Documents such as PDF, Word, Excel, or PowerPoint files that you upload to an agent as knowledge.
  - **Professional note:** Encrypted, password-protected, or confidential-labeled files aren't supported; admins can block local uploads; on the standard harness, uploaded files don't count toward the 25-source generative orchestration limit.
  - **Applies to:** standard and Microsoft Copilot harnesses · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/knowledge-add-file-upload) · **Covered in:** [Module 10](10-Knowledge-Sources-and-Grounding/README.md)
- **Usage-based billing** — Billing by actual consumption, measured in Copilot Credits, for LLM tokens, tools (including knowledge and MCP), and the harness itself.
  - **Professional note:** It applies to the Microsoft Copilot and Customer Conversation harnesses and starts when you start building. Admins can set environment credit allocations and per-agent limits; when credits run out, agents stop responding and makers can't preview or evaluate.
  - 💳 **Licensing/Region** · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/billing-credit-overview) · **Covered in:** [Module 03](03-Environment-and-Setup/README.md), [Module 17](17-Agent-Management-and-Governance/README.md)

## V

- **Variable** — A named container that stores information during a conversation, such as a user's answer, a tool result, or context.
  - **Professional note:** There are four scopes — topic, global, system, and environment — and base types including String, Boolean, Number, Table, Record, DateTime, Choice, and Blank. A variable's type is fixed after its first assignment.
  - **Applies to:** standard and Customer Conversation harnesses · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-variables-about) · **Covered in:** [Module 08](08-Variables-and-Entities/README.md)
- **Variable management node** — Nodes that set, parse, or clear variables, including clearing the conversation history the agent uses.
  - **Professional note:** Initialize variables with a literal value of the right type before assigning Power Fx results in looping topics, to avoid type errors.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-variables) · **Covered in:** [Module 07](07-Topics-and-Conversation-Design/README.md), [Module 08](08-Variables-and-Entities/README.md)
- **Visual Studio Code extension (Copilot Studio)** — A VS Code extension for cloning, editing, and synchronizing agent components outside the browser.
  - **Professional note:** Useful for advanced makers who want code-editor workflows and source control alongside the Copilot Studio UI.
  - 🟢 **GA** (January 2026) · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/visual-studio-code-extension-overview) · **Covered in:** [Module 18](18-Advanced-Agent-Development/README.md)

## W

- **Web search** — A setting (**Use information from the web** / **Web Search**) that lets an agent search all public websites indexed by Bing when a question could benefit from current web information.
  - **Professional note:** It requires generative orchestration and uses Grounding with Bing Search; review the data, privacy, and security implications before you turn it on for enterprise agents.
  - **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/data-privacy-security-web-search) · **Covered in:** [Module 10](10-Knowledge-Sources-and-Grounding/README.md)
- **WhatsApp (channel)** — A channel that lets customers chat with an agent on WhatsApp through an Azure Communication Services–based connection.
  - **Professional note:** Since 23 October 2026 you can't create new ACS-based WhatsApp connections; agents connected before that date keep working.
  - ⚠️ **Deprecated** · **Applies to:** standard harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/publication-add-bot-to-whatsapp) · **Covered in:** [Module 14](14-Publishing-and-Channels/README.md)
- **Work IQ** — The intelligence layer that grounds Microsoft Copilot and your agents in real-time organizational context — files, emails, meetings, chats, and business apps — through Data, Memory, and Inference layers.
  - **Professional note:** It's added by default to every new Microsoft Copilot harness agent with all available workloads selected, so narrow them to what the scenario needs. Write operations are on by default, subject to permissions and policies, and some workloads are in preview.
  - 🟢 **GA** (October 2026) · 💳 **Licensing/Region** · **Applies to:** Microsoft Copilot harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/add-work-iq) · **Covered in:** [Module 10](10-Knowledge-Sources-and-Grounding/README.md), [Module 18](18-Advanced-Agent-Development/README.md)
- **Workflow** — An automation built in Copilot Studio's drag-and-drop workflow designer and powered by the Microsoft Copilot harness, where steps can reason and act — combining agents, tools, AI actions, logic, and human-in-the-loop review.
  - **Professional note:** Workflows include nodes such as agent, Copilot, classification, and extract, consume capacity per action, and can be added to Microsoft Copilot harness agents as tools (preview). Agent flows remain the standard-harness format.
  - **Applies to:** Microsoft Copilot harness · [Learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/workflows-experience/flows-overview) · **Covered in:** [Module 11](11-Agent-Tools-and-Capabilities/README.md)

## Renamed and legacy terms

Use this table to translate older articles, videos, and interview questions into current terminology. Only changes verified on Microsoft Learn are listed; "terminology shift" means older official material used the former term and current documentation uses the new one, without a formal "formerly" note.

| Former term | Current term | When / notes | Source |
|---|---|---|---|
| Power Virtual Agents | Microsoft Copilot Studio | Announced November 2023 (Microsoft Ignite). PVA-era bots are now *classic chatbots*. | [Copilot Studio 2024 release wave 1 (archived): "formerly Power Virtual Agents"](https://learn.microsoft.com/en-us/previous-versions/power-platform/release-plan/2024wave1/microsoft-copilot-studio/) |
| Messages (billing unit) | Copilot Credits | 1 September 2025; no change to prepaid-pack quantity or pay-as-you-go rate. | [Standard harness licensing](https://learn.microsoft.com/en-us/microsoft-copilot-studio/billing-licensing) |
| Copilots / custom copilots | Agents | Terminology shift: 2023–2024 release plans say "copilots"; current docs say "agents." | [2024 release wave 2 (archived)](https://learn.microsoft.com/en-us/previous-versions/power-platform/release-plan/2024wave2/microsoft-copilot-studio/) · [Agents overview](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-overview) |
| Actions (and "plugins" in 2024 Copilot Studio material) | Tools | Terminology shift. In 2026, "plugin" means a **Microsoft 365 Copilot plugin** package, so don't map it to tools. | [2024 release wave 2 (archived)](https://learn.microsoft.com/en-us/previous-versions/power-platform/release-plan/2024wave2/microsoft-copilot-studio/) · [Add tools](https://learn.microsoft.com/en-us/microsoft-copilot-studio/add-tools-custom-agent) |
| Generative actions | Generative orchestration | Terminology shift; the current article's URL still ends in `advanced-generative-actions`. | [Orchestrate agent behavior with generative AI](https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-generative-actions) |
| Azure AI Studio / Azure AI Foundry | Microsoft Foundry | Brand consolidation listed in "Evolution of Foundry." | [What is Microsoft Foundry?](https://learn.microsoft.com/en-us/azure/foundry/what-is-foundry) |
| Azure AI Services | Foundry Tools | Same consolidation. | [What is Microsoft Foundry?](https://learn.microsoft.com/en-us/azure/foundry/what-is-foundry) |
| Microsoft Graph connectors | Copilot connectors | — | [Copilot connectors vs. Power Platform connectors](https://learn.microsoft.com/en-us/microsoft-copilot-studio/knowledge-graph-vs-power-platform-connectors) |
| Azure Active Directory | Microsoft Entra ID | — | [Variables overview](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-variables-about) |
| Microsoft 365 Copilot app | Microsoft Copilot (app) | 2026; primary URL moving to copilot.cloud.microsoft. The Copilot Studio channel is now labeled *Teams and Microsoft Copilot*. | [What is Microsoft Copilot?](https://learn.microsoft.com/en-us/copilot/plan/copilot-overview) · [Teams and Microsoft Copilot channel](https://learn.microsoft.com/en-us/microsoft-copilot-studio/publication-add-bot-to-microsoft-teams) |
| Microsoft 365 Copilot Chat app | Microsoft Copilot Chat | 2026. | [What is Microsoft Copilot?](https://learn.microsoft.com/en-us/copilot/plan/copilot-overview) |
| Swagger file | OpenAPI definition | Relevant to custom connectors and REST API tools. | [Custom connectors overview](https://learn.microsoft.com/en-us/connectors/custom-connectors/) |
| Records / fields (Dataverse) | Rows / columns | — | [What is Microsoft Dataverse?](https://learn.microsoft.com/en-us/power-apps/maker/data-platform/data-platform-intro) |
| Data loss prevention (DLP) policies | Data policies | Terminology shift; Learn URLs still contain `data-loss-prevention`. | [Data policies](https://learn.microsoft.com/en-us/power-platform/admin/wp-data-loss-prevention) |
| Classic chatbot (PVA or early Teams app) | Standard-harness agent | Clone and convert; retest before switching users. | [Upgrade a classic chatbot](https://learn.microsoft.com/en-us/microsoft-copilot-studio/unified-authoring-conversion) |
| Legacy Power Virtual Agents license (billed sessions) | Copilot Studio licensing with Copilot Credits | ⛔ **Retired** — no longer available for purchase since 1 January 2024. | [Legacy PVA sessions and capacity](https://learn.microsoft.com/en-us/microsoft-copilot-studio/requirements-sessions-management) |
| App registrations (agent identity) | Microsoft Entra Agent ID | New agents get Entra Agent IDs automatically (Learn cites May 2026 and July 2026); older agents keep legacy app registrations. | [Agent identities](https://learn.microsoft.com/en-us/microsoft-copilot-studio/govern-agents-identities-overview) · [What's new](https://learn.microsoft.com/en-us/microsoft-copilot-studio/whats-new) |
| Unmanaged developer environment | Managed developer environment | ⚠️ **Deprecated** — no new ones from 15 November 2026; existing ones suspended from 15 December 2026. | [Environments overview](https://learn.microsoft.com/en-us/power-platform/admin/environments-overview) |
| Dataverse for Teams environment | Dataverse environment (upgrade) | ⚠️ **Deprecated** — no new ones from 15 November 2026; suspended 15 September 2027; decommissioned 30 October 2027. | [Environments overview](https://learn.microsoft.com/en-us/power-platform/admin/environments-overview) |
| WhatsApp channel (Azure Communication Services–based) | — (no replacement named) | ⚠️ **Deprecated** — no new connections after 23 October 2026; existing connections continue. | [Publish to WhatsApp](https://learn.microsoft.com/en-us/microsoft-copilot-studio/publication-add-bot-to-whatsapp) |
| Suggested topics (topic suggestion feature) | — (deprecated) | Pending suggestions may still appear on a **Suggested topics** tab in older chatbots. | [Create and edit topics](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-create-edit-topics) |
| Topics, prompts, child agents (standard harness) | Skills, workflows, connected agents, task agents (Microsoft Copilot harness) | Concept mapping, not a rename: what to use instead when you build on, or upgrade to, the Microsoft Copilot harness. | [Microsoft Copilot harness FAQ](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/faqs-copilot-harness) |

> [!NOTE]
> Older Microsoft Learn articles and community content may still use former terms. When an article and this glossary disagree, trust the current Microsoft Learn page and its **Last updated** date.

## References

Official Microsoft Learn pages used to verify this glossary (all checked live on 18 November 2026):

### Microsoft Copilot Studio

- [About agent evaluation](https://learn.microsoft.com/en-us/microsoft-copilot-studio/analytics-agent-evaluation-intro)
- [About agents powered by the Microsoft Copilot harness](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/overview)
- [Access standard harness agents and agent flows](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/switch-experiences)
- [Add a child agent](https://learn.microsoft.com/en-us/microsoft-copilot-studio/add-agent-child-agent)
- [Add a generative answers node](https://learn.microsoft.com/en-us/microsoft-copilot-studio/nlu-boost-node)
- [Add a public website as a knowledge source](https://learn.microsoft.com/en-us/microsoft-copilot-studio/knowledge-add-public-website)
- [Add Azure AI Search as a knowledge source](https://learn.microsoft.com/en-us/microsoft-copilot-studio/knowledge-azure-ai-search)
- [Add Azure SQL tables and views as a knowledge source (Microsoft Copilot)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/knowledge-add-azure-sql-tables)
- [Add Bing Custom Search as a knowledge source](https://learn.microsoft.com/en-us/microsoft-copilot-studio/knowledge-bing-custom-search)
- [Add conditions to topics](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-using-conditions)
- [Add Dataverse tables as a knowledge source](https://learn.microsoft.com/en-us/microsoft-copilot-studio/knowledge-add-dataverse)
- [Add other agents overview](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-add-other-agents)
- [Add Power Platform connectors as knowledge (preview)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/knowledge-real-time-connectors)
- [Add SharePoint as a knowledge source](https://learn.microsoft.com/en-us/microsoft-copilot-studio/knowledge-add-sharepoint)
- [Add tools to custom agents](https://learn.microsoft.com/en-us/microsoft-copilot-studio/add-tools-custom-agent)
- [Agent flows overview](https://learn.microsoft.com/en-us/microsoft-copilot-studio/flows-overview)
- [Agent usage estimator](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agent-usage-estimator)
- [Agents overview](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-overview)
- [Agents powered by the Customer Conversation harness overview](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/overview-customer-conversation)
- [AI-based agent authoring overview](https://learn.microsoft.com/en-us/microsoft-copilot-studio/nlu-gpt-overview)
- [App registration, agent identities, and authentication](https://learn.microsoft.com/en-us/microsoft-copilot-studio/govern-agents-identities-overview)
- [Apps overview](https://learn.microsoft.com/en-us/microsoft-copilot-studio/apps-experience/apps-overview)
- [Ask a question](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-ask-a-question)
- [Assign user licenses and manage access](https://learn.microsoft.com/en-us/microsoft-copilot-studio/requirements-licensing)
- [Attach files to a conversation (Microsoft Copilot)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/attachments-overview)
- [Automate web and desktop apps with computer use](https://learn.microsoft.com/en-us/microsoft-copilot-studio/computer-use)
- [Available knowledge sources for agents (Microsoft Copilot)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/knowledge-sources-overview)
- [Billing rates and management](https://learn.microsoft.com/en-us/microsoft-copilot-studio/requirements-messages-management)
- [Configure and create multilingual agents](https://learn.microsoft.com/en-us/microsoft-copilot-studio/multilingual)
- [Configure Azure Bot Service skills for use in Copilot Studio agents](https://learn.microsoft.com/en-us/microsoft-copilot-studio/configuration-add-skills)
- [Configure customer-managed encryption keys](https://learn.microsoft.com/en-us/microsoft-copilot-studio/admin-customer-managed-keys)
- [Configure data policies for agents](https://learn.microsoft.com/en-us/microsoft-copilot-studio/admin-data-loss-prevention)
- [Configure settings for agents powered by the Microsoft Copilot harness](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/settings-overview)
- [Configure single sign-on with Microsoft Entra ID](https://learn.microsoft.com/en-us/microsoft-copilot-studio/configure-sso)
- [Configure suggested prompts for Teams and Copilot](https://learn.microsoft.com/en-us/microsoft-copilot-studio/configure-starter-prompts)
- [Configure the system fallback topic](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-system-fallback-topic)
- [Configure user authentication in Copilot Studio](https://learn.microsoft.com/en-us/microsoft-copilot-studio/configuration-end-user-authentication)
- [Connect and configure an agent for Teams and Microsoft Copilot](https://learn.microsoft.com/en-us/microsoft-copilot-studio/publication-add-bot-to-microsoft-teams)
- [Connect clients to your agent with the Model Context Protocol (MCP) and Agent2Agent (A2A) channels (Microsoft Copilot) (preview)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/publication-channels-mcp-agent-to-agent)
- [Connect to an agent over the Agent2Agent (A2A) protocol](https://learn.microsoft.com/en-us/microsoft-copilot-studio/add-agent-agent-to-agent)
- [Connect to Fabric IQ from an agent (Microsoft Copilot)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/fabric-iq-connect)
- [Connect to Foundry IQ from an agent (Microsoft Copilot)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/foundry-iq-connect)
- [Connect to Microsoft Copilot Studio with MCP](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/copilot-studio-mcp)
- [Control how transcripts are retained and accessed](https://learn.microsoft.com/en-us/microsoft-copilot-studio/admin-transcript-controls)
- [Copilot connectors versus Power Platform connectors as knowledge sources](https://learn.microsoft.com/en-us/microsoft-copilot-studio/knowledge-graph-vs-power-platform-connectors)
- [Create a custom agent from a template](https://learn.microsoft.com/en-us/microsoft-copilot-studio/template-fundamentals)
- [Create a prompt](https://learn.microsoft.com/en-us/microsoft-copilot-studio/create-custom-prompt)
- [Create a single response test set](https://learn.microsoft.com/en-us/microsoft-copilot-studio/analytics-agent-evaluation-create)
- [Create and edit topics](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-create-edit-topics)
- [Create and manage connections](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-connections)
- [Create and manage custom solutions](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-solutions-overview)
- [Create and share reusable component collections](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-export-import-copilot-components)
- [Create expressions using Power Fx](https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-power-fx)
- [Data locations in Copilot Studio](https://learn.microsoft.com/en-us/microsoft-copilot-studio/data-location)
- [Data, privacy, and security for web search](https://learn.microsoft.com/en-us/microsoft-copilot-studio/data-privacy-security-web-search)
- [Event triggers overview](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-triggers-about)
- [Events overview (Customer Conversation)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/events-overview-customer-conversation)
- [Extend your agent with Model Context Protocol](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agent-extend-action-mcp)
- [Extend your agent with tools from a REST API (preview)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agent-extend-action-rest-api)
- [FAQ for agents powered by the Microsoft Copilot harness](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/faqs-copilot-harness)
- [FAQ for generative answers](https://learn.microsoft.com/en-us/microsoft-copilot-studio/faqs-generative-answers)
- [Give your agent an account (Frontier)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/authoring-agent-account)
- [Hand off to a live agent](https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-hand-off)
- [Harnesses in Copilot Studio](https://learn.microsoft.com/en-us/microsoft-copilot-studio/harnesses-overview)
- [Hooks (Microsoft Copilot) (preview)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/hooks-overview)
- [Key concepts - Publish and deploy your agent](https://learn.microsoft.com/en-us/microsoft-copilot-studio/publication-fundamentals-publish-channels)
- [Knowledge sources summary](https://learn.microsoft.com/en-us/microsoft-copilot-studio/knowledge-copilot-studio)
- [Make HTTP requests](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-http-node)
- [Manage sessions and capacity for the legacy Power Virtual Agents license](https://learn.microsoft.com/en-us/microsoft-copilot-studio/requirements-sessions-management)
- [Manage topic inputs and outputs](https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-managing-topic-inputs-outputs)
- [Memory (Microsoft Copilot) (preview)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/memory-overview)
- [Microsoft Copilot Studio Agent inventory schema](https://learn.microsoft.com/en-us/microsoft-copilot-studio/admin-agent-inventory)
- [Monitor agent performance in Copilot Studio](https://learn.microsoft.com/en-us/microsoft-copilot-studio/analytics-overview)
- [Monitor agent performance overview (Microsoft Copilot)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/analytics-overview)
- [Monitor conversational agent effectiveness](https://learn.microsoft.com/en-us/microsoft-copilot-studio/analytics-improve-agent-effectiveness)
- [Natural language understanding (NLU) overview](https://learn.microsoft.com/en-us/microsoft-copilot-studio/nlu-overview)
- [Orchestrate agent behavior with generative AI](https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-generative-actions)
- [Overview](https://learn.microsoft.com/en-us/microsoft-copilot-studio/fundamentals-what-is-copilot-studio)
- [Overview of the Microsoft Copilot Studio extension for Microsoft Visual Studio Code](https://learn.microsoft.com/en-us/microsoft-copilot-studio/visual-studio-code-extension-overview)
- [Overview of usage-based billing](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/billing-credit-overview)
- [Preview and test an agent (Microsoft Copilot)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/preview-overview)
- [Prompts overview](https://learn.microsoft.com/en-us/microsoft-copilot-studio/prompts-overview)
- [Publish an agent to a live or demo website](https://learn.microsoft.com/en-us/microsoft-copilot-studio/publication-connect-bot-to-web-channels)
- [Publish an agent to Azure Bot Service channels](https://learn.microsoft.com/en-us/microsoft-copilot-studio/publication-connect-bot-to-azure-bot-service-channels)
- [Publish an agent to mobile or custom apps](https://learn.microsoft.com/en-us/microsoft-copilot-studio/publication-connect-bot-to-custom-application)
- [Publish an agent to WhatsApp](https://learn.microsoft.com/en-us/microsoft-copilot-studio/publication-add-bot-to-whatsapp)
- [Quickstart: Create an automated solution with natural language in the Microsoft Copilot harness (preview)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/create-automation-natural-language)
- [Responsible AI FAQs](https://learn.microsoft.com/en-us/microsoft-copilot-studio/responsible-ai-overview)
- [Review agent activity](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-review-activity)
- [Review agent readiness and issue status in Microsoft Copilot Studio](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-agent-status)
- [Select a primary AI model for your agent](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-select-agent-model)
- [Send a message](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-send-message)
- [Set topic triggers](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-triggers)
- [Share agents with other users](https://learn.microsoft.com/en-us/microsoft-copilot-studio/admin-share-bots)
- [Skills overview for agents (Microsoft Copilot)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/skills-overview)
- [Standard harness licensing](https://learn.microsoft.com/en-us/microsoft-copilot-studio/billing-licensing)
- [Sub-agents overview (Customer Conversation)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/sub-agents-overview-customer-conversation)
- [Telemetry with Application Insights overview](https://learn.microsoft.com/en-us/microsoft-copilot-studio/telemetry-overview)
- [Test your agent](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-test-bot)
- [Upgrade agents to the Microsoft Copilot harness (preview)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/upgrade-to-microsoft-copilot-from-standard-harness)
- [Upgrade classic chatbots to Copilot Studio](https://learn.microsoft.com/en-us/microsoft-copilot-studio/unified-authoring-conversion)
- [Upload files as a knowledge source](https://learn.microsoft.com/en-us/microsoft-copilot-studio/knowledge-add-file-upload)
- [US Government customers](https://learn.microsoft.com/en-us/microsoft-copilot-studio/requirements-licensing-gcc)
- [Use Adaptive Cards in Copilot Studio](https://learn.microsoft.com/en-us/microsoft-copilot-studio/adaptive-cards-overview)
- [Use connectors in Copilot Studio agents](https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-connectors)
- [Use entities and slot filling in agents](https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-entities-slot-filling)
- [Use interactive voice response in your agents](https://learn.microsoft.com/en-us/microsoft-copilot-studio/voice-overview)
- [Use system topics](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-system-topics)
- [Use task agents (Microsoft Copilot)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/task-agents-overview)
- [Use the activity trace to debug your agent (Microsoft Copilot)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/authoring-activity-trace)
- [Use the Power Platform API to quarantine agents](https://learn.microsoft.com/en-us/microsoft-copilot-studio/admin-api-quarantine)
- [Variables overview](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-variables-about)
- [What's new in Copilot Studio](https://learn.microsoft.com/en-us/microsoft-copilot-studio/whats-new)
- [Work IQ in Microsoft Copilot Studio (Microsoft Copilot)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/add-work-iq)
- [Work with global variables](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-variables-bot)
- [Work with variables](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-variables)
- [Workflows overview (Microsoft Copilot)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/workflows-experience/flows-overview)
- [Write agent instructions](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-instructions)

### Power Platform, Dataverse, and connectors

- [About the Microsoft Dataverse for Teams environment](https://learn.microsoft.com/en-us/power-platform/admin/about-teams-environment)
- [Create a Developer Environment with the Power Apps Developer Plan](https://learn.microsoft.com/en-us/power-platform/developer/create-developer-environment)
- [Custom connectors overview](https://learn.microsoft.com/en-us/connectors/custom-connectors/)
- [Data policies](https://learn.microsoft.com/en-us/power-platform/admin/wp-data-loss-prevention)
- [Managed environments overview](https://learn.microsoft.com/en-us/power-platform/admin/managed-environment-overview)
- [Official Microsoft Power Platform documentation](https://learn.microsoft.com/en-us/power-platform/)
- [Power Platform admin center overview for administrators](https://learn.microsoft.com/en-us/power-platform/admin/admin-documentation)
- [Power Platform environments overview](https://learn.microsoft.com/en-us/power-platform/admin/environments-overview)
- [Sandbox environments](https://learn.microsoft.com/en-us/power-platform/admin/sandbox-environments)
- [Security roles and privileges for Dataverse](https://learn.microsoft.com/en-us/power-platform/admin/security-roles-privileges)
- [Solution concepts with Power Platform](https://learn.microsoft.com/en-us/power-platform/alm/solution-concepts-alm)
- [Use environment variables in Power Platform solutions](https://learn.microsoft.com/en-us/power-apps/maker/data-platform/environmentvariables)
- [What is Microsoft Dataverse?](https://learn.microsoft.com/en-us/power-apps/maker/data-platform/data-platform-intro)

### Identity, security, and compliance

- [Learn about sensitivity labels](https://learn.microsoft.com/en-us/purview/sensitivity-labels)
- [Use Microsoft Purview to manage data security & compliance for Microsoft Copilot Studio](https://learn.microsoft.com/en-us/purview/ai-copilot-studio)
- [What is Microsoft Entra?](https://learn.microsoft.com/en-us/entra/fundamentals/what-is-entra)

### Microsoft 365, Microsoft Copilot, and agents

- [Agent Builder overview](https://learn.microsoft.com/en-us/plugins/agent-builder)
- [Agents hub - Start here for agentic computing at Microsoft](https://learn.microsoft.com/en-us/agents/)
- [Custom Engine Agents for Microsoft 365](https://learn.microsoft.com/en-us/microsoft-365/copilot/extensibility/overview-custom-engine-agent)
- [Declarative agents for Microsoft 365 Copilot](https://learn.microsoft.com/en-us/plugins/overview-declarative-agent)
- [Extend Microsoft 365 Copilot with Plugins](https://learn.microsoft.com/en-us/microsoft-365/copilot/extensibility/)
- [Microsoft Agent 365 overview](https://learn.microsoft.com/en-us/microsoft-agent-365/overview)
- [What is Microsoft Copilot?](https://learn.microsoft.com/en-us/copilot/plan/copilot-overview)
- [What is the Microsoft 365 Agents SDK](https://learn.microsoft.com/en-us/microsoft-365/agents-sdk/agents-sdk-overview)

### AI concepts, Azure, and Microsoft Foundry

- [Groundedness detection in Azure AI Content Safety](https://learn.microsoft.com/en-us/azure/ai-services/content-safety/concepts/groundedness)
- [How Embeddings Extend Your AI Model's Reach](https://learn.microsoft.com/en-us/dotnet/ai/conceptual/embeddings)
- [How Generative AI and LLMs work](https://learn.microsoft.com/en-us/dotnet/ai/conceptual/how-genai-and-llms-work)
- [Prompt engineering techniques](https://learn.microsoft.com/en-us/azure/foundry/openai/concepts/prompt-engineering)
- [RAG and Generative AI](https://learn.microsoft.com/en-us/azure/search/retrieval-augmented-generation-overview)
- [Understanding tokens](https://learn.microsoft.com/en-us/dotnet/ai/conceptual/understanding-tokens)
- [What is Azure Language in Foundry Tools](https://learn.microsoft.com/en-us/azure/ai-services/language-service/overview)
- [What is Microsoft Foundry?](https://learn.microsoft.com/en-us/azure/foundry/what-is-foundry)

### Contact center

- [Dynamics 365 Contact Center overview](https://learn.microsoft.com/en-us/dynamics365/contact-center/implement/overview-contact-center)
- [Microsoft Contact Center Intelligence](https://learn.microsoft.com/en-us/contact-center-intelligence/)

### Archived release plans

- [Overview of Microsoft Copilot Studio 2024 release wave 1](https://learn.microsoft.com/en-us/previous-versions/power-platform/release-plan/2024wave1/microsoft-copilot-studio/)
- [Overview of Microsoft Copilot Studio 2024 release wave 2](https://learn.microsoft.com/en-us/previous-versions/power-platform/release-plan/2024wave2/microsoft-copilot-studio/)

_Last verified against Microsoft Learn: 18 November 2026._
