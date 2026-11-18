# Module 01 — Interview Questions: Introduction to Microsoft Copilot Studio

There are 30 questions in three levels. Each has a **model answer** and a note on **what the interviewer is looking for**. Practise answering out loud in under two minutes before you read the model answer.

> [!TIP]
> Interviewers in 2026 often test whether you know the **harness** changes. Always ask yourself: "Which harness or experience does this apply to?"

## Beginner (1–10)

### 1. What is Microsoft Copilot Studio?

**Model answer:** It's Microsoft's graphical, low-code studio for building and managing AI-powered agents and workflows. You can describe an agent in natural language, give it instructions, connect knowledge and tools, test it, publish it to channels such as Teams, Microsoft Copilot, and websites, and then monitor and govern it. It's built on the Power Platform.

**Looking for:** the official framing (agents *and* workflows, low-code) and the end-to-end lifecycle.

### 2. What is an agent?

**Model answer:** An AI assistant that handles conversations and completes tasks. It follows instructions, draws on connected knowledge, and uses tools to take action, deciding the best next step from its instructions and context. Agents can be conversational, or autonomous when they're triggered by events.

**Looking for:** instructions + knowledge + tools + reasoning; the conversational vs. autonomous distinction.

### 3. What's the difference between Copilot Studio and Microsoft Copilot?

**Model answer:** Microsoft Copilot (for example, Copilot Chat) is an AI assistant people *use*. Copilot Studio is where makers *build* custom agents. Copilot Studio agents can be published into Microsoft Copilot, so the two are complementary.

**Looking for:** the use vs. build distinction, and Microsoft Copilot as a channel.

### 4. What was Power Virtual Agents, and how does it relate to Copilot Studio?

**Model answer:** PVA was Microsoft's no-code chatbot builder, generally available from December 2019. At Ignite in November 2023 its capabilities became part of Copilot Studio, which added generative AI. Older PVA bots are "classic chatbots" and can be cloned into standard harness agents if they're eligible.

**Looking for:** the timeline and the legacy implications.

### 5. What is generative AI?

**Model answer:** AI that uses language models to generate original content, such as answers, summaries, and plans, and to understand natural language. In Copilot Studio it powers generative answers, generative orchestration, and natural-language authoring.

**Looking for:** a correct definition plus concrete Copilot Studio uses.

### 6. What is a large language model, and what are tokens?

**Model answer:** An LLM is a machine-learning model trained on large datasets that enables natural language understanding and generation. It processes text as tokens (word pieces) within a limited context window and generates output token by token. Token usage matters for cost, especially with reasoning models, which are billed per 1,000 tokens.

**Looking for:** tokens, context window, and the link to cost.

### 7. What is grounding?

**Model answer:** Supplying relevant enterprise or external data to the model so its answers are accurate and aligned with organizational information. For example, the agent retrieves policy passages and answers from them with citations. It reduces fabricated answers.

**Looking for:** grounding → accuracy → citations.

### 8. What are knowledge sources? Give examples.

**Model answer:** Data the agent can use to ground answers. Supported types vary by harness. Examples include public websites, uploaded files, SharePoint and OneDrive, and Dataverse tables. The standard harness adds Bing Custom Search. On the Microsoft Copilot harness, Work IQ is added by default, and Azure SQL tables can be connected. Admins can restrict which knowledge-source types makers can add (October 2026).

**Looking for:** several current examples, plus awareness of governance.

### 9. What are Copilot Credits?

**Model answer:** The common currency for Copilot Studio usage since 1 September 2025 (formerly "messages"). Credits come from prepaid packs, pay-as-you-go through Azure, or a one-year prepurchase plan. Consumption depends on the features used and the harness.

**Looking for:** the rename and the three acquisition options.

### 10. What can you do with a Copilot Studio trial license?

**Model answer:** Sign up as an individual with a work or school account, then create agents and test them in the test chat panel. You can't publish. When the trial expires you can extend it by 30 days, and agents keep working for up to 90 days after expiry.

**Looking for:** the "no publishing" limitation.

## Intermediate (11–20)

