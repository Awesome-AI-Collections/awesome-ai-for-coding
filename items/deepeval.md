---
title: "DeepEval"
entity_type: "tool"
category: "Testing"
last_reviewed_at: "2026-04-14"
---

# DeepEval

## 一句话总结

一个面向 LLM 应用、RAG 和 agents 的开源评测框架，强调把质量评测、指标比较和回归测试接进开发与 CI 流程。

## 快速判断

- 如果你需要给 LLM apps、RAG 或 agents 建立系统化测试和评测门禁，它值得优先看
- 如果你只想做一次性人工体验评估，它可能比你的需求更工程化
- 它更像 AI 应用测试框架，而不是单纯在线评测面板

## 你会怎么用它

- 接进 AI 开发流：为 prompts、模型、RAG 流程和 agent 行为写评测用例，作为回归测试运行
- 接进日常工作流：把指标比较、数据集、局部评测和端到端评测纳入开发迭代
- 最小落地方式：先给一个最关键的 prompt 或 RAG 路径写 3 到 5 条测试，再接到本地或 CI

## 它解决什么问题

- 改 prompt、换模型、换工具调用链时，很难知道质量是否退化
- LLM 应用往往缺少类似 pytest 的工程化测试框架
- 团队需要在本地和 CI 里稳定复现评测，而不是只靠人工肉眼看输出

## 适合谁

- 维护 LLM 应用、RAG 和 AI agents 的工程团队
- 想给 AI 功能建立回归测试门禁的开发者
- 同时关注指标、对比、数据集和 CI 集成的 AI 质量团队

## 核心能力

- 丰富指标体系：覆盖回答相关性、幻觉、任务完成、工具正确性等多类评测
- 端到端 + 组件级测试：既能测整个应用，也能测某个子环节
- 数据集与 benchmark：支持合成数据集、基准评测和模型比较
- CI 集成：可纳入本地测试与流水线，形成发布门禁

## 能力边界

- 明显可用：需要系统化评测和回归测试 LLM 系统
- 效果一般：只想做轻量人工检查，不打算维护测试资产的场景
- 不要误用：它不是生产监控平台本体，也不是只看 dashboard 的无代码工具

## 集成方式

- 作为单独工具：在本地为 LLM 应用编写和运行评测
- 作为 AI 工作流组件：放在测试层，为 prompts、RAG、agents 和工具调用做质量门禁
- 作为团队流程节点：适合接在模型切换、prompt 调整、发布前验证和 CI/CD 中

## 上手建议

- 先从最核心的一条用户任务路径开始写评测，而不是一上来铺大量指标
- 最值得先试的是“最近最常出问题”的一个任务或 agent 行为
- 如果团队还没有稳定测试习惯，先把它当关键路径回归工具，不要一上来追求覆盖率

## 选型建议

- 如果你的主需求是“工程化评测 LLM 应用”，适合看它
- 如果你的主需求只是“上线前做几次主观检查”，更轻的方式可能已经够用
- 如果你同时要 agent、RAG、benchmark 和 CI 集成，DeepEval 很有代表性

## 典型使用场景

- 给 RAG 系统做回答相关性、幻觉和上下文利用评测
- 给 agent 做任务完成、工具正确性和计划执行类测试
- 在切换模型或 prompt 时做自动对比和回归门禁

## 为什么值得关注

- 它已经不只是单一指标库，而是在向完整 LLM 测试框架演进
- 对 AI 工程团队来说，评测能力越早工程化，后续迭代越稳
- 和只做在线平台不同，它强调本地与代码侧集成，对开发工作流更友好

## 类似项目

- [Promptfoo](promptfoo.md) - 同样强调评测和测试门禁，但 Promptfoo 更偏 prompt / red team / CI 实战
- [DeepTeam](deepteam.md) - 同属 Confident AI 体系，但 DeepTeam 更聚焦红队与安全对抗测试

## 官方链接

- **文档:** https://deepeval.com/docs/getting-started
- **GitHub:** https://github.com/confident-ai/deepeval
- **更新记录:** https://github.com/confident-ai/deepeval/releases

## 标签

- `LLM Evaluation`, `Testing`, `RAG`, `Agents`, `CI`

## 更新观察点

- 后续重点看 agent metrics、dataset 生成和 CI 集成是否继续增强
- 关注本地运行能力和平台层联动是否保持平衡，不要过度偏向云端面板
- 维护时优先重抓 README、文档和 releases
