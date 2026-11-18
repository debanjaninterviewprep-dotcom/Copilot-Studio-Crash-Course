# Module 01 — Answers and Explanations

> [!WARNING]
> Attempt the [assessment](ASSESSMENT.md) first. Reading answers before trying the questions greatly reduces learning.

## Section A — Multiple choice (2 points each)

**A1 → b) A graphical, low-code studio for building and managing AI-powered agents and workflows.**
This is Microsoft's own definition on the Copilot Studio overview page.
- *a) wrong:* Copilot Studio **uses** language models (for example, GPT-5-series and Claude models) but isn't a model.
- *c) wrong:* that describes Microsoft's consumer Copilot for personal accounts, not a building tool.
- *d) wrong:* Teams administration happens in the Teams admin center. Copilot Studio builds agents that *can* be published to Teams.

**A2 → b) Microsoft Copilot harness.**
The new experience creates Microsoft Copilot harness agents (🧪 production-ready preview since June 2026).
- *a) wrong:* the standard harness is reached through the **classic** experience.
- *c) wrong:* the Customer Conversation harness uses a separate creation path for customer-facing voice and chat.
- *d) wrong:* there's no "Bot Framework harness"; the term is a distractor.

**A3 → c) Topics.**
Microsoft's FAQ states that topics aren't carried over to the Microsoft Copilot harness. Custom topics are rebuilt as skills or workflows.
- *a), b), d) wrong:* skills, memory, and connected agents are all Microsoft Copilot harness capabilities. Connected agents were in preview in June 2026.

**A4 → b) November 2023.**
Copilot Studio was announced at Microsoft Ignite on 15 November 2023, and PVA *"will become part of Copilot Studio."*
- *a) wrong:* December 2019 was PVA's general availability.
- *c) wrong:* November 2024 is when autonomous agents entered preview.
- *d) wrong:* September 2025 is when messages became Copilot Credits.

**A5 → b) The component's description.**
Microsoft: *"The most important factor is the description of the topics, tools, agents, and knowledge sources."* Names and input/output parameters also matter.
- *a) wrong:* trigger phrases drive **classic** orchestration.
- *c), d) wrong:* order and icons don't influence selection.

**A6 → b) Generative orchestration is turned on.**
The event triggers article states the feature is only available for agents with generative orchestration turned on.
- *a) wrong:* it's the opposite.
- *c), d) wrong:* publishing target and connector type aren't prerequisites. Note that trigger availability **does** depend on data policies.

**A7 → b) It doesn't support authoring actions that integrate external services.**
Microsoft's comparison guide: Agent Builder *"Doesn't support authoring actions that integrate external services. Copy to Copilot Studio…"*
- *a) wrong:* Agent Builder supports Microsoft 365 knowledge sources.
- *c) wrong:* it supports sharing and submission to the org catalog.
- *d) wrong:* it **is** a guided natural-language configuration experience.

**A8 → b) 2.**
Standard harness billing rates: generative answer = 2 Copilot Credits.
- *a) wrong:* 1 is a classic answer.
- *c) wrong:* 5 is an agent action.
- *d) wrong:* 10 is tenant graph grounding.

**A9 → b) Data might be processed outside your region.**
That's the documented meaning of *cross-geo* in the model availability table.
- *a) wrong:* "Experimental" is a separate tag.
- *c) wrong:* several external models are explicitly **not** available in GCC.
- *d) wrong:* models don't change whether usage is billed. Reasoning models even add a premium.

**A10 → b) Creating and testing agents, but not publishing them.**
Microsoft: *"You can test your agents using the test chat panel. However, you can't publish the agent."*
- *a), d) wrong:* no publishing at all on a trial license.
- *c) wrong:* you can create and test, not just view.

## Section B — True or false (1 point each)

