---
title: "Web Access"
entity_type: "tool"
category: "Engineering Workflows"
last_reviewed_at: "2026-04-14"
---

# Web Access

## 一句话总结

一个给 Claude Code、Codex、Cursor、Gemini CLI 等 AI agents 补上完整联网能力的开源 skill，核心补的是联网策略选择、CDP 浏览器操作和站点经验复用。

## 快速判断

- 如果你经常让编码 agent 访问登录态网站、动态页面或需要真实浏览器交互，它很值得优先看
- 如果你只需要普通网页搜索和静态抓取，不一定非要上它
- 它更像一个“agent 浏览能力增强层”，不是单一网站爬虫

## 你会怎么用它

- 接进 AI 开发流：把 `SKILL.md` 装进 Claude Code、Codex、Cursor 等宿主，让 agent 自动选择 WebSearch、curl、Jina 或 CDP
- 接进日常工作流：让 agent 处理后台页面、视频截帧、文件上传和需要登录态的网站操作
- 最小落地方式：先完成 Chrome CDP 前置配置，再让 agent 跑一次带登录态的网站任务

## 它解决什么问题

- 原生 WebSearch / WebFetch 在复杂网站、登录态页面和动态交互场景里经常不够用
- 很多 agent 会浏览网页，但不会根据场景自动选择最合适的联网工具
- 同一个站点的操作经验如果不能复用，agent 每次都要重新试错

## 适合谁

- 经常用 AI coding agents 做网页调研、后台操作和抓取任务的开发者
- 需要浏览器自动化但又不想每次都手写 Playwright 脚本的团队
- 想把联网、抓取和浏览器操作沉淀成长期可复用 skill 的使用者

## 核心能力

- 联网工具自动选择：能按任务场景组合 WebSearch、WebFetch、curl、Jina 和 CDP
- CDP Proxy：直连用户本机 Chrome，天然继承登录态，适合动态站点
- 更真实的交互：支持多种点击方式、文件上传和媒体提取
- 并行执行：多目标任务可分发给子 agent 并行处理
- 站点经验积累：按域名记录经验和陷阱，跨 session 复用

## 能力边界

- 它强在 agent 浏览与操作策略，不是低门槛的通用浏览器录制器
- 依赖 Chrome 远程调试和 Node.js 环境，前置配置比简单 skill 多一些
- 如果目标站点本身风控很强，它也不是“永不失手”的万能浏览器外挂

## 集成方式

- 作为单独工具：把仓库装成 skill，直接给 agent 用自然语言下浏览任务
- 作为 AI 工作流组件：适合放在“联网采集 / 浏览器操作 / 登录态任务执行”这一层
- 作为团队流程节点：可把复杂网页操作标准化，减少手工浏览和重复试错

## 上手建议

- 先检查 Node.js 版本和 Chrome CDP 前置项，不要一上来就跑复杂目标
- 最值得先试的是一个你自己已登录的网站，看 agent 能否稳定完成读取和点击
- 如果只是在查公开网页，先轻量使用 Jina / curl 路径，不一定要直接上 CDP

## 选型建议

- 如果你的核心需求是“让 agent 更像人一样上网”，它很合适
- 如果你的核心需求只是单站点定制抓取，可能更适合专门 scraper
- 如果你需要的是浏览器能力增强 skill，而不是完整自动化平台，它的定位很清楚

## 典型使用场景

- 让 Claude Code 读取登录后台的数据或页面状态
- 让 Codex 处理需要真实点击、文件上传和视频截帧的网站任务
- 为常用站点积累经验，提升后续 agent 浏览稳定性

## 为什么值得关注

- 它补的是很多 agent 真正缺的“联网策略层”，不是重复造一个浏览器
- 明确兼容多种支持 `SKILL.md` 的宿主，适配面比较广
- 有站点经验积累和并行分治设计，说明不是一次性 demo

## 类似项目

- [Apify MCP Server](./apify-mcp-server.md) - 更偏平台化抓取器接入，而 `Web Access` 更偏浏览与操作策略层
- [MindFS](./mindfs.md) - 更偏远程接入本地 agent 与文件系统，不负责网页浏览增强

## 官方链接

- **官网:** https://web-access.eze.is
- **GitHub:** https://github.com/eze-is/web-access
- **设计说明:** https://mp.weixin.qq.com/s/rps5YVB6TchT9npAaIWKCw

## 标签

- `Agent Skill`, `Browser Automation`, `CDP`, `Web Access`, `Claude Code`

## 更新观察点

- 后续重点看 CDP 交互能力、站点经验机制和多宿主安装方式是否继续扩展
- 优先重抓 README 和脚本目录，确认前置配置与运行模式有没有变化
- 如果后续新增更多跨平台浏览事实和代理策略，值得补进正文
