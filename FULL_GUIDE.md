# Google Advent of Agents 2025 完整指南

**25 天。从零到生产就绪的 AI Agents，全部基于 Google Cloud。**

---

## 📖 目录大纲

| 章节 | 标题 | 一句话总结 |
|------|------|-----------|
| [Day 1](#day-1-advent-of-agents-2025-正式开始) | Advent of Agents 2025 正式开始 | 25 天的 AI Agent 学习之旅正式启程，涵盖 Gemini 3、ADK、Vertex AI Agent Engine 等核心工具。 |
| [Day 2](#day-2-用-yaml-构建第一个-ai-agent) | 用 YAML 构建第一个 AI Agent | 只需 4 行 YAML 代码，无需编程即可创建一个由 Gemini 3 驱动的可运行 AI Agent。 |
| [Day 3](#day-3-gemini-3-与-adk-的强大组合) | Gemini 3 与 ADK 的强大组合 | 使用 Gemini 3 和 ADK 获得 Google 搜索落地、Computer Use、Live API 等原生能力。 |
| [Day 4](#day-4-源码部署到生产环境) | 源码部署到生产环境 | Agent Engine 支持基于源码的部署，本地代码直接部署到生产，消除序列化问题。 |
| [Day 5](#day-5-生产级可观测性) | 生产级可观测性 | Agent Starter Pack 内置零配置的企业级可观测性，包括遥测和日志记录。 |
| [Day 6](#day-6-ide-配置与-adk-速查表) | IDE 配置与 ADK 速查表 | 构建 Agent 无需繁琐配置，Agent Starter Pack 内置 ADK 速查表适配多种 IDE。 |
| [Day 7](#day-7-代码执行器) | 代码执行器 | ADK 的 BuiltInCodeExecutor 让 Agent 能够编写、执行、调试和迭代代码。 |
| [Day 8](#day-8-上下文管理) | 上下文管理 | ADK 将上下文视为编译视图，通过分层架构避免"中间丢失"幻觉问题。 |
| [Day 9](#day-9-时间旅行与检查点) | 时间旅行与检查点 | ADK 的 rewind 功能让你能够回退到任意步骤，同时保留完整审计轨迹。 |
| [Day 10](#day-10-上下文缓存与压缩) | 上下文缓存与压缩 | 通过上下文缓存和滑动窗口压缩，解决长会话的延迟和历史膨胀问题。 |
| [Day 11](#day-11-托管-mcp-连接-google-服务) | 托管 MCP 连接 Google 服务 | Google 托管的 MCP 提供 Maps、BigQuery、GKE 等服务的统一安全接口。 |
| [Day 12](#day-12-双向流式传输) | 双向流式传输 | ADK Bidi-streaming 通过 WebSocket 实现音频、视频、文本的实时同步传输。 |
| [Day 13](#day-13-interactions-api) | Interactions API | 从无状态转向有状态工作流，支持后台执行和 Deep Research Agent 集成。 |
| [Day 14](#day-14-agent2agent-a2a-协议) | Agent2Agent (A2A) 协议 | A2A 协议让不同团队、框架、语言构建的 Agent 能够相互通信协作。 |
| [Day 15](#day-15-a2ui-agent-到用户界面) | A2UI - Agent 到用户界面 | A2UI 让 Agent 能够生成结构化 UI 组件，跨框架渲染按钮、表单等原生元素。 |
| [Day 16](#day-16-langgraph-与-a2a-集成) | LangGraph 与 A2A 集成 | 使用 Agent Starter Pack 的 langgraph_base 模板构建支持 A2A 的 LangGraph Agent。 |
| [Day 17](#day-17-gemini-3-flash-新功能) | Gemini 3 Flash 新功能 | Gemini 3 Flash 带来可配置思考级别、精细媒体分辨率和思维签名等新控制功能。 |
| [Day 18](#day-18-cloud-api-registry-工具治理) | Cloud API Registry 工具治理 | Vertex AI Agent Builder 集成 Cloud API Registry，实现集中式工具管理。 |
| [Day 19](#day-19-注册到-gemini-enterprise) | 注册到 Gemini Enterprise | 一条命令将你的 Agent 注册到 Gemini Enterprise，实现企业范围内的可发现性。 |
| [Day 20](#day-20-a2a-扩展边车模式) | A2A 扩展"边车"模式 | A2A 扩展字段让你能够携带自定义数据，同时保持向后兼容。 |
| [Day 21](#day-21-agent-竞赛获奖者名人堂) | Agent 竞赛获奖者名人堂 | 11000+ 团队竞赛结果揭晓，展示安全门、自我纠正、并行专家等获胜架构模式。 |
| [Day 22](#day-22-agent-安全策略) | Agent 安全策略 | ADK 通过 Callbacks 和 Model Armor 实现分层安全架构，替代传统提示词工程。 |
| [Day 23](#day-23-持久执行restate-插件) | 持久执行(Restate 插件) | Restate 插件让 Agent 能够暂停数天、在服务器重启后恢复、永不丢失进度。 |
| [Day 24](#day-24-a2a-化任何示例) | A2A 化任何示例 | 使用 Agent Starter Pack 为任何 ADK 或 LangGraph 示例添加完整 A2A 功能。 |

---

# Day 1: Advent of Agents 2025 正式开始

**25 天。从零到生产就绪的 AI Agents，全部基于 Google Cloud。**

## 每天直到圣诞节：

- ⚡ 一个功能，不到 5 分钟即可体验
- 💻 真正可用的复制粘贴命令
- 📖 文档链接

从快速入门 Agent 到多 Agent 编排。从本地开发到生产部署。

## 中心枢纽

收藏这个网站！每天我们都会解锁新内容和实用的代码片段。这是你的永久档案，可以补上错过的日子、找回过去的帖子，获取你在圣诞节前构建生产级 Agent 所需的代码。

## 我们将涵盖的内容

我们将深入探讨最新的工具：

- **Gemini 3**：上下文工程、Computer Use、Live API 和高级模式
- **Google ADK**：Agent 开发工具包（Python）
- **Vertex AI Agent Engine**：几分钟内部署一个 Agent
- **Agent Starter Pack**：端到端生产就绪模板

## 📚 推荐阅读

首先，请查阅作为 Kaggle「5 Days of Agents」活动一部分发布的《Agent 入门白皮书》。

**让我们准备开始构建吧！**

---

# Day 2: 用 YAML 构建第一个 AI Agent

只需不到 5 分钟，无需编写任何代码，即可使用 Gemini 3 构建你的第一个 AI Agent。

**4 行文本 = 1 个可运行的 AI Agent。**

不需要 Python。不需要编程。只需要 YAML。

我说的不是那些有限制的无代码工具。我说的是代码优先的 Agent —— 开发者为真实世界部署而构建的那种。

## 使用 4 行 YAML 你将获得：

- 一个由 Gemini 3 驱动的可运行 AI Agent
- Google 搜索集成
- 随时可部署
- 零编程知识要求

复制。粘贴。使用内置 Web UI 运行。就这么简单。

## 有趣的地方来了：

一旦你有了 YAML Agent，你可以添加：

- 内置工具 (google_search, code_execution)
- 自定义 Python 工具（当你准备好的时候）
- 用于复杂工作流的子 Agent
- 多 Agent 编排

从简单开始。按需扩展。

## 今天你将构建的内容：

尝试使用 Google ADK（纯 YAML）构建一个带有 MCP 的多 Agent 应用。

---

# Day 3: Gemini 3 与 ADK 的强大组合

Gemini 3 是 Google 迄今为止最智能的模型。只需几分钟，你就可以使用 Gemini 3 和 ADK 构建一个强大的 AI Agent，并在第一天就获得其最先进功能的原生支持。

## 使用 ADK 和 Gemini 3 你将获得：

- **Google 搜索落地**：原生访问实时网络数据
- **Computer Use（计算机操作）**：能够导航和交互 UI 的 Agent
- **Live API（实时 API）**：用于语音和视频 Agent 的实时流传输
- **原生可观测性**：完全可视化 Gemini 调用、工具使用和 Agent 推理过程

## 只需一条命令即可开始：

```bash
uvx agent-starter-pack create -y --api-key YOUR_GEMINI_API_KEY
```

无需从头编写代码。使用 Gemini CLI 或 Antigravity IDE 来生成你的 Agent。agent-starter-pack 包含一份 ADK 速查表，帮助你了解所有内容。

---

# Day 4: 源码部署到生产环境

Agent Engine 现在支持基于源码的部署。你的源代码可以直接部署到生产环境，消除常见的部署摩擦。

## 不再需要处理：

- Pickle 错误
- 序列化噩梦
- 模块路径问题

本地运行的代码现在可以直接在生产环境运行。开发和部署之间的鸿沟消失了。

## 使用 Agent Starter Pack 开始：

**创建新项目：**

```bash
uvx agent-starter-pack create my-agent -a adk_base -d agent_engine
```

**已有 ADK Agent？使用 enhance：**

```bash
uvx agent-starter-pack enhance --d agent_engine
```

然后运行 `make deploy`，搞定。

---

# Day 5: 生产级可观测性

你的 Agent 已经部署了。但它实际上在做什么？

Agent Starter Pack 现在包含生产级可观测性。零配置要求。

**企业所需的完整生产级可观测性，从第一天起就内置。**

## 两个级别的可观测性，自动配置：

### 1. Agent 遥测
- Cloud Trace 捕获每次执行
- LLM 调用及延迟细分
- 工具执行计时
- 完整对话流程可视化

### 2. Prompt-Response 日志（自动启用）
- 通过 Terraform 配置完整的端到端链路
- Log Analytics + Log Buckets 支持自定义保留期
- BigQuery Delta Lake 配合自定义视图便于查询
- 日志中无敏感数据 - 所有内容写入 GCS

## 一条命令部署：

```bash
uvx agent-starter-pack create my-agent -a adk_base -d agent_engine
make deploy
```

大多数团队需要花费数周时间搭建可观测性基础设施。而你只需几分钟即可获得。无需配置。无需设置。无需自定义埋点。只需部署并开始监控。

---

# Day 6: IDE 配置与 ADK 速查表

构建 Agent 不应该需要花一个小时进行环境配置。如果你使用 Agent Starter Pack，你已经为 Agent Development Kit (ADK) 内置了 IDE 磁吸上下文。

在附带的视频中，你可以看到 Antigravity 在零配置的情况下就能理解 ADK 的工作方式，这要归功于 Agent Starter Pack 附带的默认开启的 ADK 速查表，它适用于大多数 IDE。

## 超短命令：

```bash
uvx agent-starter-pack create deep_search --adk
```

## 资源：

- 查看 Agent Starter Pack
- 查看 ADK 文档
- 查看 ADK 速查表
- 查看 llms.txt 说明

---

# Day 7: 代码执行器

LLM 可以编写代码，在沙箱中，它们还可以执行代码。

**代码执行不仅仅是用于 vibecoding。它是解决复杂问题最有效的方式之一。**

当然对数学很有用，但我们不仅仅在谈论数学。我说的是可以在需要时编写、执行、调试、优化并交付可用"工具"的 Agent。

## 为什么代码执行对 Agent 很重要

很多时候，几行代码就是最有效的解决方案。代码是确定性的。代码是精确的。代码只是描述过程的另一种语言。

## 使用 ADK 的代码执行器你将获得：

- **BuiltInCodeExecutor** 开箱即用
- 在本地机器或托管云沙箱中运行
- 兼容 Agent Engine、Google Kubernetes Engine 和 Daytona 等云沙箱
- Agent 可以编写、测试、调试和迭代代码
- 最终输出：代码执行的结果或可运行的代码本身
- 无需复杂设置。只需启用该工具。

---

# Day 8: 上下文管理

**停止往你的 Agent LLM 里塞意大利面条式的上下文。**

"追加一切"策略是通往延迟螺旋和"中间丢失"幻觉的单程票。Google ADK 通过将上下文视为编译视图（而非巨型字符串）来转变范式。ADK 不再将原始历史记录塞入窗口，而是使用处理器流水线来动态过滤、压缩和格式化一个干净的"工作上下文"，该上下文源自结构化、持久的会话状态。

## 真正的工程需要精细控制，而不仅仅是更大的上下文窗口。

ADK 的分层架构将存储与展示分离，允许你将大型文件外部化为 Artifacts（使用句柄模式），并仅在严格必要时通过可搜索的 Memory 检索长期数据。

## 使用优化模型能力的模式为生产规模构建。

ADK 通过强制区分"静态指令"（不变的策略和模式）和"轮次指令"（动态的、控制器拥有的引导）来实施上下文缓存。

正如 Kaggle 5 天强化课程第 3 天所述，Agent 很大程度上就是"上下文管理"。

---

# Day 9: 时间旅行与检查点

你的 Agent 执行步骤 1、2、3、4……但如果你发现步骤 2 是个错误，想要倒回时间从那里重新开始呢？

**现在 ADK 有了时间旅行和检查点功能！**

运行器不会破坏性地删除历史记录，而是计算"现在"和"那时"之间的差异（状态和工件增量），并将回退事件追加到日志中。这允许你将应用程序状态恢复到特定的时间戳或调用 ID，同时保留完整的审计轨迹。

## 简单的修复方式

你不只是"回退"——你将世界恢复到完全相同的状态，并保留回退路径以备需要。

作为开发者，你可以使用 rewind 来撤销对话中的一个步骤，或者恢复到应用程序的先前状态。如果你已将其配置为知道如何执行此操作，Agent 也可以将此作为工具使用。

---

# Day 10: 上下文缓存与压缩

长时间运行的 Agent 会话面临两个敌人：**延迟**和**"中间丢失"综合症**。随着对话历史的增长，重新发送大量系统指令变得昂贵，模型也难以在最近的噪音中优先处理早期规则。

## ADK 通过两管齐下的方法解决这个问题

**第一，上下文缓存**允许你缓存提示词的不可变部分（系统指令、少样本示例），这样你就不必在每一轮都支付计算成本。

**第二，上下文压缩**防止历史膨胀。ADK 不会无限追加原始消息，而是使用滑动窗口将较旧的事件总结为简洁的"记忆"块，同时保持最近的交互逐字记录以确保精确。

---

# Day 11: 托管 MCP 连接 Google 服务

**使用托管 MCP 将 Agent 连接到 Google 服务。**

虽然 MCP 已经标准化了模型连接工具的方式，但维护社区构建服务器的负担往往导致脆弱、无管理的实现。Google 新的托管 MCP 支持通过将现有 API 基础设施升级为跨 Google Cloud 服务的统一远程层来消除这一开销。

## 统一、受治理的接口

- **Google Maps**：提供"Grounding Lite"，为 Agent 提供新鲜的地理空间数据和路线详情，防止关于物理位置的幻觉。
- **BigQuery**：使 Agent 能够解释模式并就地执行查询，无需将大量数据集移入上下文窗口。
- **GKE & Compute Engine**：将基础设施管理作为可发现的工具公开，允许真正的"Day-2"自主操作。

## 内置安全性，而非后期添加

管理员可以通过 Google Cloud IAM 管理访问权限，并使用 Google Cloud Model Armor 防御间接提示注入。

---

# Day 12: 双向流式传输

**魔法不在提示词中——而在事件循环中。**

大多数 AI Agent 依赖 HTTP（请求 → 等待 → 响应）。这会引入延迟，并使"中断" AI 变得不可能。我们使用双向流式传输打破这个循环，即 ADK Bidi-streaming。通过打开到 Gemini 的持久 WebSocket 连接，客户端输入（音频/视频/文本）和服务器输出可以同时流动。

## 工作原理：

- **应用程序初始化**：在启动时创建 Agent、SessionService 和 Runner
- **会话初始化**：为每个连接建立 Session、RunConfig 和 LiveRequestQueue
- **双向流式传输**：并发的上游和下游任务
- **优雅终止**：正确清理连接

## 特性：

- **WebSocket 通信**：实时双向流式传输
- **多模态请求**：文本、音频和图像/视频输入
- **会话恢复**：重连支持
- **Google 搜索集成**

---

# Day 13: Interactions API

AI 开发的格局正在从无状态的请求-响应循环转向有状态的多轮 Agent 工作流。随着 **Interactions API** 的 Beta 版发布，Google 提供了一个专为这个新时代设计的统一接口。

## 今天可以使用的两种方式：

### 1. "引擎"升级 (ADK)

通过设置 `use_interactions_api=True`，将对话历史和状态管理移至服务器端。这允许后台执行——非常适合长时间运行任务。

### 2. "桥接器" (A2A)

`InteractionsApiTransport` 将 A2A 消息直接映射到 Interactions API，允许现有客户端向 Deep Research Agent 发送任务。

## Interactions API 标志着根本性转变

- 将整个推理状态和历史管理卸载到 Google 的基础设施
- 启用"即发即忘"的后台执行
- 为原始模型和托管 Agent 提供统一原语

---

# Day 14: Agent2Agent (A2A) 协议

你的客户服务 Agent 需要产品信息。你的产品目录 Agent 拥有这些信息。但它们是独立的服务。

**它们如何相互通信？**

这正是 **Agent2Agent (A2A) 协议**解决的问题。A2A 是让 Agent 跨团队、框架和语言进行通信的标准。

## ADK 让实现 A2A 变得简单

将 Agent 包装在 `A2AServer` 中暴露，使用 `RemoteA2aAgent` 消费远程 Agent。感觉就像调用本地工具一样。

## Agent Starter Pack 提供：

- 带有发现端点的生产就绪 A2A Agent
- 集成测试和负载测试
- Terraform 和 CI/CD
- 预配置的可观测性

---

# Day 15: A2UI - Agent 到用户界面

🚧 聊天界面有其局限性。当 Agent 需要收集结构化数据或呈现复杂选项时，简单的文本变得繁琐。

🚀 **A2UI（Agent-to-User Interface）**将 UI 定义与渲染引擎解耦。Agent 生成结构化输出并将 JSON 行流式传输到客户端，客户端渲染原生组件。

## 使用 A2UI 你将获得：

- 🔌 **传输无关**：HTTP、SSE、WebSockets 等都可行
- 🏗️ **框架无关**：Angular、React、Flutter 或 Android
- 🔒 **安全性**：原生安全消息格式
- ✨ **生成式**：动态生成 UI 组件

⚠️ 目前处于 v0.8 公开预览版本。

---

# Day 16: LangGraph 与 A2A 集成

**使用 A2A 支持构建 LangGraph Agent！**

Agent Starter Pack 中的 `langgraph_base` 模板提供一个可用于生产的、使用 A2A 协议的 LangGraph Agent：

- **开箱即用的 A2A 服务器**
- **连接任何 UI**
- **生产就绪测试**
- **部署就绪**：为 Cloud Run 或 Agent Engine 生成 Terraform 和 CI/CD
- **Gemini Enterprise 就绪**

**一条命令创建你的 Agent。**

---

# Day 17: Gemini 3 Flash 新功能

Google 最快的模型变得更加智能了。**Gemini 3 Flash** 将旗舰级推理能力与速度和成本效益相结合。

## 基准测试性能

- MMMU-Pro 得分 **81.2%** 超越所有竞争对手
- 仅需 **$0.50/百万输入 token** 和 **$3.00/百万输出 token**

## 为开发者提供的强大新控制功能：

- 🧠 **可配置思考级别**：`high`、`low`、`minimal`
- 👁️ **精细媒体分辨率**：`low`、`medium`、`high`
- 🔐 **稳健的思维签名**：在多轮函数调用期间保留推理状态

**ADK 自动处理 Thought Signatures 的复杂流转。**

---

# Day 18: Cloud API Registry 工具治理

企业 Agent 开发中最大的摩擦不是模型——而是工具。🛑

## 解决方案：集中式工具仓库 🏛️

Vertex AI Agent Builder 与 Cloud API Registry 集成，充当私有目录，管理员策划授权的工具和 MCP 服务器。

### 工作原理：

1. 👨‍💼 **管理员**使用控制台或 CLI 启用和配置工具
2. 👨‍💻 **开发者**使用 ADK 中的 ApiRegistry 对象动态获取定义

这消除了硬编码的 API 密钥和复杂的客户端配置。

---

# Day 19: 注册到 Gemini Enterprise

**将你的 Agent 注册到 Gemini Enterprise！** 🌐

Gemini Enterprise 是 Google 为组织提供的内网搜索、AI 助手和 Agent 平台。

## Agent 画廊 🖼️

你可以注册自己的自定义 Agent。注册后，你的 Agent 就可以被组织中的每个人发现。

## 简单注册 ⚡

- 自动检测 Agent 类型
- 列出可用应用
- 获取显示名称
- 直接控制台链接

你的 Agent 从已部署变为可发现。企业范围内的可见性，零摩擦。

---

# Day 20: A2A 扩展"边车"模式

A2A 协议依赖于严格的格式。但现实世界通常需要规范中没有的数据（如 `billing_id`）。

## 解决方案：A2A 扩展 🧩

专用的扩展字段像"边车"一样附加在消息上，携带自定义数据但不改变核心结构。

## 黄金法则：非破坏性 ✨

**如果你不理解它，就忽略它。** 这允许升级 Agent 而不破坏与旧 Agent 的通信。

---

# Day 21: Agent 竞赛获奖者名人堂

## 🏆 超过 11,000 支团队参与竞争

### 四个赛道的获奖者：

**🟢 公益 Agent 赛道**
- 🏆 碳足迹优化引擎

**🏢 企业 Agent 赛道**
- 🏆 Chaos Playbook Engine

**🛎️ 礼宾 Agent 赛道**
- 🏆 NewsPulse AI Agent

**🎨 自由赛道**
- 🏆 Daedalus - The Agentic Toolsmith

## 🧠 获胜架构模式

1. **"安全门"模式**：风险分数超过阈值时暂停执行
2. **"自我纠正"模式**：迭代测试直到通过
3. **"并行专家"模式**：同时调度多个子 Agent

---

# Day 22: Agent 安全策略

## 提示词工程不是安全策略 🚫

企业安全需要**确定性执行**，而不是概率性合规。

## ADK 通过分层架构将"信任"替换为"验证"：

### 开发者层（Callbacks）👨‍💻
在 Agent 执行前注入确定性 Python 逻辑，剥离 PII、验证模式、阻止未授权意图。

### 基础设施层（Model Armor）🛡️
网关级别检查每个输入和输出，提供全局终止开关。

## 先保护载荷，再保护实体 🔐
Agent Identity + A2A Protocol 确保可追踪、可观察、严格授权。

---

# Day 23: 持久执行(Restate 插件)

## 不死的 Agent 🛡️

大多数 Agent 很脆弱：进程死亡，内存也会死亡。

**持久执行登场。** Restate 插件让 Agent 能够：

- ✅ **永不丢失进度** - 崩溃后准确恢复
- ✅ **休眠数天** - 暂停等待人工批准
- ✅ **优雅恢复** - 自动重试和超时
- ✅ **简化逻辑** - 标准过程式代码

代码可以暂停执行数天、在服务器重启后存活、在停止的那行代码处准确唤醒。

---

# Day 24: A2A 化任何示例

**A2A 化一切！** 将任何 ADK 或 LangGraph 示例与 A2A 一起启动。

`google/adk-samples` 仓库包含即用型 Agent：深度研究、客户服务、数据工程、财务咨询、旅行规划等。

## Agent Starter Pack 添加完整 A2A 功能：

- **自动生成的 Agent 卡片**
- **A2A 端点暴露**
- **生产基础设施**：Terraform、CI/CD、可观测性

**已经有 Agent？** 使用 `enhance` 命令添加 A2A 功能。

---

## 🎄 结语

恭喜你完成了 Google Advent of Agents 2025 的 24 天学习之旅！

从零开始到生产就绪，你已经掌握了：

- **Gemini 3** 的核心能力
- **Google ADK** 的完整工作流
- **Agent Engine** 的部署和可观测性
- **A2A 协议** 的多 Agent 协作
- **安全与治理** 的最佳实践

**Let's keep building!** 🚀
