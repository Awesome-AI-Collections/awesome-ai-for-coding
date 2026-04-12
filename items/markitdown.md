---
title: "MarkItDown"
entity_type: "tool"
category: "Documentation"
last_reviewed_at: "2026-04-13"
---

# MarkItDown

## 一句话总结

微软开源的文件转 Markdown 工具，适合做 Office 文档和杂格式资料的统一转换层，但在 PDF 标题与表格保真上明显偏弱。

## 快速判断

- 如果你想先用一个统一入口把 Word、Excel、PowerPoint、网页和杂格式文件转成 LLM 可消费文本，它值得优先看
- 如果你最在意 PDF 的标题层级、表格结构和版面语义，先看别的方案
- 它更像文档 ingestion 的统一转换层和粘合层，不是单一格式上的最强解析器

## 你会怎么用它

- 接进 AI 开发流：放在 RAG、agent、知识库或文档抽取链路的最前面，先把杂格式统一转成 Markdown
- 接进日常工作流：把日常收到的 Office、网页、媒体资料先规范化成纯文本，再做整理、摘要、搜索或归档
- 最小落地方式：先挑一份 Word 或 Excel 文档跑通 CLI 或 Python API，再决定是否接入整条 ingestion 流

## 它解决什么问题

- 文档、表格、网页、音频和图片等资料格式分散，不利于统一送进 LLM 或检索管道
- 团队常常想先用一个统一入口处理杂格式资料，但不同格式的真实转换质量差异很大
- 如果不把 Office 文档和 PDF 区分开看，很容易因为它“很火”就误选到不适合的场景

## 适合谁

- 想把多种文件统一转成 LLM 友好文本的开发者
- 主要处理 Word、Excel、PowerPoint、网页和杂格式资料的工程团队
- 想先用统一接口打通文档 ingestion，再按格式逐步替换专精工具的人

## 核心能力

- 多格式转换：支持 PDF、Word、Excel、PowerPoint、图片、音频、HTML、ZIP、EPub、YouTube 等输入
- CLI 与 Python API：既能命令行批量处理，也能嵌入 Python 流水线
- 插件扩展：支持第三方插件与 OCR 扩展，便于增强特定格式处理能力
- LLM 集成：输出目标明确面向 LLM、文本分析和 MCP 场景，而非纯展示用途
- Office 文档表现更稳：就当前资料来看，Word 是它最强的格式，Excel 和 PowerPoint 也更接近“可用”水位
- PDF 能力边界明显：如果你在意标题层级、表格结构和版面语义，MarkItDown 往往不是优先选项

## 能力边界

- 明显可用：Word 文档、Excel、PowerPoint、网页和各种“先统一转文本再处理”的杂格式场景
- 效果一般：图片、音频这类依赖额外后端或外部服务的场景，通常要看额外配置
- 不要误用：不要把它当成高质量 PDF 结构化解析器，尤其不要默认它能很好保留标题和表格

## 集成方式

- 作为单独工具：直接用 CLI 或 Python API 做批量文件转 Markdown
- 作为 AI 工作流组件：适合放在采集之后、检索 / 抽取 / 摘要之前的“统一转换层”
- 作为团队流程节点：把来自邮件、文档库、共享盘的杂格式资料先标准化，减少后面每个环节重复写解析逻辑

## 上手建议

- 第一步先用你手头最典型的 Word 或 Excel 文件验证输出质量
- 最值得先试的场景是“多格式资料统一进 RAG / agent 上下文”
- 如果你的主需求是 PDF，先做轻量试用，不要在没对比 Docling 之类方案前就重投入

## 选型建议

- 如果你的主需求是 Office 文档和杂格式统一转换，适合用它
- 如果你的主需求是 PDF 高质量结构化解析，更适合看 [Docling](../../awesome-ai-for-everything-in-life/items/docling.md) 一类方案
- 如果你需要的是“统一入口”而不是“单项最强”，MarkItDown 的价值会比较明显

## 为什么值得关注

- 它不是普通文档转换器，而是明确围绕 LLM 语料和文本分析管道设计
- 统一接口、CLI、API、插件和 MCP 方向都比较完整，适合做底层粘合层
- 但它并不是“每种格式都同样强”，尤其 PDF 场景和 Office 场景要分开判断

## 类似项目

- [Docling](../../awesome-ai-for-everything-in-life/items/docling.md) - 更偏高质量文档解析，尤其 PDF 结构、表格和标题保持通常更强；MarkItDown 更偏统一转换入口。
- [Skill Seekers](skill-seekers.md) - 更偏多源资料采集、分析和打包成技能或 RAG 资产，而 MarkItDown 更专注统一转换层。
- [jina-cli](jina-cli.md) - 更偏网页读取与即时 LLM 友好化，而 MarkItDown 处理的文件类型和离线资料范围更广。

## 官方链接

- **GitHub:** https://github.com/microsoft/markitdown
- **更新记录:** https://github.com/microsoft/markitdown/releases

## 标签

- `Markdown`, `Document Conversion`, `LLM`, `RAG`, `Python`, `Microsoft`, `Office`, `PDF`

## 参考依据

- 这条说明主要依据项目 README、已收录信息，以及用户补充的评测结论整理而成
- 关于“Office 较强、PDF 明显偏弱”的边界，属于结合公开资料和用户补充判断后的维护结论，不是官方承诺

## 更新观察点

- 后续重点看插件生态和 OCR / MCP 相关能力是否继续扩展
- 优先观察它在 PDF 标题识别、表格保真和版面语义上的改进，而不只是支持格式列表
- 关注支持格式、可选依赖拆分和 Python API 稳定性是否持续演进
- 持续跟踪 releases，判断它是否从转换工具进一步演化成更完整的文档 ingestion 层
