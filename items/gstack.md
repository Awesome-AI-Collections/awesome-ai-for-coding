---
title: "gstack"
entity_type: "tool"
category: "Engineering Workflows"
last_reviewed_at: "2026-04-13"
---

# gstack

## 一句话总结

一个把 Claude Code 组织成虚拟创业团队的软件工厂框架，用 23 个 skills 把产品规划、设计、实现、审核、测试、发布、监控和复盘串成完整工程闭环。

## 快速判断

- 如果你想把 Claude Code 从“会写代码的助手”升级成“有角色分工的完整软件工厂”，它值得优先看
- 如果你只想补几个零散 prompt 或单点技能，不一定需要它这么重的流程化体系
- 它更像一套可执行的 AI 工程组织方法，而不是单个高光技巧仓库

## 你会怎么用它

- 接进 AI 开发流：把需求澄清、设计评审、代码审核、QA、安全、发布和复盘变成可重复执行的 slash command 链路
- 接进日常工作流：让自己或小团队在一个 Claude Code 体系里，按“想清楚 -> 写 -> 审 -> 测 -> 发 -> 复盘”固定节奏工作
- 最小落地方式：先挑一条最痛的链路，例如 `/office-hours + /plan-eng-review + /review`，验证这种角色化流程是不是比你现在更稳

## 它解决什么问题

- 很多 Claude Code 用法仍然停留在“开个会话直接写”，缺少角色分工和阶段边界
- 开发者想把产品判断、工程评审、浏览器 QA 和发布流程都交给 AI，却没有统一工作台
- 即使有多 agent，没有流程的话也容易变成并行混乱而不是并行产出

## 适合谁

- 想把 Claude Code 用成完整研发工作台的开发者
- 希望把 AI 编码流程角色化、流程化的个人和小团队
- 重视 review、QA、ship 和安全检查闭环的 AI 原生构建者

## 核心能力

- 多角色技能系统：把 CEO、工程经理、设计师、QA、安全和发布等角色做成可调用技能
- 端到端流程链路：覆盖 `/office-hours`、规划评审、实现、review、QA、ship、retro 等完整环节
- 浏览器与验证能力：强调真实浏览器 QA、部署检查和发布前验证
- 可复制的软件工厂：通过 Markdown 技能和命令，把个人经验转成可复用流程

## 能力边界

- 明显可用：想把 Claude Code 工作流组织成完整工程闭环，而不是临时聊天式协作
- 效果一般：项目规模很小、流程要求很轻、只想快速写几段代码的场景
- 不要误用：不要把它理解成“装上就自动高效”，它本质上仍然需要你接受一套更重的工程纪律

## 集成方式

- 作为单独工具：直接把整套 skill 仓库装进 Claude Code，使用 slash commands 驱动不同阶段
- 作为 AI 工作流组件：适合放在你整个研发系统的“流程编排层”，由不同 skills 分别承接规划、审核、测试、发布
- 作为团队流程节点：适合团队把个人经验和决策顺序沉淀成一致的 AI 操作规范

## 上手建议

- 第一步先不要一次吃下 23 个 skills，先挑规划、review、QA 这三段最核心的链路试运行
- 最值得先试的场景是“过去最容易返工”的那一段，比如需求没想清楚就开写，或上线前缺 QA
- 如果你当前还没有稳定的工程节奏，先轻量试用几条高回报 skill，再逐步扩展到完整闭环

## 选型建议

- 如果你的主需求是“把 Claude Code 组织成完整研发系统”，适合用它
- 如果你的主需求只是“增强单个环节”，可能更适合先看更轻量的专项工具或 skill
- 如果你最认同的是 `Thin Harness, Fat Skills` 这种思路，gstack 是很值得深入拆解的参考样本

## 为什么值得关注

- 它不是单点提示词合集，而是完整的软件工厂打法
- 公开透明地展示了一个重度 AI 原生开发者如何高频交付
- 对想把 Claude Code 从“助手”升级成“工程系统”的人很有参考价值

## 23 个 Skills 在做什么

- 产品规划：`/office-hours`、`/plan-ceo-review`、`/plan-eng-review`、`/autoplan`
- 设计：`/plan-design-review`、`/plan-devex-review`、`/design-consultation`、`/design-shotgun`、`/design-html`
- 审核：`/review`、`/design-review`、`/devex-review`、`/cso`
- 测试：`/qa`、`/qa-only`、`/browse`
- 调试：`/investigate`
- 发布：`/ship`、`/land-and-deploy`、`/canary`、`/document-release`
- 复盘：`/retro`

## 最值得学的点

- 重点不只是某个具体 skill，而是它把完整工程闭环 skill 化了
- 它把“想清楚 -> 设计 -> 写代码 -> 审代码 -> 测试 -> 发版 -> 监控 -> 复盘”组织成了可重复执行的链路
- 这种做法很符合 Steve Yegge 提到的 `Thin Harness, Fat Skills`：不重改宿主，把判断力和流程沉淀进 skill 文件

## 类似项目

- [Superpowers](superpowers.md) - 同样强调技能系统和软件工程纪律，但 Superpowers 更偏方法论与执行约束；gstack 更像一套高频实战的软件工厂。
- [Get Shit Done](get-shit-done.md) - 同样重视 context engineering 和流程稳定性，但 GSD 更偏上下文治理；gstack 更强调多角色工作流与实际 ship 链路。

## 官方链接

- **GitHub:** https://github.com/garrytan/gstack
- **文档目录:** https://github.com/garrytan/gstack/tree/main/docs
- **更新记录:** https://github.com/garrytan/gstack/releases

## 标签

- `Claude Code`, `Skills`, `Engineering Workflow`, `QA`, `Code Review`, `Agentic Development`

## 参考依据

- 这条说明主要依据项目 README 和已收录信息整理而成
- 关于“最值得学的是完整闭环 skill 化而不是某个单 skill”的判断，来自用户补充总结与 README 的整体结构共同支撑

## 更新观察点

- 持续看技能集是否继续扩展到更多工程环节
- 关注 `/browse`、QA、ship 相关工作流是否进一步产品化
- 也值得观察它会不会从 Claude Code 重度绑定逐步扩展到更多 agent runtime
