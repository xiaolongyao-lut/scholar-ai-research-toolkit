# Scholar AI Research Toolkit

[中文](README.md) · [English](README.en.md) · [Scholar AI](https://github.com/xiaolongyao-lut/Scholar-AI)

This repository collects public research workflow recipes and skill cards that were designed, verified, or distilled inside the Scholar AI project. It focuses on paper reading, evidence work, translation, academic writing, OCR, and experiment design.

It does not contain local credentials, logs, runtime databases, private papers, or user project data. It is a reusable workflow companion for Scholar AI and other open-source research setups.

## Related Repositories

| Repository | Contents |
|---|---|
| [Scholar AI](https://github.com/xiaolongyao-lut/Scholar-AI) | Local research workspace, [RAG and evidence architecture](https://github.com/xiaolongyao-lut/Scholar-AI/blob/main/docs/rag-evidence-architecture.en.md), [MCP toolbox](https://github.com/xiaolongyao-lut/Scholar-AI/blob/main/docs/claude-codex-toolbox.en.md), backend, desktop app, retrieval, OCR, writing, and tests. |
| [scholar-ai-research-toolkit](https://github.com/xiaolongyao-lut/scholar-ai-research-toolkit) | This repository: public Scholar AI workflow recipes and skill cards. |

## Workflows, Skills, And Dependencies

| Area | Workflow Entry | Related Skill | Main Dependencies |
|---|---|---|---|
| Evidence pack | [workflows/evidence-pack.md](workflows/evidence-pack.md) | [Scholar AI MCP toolbox](https://github.com/xiaolongyao-lut/Scholar-AI/blob/main/docs/claude-codex-toolbox.en.md) | [Scholar AI RAG and evidence architecture](https://github.com/xiaolongyao-lut/Scholar-AI/blob/main/docs/rag-evidence-architecture.en.md), local project, indexed materials, `literature.search_refs` / `evidence_pack_build` / `evidence_integrity_gate` |
| Single-paper reading | [workflows/single-paper-reading.md](workflows/single-paper-reading.md) | [Scholar AI MCP toolbox](https://github.com/xiaolongyao-lut/Scholar-AI/blob/main/docs/claude-codex-toolbox.en.md) | [Scholar AI RAG and evidence architecture](https://github.com/xiaolongyao-lut/Scholar-AI/blob/main/docs/rag-evidence-architecture.en.md), material id, page-level chunks, figure candidate tools, Agent Workspace |
| Paper to Chinese Word | [workflows/zh-paper-word.md](workflows/zh-paper-word.md) | [中文论文 Word 转写](skills/zh-paper-word.md) (`zh-paper-word`) | Python, PyMuPDF, Pandoc, python-docx, optional OCR, user-selected translation model |
| Academic writing export | [workflows/academic-writing-export.md](workflows/academic-writing-export.md) | [学术英语话语库](skills/academic-english-discourse.md) (`academic-english-discourse`) | [Scholar AI RAG and evidence architecture](https://github.com/xiaolongyao-lut/Scholar-AI/blob/main/docs/rag-evidence-architecture.en.md), [evidence pack](https://github.com/xiaolongyao-lut/Scholar-AI/blob/main/docs/claude-codex-toolbox.en.md), writing lint, citation source checks, optional DOCX export |
| OCR material processing | [workflows/ocr-material-processing.md](workflows/ocr-material-processing.md) | [Scholar AI OCR chain](https://github.com/xiaolongyao-lut/Scholar-AI/blob/main/docs/claude-codex-toolbox.en.md) | Scholar AI OCR config, OCR engine health, scanned PDFs, user-authorized local or remote OCR |
| Orthogonal design | [workflows/orthogonal-design.md](workflows/orthogonal-design.md) | [正交实验设计](skills/orthogonal-design.md) (`orthogonal-design`) | Factor-level table, Taguchi orthogonal arrays, Python CSV/Excel output, optional response data |

## Safety Boundary

- Do not commit API keys, tokens, `.env`, cookies, browser profiles, databases, logs, or runtime state.
- Do not commit private paper full text, download caches, OCR outputs, or user project data.
- Recipes describe public process and interface shapes. Real material paths, credentials, and provider config stay local.
- When using Scholar AI, prefer its [MCP toolbox](https://github.com/xiaolongyao-lut/Scholar-AI/blob/main/docs/claude-codex-toolbox.en.md) and backend settings instead of embedding secrets in recipes.

## License

MIT for repository documentation. Third-party tools, papers, and datasets keep their own licenses and terms.
