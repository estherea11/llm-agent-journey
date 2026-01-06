# ReAct: Reason + Act

[English version below ⬇️]

---

## 中文说明

### ReAct 解决了什么问题？

纯粹依赖 LLM 生成文本，在以下场景中往往不稳定：

- 需要调用外部工具
- 需要多步推理
- 需要根据中间结果动态调整策略

ReAct（Reason + Act）通过 **交替生成推理与行动**，使模型能够在推理、执行与观察之间形成闭环。

---

### 核心循环（Core Loop）

一个最小的 ReAct Agent 循环可以抽象为：

1. 观察当前状态（Observation）
2. 推理下一步行动（Reasoning）
3. 执行动作（Action，例如调用工具）
4. 获取新的观察结果
5. 重复上述过程，直到满足终止条件

在本项目中，该循环被 **显式实现**，而非隐藏在任何框架内部。

---

### 实现笔记（agent-react-lab）

关键设计决策包括：

- 显式的 step 限制，用于防止无限循环
- 使用确定性工具（calculator）降低随机性
- 将工具调用视为控制流问题，而非 Prompt 技巧

---

### 当前限制

- 不包含长期记忆机制
- 不包含任务规划或分解
- 尚未引入系统化评测指标

这些限制是 **有意为之**，
将在后续实验中逐步解决。

---

## English Version

### What problem does ReAct solve?

Pure LLM prompting often struggles with tasks that require:

- External tools
- Multi-step reasoning
- Dynamic adjustment based on intermediate observations

ReAct (Reason + Act) interleaves reasoning and actions, allowing the model to form a closed loop of thinking, acting, and observing.

---

### Core Loop

A minimal ReAct-style agent loop can be abstracted as:

1. Observe the current state
2. Reason about the next action
3. Take an action (e.g., tool call)
4. Receive a new observation
5. Repeat until a termination condition is met

In this project, the loop is implemented explicitly, without relying on any agent framework.

---

### Implementation Notes (agent-react-lab)

Key design decisions include:

- Explicit step limits to prevent infinite loops
- Deterministic tools (calculator) to reduce variance
- Treating tool invocation as a control-flow problem, not a prompting trick

---

### Current Limitations

- No long-term memory
- No task planning or decomposition
- No systematic evaluation metrics yet

These limitations are intentional
and will be addressed in later labs.
