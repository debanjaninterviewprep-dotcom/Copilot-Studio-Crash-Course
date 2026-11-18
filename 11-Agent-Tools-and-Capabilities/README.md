# Module 11 — Agent Tools and Capabilities

> [!NOTE]
> **Status: 🔜 Planned.** This syllabus is published; the full lesson files are developed in Step 7 of the [course build plan](../COURSE-ROADMAP.md).

Knowledge lets an agent *answer*; tools let it *act* — look up live data, create records, send messages, or run a process. This module stays focused on the native tools and capabilities you configure inside Copilot Studio, how the orchestrator chooses and invokes them, and how to secure and troubleshoot them.

> [!NOTE]
> **Scope:** this course doesn't include external integration development. You'll *use* existing connectors, agent flows, MCP servers, and APIs that are available to you; building custom connectors, MCP servers, or APIs is out of scope.

## At a glance

| Item | Details |
|---|---|
| **Level** | Intermediate |
| **Estimated time** | 6 hours |
| **Prerequisites** | [Module 10 — Knowledge Sources and Grounding](../10-Knowledge-Sources-and-Grounding/README.md) |
| **Harness focus** | Both, with per-harness differences — the standard harness offers more tool types today, while the Microsoft Copilot harness adds built-in file and reasoning capabilities. |
| **Lab** | Configure and test an agent using available tools |

## Why this module matters

**For beginners:** tools are what turn an assistant into a helper that gets things done — "check my order", "book the room", "open a ticket". Configuring them well is mostly about clear names, clear descriptions, and sensible inputs, not code.

**For the enterprise:** every tool is a path to a business system, so every tool is a security and governance decision. Professionals choose between user and maker credentials deliberately, require confirmation before consequential actions, respect data policies that block connectors, and design error handling so a failed call never leaves a customer stranded.

## Learning objectives

By the end of this module you will be able to:

1. **Define** what a tool is and **distinguish** tools from knowledge sources and (on the Microsoft Copilot harness) skills.
2. **Identify** the tool types available on each harness and the built-in capabilities each harness provides.
3. **Add** a prebuilt connector tool and an agent flow tool to an agent and **configure** their details, inputs, and completion behavior.
4. **Write** tool names and descriptions that lead the orchestrator to the right tool at the right time.
5. **Configure** tool inputs (dynamic filling with AI or customized collection) and **use** tool outputs in responses and topics.
6. **Choose** between end-user and maker-provided credentials and **justify** the choice for a given scenario.
7. **Invoke** tools through generative orchestration and explicitly from a topic, and **trace** each call in the activity map.
8. **Diagnose** tool errors — invalid inputs, missing connections, and tools blocked by data policies — and **manage** tools over their lifecycle.

## Topics covered

- **What are tools?** — capabilities an agent invokes to interact with external systems: look up data, take actions, and run workflows; how tools differ from knowledge, and how Microsoft 365 Copilot plugins differ from tools inside your agent.
- **Built-in capabilities** — what each harness does without extra tools: on the Microsoft Copilot harness, natively creating and editing Word, Excel, PowerPoint, and PDF files, a native code interpreter, and built-in skills; on the standard harness, an opt-in code interpreter and file input from users.
- **Agent tools** — standard-harness tool types: prebuilt connector, custom connector, agent flow, prompt, REST API (🧪 **Preview**), Model Context Protocol (MCP) server, and computer use (🟢 **GA**). Microsoft Copilot harness tool types: connectors, MCP servers (🧪 **Preview**), and workflows (🧪 **Preview**); computer use is listed as *planned* there.
- **Tool descriptions** — writing names and descriptions that say what the tool does and when to use it, because generative orchestration relies on them.
- **Tool selection** — how the orchestrator weighs descriptions, instructions, and context; restricting a tool so it runs only when a topic or child agent calls it.
- **Tool inputs and outputs** — **Dynamically fill with AI** versus customized input collection, required inputs, and using outputs in responses, topics, and conditions.
- **Tool configuration** — the tool's **Details**, **Inputs**, and **Completion** sections, including **Ask the end user before running** for consequential actions.
- **Tool invocation** — automatic invocation under generative orchestration, explicit invocation from a topic node (the only option under classic orchestration), and MCP's requirement for generative orchestration.
- **Authentication configuration** — end-user credentials (the default) versus maker-provided credentials, the connection card users see when they must connect, admin controls on maker-provided credentials, and why agents set to **No authentication** can't run tools with user credentials.
- **Tool errors** — reading errors in the activity map, missing or failed connections, connector request failures, and tools that appear unavailable because a data policy blocks them.
- **Tool management** — the classic **Tools** page and the Build-tab tools list, enabling, disabling, and deleting tools, shared tools on the **Tools** page, and keeping the number of tools (including MCP servers) manageable.
- **Agent orchestration with tools** — combining tools with knowledge and topics in one plan, multistep tool chaining, and avoiding overlap between similar tools.

