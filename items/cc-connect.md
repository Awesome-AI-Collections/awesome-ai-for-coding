---
title: "cc-connect"
entity_type: "tool"
category: "Engineering Workflows"
last_reviewed_at: "2026-04-14"
---

# cc-connect

## 一句话总结

一个把本地 Claude Code、Codex、Gemini CLI 等 coding agents 桥接到飞书、钉钉、Slack、Telegram 等聊天平台的远程协作工具。

## 快速判断

- 如果你想随时从手机或聊天软件控制本地 coding agents，它值得看
- 如果你只在本机终端里使用 agent，不一定需要它的消息桥接层
- 它更像 coding agent 的 remote ops 层，而不是普通聊天机器人

## 你会怎么用它

- 接进 AI 开发流：把本地 coding agents 暴露到团队常用消息渠道，远程发任务、收回复、看状态
- 接进日常工作流：在飞书、Telegram、Slack 等平台里直接继续你的 agent 会话
- 最小落地方式：先绑定一个最常用消息平台和一个本地 agent，验证远程控制体验

## 它解决什么问题

- 本地 coding agents 离开电脑就断了操作入口
- 团队沟通平台和 agent 会话分裂，消息和执行状态很难统一
- 多种平台、多种 agents 的桥接配置容易重复劳动

## 适合谁

- 想随时远程操控 coding agents 的开发者
- 需要把 AI 编码助手接进团队沟通渠道的工程团队
- 同时使用多个 agent 和多个消息平台的用户

## 核心能力

- 多平台桥接：支持飞书、钉钉、Slack、Telegram、Discord 等
- 多 agent 支持：覆盖 Claude Code、Codex、Gemini CLI、OpenCode 等
- 远程控制：支持从聊天平台发命令、切换模型、管理会话
- 调度与记忆：支持 cron、memory、目录切换等运维型操作

## 能力边界

- 明显可用：需要远程控制或群聊协作 coding agents
- 效果一般：纯本地单人使用、没有消息桥接需求的场景
- 不要误用：它不是消息平台自动化大全，核心是服务 coding agents

## 集成方式

- 作为单独工具：单机运行，桥接一个或多个消息平台
- 作为 AI 工作流组件：放在远程协作和通知层，承接 coding agent 会话入口
- 作为团队流程节点：适合让 agent 会话进入团队日常沟通链路

## 上手建议

- 第一步先绑定一个消息平台和一个 agent，不要一开始就全平台铺开
- 最值得先试的是“离开电脑也要继续盯 agent”的场景
- 如果你的团队对权限边界敏感，先把 admin 和 command 范围收紧再扩大

## 选型建议

- 如果你的主需求是“远程控制 coding agents”，适合看它
- 如果你的主需求只是“本地并行跑 agents”，更偏本地工作台的工具可能更适合
- 如果你要的是消息平台桥接而不是新 agent，本条目更有价值

## 为什么值得关注

- 它把 coding agent 会话真正延伸到了移动端和消息平台
- 对长期运行的 agent 来说，消息桥接能显著降低盯盘成本
- 这是很典型的 AI coding workflow 外围基础设施

## 官方链接

- **GitHub:** https://github.com/chenhg5/cc-connect
- **更新记录:** https://github.com/chenhg5/cc-connect/releases

## 标签

- `Coding Agents`, `Remote Control`, `Chat Platforms`, `Claude Code`, `Codex`
