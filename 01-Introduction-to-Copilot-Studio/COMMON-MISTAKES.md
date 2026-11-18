# Module 01 — Common Mistakes and How to Avoid Them

These are the mistakes beginners (and many experienced makers) make when they first meet Copilot Studio in 2026. Each one explains **why it happens**, **what's actually true**, and **how to avoid or fix it**, with a link to the lesson.

## A. Concepts and terminology

### 1. "Copilot Studio is just a chatbot builder."

- **Why it happens:** the product grew out of Power Virtual Agents, a chatbot tool.
- **Reality:** Copilot Studio builds **agents and workflows**. Agents can act through tools, run autonomously on events, collaborate with other agents, and be governed and evaluated.
- **Avoid it:** describe agents by what they *do* (answer, act, automate), not only by the chat window. See [Lesson 1](CONCEPTS.md#lesson-1-what-is-microsoft-copilot-studio).

### 2. Mixing up "Copilot" products

- **Why it happens:** Microsoft Copilot, Copilot Chat, Microsoft 365 Copilot, Agent Builder, and Copilot Studio share a name.
- **Reality:** people *use* Microsoft Copilot and Microsoft 365 Copilot. Makers *build* with Agent Builder (simple declarative agents) or **Copilot Studio** (governed, integrated agents).
- **Avoid it:** always name the specific product. See Lessons [4](CONCEPTS.md#lesson-4-copilot-studio-vs-microsoft-copilot) and [5](CONCEPTS.md#lesson-5-copilot-studio-vs-microsoft-365-copilot).

### 3. Following outdated tutorials literally

- **Why it happens:** many videos and blogs predate the 2026 harness changes, or still say "PVA", "bot", or "messages".
- **Reality:** UI, terminology, and billing have changed: harnesses, the classic vs. new experience, Copilot Credits, and the **Monitor** page.
- **Avoid it:** check the article date and the harness. Prefer current Microsoft Learn articles and [What's new](https://learn.microsoft.com/en-us/microsoft-copilot-studio/whats-new). See [Lesson 3](CONCEPTS.md#lesson-3-evolution-from-power-virtual-agents).

## B. Harnesses and experiences

### 4. Building in the wrong harness

- **Why it happens:** the new experience (Microsoft Copilot harness) is the default, so beginners build there without choosing.
- **Reality:** topics, trigger phrases, nodes, variables, and entities exist only on the **standard** harness. The Microsoft Copilot harness uses skills, workflows, and memory instead.
- **Avoid it:** decide the harness *first*. For Modules 05–08, use the classic experience. See [Lesson 2](CONCEPTS.md#lesson-2-harnesses-and-the-new-vs-classic-experience).

### 5. Expecting the classic experience to "stick"

- **Why it happens:** you switched once and assume it's saved.
- **Reality:** the classic experience applies to the **current session only**, and there's no tenant-wide default.
- **Fix:** reopen it each session with **…** > **Open classic experience**, or use **Other ways to build**.

### 6. Treating preview features as production-ready by default

- **Why it happens:** "production-ready preview" sounds final.
- **Reality:** preview features can change. The Microsoft Copilot harness, the Customer Conversation harness, and many 2026 capabilities are 🧪 Preview.
- **Avoid it:** pilot in non-production environments, accept preview terms knowingly, keep fallbacks, and track GA announcements.

### 7. Expecting cross-harness agents to call each other

- **Reality:** connected agents on the Microsoft Copilot harness can currently delegate only to other agents built on the Microsoft Copilot harness. Standard and Copilot harness agents can't invoke each other directly.
- **Avoid it:** keep collaborating agents on the same harness.

## C. Generative AI fundamentals

### 8. Expecting deterministic answers from generative AI

- **Reality:** generative answers vary with context and between sessions. Microsoft documents this as expected.
- **Avoid it:** use authored topics with message nodes where wording must be exact. Compare answers in **new** test sessions. See [Lesson 8](CONCEPTS.md#lesson-8-generative-ai-fundamentals).

### 9. Assuming the model "knows" your company

- **Reality:** the model only knows what you ground it in. Microsoft doesn't train foundation models on your data.
- **Avoid it:** connect the right knowledge sources, write instructions about what to do when the answer isn't found, and keep **Allow ungrounded responses** off for regulated agents.

### 10. Choosing the most powerful model "just in case"

- **Reality:** reasoning models add a premium (10 Copilot Credits per 1,000 tokens on the standard harness) and add latency. Cross-geo models may process data outside your region.
- **Avoid it:** start with the default GA model, and justify any change with evaluations. See [Lesson 9](CONCEPTS.md#lesson-9-large-language-models-llms).

### 11. Writing vague descriptions

- **Reality:** with generative orchestration, the **description** is the most important factor in selecting topics, tools, agents, and knowledge.
- **Avoid it:** write specific, distinct descriptions that say *when* to use each component. See [Lesson 6](CONCEPTS.md#lesson-6-copilot-studio-vs-traditional-chatbots).

## D. Architecture and use cases

### 12. The "god agent"

- **Reality:** one agent with dozens of tools and topics confuses orchestration and is hard to own.
- **Avoid it:** give each agent one clear purpose. Split specialists into child or connected agents later ([Module 18](../18-Advanced-Agent-Development/README.md)). See [Lesson 11](CONCEPTS.md#lesson-11-agent-architecture).

### 13. Building before defining the use case and metrics

- **Reality:** projects fail on scope and measurement more often than on technology.
- **Avoid it:** complete a use-case canvas with baseline and target metrics *before* building. See [Lesson 12](CONCEPTS.md#lesson-12-enterprise-use-cases).

### 14. Autonomous agents without guardrails

- **Reality:** event triggers act without a person. A frequent trigger multiplies cost, and conflicting payload instructions cause errors.
- **Avoid it:** add human approval for high-impact actions, align instructions, set trigger conditions, and estimate credits. See [Lesson 7](CONCEPTS.md#lesson-7-ai-agents-and-autonomous-agents).

## E. Licensing and cost

### 15. Planning to publish from a trial

- **Reality:** a trial lets you create and test but **not publish**.
- **Fix:** arrange a license or pay-as-you-go access before the pilot date. See [Lesson 13](CONCEPTS.md#lesson-13-licensing-fundamentals).

### 16. Forgetting that the Microsoft Copilot harness bills from build time

- **Reality:** natural-language creation, testing, and evaluations on the Microsoft Copilot harness consume Copilot Credits **before** you publish.
- **Avoid it:** ask admins for agent limits and environment allocations, and budget test cycles.

### 17. Assuming every internal user is "free"

- **Reality:** the inclusion for core answers and tenant graph grounding applies only to users **licensed for Microsoft 365 Copilot**, using a standard harness agent with their authenticated identity in Copilot Chat, Teams, or SharePoint, and subject to fair use. Unlicensed employees and external users consume credits. Microsoft Copilot harness usage isn't included with a Microsoft 365 Copilot license at all.
- **Avoid it:** model costs separately for licensed, unlicensed, and external users.

### 18. Assuming unused credits roll over

- **Reality:** prepaid capacity is enforced monthly, and unused credits don't carry over. Overage enforcement can deny service.
- **Avoid it:** right-size packs, use pay-as-you-go for spikes, and monitor consumption in the Power Platform admin center.

## Quick troubleshooting reference

| Symptom | Most likely cause | Go to |
|---|---|---|
| Can't find **Topics** | New experience (Microsoft Copilot harness) | Mistake 4 |
| Classic experience disappeared | Session-only setting | Mistake 5 |
| Credits consumed with nothing published | Microsoft Copilot harness bills from build time | Mistake 16 |
| Can't publish | Trial license | Mistake 15 |
| Different answers each time | Generative non-determinism and context | Mistake 8 |
| Wrong tool or topic chosen | Weak or overlapping descriptions | Mistake 11 |
| Cost spike | Reasoning model, frequent triggers, unlicensed users | Mistakes 10, 14, 17 |

## Self-check before moving to Module 02

- [ ] I can explain Copilot Studio in 60 seconds without confusing it with Microsoft Copilot.
- [ ] I can name the three harnesses, their status, and when to use each.
- [ ] I know how to open the classic experience and why I'll need it in Modules 05–08.
- [ ] I can explain grounding, RAG, tokens, and why answers vary.
- [ ] I can list the components of an agent.
- [ ] I can explain Copilot Credits, the three ways to buy them, and the trial limitation.

## References

- [Harnesses in Copilot Studio](https://learn.microsoft.com/en-us/microsoft-copilot-studio/harnesses-overview)
- [FAQ for agents powered by the Microsoft Copilot harness](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/faqs-copilot-harness)
- [Access standard harness agents and agent flows](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/switch-experiences)
- [AI-based agent authoring overview](https://learn.microsoft.com/en-us/microsoft-copilot-studio/nlu-gpt-overview)
- [Orchestrate agent behavior with generative AI](https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-generative-actions)
- [Event triggers overview](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-triggers-about)
- [Billing rates and management](https://learn.microsoft.com/en-us/microsoft-copilot-studio/requirements-messages-management)
- [Overview of usage-based billing](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/billing-credit-overview)
- [Get access to Copilot Studio](https://learn.microsoft.com/en-us/microsoft-copilot-studio/requirements-licensing-subscriptions)
- [What's new in Copilot Studio](https://learn.microsoft.com/en-us/microsoft-copilot-studio/whats-new)

_Last verified against Microsoft Learn: 18 November 2026._