### 11. Explain the three harnesses and when you'd use each.

**Model answer:** A harness is the runtime between your design and the model.

- **Microsoft Copilot harness** (new experience, 🧪 production-ready preview): reasoning-heavy multistep processes, native Office and PDF file work, skills, memory, a secure sandbox, usage-based billing from build time. Example: accounts payable.
- **Customer Conversation harness** (🧪 preview): customer voice and chat, with a primary agent, sub-agents, and escalation to human representatives.
- **Standard harness** (classic experience, 🟢 GA): rule-based, predictable conversations with topics. Billing starts after publish.

**Looking for:** an accurate runtime definition, status awareness, and billing differences.

### 12. Compare generative and classic orchestration.

**Model answer:** Both are standard harness modes.

- **Classic orchestration** triggers the single topic whose trigger phrases best match the query. Tools can be called only from topics, and knowledge is a fallback.
- **Generative orchestration** (the default for new agents) selects topics, tools, other agents, and knowledge by their descriptions. It can combine several, generates questions for missing inputs, and composes the response.

An admin can turn generative orchestration off for an environment.

**Looking for:** the descriptions-vs-trigger-phrases contrast, multi-intent handling, and admin control.

### 13. What are event triggers, and what constraints apply?

**Model answer:** Event triggers let a standard harness agent act autonomously when an event occurs, such as a new SharePoint item or a recurrence schedule. A trigger payload is sent through a connector, and the agent follows its instructions and the payload instructions.

Constraints:

- They require **generative orchestration**.
- Trigger availability depends on **data policies**.
- Every payload is billed like a user message.
- Trigger connectors authenticate with the maker's credentials.

**Looking for:** autonomy, the generative orchestration prerequisite, governance, and cost.

### 14. When would you choose Agent Builder over Copilot Studio?

**Model answer:** When instructions plus supported Microsoft 365 knowledge and capabilities meet the need, there are no external-service actions or external channels, and Microsoft 365 sharing and org-catalog publishing are sufficient. Choose based on capabilities and operating model, not audience size. If needs grow, copy the agent to Copilot Studio. The copy is a snapshot, not synchronized.

**Looking for:** Microsoft's decision criteria and the copy caveat.

### 15. How do Microsoft 365 Copilot licenses affect Copilot Studio costs?

**Model answer:** For employee-facing scenarios where the user has a Microsoft 365 Copilot license and the agent runs with that user's authenticated identity in Copilot Chat, Teams, or SharePoint, classic answers, generative answers, and tenant graph grounding aren't charged, subject to fair use. This rule comes from the standard harness billing rates.

Exceptions:

- Agent flows are included only through the *When an agent calls the flow* trigger.
- Computer use isn't included.
- Flows called while responding to event triggers are billed at the standard rate.
- **Microsoft Copilot harness** usage (building, testing, evaluating, running) consumes Copilot Credits and isn't included with a Microsoft 365 Copilot license.

**Looking for:** precise conditions and exceptions, including the harness distinction.

### 16. What is the activity map, and why use it?

**Model answer:** It's a visual representation of the plan an agent generated: which topics, tools, knowledge, and agents it used, with inputs, outputs, and errors. You can show it in real time in the test panel (**…** > **Show activity map when testing**) and review it for every activity on the **Activity** page. It's the main tool for understanding and debugging generative orchestration.

**Looking for:** where to find it and its debugging value.

### 17. How do you decide between authored topics and generative answers?

**Model answer:**

- Use **authored topics** where wording must be exact or the process must be deterministic and auditable (legal, identity verification).
- Use **generative answers** for the long tail of varied questions answered from documents.

Most production agents are hybrid. For generative topics, return results as outputs so the orchestrator can compose contextual responses.

**Looking for:** a risk-based, hybrid reasoning.

### 18. How do descriptions influence generative orchestration?

**Model answer:** The description is the most important factor when the planner selects topics, tools, agents, and knowledge. Names and input/output parameters and their descriptions matter too. Good descriptions are specific, distinct, and say when to use the component. When you switch an existing agent to generative orchestration, Copilot Studio auto-generates topic descriptions from trigger phrases, and you should review them.

