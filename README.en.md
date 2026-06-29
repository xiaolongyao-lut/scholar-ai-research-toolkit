# Scholar AI Research Toolkit

[中文](README.md) · [English](README.en.md) · [Scholar AI](https://github.com/xiaolongyao-lut/Scholar-AI)

This repository collects public research workflow recipes and skill cards that were designed, verified, or distilled inside the Scholar AI project. It focuses on paper reading, evidence work, translation, academic writing, OCR, and experiment design.

It does not contain local credentials, logs, runtime databases, private papers, or user project data. It is a reusable workflow companion for Scholar AI and other open-source research setups.

## Related Repositories

| Repository | Contents |
|---|---|
| [Scholar AI](https://github.com/xiaolongyao-lut/Scholar-AI) | Local research workspace, MCP toolbox, backend, desktop app, retrieval, OCR, writing, and tests. |
| [scholar-ai-research-toolkit](https://github.com/xiaolongyao-lut/scholar-ai-research-toolkit) | This repository: public Scholar AI workflow recipes and skill cards. |

## Workflows

| Workflow | Entry | Use Case |
|---|---|---|
| Evidence pack | [workflows/evidence-pack.md](workflows/evidence-pack.md) | Search local literature refs, build evidence packs, and run integrity checks. |
| Single-paper reading | [workflows/single-paper-reading.md](workflows/single-paper-reading.md) | Read one paper, collect chunks, figure candidates, summary, and handoff notes. |
| Paper to Chinese Word | [workflows/zh-paper-word.md](workflows/zh-paper-word.md) | Convert foreign papers into Chinese journal-style DOCX. |
| Academic writing export | [workflows/academic-writing-export.md](workflows/academic-writing-export.md) | Turn evidence packs into outlines, checked prose, and Word output. |
| OCR material processing | [workflows/ocr-material-processing.md](workflows/ocr-material-processing.md) | Check OCR policy, engines, health, and authorized processing path. |
| Orthogonal design | [workflows/orthogonal-design.md](workflows/orthogonal-design.md) | Design Taguchi orthogonal experiments and analyze S/N ratios or responses. |

## Skill Cards

| Chinese Name | Skill ID | Card | Use Case |
|---|---|---|---|
| 中文论文 Word 转写 | `zh-paper-word` | [skills/zh-paper-word.md](skills/zh-paper-word.md) | Structured conversion from foreign papers to Chinese journal-style Word documents. |
| 正交实验设计 | `orthogonal-design` | [skills/orthogonal-design.md](skills/orthogonal-design.md) | Taguchi orthogonal experiment design and analysis. |
| 学术英语话语库 | `academic-english-discourse` | [skills/academic-english-discourse.md](skills/academic-english-discourse.md) | Academic English discourse, literature-review writing, and CN/EN translation strategy. |

## Safety Boundary

- Do not commit API keys, tokens, `.env`, cookies, browser profiles, databases, logs, or runtime state.
- Do not commit private paper full text, download caches, OCR outputs, or user project data.
- Recipes describe public process and interface shapes. Real material paths, credentials, and provider config stay local.
- When using Scholar AI, prefer its MCP toolbox and backend settings instead of embedding secrets in recipes.

## License

MIT for repository documentation. Third-party tools, papers, and datasets keep their own licenses and terms.
