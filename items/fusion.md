---
title: "Fusion"
slug: "fusion"
info_type: "awesome-ai-for-coding"
entity_type: "tool"
category: "Engineering Workflows"
featured: false
last_reviewed_at: "2026-04-29T08:06:58+00:00"
---

# Fusion

## 一句话总结

Fusion 是一个开源多节点编码 agent 编排器，把需求规格、计划、执行、评审、质量门禁、git worktree 和自动合并串进同一块工程任务看板。

## 它解决什么问题

- 多个编码 agent 并行跑任务时，分支、worktree、依赖顺序和冲突处理很容易失控
- 粗略想法直接交给 agent 写代码，容易缺少明确验收标准、评审步骤和质量门禁
- 团队想跨笔记本、本地工作站、Linux 服务器和云 VM 调度 agent，但状态和任务进度分散在多个机器上
- 长周期 agent 工作流如果没有任务层级、预算、心跳和暂停机制，很难稳定跑到可交付结果

## 适合谁

- 想把 Claude Code、Codex、Hermes、Ollama 等模型或 agent 统一编排起来的开发者
- 需要用 isolated git worktree 并行推进多项软件工程任务的团队
- 希望把需求澄清、计划评审、执行评审、QA、安全、性能和可访问性检查都放进同一流程的人
- 想试验“agent company”式长期任务、角色协作和跨节点执行的工程团队

## 核心能力

- 自动任务规格：把自然语言需求转成 `PROMPT.md`，补上验收标准后再让执行 agent 动手
- 流程门禁：按 Plan → Review → Execute → Review 推进任务，并支持 pre-merge / post-merge 质量检查
- worktree 隔离：每个任务运行在独立分支和 worktree，减少并行开发互相踩文件的概率
- 多节点编排：在笔记本、Mac、Linux、云 VM 等节点之间同步任务、设置、mission 和 board state
- git 管理：提供分支、worktree、stash、remote、diff、GitHub issue / PR sync 和自动 squash merge
- 长期任务组织：用 Mission → Milestone → Slice → Feature → Task 层级管理更大的工程目标
- agent 协作与学习：支持 agent 之间 mailbox 消息、任务后反思和 `AGENTS.md` 自我改进

## 典型使用场景

- 把一个功能需求拆成 spec、计划、执行、评审和合并步骤
- 在多台机器上分摊 agent 执行任务，同时保持统一任务看板和共享状态
- 让多个编码 agent 并行处理独立任务，并在依赖任务完成后自动 rebase 和合并
- 导入 Paperclip / companies 形式的 agent company，用角色、技能和组织结构跑长期 mission

## 为什么值得关注

- 它把“多 agent 编码”落到 git、worktree、任务看板和质量门禁这些工程基础设施上，而不是只停留在聊天式调度
- 多节点 mesh 和 per-task model lane 让它更接近一套分布式 agent 工程控制台
- 和 Superconductor、Conductor、cmux 这类本地多会话工具相比，Fusion 更强调长周期 mission、自动规格、自动合并和 agent company 导入

## 类似项目

- [Superconductor](superconductor.md) - 同样关注隔离 worktree 和多编码 agent 并行，但更偏原生 macOS 多 Agent 编排工作台。
- [Conductor](conductor.md) - 更偏本机 Claude Code / Codex 会话和 worktree 的桌面编排。
- [cmux](cmux.md) - 更偏 macOS 上监控多个 AI 会话的多智能体终端。
- [gstack](gstack.md) - 更偏把 Claude Code 组织成虚拟创业团队的方法论和 skills 框架。

## 官方链接

- **官网:** https://runfusion.ai/
- **GitHub:** https://github.com/Runfusion/Fusion
- **文档:** https://github.com/Runfusion/Fusion#readme
- **npm:** https://www.npmjs.com/package/@runfusion/fusion

## 标签

- `Coding Agents`, `Agent Orchestration`, `Git Worktree`, `Engineering Workflow`, `Multi-node`

## 更新观察点

- 继续观察 multi-node mesh、自动合并、冲突解决和 GitHub issue / PR sync 是否稳定成熟
- 关注 Fusion 与 Pi、Hermes、Paperclip companies 生态之间的集成边界
- 重点看 README、npm 包和 GitHub releases，判断 early preview 阶段的安装方式与核心工作流是否持续收敛
