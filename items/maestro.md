---
title: "Maestro"
entity_type: "tool"
category: "AI IDEs / Editors"
last_reviewed_at: "2026-04-14"
---

# Maestro

## 一句话总结

一个让你并行运行 1 到 6 个 Claude Code、Codex、Gemini CLI 等会话的桌面开发环境，每个会话都有独立 git worktree。

## 快速判断

- 如果你想并行跑多个 coding agent，它值得优先看
- 如果你只需要一个终端里跑一个 agent，它可能偏重
- 它更像多 agent 桌面开发环境，而不是普通终端工具

## 你会怎么用它

- 接进 AI 开发流：为不同 feature、bugfix、refactor 同时开多个独立 agent 会话
- 接进日常工作流：用 worktree 隔离分支、统一看状态、切换会话和管理插件
- 最小落地方式：先开 2 个会话并行处理两个不同任务，验证 worktree 隔离和切换效率

## 它解决什么问题

- 单个 coding assistant 串行工作时，等待和上下文切换成本很高
- 多 agent 并行时，分支、目录和会话边界容易混乱
- 开发者需要一个专门为 AI coding workflow 设计的桌面入口

## 适合谁

- 想并行使用多个 coding agent 的开发者
- 重视 worktree 隔离和多终端会话管理的工程团队
- 想把多 agent 开发做成稳定桌面工作台的用户

## 核心能力

- 并行会话：同时运行 1 到 6 个 AI coding sessions
- Worktree 隔离：每个会话分支与目录分开，减少互相污染
- 多 agent 支持：Claude Code、Codex、Gemini CLI 等统一入口
- 桌面工作台：状态、分屏、快捷键、插件和 git graph 都集中在一个 app 里

## 能力边界

- 明显可用：多任务并行 AI coding 场景
- 效果一般：只用单一 agent、单一会话的轻量场景
- 不要误用：它不是 provider 路由层，也不是普通 shell 管理器

## 集成方式

- 作为单独工具：直接作为日常主工作台使用
- 作为 AI 工作流组件：放在多 agent 执行与上下文隔离层
- 作为团队流程节点：适合个人或小团队形成稳定的并行 AI coding 习惯

## 上手建议

- 先从 2 个并行会话开始，不要一上来开满
- 最值得先试的是“一个功能开发 + 一个 bugfix”这种天然可并行的组合
- 如果你目前的 git worktree 习惯还不稳定，先把分支和清理规则理顺

## 选型建议

- 如果你的主需求是“多 agent 并行开发桌面环境”，适合看它
- 如果你的主需求只是“找一个 AI CLI”，它不是这类项目
- 如果你想要 Emdash 之外更偏本地桌面工作台的方案，它值得比较

## 为什么值得关注

- 它明确围绕“并行 AI coding”这个高价值场景设计
- worktree 隔离和桌面可视化结合得很直接
- 对重度 AI 编程用户来说，这类工作台工具有明显复利

## 官方链接

- **官网:** https://its-maestro-baby.github.io/maestro/
- **GitHub:** https://github.com/its-maestro-baby/maestro
- **更新记录:** https://github.com/its-maestro-baby/maestro/releases

## 标签

- `Parallel Agents`, `Desktop App`, `Worktrees`, `Claude Code`, `Codex`