**Looking for:** "description is the selection signal" plus practical writing guidance.

### 19. What role do Power Platform environments play?

**Model answer:** Agents are created inside an environment, which is a container with its own Dataverse, data, security, and policies. Agents are solution-aware (solution and schema name), so they can be moved through dev, test, and prod. Environments also scope data policies, credit allocations, and governance controls.

**Looking for:** environment as a container, plus ALM and governance links.

### 20. What's the difference between the new and classic experiences, and how do you reach classic?

**Model answer:** The new experience is the default UI and builds Microsoft Copilot harness agents (**Build** tab, **Agent settings** dialog, skills, memory). The classic experience builds standard harness agents and agent flows (topics, nodes, variables). Reach it from **…** at the bottom of the side bar > **Open classic experience**, or from **Other ways to build** on Home. The choice lasts for the session only, and there's no tenant-wide default.

**Looking for:** current navigation and the session-only behavior.

## Advanced and scenario (21–30)

### 21. A stakeholder wants to move every agent to the Microsoft Copilot harness now. What do you advise?

**Model answer:** Don't do a blanket migration.

- The standard harness remains fully supported with no forced switch. The Microsoft Copilot harness is a production-ready preview, and the upgrade tool is in preview too.
- The Copilot harness supports fewer channels today.
- Cross-harness agents can't call each other.
- The upgrade doesn't migrate knowledge sources, Power Fx, or child agents, and it consumes credits.

Assess each agent instead: move those that benefit from multistep reasoning or file work, pilot them in a separate environment with credit limits, and keep deterministic agents on the standard harness.

**Looking for:** facts plus a risk-managed, per-agent approach.

### 22. Design an IT helpdesk agent and justify the components.

**Model answer:** Standard harness with generative orchestration.

- **Instructions:** IT role and tone, never request passwords.
- **Knowledge:** the IT KB SharePoint site.
- **Tools:** "Create ticket" agent flow and "Check status" connector, each with clear descriptions.
- **Topics:** password reset (scripted), plus the Escalate system topic.
- **Channel and identity:** Teams and Microsoft Copilot, with Microsoft Entra ID authentication.
- **Environments:** dev, test, and prod.
- **Governance:** data policies.
- **Quality:** evaluations before release, and Monitor-page KPIs (resolution and escalation).

**Looking for:** coherent architecture, least privilege, and an operations plan.

### 23. How would you estimate and control credits for an autonomous agent?

**Model answer:** Estimate runs per month from the trigger frequency, times the credits per run (agent actions, generative answers, flow actions per 100, and the reasoning premium if any), using the official estimator. Reduce cost with trigger conditions, lower frequency, standard (non-reasoning) models, concise instructions, and efficient flows. Control spend with admin agent limits, environment allocations, and blocking environments from drawing on the tenant pool. Monitor the Activity and Monitor pages.

**Looking for:** quantitative reasoning and both design and admin controls.

### 24. A regulated bank wants "zero hallucinations". What do you design?

**Model answer:** Explain first that generative output can't be guaranteed hallucination-free. Then minimize the risk:

- Ground the agent in curated, permissioned sources with citations.
- Turn off ungrounded responses.
- Write instructions to decline and escalate when the answer isn't found.
- Use authored topics with exact wording for regulated answers.
- Evaluate groundedness and content safety with test sets before each release.
- Choose GA in-region models.
- Monitor in production, and review transcripts with the appropriate roles.

**Looking for:** honest framing plus layered mitigations.

### 25. How do model choices affect an agent, and how do you manage model upgrades?

**Model answer:** The model drives quality, latency, cost, and compliance.

- Reasoning models add a premium per-token charge.
- Cross-geo models may process data outside your region.
- Some external models aren't available in GCC.

Use GA in-region models for production. When Microsoft upgrades the default model, use the 30-day window to stay on the current model while you rerun evaluation test sets, then switch.

**Looking for:** trade-offs plus a change-management process.

### 26. How would you migrate a classic PVA chatbot?

