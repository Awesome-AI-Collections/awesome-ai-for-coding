---
title: "AionUi"
entity_type: "tool"
category: "Coding Agents"
last_reviewed_at: "2026-04-14"
---

# AionUi

## 一句话总结

一个把内置 agent 与 Claude Code、Codex、OpenClaw、Qwen Code 等多种 coding agent 汇总到同一 Cowork 桌面工作台的开源应用。

## 快速判断

- 如果你想在一个界面里同时使用内置 agent 和多种外部 coding agent，它值得优先看
- 如果你只用单一 CLI agent，不一定需要它的 Cowork 平台层
- 它更像多 agent 协作工作台，而不是单纯聊天客户端

## 你会怎么用它

- 接进 AI 开发流：让内置 agent 和 Claude Code、Codex、OpenClaw 等在一个统一工作台里并行协作
- 接进日常工作流：把文件读写、web 搜索、MCP、文档生成和 coding agent 会话统一到同一桌面入口
- 最小落地方式：先用内置 agent 跑一个真实任务，再接入你已安装的一个外部 coding agent 比较体验

## 它解决什么问题

- 开发者同时使用多个 agent 时，往往界面和会话分散在不同工具里
- 很多产品要么只有内置 agent，要么只能依赖外部 CLI，不容易兼顾
- 持续运行、远程接入和多 agent 协作常常需要额外拼装

## 适合谁

- 想把多个 coding agent 放进统一界面的开发者
- 既想开箱即用，又想兼容外部 CLI agent 的用户
- 重视持续运行和远程接入的 AI 原生工程团队

## 核心能力

- 内置 agent：安装后即可用，不必先装外部 CLI 才开始
- 多 agent Cowork：可接入 Claude Code、Codex、OpenClaw、Qwen Code 等多种 agent
- 技能与助手系统：内置多个专业助手，并支持自定义 skills
- 持续运行能力：支持远程访问、计划任务和长期运行场景

## 能力边界

- 明显可用：想把多种 coding agent 收敛到统一工作台
- 效果一般：只想在终端里使用单个 CLI agent 的场景
- 不要误用：它不是纯 CLI 工具链，也不是只面向生活效率的泛助手平台

## 集成方式

- 作为单独工具：直接作为主 Cowork 桌面应用使用
- 作为 AI 工作流组件：放在多 agent 会话和工具协调层，承接内置 agent、外部 CLI 和 MCP
- 作为团队流程节点：适合个人或小团队统一一套 agent 入口和助手体系

## 上手建议

- 第一步先用内置 agent 验证文件、任务和工具能力是否满足你的需求
- 最值得先试的是把一个你常用的外部 coding agent 接入同一界面
- 如果你目前已经有重配置的终端工作流，先把它当增量入口试用，不要一开始就全量替换

## 选型建议

- 如果你的主需求是“统一多种 coding agent 的工作台”，适合看它
- 如果你的主需求只是“找一个开源 CLI agent”，更轻量的终端工具可能更适合
- 如果你很在意零配置内置 agent + 外部 agent 兼容，这条会更有价值

## 典型使用场景

- 在一个桌面应用里并行使用内置 agent 和多个外部 coding agent
- 用统一的 MCP 和 skills 管理方式服务多个 agent
- 把持续运行、远程接入和开发助手整合成同一工作台

## 为什么值得关注

- 它把“内置 agent + 外部 coding agent 汇聚”做成了一个比较完整的产品形态
- 对不想只押注单一 agent 生态的用户来说，灵活性很高
- 对 AI coding 工作台的演进方向有参考价值

## 类似项目

- [Emdash](emdash.md) - 同样是 agent 开发工作台，但 Emdash 更偏 ticket、worktree 和 PR 闭环
- [Visual Studio Code](visual-studio-code.md) - 同样能承载多种 AI 能力，但 VS Code 更偏编辑器生态，AionUi 更偏 Cowork 平台

## 官方链接

- **官网:** https://www.aionui.com
- **GitHub:** https://github.com/iOfficeAI/AionUi

## 标签

- `Coding Agents`, `Cowork`, `Desktop App`, `Multi-Agent`, `OpenClaw`

## 更新观察点

- 后续重点看支持的外部 agent 列表、MCP 同步和远程访问能力是否继续增强
- 关注内置 agent 和外部 agent 之间的边界是否越来越清晰
- 维护时优先重抓 README、AGENTS 和官网
