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

## 工作流、技能与依赖

| 方向 | 工作流入口 | 关联技能 | 主要依赖 |
|---|---|---|---|
| 论文证据包 | [workflows/evidence-pack.md](workflows/evidence-pack.md) | Scholar AI MCP 工具箱 | Scholar AI 本地项目、可检索材料、`literature.search_refs` / `evidence_pack_build` / `evidence_integrity_gate` |
| 单篇论文研读 | [workflows/single-paper-reading.md](workflows/single-paper-reading.md) | Scholar AI MCP 工具箱 | Scholar AI material id、页码级 chunks、图表候选工具、Agent Workspace |
| 中文论文 Word 转写 | [workflows/zh-paper-word.md](workflows/zh-paper-word.md) | [中文论文 Word 转写](skills/zh-paper-word.md) (`zh-paper-word`) | Python、PyMuPDF、Pandoc、python-docx、可选 OCR、用户自选翻译模型 |
| 学术写作与导出 | [workflows/academic-writing-export.md](workflows/academic-writing-export.md) | [学术英语话语库](skills/academic-english-discourse.md) (`academic-english-discourse`) | Scholar AI 证据包、写作 lint、引用来源检查、可选 DOCX 导出 |
| OCR 材料处理 | [workflows/ocr-material-processing.md](workflows/ocr-material-processing.md) | Scholar AI OCR 链路 | Scholar AI OCR 配置、OCR engine health、扫描型 PDF、用户授权的本地或远程 OCR |
| 正交实验设计 | [workflows/orthogonal-design.md](workflows/orthogonal-design.md) | [正交实验设计](skills/orthogonal-design.md) (`orthogonal-design`) | 因素/水平表、Taguchi 正交表、Python CSV/Excel 输出、响应数据可选 |

## 安全边界

- 不提交 API key、token、`.env`、cookie、浏览器配置、数据库、日志或本地运行状态。
- 不提交私人论文全文、下载缓存、OCR 产物或用户项目数据。
- workflow 只描述公开流程和接口形状；真实材料路径、模型凭证和供应商配置由用户本机管理。
- 需要调用 Scholar AI 时，优先使用它的 MCP 工具箱和本地后端设置，而不是把密钥写进 workflow。

## 许可

本仓库文档使用 MIT License 发布。第三方工具、论文和数据仍适用各自许可证与使用条款。