**Model answer:**

1. Check eligibility: English only, no Omnichannel handoff, no Knowledge Management extensions.
2. Clone it to a new standard harness agent. The original isn't changed.
3. Reconfigure authentication, channels, and security.
4. Reconnect Bot Framework skills and verify flows.
5. Update pipelines and reports that use the old bot ID.
6. Add generative capabilities where they help, and run regression tests before cutover.

**Looking for:** procedure and risk awareness.

### 27. You have 20 agent ideas. How do you prioritize?

**Model answer:** Use a use-case canvas and score each idea on value (volume, time saved), feasibility (data readiness, integrations, harness and channel support, licensing), and risk (impact of errors, need for approvals). Pick high-value, low-risk, data-ready cases, define baseline metrics, run time-boxed pilots in dedicated environments with evaluation sets and budgets, and scale only what meets its targets.

**Looking for:** a structured framework and measurable outcomes.

### 28. How do you handle preview features in enterprise roadmaps?

**Model answer:** Label them clearly. Pilot them in non-production environments with limited users and accepted preview terms, keep humans in the loop, set cost limits, have fallbacks on GA capabilities, track What's new and the roadmap for GA, and re-evaluate at GA before scaling.

**Looking for:** risk governance without blocking innovation.

### 29. Why might the same question get different answers in the test panel and in Teams?

**Model answer:** Generative orchestration uses conversation history and context, so a fresh test session and a long-running Teams conversation can differ. Microsoft documents this as expected. Teams also reuses the same conversation ID across sessions. Other causes: the published version differs from the draft, or user identity and permissions affect what knowledge is retrieved. To test reliably, start new sessions, publish your changes, and test as representative users.

**Looking for:** context effects and identity effects.

### 30. Explain to a CISO how Copilot Studio agents are governed.

**Model answer:**

- **Identity:** Microsoft Entra ID authentication by default for new standard agents, plus an automatically created Entra Agent ID for each new agent.
- **Data and connectors:** data policies and advanced connector policies, and admin restrictions on knowledge-source types.
- **Access:** Dataverse security roles control who can build. Managed environment sharing controls and security groups control who agents are shared with.
- **Operations:** agent inventory, usage reports, block or quarantine, credit limits, and onboarding to Microsoft Agent 365 for centralized governance.
- **Data handling:** knowledge is grounded in content the user has permission to access, and Microsoft doesn't train foundation models on customer data.

Details are in Modules 13 and 17.

**Looking for:** layered controls described accurately and concisely.

## References

- [Overview – Microsoft Copilot Studio](https://learn.microsoft.com/en-us/microsoft-copilot-studio/fundamentals-what-is-copilot-studio)
- [Harnesses in Copilot Studio](https://learn.microsoft.com/en-us/microsoft-copilot-studio/harnesses-overview)
- [FAQ for agents powered by the Microsoft Copilot harness](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/faqs-copilot-harness)
- [Orchestrate agent behavior with generative AI](https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-generative-actions)
- [Event triggers overview](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-triggers-about)
- [Review agent activity](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-review-activity)
- [Choose between Agent Builder and Copilot Studio](https://learn.microsoft.com/en-us/microsoft-365/copilot/extensibility/copilot-studio-experience)
- [Billing rates and management](https://learn.microsoft.com/en-us/microsoft-copilot-studio/requirements-messages-management)
- [Standard harness licensing](https://learn.microsoft.com/en-us/microsoft-copilot-studio/billing-licensing)
- [Select a primary AI model for your agent](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-select-agent-model)
- [Upgrade classic chatbots to Copilot Studio](https://learn.microsoft.com/en-us/microsoft-copilot-studio/unified-authoring-conversion)
- [Use system topics](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-system-topics)
- [What's new in Copilot Studio](https://learn.microsoft.com/en-us/microsoft-copilot-studio/whats-new)
- [Application Card for Microsoft Copilot Studio](https://learn.microsoft.com/en-us/microsoft-copilot-studio/system-service-card-copilot-studio)

_Last verified against Microsoft Learn: 18 November 2026._
