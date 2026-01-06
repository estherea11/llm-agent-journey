# llm-agent-journey
系统性记录从零构建 LLM Agent 的学习与实验过程，涵盖 ReAct、工具调用、记忆、规划、评测与 Agent 系统设计。
Systematically document the learning and experimentation process of building an LLM Agent from scratch, covering ReAct, tool invocation, memory, planning, evaluation, and agent system design.

[English version below ⬇️]

---

## 中文说明

这是一个关于 **从零理解、实现并评估 LLM Agent 系统** 的长期学习与实验仓库。

本仓库的目标不是快速搭建 Demo，而是从第一性原理出发，系统性拆解 LLM Agent 的核心组成部分，包括：

- 推理-行动循环（ReAct）
- 工具调用与错误恢复
- 记忆机制（短期 / 长期）
- 任务规划与重规划
- Agent 的评测方法与失败模式分析
- Agent 系统的整体架构设计

### 仓库结构说明

- 本仓库（llm-agent-journey）：
  - 学习路线图
  - 论文阅读笔记
  - 设计思考与实验总结

- 子仓库（Labs）：
  - agent-react-lab：最小 ReAct agent 循环
  - agent-tools-lab：工具调用与鲁棒性
  - agent-memory-lab：记忆机制设计
  - agent-planning-lab：任务规划与分解
  - agent-eval-bench：评测与基准
  - agent-final-system：完整 Agent 系统整合

本项目将逐步演进，记录假设、实验、失败与改进过程。

## 当前进度

- [x] ReAct agent (minimal loop)
- [ ] Tool robustness
- [ ] Memory design
- [ ] Planning
- [ ] Evaluation

---

## English Version

This repository documents my step-by-step journey to understand, implement, and evaluate LLM-based agents from first principles.

The goal is not to build demos, but to develop a deep understanding of agent architectures, failure modes, and system-level design choices, eventually leading to a Flowise-like agent workflow engine.

## Structure

- This repo (llm-agent-journey):
  - Learning roadmap
  - Paper notes
  - Design decisions and reflections

- Labs (separate repositories):
  - agent-react-lab: minimal ReAct loop
  - agent-tools-lab: tool calling & error recovery
  - agent-memory-lab: short/long-term memory
  - agent-planning-lab: task decomposition & replanning
  - agent-eval-bench: evaluation & benchmarks
  - agent-final-system: integrated agent system

This project will evolve incrementally, documenting hypotheses, experiments, failures, and improvements.

## Current Status

- [x] ReAct agent (minimal loop)
- [ ] Tool robustness
- [ ] Memory design
- [ ] Planning
- [ ] Evaluation