| # | Answer | Explanation |
|---|---|---|
| B1 | **False** | The classic experience applies to the current session only. Microsoft states there's no tenant-wide setting to make it the default. |
| B2 | **False** | The Application Card states Microsoft *"does not train foundation models using customer data."* |
| B3 | **False** | Purchased capacity is enforced monthly, and unused credits don't carry over. |
| B4 | **True** | Microsoft Copilot harness billing *"starts when you start building."* Natural-language creation, preview and testing, and evaluations consume credits. |
| B5 | **True** | What's new, July 2026: Copilot Studio automatically creates a Microsoft Entra Agent ID for every new agent, with no environment-level opt-out. Timing depends on the harness: at creation on the standard harness, and at first publish on the Microsoft Copilot harness. |

## Section C — Short answer (3 points each)

Award **1 point per key idea** (maximum 3).

**C1. Harness.**
*Model answer:* A harness is the runtime between your agent design and the model. It decides when to call the model, what to send, how to interpret the results, and which tools to call. It determines capabilities, channels, and billing. The three harnesses:
- **Microsoft Copilot:** reasoning-heavy multistep processes such as accounts payable.
- **Customer Conversation:** customer voice and chat with escalation to human representatives.
- **Standard:** rule-based, predictable conversations, such as an internal help desk.

*Key ideas:* (1) runtime definition; (2) all three named correctly; (3) a suitable use for each.

**C2. Grounding and RAG.**
*Model answer:* Grounding gives the model relevant, trusted data (your documents, sites, or Graph data) so its answer is based on facts rather than its general training. RAG is one way to ground: first **retrieve** passages relevant to the question, then **generate** the answer from them, usually with citations. Because the model works from retrieved evidence, it's less likely to invent facts, and users can verify answers.

*Key ideas:* (1) grounding definition; (2) the retrieve-then-generate sequence; (3) why it reduces hallucination (evidence and citations).

**C3. Copilot Studio vs. Microsoft Copilot Chat.**
*Model answer:* Copilot Chat is an AI assistant people **use**. Copilot Studio is a studio for **building** custom agents. Copilot Chat (Basic) mainly uses web data, while a Copilot Studio agent uses the knowledge, tools, and instructions you configure, and can serve external customers on websites. They work together because Copilot Studio agents can be **published to Microsoft Copilot** (and Teams), so users access specialized agents inside the familiar Copilot experience.

*Key ideas:* (1) use vs. build; (2) a grounding, tools, or audience difference; (3) publishing to Microsoft Copilot as a channel.

**C4. Agent components.** Any four, explained (award 3 points for four correct):
- **Instructions:** role, scope, tone, rules.
- **Knowledge:** grounding content.
- **Tools:** actions in other systems.
- **Topics (standard) or skills (Microsoft Copilot):** structured or reusable behavior.
- **Other agents:** child or connected agents for delegation.
- **Triggers:** autonomous starts.
- **Variables or memory:** state.
- **Model:** reasoning and generation.
- **Channels:** where users interact.
- **Settings:** for example, orchestration and security.

**C5. Acquiring Copilot Credits.**
*Model answer:*
1. **Prepaid Copilot Credit pack subscription:** tenant capacity, enforced monthly, no carry-over.
2. **Pay-as-you-go:** billed monthly through an Azure subscription linked to environments by a billing policy in the Power Platform admin center. No upfront commitment.
3. **Copilot Credit prepurchase plan:** a one-year prepaid pool of Copilot Credit Commit Units, bought in the Azure portal. Requires a billing policy.

*Key ideas:* one point per option correctly characterized.

## Section D — Practical tasks (15 points each)

### D1. Build and evidence a first agent: expected outcome

- *Copilot Studio Learning Buddy* exists in the learner's environment and opens in the **classic experience** (standard harness).
- The **Overview** page shows a meaningful description, generated instructions, and the default model with its tags.
- The **Knowledge** page lists `https://learn.microsoft.com/microsoft-copilot-studio` with a clear description.
- Three test answers include **citations** to Microsoft Learn. The activity map shows a knowledge search for at least one answer.
- The Part 7 comparison shows answers changing to a three-bullet format after the instruction change, and reverting afterwards.

