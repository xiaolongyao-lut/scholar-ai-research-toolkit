# Skill Card: 开源项目页写作 (`open-source-project-page`)

Purpose: write GitHub README and project-page copy that reads like a mature open-source repository.

Best for:

- Rewriting a README first screen.
- Removing AI-ish product copy, pain-point storytelling, and internal planning language.
- Turning architecture details into a short public spine with links to deeper docs.
- Adding clear entry points for docs, Releases, screenshots, quick start, and related repositories.

Core flow:

```text
repo identity -> verified entry points -> user-facing capabilities -> quick start -> docs/release links -> compact architecture -> safety boundary
```

Voice rules:

- Start with what the repository is and what can be run, installed, inspected, or reused.
- Prefer concrete nouns: local workspace, desktop app, MCP server, backend, workflow recipe, evidence pack, OCR check, export helper.
- Put architecture details in a short section or diagram, then link to dedicated docs for module tables, code entry points, fallbacks, and boundaries.
- Keep claims tied to files, screenshots, commands, docs, tests, or Releases that exist in the repository.
- Avoid "不是 X，而是 Y" unless it prevents a common misunderstanding.
- Avoid dramatic openings such as "它想解决的不是..." or "科研里更日常的麻烦...".
- Avoid forced human/tool contrasts such as "人负责判断，工具负责...".
- Avoid abstract capability bundles such as "把 A、B、C 整理成可调用工具" when a concrete entry point is clearer.
- Avoid saying RAG, MCP, agent, or AI in the first paragraph unless the repository's primary object is that interface.
- Do not claim integrations, workflows, docs, screenshots, installers, or datasets that are not present.

Useful mature patterns:

- `cc-switch`: name, one-line purpose, screenshots, installation, user guide, releases.
- `fastmcp`: concise positioning, install-first path, small examples, docs.
- `modelcontextprotocol/inspector`: direct tool identity, run commands, screenshots, protocol context.
- `PDFMathTranslate`: exact domain, demo, install paths, CLI/API/GUI options, limitations.
- `goose`: product surfaces and extension ecosystem are visible early.
- `mempalace`: local-first positioning and usage flow before deep internals.

Rewrite examples:

| Avoid | Prefer |
|---|---|
| 它想解决的不是“再做一个聊天框”，而是科研里更日常的麻烦：PDF 放散了，笔记找不到，引用页码对不上。 | Scholar AI is a local research workspace for PDFs, evidence, notes, and literature-review writing. |
| 它把文献检索、证据包、OCR、写作导出、工作流产物和安全源码查看这些能力整理成可调用工具。 | The MCP server exposes selected Scholar AI functions to Claude and Codex: source search, literature refs, evidence packs, OCR checks, export helpers, and safe source inspection. |
| Scholar AI 的 RAG 不是只把文本丢进向量库。 | The RAG layer stores project, material, page, chunk, and integrity metadata with retrieved evidence. See the architecture docs for details. |

README first-screen checklist:

- One-sentence identity.
- Language switch and stable docs links.
- Screenshot or demo if the project has a UI.
- Install, run, or quick-start command near the top.
- Releases link when versioned downloads exist.
- No private-state, credential, or local-machine assumptions.

## Dependencies

- Target repository files: README, translated README, docs index, screenshots, release notes, and package metadata.
- Verified source links for architecture or workflow claims.
- Mature README references from comparable open-source projects.
- GitHub Releases link if the project publishes versioned downloads.
- Secret scan before committing public docs.

## Inputs

- Repository identity in one sentence.
- Verified capabilities and public boundaries.
- Existing docs links, screenshot paths, quick-start commands, and release links.
- Any sentences the user disliked or wants replaced.

## Outputs

- README or project-page copy in a calm open-source style.
- Before/after rewrites for disputed paragraphs.
- Link placement recommendations for docs, Releases, architecture, workflows, and related repositories.
- A short check report covering links, claims, public boundary, and secret scan.

## Boundary

This skill writes public-facing repository copy. It should not invent features, copy prose from reference projects, expose private planning language, or describe local credentials and runtime state.
