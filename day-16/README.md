# Day 16: LangGraph + A2A

## 概述

使用 **LangGraph** 构建 Agent，通过 **Agent Starter Pack** 让你的 Agent 具备完整的 A2A 能力，可被其他 Agent 即时发现和调用。

## 核心知识点

### LangGraph 三大核心组件

```
┌─────────────────────────────────────────────────────────────┐
│    [START] ──► [Node A] ──► [Node B] ──► [END]             │
│                   │            ▲                            │
│                   └──► [Node C]┘  (条件边)                  │
└─────────────────────────────────────────────────────────────┘
```

| 组件 | 说明 |
|------|------|
| **State** | 共享内存对象，在所有节点间流转 |
| **Nodes** | 执行逻辑的函数，接收状态返回更新 |
| **Edges** | 节点间转换（静态边/条件边） |

### LangGraph vs ADK

| 特性 | LangGraph | ADK |
|------|-----------|-----|
| 设计 | 图驱动，显式控制流 | Agent 驱动，声明式 |
| A2A | 需要包装 | 原生 `to_a2a()` |
| 适用 | 复杂工作流 | 快速开发 |

### Agent Starter Pack

Google Cloud 提供的生产级模板：
- 支持 ADK、LangGraph、LangChain、CrewAI
- 一键部署到 Agent Engine / Cloud Run / GKE
- 内置 CI/CD、监控、安全配置

## 项目结构

```
day-16/
├── README.md
├── requirements.txt
├── langgraph_agent/
│   └── agent.py           # LangGraph Agent + A2A 服务
└── client/
    └── test_client.py     # 测试客户端
```

## 运行示例

### 1. 安装依赖

```bash
uv pip install langgraph langchain-google-genai
```

### 2. 启动服务 (Terminal 1)

```bash
cd day-16
uv run python -m langgraph_agent.agent
```

输出：
```
============================================================
Day 16: LangGraph + A2A
============================================================
Agent 信息:
  名称: langgraph_react_agent
  框架: LangGraph + ADK
A2A 服务端点:
  URL: http://localhost:8016
============================================================
```

### 3. 运行测试 (Terminal 2)

```bash
cd day-16
uv run python -m client.test_client
```

### 4. 验证服务

```bash
curl http://localhost:8016/.well-known/agent.json
```

### 5. 纯 LangGraph 演示（可选）

```bash
uv run python -m langgraph_agent.agent --demo
```

## 代码核心

### 构建 LangGraph 图

```python
from langgraph.graph import StateGraph, END

# 1. 定义状态
class AgentState(TypedDict):
    messages: Annotated[list, add]
    thoughts: list
    final_answer: str

# 2. 创建图并添加节点
graph = StateGraph(AgentState)
graph.add_node("reasoning", reasoning_node)
graph.add_node("answer", answer_node)

# 3. 定义边（包括条件边）
graph.set_entry_point("reasoning")
graph.add_conditional_edges("reasoning", should_continue, {...})
graph.add_edge("answer", END)

# 4. 编译
app = graph.compile()
```

### 包装为 A2A 服务

```python
from google.adk.agents import LlmAgent
from google.adk.a2a.utils.agent_to_a2a import to_a2a

# 使用 ADK 的 to_a2a() 一行代码转换
agent = LlmAgent(name="langgraph_agent", ...)
app = to_a2a(agent, host="localhost", port=8016)
```

## 关键学习点

1. **State 设计** - 合理设计状态结构是 LangGraph 成功的关键
2. **条件边** - 实现动态控制流的核心机制（ReAct 循环）
3. **混合架构** - LangGraph 构建复杂逻辑 + ADK `to_a2a()` 提供 A2A 服务
4. **Agent Starter Pack** - 生产级部署的最佳起点

## 扩展阅读

- [LangGraph 官方文档](https://langchain-ai.github.io/langgraph/)
- [Agent Starter Pack](https://github.com/GoogleCloudPlatform/agent-starter-pack)
- [A2A Protocol](https://a2a-protocol.org/)