| Criterion | Excellent (full points) | Partial | Missing | Points |
|---|---|---|---|---|
| Agent on standard harness, correctly named | Evidence of classic experience + name | Name only | No evidence | 3 |
| Overview evidence (description, instructions, model) | All three shown | 1–2 shown | None | 3 |
| Knowledge source with description | URL + description | URL only | None | 3 |
| Three cited answers + activity-map notes | All three with notes | 1–2 | None | 3 |
| Instruction before/after comparison | Clear before/after + revert | Partial | None | 3 |
| **Total** | | | | **15** |

### D2. Orchestration comparison and recommendation: expected outcome

- **Observation:** under generative orchestration, the two-part question ("What is Copilot Studio, and how is it licensed?") is typically answered in a single combined, cited response. Under classic orchestration, the agent relies on topic matching through trigger phrases, with knowledge as a fallback, so coverage of both parts may be less complete. Accept any well-documented, honest observation; results vary.
- **Recommendation (model):** Use the **standard harness** (GA, predictable, broad channel support including Teams and Microsoft Copilot, no build-time credit consumption) with **generative orchestration** (answers the long tail of policy questions from the cited policy library and handles multi-part questions). Add a few **authored topics** for sensitive questions that need exact wording, and an **Escalate** path to HR. Licensing: employees with Microsoft 365 Copilot licenses who use it in Teams with their identity aren't charged for core answers. Avoid preview harnesses for this production HR use case.

| Criterion | Points |
|---|---|
| Accurate, specific documentation of both runs | 5 |
| Correct harness choice with ≥ 1 justification | 3 |
| Correct orchestration choice with ≥ 1 justification | 3 |
| Uses ≥ 3 module concepts correctly (for example, citations, licensing, channels, preview status, determinism) | 3 |
| Within 150–200 words, clear structure | 1 |
| **Total** | **15** |

## Section E — Real-world scenario challenge (15 points)

### Model answer

| | HR Policy Agent | Order Help Agent | Invoice Agent |
|---|---|---|---|
| **a) Harness** | **Standard** (GA): predictable policy answers, topics for sensitive wording | **Standard** today for web chat with live-agent handoff. Evaluate the **Customer Conversation** harness (🧪 Preview) for the future voice and contact-center scenario. | **Microsoft Copilot** (🧪 Preview): multistep reasoning over PDF files, matching POs, routing exceptions |
| **b) Channels** | Teams and Microsoft Copilot | Website (custom website or demo first); phone later | Teams and Microsoft Copilot for finance staff |
| **c) Knowledge / tools** | HR policy SharePoint library; Escalate topic; later an "Open HR case" tool | Order-status tool (connector or agent flow); returns policy knowledge; human handoff | Invoices and PO data; tools to look up POs and route approvals; human approval step |
| **d) Licensing / billing** | 3,000 Microsoft 365 Copilot users: core answers not charged when authenticated in Teams or Microsoft Copilot. The other 9,000 consume credits (2 per generative answer; avoid unnecessary tenant graph grounding at 10). | External customers aren't covered by Microsoft 365 Copilot licenses: plan Copilot Credits (pack, PAYG, or prepurchase) and estimate volumes | Usage-based credits from build time, **not** included in Microsoft 365 Copilot licenses: set agent limits and environment allocations; estimate per-invoice cost |
| **e) Risk → mitigation** | Wrong policy answer → ground in the policy, cite sources, turn off ungrounded responses, escalate | Privacy leak of order data → authenticate customers before order lookup; least-privilege tool | Wrong payment routing → human approval for exceptions, pilot in a non-production environment |

