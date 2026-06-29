# Scholar AI Research Toolkit

[中文](README.md) · [English](README.en.md) · [Scholar AI](https://github.com/xiaolongyao-lut/Scholar-AI)

这是一个面向科研工作的公开工具流仓库，只整理 Scholar AI 项目里已经设计、验证或沉淀出来的 workflow recipes 和 skill cards。它不包含本机凭据、日志、运行时数据库或私人文献。

这个仓库适合三类用途：

- 给 Claude / Codex 等 AI 客户端提供科研任务的操作脚本式说明。
- 给 Scholar AI 用户一个独立的工作流目录，快速找到论文阅读、翻译、写作、OCR、证据检查和实验设计流程。
- 给其他开源项目复用这些流程，而不依赖 Scholar AI 的私有运行状态。

## 与 Scholar AI 的关系

| 仓库 | 内容 |
|---|---|
| [Scholar AI](https://github.com/xiaolongyao-lut/Scholar-AI) | 本地文献工作台、MCP 工具箱、后端、桌面端、检索、OCR、写作和测试。 |
| [scholar-ai-research-toolkit](https://github.com/xiaolongyao-lut/scholar-ai-research-toolkit) | 本仓库，公开 Scholar AI 沉淀出来的科研 workflow recipes 与 skill cards。 |

## 工作流目录

| 工作流 | 入口 | 适用场景 |
|---|---|---|
| 论文证据包 | [workflows/evidence-pack.md](workflows/evidence-pack.md) | 从本地文献库检索 refs，构建证据包，做完整性检查。 |
| 单篇论文研读 | [workflows/single-paper-reading.md](workflows/single-paper-reading.md) | 阅读一篇论文，抽取 chunk、图表候选、摘要和交接卡。 |
| 外文论文转中文 Word | [workflows/zh-paper-word.md](workflows/zh-paper-word.md) | 将外文 PDF 或 LaTeX/Pandoc 输出整理为中文期刊风格 DOCX。 |
| 学术写作与导出 | [workflows/academic-writing-export.md](workflows/academic-writing-export.md) | 从证据包生成提纲、检查写作、导出 Word。 |
| OCR 材料处理 | [workflows/ocr-material-processing.md](workflows/ocr-material-processing.md) | 处理扫描型 PDF 前检查 OCR 策略、引擎和健康状态。 |
| 正交实验设计 | [workflows/orthogonal-design.md](workflows/orthogonal-design.md) | 构建设计表、选择 Taguchi 正交表、分析 S/N 比和响应。 |

## Skill Cards

| Skill | Card | 用途 |
|---|---|---|
| `zh-paper-word` | [skills/zh-paper-word.md](skills/zh-paper-word.md) | 外文论文到中文 Word 的结构化流程。 |
| `orthogonal-design` | [skills/orthogonal-design.md](skills/orthogonal-design.md) | Taguchi 正交实验设计与分析。 |
| `academic-english-discourse` | [skills/academic-english-discourse.md](skills/academic-english-discourse.md) | 英文学术话语、综述写作和中英翻译策略。 |

## 安全边界

- 不提交 API key、token、`.env`、cookie、浏览器配置、数据库、日志或本地运行状态。
- 不提交私人论文全文、下载缓存、OCR 产物或用户项目数据。
- workflow 只描述公开流程和接口形状；真实材料路径、模型凭证和供应商配置由用户本机管理。
- 需要调用 Scholar AI 时，优先使用它的 MCP 工具箱和本地后端设置，而不是把密钥写进 workflow。

## 许可

本仓库文档使用 MIT License 发布。第三方工具、论文和数据仍适用各自许可证与使用条款。