## Planned hands-on lab

**Lab: Configure and test an agent using available tools**

After the lab you will have:

- A standard-harness agent with a prebuilt connector tool and an agent flow tool, each with a precise description.
- Inputs configured for both tools (one filled dynamically by AI, one customized) and confirmation turned on for the consequential action.
- A documented authentication decision for each tool (end-user versus maker-provided credentials) with the risks of each.
- Each tool invoked both through generative orchestration and explicitly from a topic, with calls traced in the activity map.
- At least one deliberately triggered tool error (bad input or missing connection) diagnosed and fixed.

**What you need:**

- Your course environment and solution; a trial license is enough to build and test (the trial **can't publish**).
- Connectors your organization's data policies allow. 💳 **Licensing/Region:** premium connectors and some tool types depend on your licensing.
- 💳 Optional comparison: adding tools to a **Microsoft Copilot harness** agent and testing them consumes Copilot Credits.

## Planned assessment

`ASSESSMENT.md` will follow the course-wide 24-item pattern, and `ANSWERS.md` will provide correct answers, detailed explanations (including why incorrect options are wrong), expected practical outcomes, and rubrics.

| Item type | Count | Planned focus for this module |
|---|---|---|
| Multiple-choice questions | 10 | Tool types per harness, configuration sections, authentication modes, invocation |
| True/false questions | 5 | Statements such as "classic orchestration can call tools without a topic" |
| Short-answer questions | 5 | When to require confirmation; end-user vs maker credentials |
| Practical implementation tasks | 2 | Configure a connector tool with customized inputs; call a tool from a topic and use its output |
| Real-world scenario challenge | 1 | Design safe tool use for an IT agent that can reset passwords |
| Troubleshooting challenge | 1 | A tool shows as unavailable and another fails at runtime — diagnose data policy and connection issues |
| **Total** | **24** | |

**Grading bands:** 0–59% Beginner · 60–74% Intermediate · 75–89% Advanced · 90–100% Professional Ready.

## Files in this module

| File | Purpose | Status |
|---|---|---|
| `README.md` | Syllabus: objectives, topics, lab outline, assessment plan (this file) | ✅ Syllabus |
| `CONCEPTS.md` | Full lessons for every topic using the course teaching sequence | 🔜 Planned |
| `STEP-BY-STEP-LAB.md` | Guided tools lab with checkpoints | 🔜 Planned |
| `EXAMPLES.md` | Tool description patterns and configuration examples | 🔜 Planned |
| `ASSESSMENT.md` | 24-item module assessment | 🔜 Planned |
| `ANSWERS.md` | Answers, explanations, and rubrics | 🔜 Planned |
| `INTERVIEW-QUESTIONS.md` | Interview questions with model answers | 🔜 Planned |
| `COMMON-MISTAKES.md` | Common mistakes, symptoms, and fixes | 🔜 Planned |

## Key official documentation

- [Add tools to custom agents (standard harness)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/add-tools-custom-agent)
- [Tools overview for agents (Microsoft Copilot harness)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/tools-overview)
- [Available tools for agents (Microsoft Copilot harness)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/tools-available)
- [Use connectors as tools](https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-connectors)
- [Use agent flows with your agent](https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-flow)
- [Extend your agent with Model Context Protocol](https://learn.microsoft.com/en-us/microsoft-copilot-studio/agent-extend-action-mcp)
- [Automate web and desktop apps with computer use](https://learn.microsoft.com/en-us/microsoft-copilot-studio/computer-use)
- [Configure user authentication for tools](https://learn.microsoft.com/en-us/microsoft-copilot-studio/configure-enduser-authentication)

## Navigation

⬅️ [Module 10 — Knowledge Sources and Grounding](../10-Knowledge-Sources-and-Grounding/README.md) | 🗺️ [Course roadmap](../COURSE-ROADMAP.md) | 📈 [Learning progress](../LEARNING-PROGRESS.md) | ➡️ [Module 12 — Prompts and Generative Answers](../12-Prompts-and-Generative-Answers/README.md)

## References

- https://learn.microsoft.com/en-us/microsoft-copilot-studio/add-tools-custom-agent
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/tools-overview
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/agents-experience/tools-available
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-connectors
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/advanced-flow
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/agent-extend-action-mcp
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/computer-use
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/configure-enduser-authentication

_Last verified against Microsoft Learn: 18 November 2026._