**Preview handling:** Treat the Microsoft Copilot harness and the Customer Conversation harness as **preview**. Pilot them in separate environments, accept preview terms, set credit limits, keep a human in the loop, define rollback plans, track [What's new](https://learn.microsoft.com/en-us/microsoft-copilot-studio/whats-new) for GA announcements, and avoid making business-critical processes depend on them without risk sign-off.

| Rubric criterion | Points |
|---|---|
| Correct harness per agent, justified (3 × 2) | 6 |
| Sensible channels, knowledge, and tools | 3 |
| Licensing/billing reasoning (B2E licensed vs. external, harness billing) | 3 |
| Risks with credible mitigations | 2 |
| Preview handling | 1 |
| **Total** | **15** |

## Section F — Troubleshooting challenge (15 points)

### Model answer

| # | Problem | Root cause | Fix / recommendation |
|---|---|---|---|
| 1 | No **Topics** page | The agent was created in the **new experience** (Microsoft Copilot harness), which has no topics. The 2024 tutorial targets the standard harness. | Rebuild the topic logic as a **skill** or **workflow**. If topics are required, create the agent in the **classic experience** (standard harness). |
| 2 | Classic experience "gone" today | The classic experience applies to the **current session only**, with no tenant-wide default | Reopen it with **…** > **Open classic experience**, or use **Other ways to build** |
| 3 | Credits used before publishing | Microsoft Copilot harness billing starts **at build time**; testing and evaluations consume credits | Ask the admin to set **agent limits** and **environment allocations**, budget testing, and prototype on the standard harness if appropriate |
| 4 | Can't publish to Teams | **Trial license**: create and test only, no publishing | Get a Copilot Studio license or pay-as-you-go access from the admin |
| General | Confusion from outdated content | Tutorials predate 2026 harness changes | Check the harness and experience first. Prefer current Microsoft Learn articles and [What's new](https://learn.microsoft.com/en-us/microsoft-copilot-studio/whats-new) over older videos. |

| Rubric criterion | Points |
|---|---|
| Problem 1 correctly diagnosed and fixed | 4 |
| Problem 2 correctly diagnosed and fixed | 3 |
| Problem 3 correctly diagnosed and fixed | 4 |
| Problem 4 correctly diagnosed and fixed | 3 |
| General prevention recommendation | 1 |
| **Total** | **15** |

---

## Calculate your result

1. Add up your points (maximum 100).
2. Find your level: 0–59 **Beginner** · 60–74 **Intermediate** · 75–89 **Advanced** · 90–100 **Professional Ready**.
3. If you scored below 75, revisit the lessons linked from the questions you missed and retake Sections A–C after 24 hours.
4. Record the score in [LEARNING-PROGRESS.md](../LEARNING-PROGRESS.md).

## References

- [Overview – Microsoft Copilot Studio](https://learn.microsoft.com/en-us/microsoft-copilot-studio/fundamentals-what-is-copilot-studio)
- [Harnesses in Copilot Studio](https://learn.microsoft.com/en-us/microsoft-copilot-studio/harnesses-overview)
- [FAQ for agents powered by the Microsoft Copilot harness](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/faqs-copilot-harness)
- [Access standard harness agents and agent flows](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/switch-experiences)
- [Orchestrate agent behavior with generative AI](https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-generative-actions)
- [Event triggers overview](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-triggers-about)
- [Choose between Agent Builder and Copilot Studio](https://learn.microsoft.com/en-us/microsoft-365/copilot/extensibility/copilot-studio-experience)
- [Billing rates and management](https://learn.microsoft.com/en-us/microsoft-copilot-studio/requirements-messages-management)
- [Standard harness licensing](https://learn.microsoft.com/en-us/microsoft-copilot-studio/billing-licensing)
- [Overview of usage-based billing](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/billing-credit-overview)
- [Select a primary AI model for your agent](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-select-agent-model)
- [Get access to Copilot Studio](https://learn.microsoft.com/en-us/microsoft-copilot-studio/requirements-licensing-subscriptions)
- [Application Card for Microsoft Copilot Studio](https://learn.microsoft.com/en-us/microsoft-copilot-studio/system-service-card-copilot-studio)
- [What's new in Copilot Studio](https://learn.microsoft.com/en-us/microsoft-copilot-studio/whats-new)

_Last verified against Microsoft Learn: 18 November 2026._
