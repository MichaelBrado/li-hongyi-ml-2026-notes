# 第1课：AI Agent 基础

> 解剖小龙虾 — 以 OpenClaw 为例介绍 AI Agent 的运作原理

## 基本概念

### OpenClaw（AI Agent）是什么？

OpenClaw（AI Agent）**不是人工智能（语言模型）**，而是在语言模型基础上构建的系统。

### 语言模型

| 术语 | 说明 |
|------|------|
| **call** | 输入（给 prompt） |
| **response** | 输出（对应 call 的文字接龙回答） |
| **Context Window** | 输入+输出的长度，有限 |

## 如何知道自己是谁 — System Prompt

System Prompt 包含以下关键组成部分：

- 身份相关: SOUL.md, IDENTITY.md, USER.md, MEMORY.md
- 使用工具相关: 可以使用的 SKILL，行为相关 (AGENT.md)
- 记忆相关

> 注意: 每次 call 语言模型的 prompt 上都会附上 system prompt，但由于无记忆机制，可能导致 token 急剧增加。

## 如何用电脑

- 通过 `exec` 执行 shell command，即文字指令操控
- **安全风险防范**:
  1. 通过 MEMORY.md（prompt 层面，不够保险）
  2. 人工核验指令

## 如何使用工具

- Agent 会自己创建工具
- **Sub-agent**: 即 `sessions_spawn`（繁殖新的龙虾）

## 相关资源

- [李宏毅老师 YouTube 频道](https://www.youtube.com/c/LeeHungyi)
- [原始飞书笔记](https://scnnqvnk0vfw.feishu.cn/wiki/VoJCwwB88iQEfjkLWf2cmSCUnAh)