---
title: "Loopwise"
entity_type: "tool"
category: "Code Review"
last_reviewed_at: "2026-04-14"
---

# Loopwise

## 一句话总结

一个把 Claude Code 生成和 Codex 审查串成自动 review loop 的工具，适合给计划和代码多加一层交叉审查。

## 快速判断

- 如果你想把“Claude 先写、Codex 再审、再回给 Claude 修”的闭环接进开发流程，它值得优先看
- 如果你只想要单模型快速出结果，不想引入多轮审查和额外调用成本，先看更轻的方案
- 它更像 AI code review 工作流编排器，不是单一模型客户端

## 你会怎么用它

- 接进 AI 开发流：放在 plan review、code review、commit gate 或大改前复核环节
- 接进日常工作流：在写完方案、实现关键模块或提交前，用它做“第二双眼睛”检查
- 最小落地方式：先从 `/loopwise-gate` 或单文件 review 开始，验证值不值得进入正式流程

## 它解决什么问题

- 单一模型容易在方案合理性、边界条件或代码风险上出现盲区
- 开发者想把 AI review 变成稳定流程，而不是一次性问答
- 方案评审、实现评审和提交前检查往往分散，难以形成闭环

## 适合谁

- 想把 Claude Code 与 Codex 组合成审查闭环的开发者
- 需要在计划评审、实现评审和提交前 gate 上加一道 AI review 的团队
- 想减少单模型盲区、提升代码与方案质量的人

## 核心能力

- 双模型交叉审查：Claude 负责生成与修订，Codex 负责结构化 review
- 多入口：既支持 Claude Code slash commands，也支持独立 shell command
- Review Gate：可以在提交前快速审 git diff
- 背景执行与状态查询：适合把 review 放进不阻塞主线程的工作流
- 审查结果结构化：输出 findings、严重级别和 disposition，而不是纯自然语言吐槽

## 能力边界

- 明显可用：高风险改动、设计评审、重构前复核、提交前 gate
- 效果一般：极小改动、一次性脚本或你根本不需要第二审稿人的场景
- 不要误用：它不能替代真实测试、运行验证和最终的人类判断；也不是零成本的“自动更强”

## 集成方式

- 作为单独工具：直接在 Claude Code 里跑 `/loopwise` 或在 shell 里跑 `loopwise`
- 作为 AI 工作流组件：放在生成之后、提交之前的 review 层和质量门禁层
- 作为团队流程节点：适合加在 spec review、大改前复核和 pre-commit diff 检查阶段

## 上手建议

- 第一步先用它审一份已有 plan 或单个关键文件，不要先上全仓大循环
- 最值得先试的是“你本来就想找第二视角复核”的改动
- 如果团队对双模型调用成本敏感，先用 gate 模式验证收益，再决定是否全流程化

## 选型建议

- 如果你的主需求是把 AI review 变成可重复闭环，适合用它
- 如果你的主需求只是单次代码问答，直接用 Claude Code 或 Codex 就够了
- 如果你最看重的是终端入口，它有 CLI；但真正的核心价值仍然是 code review 质量闭环

## 为什么值得关注

- 它不是“又一个 CLI”，而是把双模型交叉审查显式产品化了
- 对计划和代码都能用，覆盖范围比单纯 PR review 更广
- 很适合那些已经在并用 Claude Code 和 Codex 的开发者，把零散习惯收敛成固定流程

## 类似项目

- [cc-connect](cc-connect.md) - 更偏本地 AI coding agents 之间的桥接；Loopwise 更聚焦 plan/code review 闭环。
- [Emdash](../../awesome-cli-for-ai/items/emdash.md) - 更偏 agentic development environment；Loopwise 更具体地解决双模型审查流程。

## 官方链接

- **GitHub:** https://github.com/haohappy/loopwise
- **更新记录:** https://github.com/haohappy/loopwise/releases

## 标签

- `Code Review`, `Claude Code`, `Codex`, `CLI`, `Automation`

## 参考依据

- 这条说明主要依据项目 README、命令设计、使用示例和 releases 页面整理而成
- 关于“归入 code review 而非 CLI 本体”的判断，来自它的主价值明显发生在开发评审流程里

## 更新观察点

- 后续重点看 review report、gate、background 执行这些能力是否继续稳定
- 关注它对更多模型、更多 review 模式和 CI 集成的支持
- 观察它是否继续强化 findings 结构化输出和误报控制
