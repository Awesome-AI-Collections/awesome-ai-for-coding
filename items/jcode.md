---
title: "jcode"
slug: "jcode"
info_type: "awesome-ai-for-coding"
entity_type: "tool"
category: "Coding Agents"
featured: false
last_reviewed_at: "2026-04-29T08:28:00+00:00"
---

# jcode

## 一句话总结

jcode 是一个高性能 coding agent harness，面向多会话、长期记忆、swarm 协作、多 provider / MCP 接入和可自我修改的编码 agent 工作流。

## 它解决什么问题

- 许多编码 agent 在多会话并行时资源占用高，启动和交互延迟会拖慢高频迭代
- 长会话和跨会话上下文容易丢失，agent 很难自动记住过去的项目经验和用户偏好
- 多个 agent 在同一个仓库里协作时，文件变动、冲突提醒和 agent 之间沟通通常需要额外拼装
- 开发者同时使用 Claude、OpenAI、Gemini、Copilot、本地模型和 MCP 时，账号、provider 和工具配置分散

## 适合谁

- 想要开源、高性能 coding agent harness 的开发者
- 需要在同一项目中同时运行多个 agent 会话的人
- 重视长期记忆、MCP、provider 切换和多账号切换的工程团队
- 想让 agent 直接改造 harness 本身、尝试 self-dev 工作流的高级用户

## 核心能力

- 高性能会话运行：README 强调低 RAM 增量、低启动延迟和高帧率渲染，适合多会话工作流
- Agent memory：把对话 turn / response 嵌入为语义向量，并支持被动召回、主动搜索、存储和自动整理
- Swarm 协作：支持在同一 repo 中启动多个 agent，自动感知文件变动，并通过 DM / broadcast 协调任务
- Provider 与 OAuth：支持 Claude、OpenAI、Gemini、GitHub Copilot、Azure、Ollama、LM Studio、自定义 OpenAI-compatible 等多种接入
- MCP 配置：支持全局和项目级 MCP 配置，并可从 Claude / Codex 配置导入部分服务器
- 会话恢复：可从 Codex、Claude Code、OpenCode、Pi 等 harness 恢复会话继续工作
- 自我开发：支持让 jcode agent 进入 self-dev 模式，修改自身源码、构建、测试并 reload

## 典型使用场景

- 用一个轻量 harness 同时跑多个编码 agent 会话
- 在一个 repo 里让多个 agent 并行协作，并在文件变化时互相提醒
- 给编码 agent 接入长期记忆、MCP 工具和多 provider 模型
- 从 Claude Code、Codex、OpenCode 等会话中恢复上下文，继续未完成任务

## 为什么值得关注

- 它不是单纯的 provider wrapper，而是尝试把性能、记忆、UI、swarm 和 provider 接入都放进同一个 coding agent harness
- 对多会话场景的资源占用和响应延迟有明确优化目标，适合关注本地效率的重度 agent 用户
- Swarm、自我开发和跨 harness 会话恢复让它更像下一代 agent harness 实验场

## 类似项目

- [OpenCode](opencode.md) - 同样是开源编码 agent；OpenCode 更强调多入口运行，jcode 更强调高性能 harness、记忆和 swarm。
- [Claude Squad](claude-squad.md) - 更偏多个 Claude 会话的统一管理；jcode 则是完整 coding agent harness。
- [cmux](cmux.md) - 更偏 macOS 上监控多个 AI 会话的终端；jcode 更强调 agent runtime、memory 和 provider 接入。
- [Superconductor](superconductor.md) - 更偏 worktree 隔离和多 agent 编排工作台；jcode 更偏单个 harness 的高性能和可定制性。

## 官方链接

- **GitHub:** https://github.com/1jehuang/jcode
- **文档:** https://github.com/1jehuang/jcode#readme
- **更新记录:** https://github.com/1jehuang/jcode/releases

## 标签

- `Coding Agent`, `Agent Harness`, `CLI`, `Multi-Session`, `Memory`, `MCP`, `Swarm`

## 更新观察点

- 继续关注 memory、swarm、自我开发和跨 harness session resume 是否稳定成熟
- 观察 provider、OAuth、MCP 配置导入和多账号切换能力是否继续扩展
- 重点看 GitHub releases 和 README，确认性能数据、平台支持和安装方式是否持续更新
