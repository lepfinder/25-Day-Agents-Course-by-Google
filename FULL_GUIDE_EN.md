# Google Advent of Agents 2025 Complete Guide

**25 days. Zero to Production-Ready AI Agents on Google Cloud.**

---

## 📖 Table of Contents

| Day | Title | Summary |
|-----|-------|---------|
| [Day 1](#day-1-advent-of-agents-2025-starts-now) | Advent of Agents 2025 Starts NOW | A 25-day journey covering Gemini 3, ADK, Vertex AI Agent Engine, and the Agent Starter Pack. |
| [Day 2](#day-2-build-your-first-ai-agent-with-yaml) | Build Your First AI Agent with YAML | Create a working Gemini 3-powered AI Agent with just 4 lines of YAML—no coding required. |
| [Day 3](#day-3-gemini-3-and-adk-powerful-combination) | Gemini 3 and ADK Powerful Combination | Get native access to Google Search grounding, Computer Use, Live API, and full observability. |
| [Day 4](#day-4-source-based-deployment-to-production) | Source-Based Deployment to Production | Agent Engine supports source-based deployment—your local code runs directly in production. |
| [Day 5](#day-5-production-grade-observability) | Production-Grade Observability | Agent Starter Pack includes zero-config enterprise observability with telemetry and logging. |
| [Day 6](#day-6-ide-configuration-and-adk-cheatsheet) | IDE Configuration and ADK Cheatsheet | Build agents without tedious setup—Agent Starter Pack includes ADK cheatsheet for multiple IDEs. |
| [Day 7](#day-7-code-executor) | Code Executor | ADK's BuiltInCodeExecutor lets agents write, execute, debug, and iterate on code. |
| [Day 8](#day-8-context-management) | Context Management | ADK treats context as a compiled view, using tiered architecture to avoid "lost in the middle" issues. |
| [Day 9](#day-9-time-travel-and-checkpointing) | Time Travel and Checkpointing | ADK's rewind feature lets you revert to any step while preserving a complete audit trail. |
| [Day 10](#day-10-context-caching-and-compaction) | Context Caching and Compaction | Solve long-session latency and history bloat with context caching and sliding window compression. |
| [Day 11](#day-11-managed-mcp-for-google-services) | Managed MCP for Google Services | Google's managed MCP provides unified, secure interfaces for Maps, BigQuery, GKE, and more. |
| [Day 12](#day-12-bidirectional-streaming) | Bidirectional Streaming | ADK Bidi-streaming enables real-time audio, video, and text flow via WebSocket connections. |
| [Day 13](#day-13-interactions-api) | Interactions API | Shift from stateless to stateful workflows with background execution and Deep Research Agent integration. |
| [Day 14](#day-14-agent2agent-a2a-protocol) | Agent2Agent (A2A) Protocol | A2A protocol enables agents built by different teams, frameworks, and languages to communicate. |
| [Day 15](#day-15-a2ui-agent-to-user-interface) | A2UI - Agent to User Interface | A2UI lets agents generate structured UI components that render as native elements across frameworks. |
| [Day 16](#day-16-langgraph-with-a2a-integration) | LangGraph with A2A Integration | Build A2A-enabled LangGraph agents using Agent Starter Pack's langgraph_base template. |
| [Day 17](#day-17-gemini-3-flash-new-features) | Gemini 3 Flash New Features | Gemini 3 Flash brings configurable thinking levels, granular media resolution, and thought signatures. |
| [Day 18](#day-18-cloud-api-registry-tool-governance) | Cloud API Registry Tool Governance | Vertex AI Agent Builder integrates with Cloud API Registry for centralized tool management. |
| [Day 19](#day-19-register-to-gemini-enterprise) | Register to Gemini Enterprise | Register your agent to Gemini Enterprise with one command for enterprise-wide discoverability. |
| [Day 20](#day-20-a2a-extensions-sidecar-pattern) | A2A Extensions "Sidecar" Pattern | A2A extension fields let you carry custom data while maintaining backward compatibility. |
| [Day 21](#day-21-agent-competition-hall-of-fame) | Agent Competition Hall of Fame | 11,000+ teams competed—discover the winning architectures: Safety Gate, Self-Correcting, Parallel Specialist. |
| [Day 22](#day-22-agent-security-strategy) | Agent Security Strategy | ADK implements layered security with Callbacks and Model Armor, replacing trust with verification. |
| [Day 23](#day-23-durable-execution-restate-plugin) | Durable Execution (Restate Plugin) | Restate plugin lets agents pause for days, survive server reboots, and never lose progress. |
| [Day 24](#day-24-a2a-ify-any-sample) | A2A-ify Any Sample | Use Agent Starter Pack to add full A2A capabilities to any ADK or LangGraph sample. |

---

# Day 1: Advent of Agents 2025 Starts NOW

**25 days. Zero to Production-Ready AI Agents on Google Cloud.**

## Every day until Christmas:

- ⚡ One feature, < 5 min to try
- 💻 Copy-paste commands that actually work
- 📖 Links to docs

From quickstart agents to multi-agent orchestration. From local dev to production deployment.

## The Hub

Bookmark this site! Each day we unlock new content along with helpful code snippets. It's your permanent archive to catch up on missed days, recover past posts, and grab the code you need to build your production agent by Christmas.

## What we are covering

We're going deep on the latest tools:

- **Gemini 3**: Context engineering, Computer Use, Live API, and advanced patterns
- **Google ADK**: The Agent Development Kit (Python)
- **Vertex AI Agent Engine**: Deploy an Agent in minutes
- **The Agent Starter Pack**: E2E production-ready templates

## 📚 Recommended Reading

To kick things off, check out the Introduction to Agents whitepaper, released as part of the 5 Days of Agents with Kaggle.

**Let's get ready to build!**

---

# Day 2: Build Your First AI Agent with YAML

Build your first AI agent with Gemini 3 in under 5 minutes without writing a single line of code.

**4 lines of text = 1 working AI agent.**

No Python. No coding. Just YAML.

I'm not talking about no-code tools with limitations. I'm talking about code-first agents. The ones developers build for real world deployment.

## What you get with 4 lines of YAML:

- A working AI agent powered by Gemini 3
- Google Search integration
- Ready to deploy
- Zero programming knowledge needed

Copy. Paste. Run with built in web UI. That's it.

## And here's where it gets interesting:

Once you have your YAML agent, you can add:

- Built-in tools (google_search, code_execution)
- Custom Python tools (when you're ready)
- Sub-agents for complex workflows
- Multi-agent orchestration

Start simple. Scale when needed.

## What you'll build today:

Try building a multi-agent app with MCP using Google ADK (pure YAML).

---

# Day 3: Gemini 3 and ADK Powerful Combination

Gemini 3 is Google's most intelligent model yet. In just a few minutes, you can build a powerful AI Agent using Gemini 3 and ADK with native, day-one support for its most advanced capabilities.

## What you get with ADK and Gemini 3:

- **Google Search grounding**: Native access to real-time web data
- **Computer use**: Agents that navigate and interact with UIs
- **Live API**: Real-time streaming for voice and video agents
- **Native observability**: Full visibility into Gemini calls, tool use, and agent reasoning

## Get started with just one command:

```bash
uvx agent-starter-pack create -y --api-key YOUR_GEMINI_API_KEY
```

No need to code from scratch. Use Gemini CLI or Antigravity IDE to generate your agent. The agent-starter-pack includes an ADK cheatsheet to guide you through everything.

---

# Day 4: Source-Based Deployment to Production

Agent Engine now supports source-based deployment. Your source code deploys directly to production, eliminating common deployment friction.

## No more dealing with:

- Pickle errors
- Serialization nightmares
- Module path headaches

What runs locally now runs in production. The gap between development and deployment is gone.

## Get started with Agent Starter Pack:

**For a new project:**

```bash
uvx agent-starter-pack create my-agent -a adk_base -d agent_engine
```

**Already have an ADK agent? Use enhance:**

```bash
uvx agent-starter-pack enhance --d agent_engine
```

Then run `make deploy` and you're done.

---

# Day 5: Production-Grade Observability

Your agent is deployed. But what's it actually doing?

Agent Starter Pack now includes production observability. Zero config required.

**Full production-grade observability that enterprises need, built-in from day one.**

## Two levels of observability, automatically configured:

### 1. Agent Telemetry
- Cloud Trace captures every execution
- LLM calls with latency breakdown
- Tool execution timing
- Full conversation flow visibility

### 2. Prompt-Response Logging (Auto-enabled)
- Full E2E journey provisioned via Terraform
- Log Analytics + Log Buckets with custom retention
- BigQuery Delta Lake with custom views for easy querying
- No sensitive data in logs - all content written to GCS

## Deploy with one command:

```bash
uvx agent-starter-pack create my-agent -a adk_base -d agent_engine
make deploy
```

Most teams spend weeks setting up observability infrastructure. You get it in minutes.

---

# Day 6: IDE Configuration and ADK Cheatsheet

Building agents shouldn't require an hour of environment configuration. If you use the Agent Starter Pack you already have IDE magnet context baked in for the Agent Development Kit (ADK).

In the attached video, you can see the Antigravity with zero config aware of how ADK works, thanks to that default-on ADK cheatsheet which ships with the Agent Starter Pack and works with most IDEs.

## Super Short Command:

```bash
uvx agent-starter-pack create deep_search --adk
```

## Resources:

- Check out the Agent Starter Pack
- Check out the ADK Documentation
- Check out the ADK Cheat Sheet
- Check out the llms.txt explanation

---

# Day 7: Code Executor

LLMs can write code, and in a sandbox, they can execute it too.

**Code execution is not just for vibecoding. It's one of the most effective ways to solve complex problems.**

Certainly useful for math, but we aren't only talking about math. I'm talking about agents that can write, execute, debug, refine, and deliver working "tools", whenever they are needed.

## Why code execution matters for agents

Many times, a few lines of code is the most efficient solution. Code is deterministic. Code is precise. And code is simply another language for describing a process.

## What you get with ADK's Code Executor:

- **BuiltInCodeExecutor** that works out of the box
- Runs on your local machine or in managed cloud sandboxes
- Compatible with cloud sandboxes like Agent Engine, Google Kubernetes Engine, and Daytona
- Agents can write, test, debug, and iterate on code
- Final output: either the result of code execution or the working code itself
- No complex setup. Just enable the tool.

---

# Day 8: Context Management

**Stop stuffing spaghetti context into your agent's LLM.**

The "append-everything" strategy is a one-way ticket to latency spirals and "lost in the middle" hallucinations. Google ADK shifts the paradigm by treating context as a compiled view (not a giant string). Instead of shoveling raw history into the window, ADK uses a pipeline of processors to dynamically filter, compact, and format a clean "working context" derived from a structured, durable session state.

## Real engineering requires granular control, not just a bigger context window.

ADK's tiered architecture separates storage from presentation, allowing you to externalize massive files as Artifacts (using a handle pattern) and retrieve long-term data via searchable Memory only when strictly necessary.

## Build for production scale with patterns that optimize for model capabilities.

ADK operationalizes Context Caching by enforcing a clear separation between "Static Instructions" (invariant policies and schemas) and "Turn Instructions" (dynamic, controller-owned steering).

As described in Day 3 of our Kaggle 5 Day intensive course, Agents are largely "context management".

---

# Day 9: Time Travel and Checkpointing

Your agent does step 1, 2, 3, 4... but what if you realize step 2 was a mistake and you want to rewind time and start from there?

**Now the ADK has time travel and checkpointing!**

Instead of destructively deleting history, the runner calculates the difference between "now" and "then" (State & Artifact Deltas) and appends a rewind event to the log. This allows you to revert the application state to a specific timestamp or invocation ID while keeping a complete audit trail of what happened.

## The simple fix

You don't just "go back"—you restore the world to exactly how it was, and you keep the rewound path in case you need it.

As a developer, you can use rewind to undo a step in the conversation, or to revert to a previous state of the application. The agent can also take this action as a tool, if you have configured it to know how to do so.

---

# Day 10: Context Caching and Compaction

Long-running agent sessions face two enemies: **latency** and **"lost in the middle" syndrome**. As conversation history grows, re-sending massive system instructions becomes expensive, and the model struggles to prioritize earlier rules against recent noise.

## The ADK solves this with a two-prong approach

**First, Context Caching** allows you to cache the immutable parts of your prompt (system instructions, few-shot examples) so you don't pay the compute cost on every turn.

**Second, Context Compaction** prevents history bloat. Instead of appending raw messages indefinitely, the ADK uses a sliding window to summarize older events into a concise "memory" block while keeping recent interactions verbatim for precision.

---

# Day 11: Managed MCP for Google Services

**Connect Agents to Google Services with Managed MCP.**

While MCP has standardized how models connect to tools, the burden of maintaining community-built servers often leads to fragile, unmanaged implementations. Google's new Managed MCP support eliminates this overhead by upgrading our existing API infrastructure into a unified, remote layer across Google Cloud services.

## A Unified, Governed Interface

- **Google Maps**: Provides "Grounding Lite" to give agents fresh geospatial data and routing details, preventing hallucinations about physical locations.
- **BigQuery**: Enables agents to interpret schemas and execute queries in-place without moving massive datasets into the context window.
- **GKE & Compute Engine**: Exposes infrastructure management as discoverable tools, allowing for true "Day-2" autonomous operations.

## Security built-in, not bolted on

Administrators can govern access via Google Cloud IAM and defend against indirect prompt injection using Google Cloud Model Armor.

---

# Day 12: Bidirectional Streaming

**The magic isn't in the prompt—it's in the Event Loop.**

Most AI agents rely on HTTP (Request → Wait → Response). This introduces latency and makes "interrupting" the AI impossible. We break that cycle using Bi-Directional Streaming, better known as ADK Bidi-streaming. By opening a persistent WebSocket connection to Gemini, client input (audio/video/text) and server output can flow simultaneously.

## How it works:

- **Application Initialization**: Creates Agent, SessionService, and Runner at startup
- **Session Initialization**: Establishes Session, RunConfig, and LiveRequestQueue per connection
- **Bidirectional Streaming**: Concurrent upstream and downstream tasks
- **Graceful Termination**: Proper cleanup of connections

## Features:

- **WebSocket Communication**: Real-time bidirectional streaming
- **Multimodal Requests**: Text, audio, and image/video input
- **Session Resumption**: Reconnection support
- **Google Search Integration**

---

# Day 13: Interactions API

The landscape of AI development is shifting from stateless request-response cycles to stateful, multi-turn agentic workflows. With the beta launch of the **Interactions API**, Google is providing a unified interface designed specifically for this new era.

## Two ways to use this today:

### 1. The "Engine" Upgrade (ADK)

By setting `use_interactions_api=True`, you move conversation history and state management to the server. This allows for background execution—perfect for long-running tasks.

### 2. The "Bridge" (A2A)

The new `InteractionsApiTransport` maps A2A messages directly to the Interactions API, allowing existing clients to send tasks to the Deep Research Agent.

## Interactions API marks a fundamental shift

- Offload entire reasoning state and history management to Google's infrastructure
- Enable "fire-and-forget" background execution
- Single, unified primitive for raw models and managed agents

---

# Day 14: Agent2Agent (A2A) Protocol

Your Customer Service Agent needs product info. Your Product Catalog Agent has it. But they're separate services.

**How do they talk to each other?**

That's exactly what the **Agent2Agent (A2A) Protocol** solves. A2A is a standard for agents to communicate—across teams, frameworks, and languages.

## ADK makes implementing A2A simple

Wrap your agent in an `A2AServer` to expose it. Use `RemoteA2aAgent` to consume remote agents. Feels just like calling a local tool.

## Agent Starter Pack gives you:

- Production-ready A2A agent with discovery endpoint
- Integration and load tests included
- Terraform and CI/CD generated
- Observability pre-configured

---

# Day 15: A2UI - Agent to User Interface

🚧 Chat interfaces have a ceiling. When an agent needs to collect structured data or present complex options, simple text becomes tedious.

🚀 **A2UI (Agent-to-User Interface)** decouples the UI definition from the rendering engine. Your agent generates structured outputs and streams JSON lines to the client, which renders native components.

## What you get with A2UI:

- 🔌 **Transport Agnostic**: HTTP, SSE, WebSockets, etc are feasible
- 🏗️ **Framework Agnostic**: Angular, React, Flutter, or Android
- 🔒 **Security**: Native secure message format
- ✨ **Generative**: Agents can generate UI components on the fly

⚠️ Currently in v0.8 (Public Preview).

---

# Day 16: LangGraph with A2A Integration

**Build LangGraph agents with A2A support!**

The `langgraph_base` template in the Agent Starter Pack gives you a production-ready LangGraph agent that speaks the A2A protocol:

- **A2A server out of the box**
- **Connect to any UI**
- **Production-ready testing**
- **Deployment ready**: Terraform and CI/CD for Cloud Run or Agent Engine
- **Gemini Enterprise ready**

**Create your agent with one command.**

---

# Day 17: Gemini 3 Flash New Features

Google's fastest model just got a lot smarter. **Gemini 3 Flash** combines flagship-level reasoning with the speed and cost-efficiency you expect from the Flash series.

## Benchmark Performance

- **MMMU-Pro**: 81.2% outscoring all competitors
- Only **$0.50/1M input tokens** and **$3.00/1M output tokens**

## Powerful new controls for developers:

- 🧠 **Configurable Thinking Levels**: `high`, `low`, `minimal`
- 👁️ **Granular Media Resolution**: `low`, `medium`, `high`
- 🔐 **Robust Thought Signatures**: Preserve reasoning state during multi-turn function calling

**ADK automatically handles the complex circulation of Thought Signatures.**

---

# Day 18: Cloud API Registry Tool Governance

The biggest friction in enterprise agent development isn't the model—it's the tools. 🛑

## The Solution: A Centralized Tool Repository 🏛️

Vertex AI Agent Builder integrates with Cloud API Registry. This acts as a private catalog where administrators curate authorized tools and MCP servers.

### How it works:

1. 👨‍💼 **Admins** enable and configure tools using the console or CLI
2. 👨‍💻 **Developers** use the ApiRegistry object in the ADK to dynamically fetch definitions

This eliminates hardcoded API keys and complex client-side configuration.

---

# Day 19: Register to Gemini Enterprise

**Register your agent to Gemini Enterprise!** 🌐

Gemini Enterprise is Google's intranet search, AI assistant, and agentic platform for organizations.

## The Agents Gallery 🖼️

Register your own custom agents. Once registered, your agent becomes discoverable to everyone in your organization.

## Simple Registration ⚡

- Auto-detects agent type
- Lists available apps
- Fetches display name
- Direct console link

Your agent goes from deployed to discoverable. Enterprise-wide visibility, zero friction.

---

# Day 20: A2A Extensions "Sidecar" Pattern

The A2A protocol relies on a strict format. But real-world complexity often requires data that isn't in the spec (e.g., `billing_id`).

## The Solution: A2A Extensions 🧩

A dedicated extension field acts like a "Sidecar" attached to your message, carrying custom data without altering the core structure.

## The Golden Rule: Non-Breaking ✨

**If you don't understand it, ignore it.** This allows upgrading agents without breaking communication with older agents.

---

# Day 21: Agent Competition Hall of Fame

## 🏆 Over 11,000 teams competed

### Winners across four tracks:

**🟢 Agents for Good Track**
- 🏆 Carbon Footprint Optimization Engine

**🏢 Enterprise Agents Track**
- 🏆 Chaos Playbook Engine

**🛎️ Concierge Agents Track**
- 🏆 NewsPulse AI Agent

**🎨 Freestyle Track**
- 🏆 Daedalus - The Agentic Toolsmith

## 🧠 Winning Architectures

1. **The "Safety Gate" Pattern**: Pause execution when risk scores exceed threshold
2. **The "Self-Correcting" Pattern**: Iterate until tests pass
3. **The "Parallel Specialist" Pattern**: Dispatch multiple sub-agents simultaneously

---

# Day 22: Agent Security Strategy

## Prompt Engineering is not a Security Strategy 🚫

Enterprise security requires **deterministic enforcement**, not probabilistic compliance.

## ADK replaces "trust" with "verification" through a tiered architecture:

### The Developer Layer (Callbacks) 👨‍💻
Inject deterministic Python logic before agent execution—stripping PII, validating schemas, blocking unauthorized intents.

### The Infrastructure Layer (Model Armor) 🛡️
Gateway-level inspection of every input and output, providing a global kill-switch.

## Secure the Payload, then Secure the Entity 🔐
Agent Identity + A2A Protocol ensures traceable, observable, strictly authorized communication.

---

# Day 23: Durable Execution (Restate Plugin)

## The Unkillable Agent 🛡️

Most agents are fragile: if the process dies, the memory dies.

**Enter Durable Execution.** The Restate plugin lets agents:

- ✅ **Never lose progress** - Resume exactly where it stopped
- ✅ **Sleep for days** - Pause for human approval
- ✅ **Recover gracefully** - Automatic retries and timeouts
- ✅ **Simplify Logic** - Standard procedural code

Code can pause execution for days, survive server reboots, and wake up exactly on the line where it left off.

---

# Day 24: A2A-ify Any Sample

**A2A-ify anything!** Take any ADK or LangGraph sample and launch it with A2A on top.

The `google/adk-samples` repository contains ready-to-use agents: deep research, customer service, data engineering, financial advising, travel planning, and more.

## Agent Starter Pack adds full A2A capabilities:

- **Auto-generated agent card**
- **A2A endpoint exposed**
- **Production infrastructure**: Terraform, CI/CD, observability

**Already have an agent?** Use the `enhance` command to add A2A capabilities.

---

## 🎄 Conclusion

Congratulations on completing the 24-day Google Advent of Agents 2025 journey!

From zero to production-ready, you've mastered:

- **Gemini 3** core capabilities
- **Google ADK** complete workflows
- **Agent Engine** deployment and observability
- **A2A Protocol** multi-agent collaboration
- **Security & Governance** best practices

**Let's keep building!** 🚀
