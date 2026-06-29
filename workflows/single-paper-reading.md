# Single-Paper Reading Workflow

Goal: read one paper into a reusable packet with metadata, chunks, figure candidates, key claims, limitations, and handoff notes.

Scholar AI toolbox reference: [Claude / Codex Toolbox](https://github.com/xiaolongyao-lut/Scholar-AI/blob/main/docs/claude-codex-toolbox.en.md).

## Inputs

- Scholar AI project id from the [Scholar AI MCP toolbox](https://github.com/xiaolongyao-lut/Scholar-AI/blob/main/docs/claude-codex-toolbox.en.md).
- Material id for one paper.
- Reading purpose, such as background, method extraction, comparison, or citation support.

## Tool Chain

```text
literature.read_material
-> literature.get_material_chunks
-> literature.figures_candidates
-> literature.agent_resource_read
-> literature.agent_handoff_card
```

## Steps

1. Read material metadata and confirm title, authors, source, and local availability.
2. Pull bounded chunks around abstract, introduction, method, results, figures, discussion, and references.
3. Extract figure/table candidates when visual evidence matters.
4. Read only the refs needed for the current question through bounded resource reads.
5. Create a handoff card with claims, uncertainty, useful chunks, missing evidence, and next actions.

## Output

- Paper identity and reading purpose.
- Key claims and evidence refs.
- Method or dataset notes.
- Figure/table candidates.
- Limitations and open questions.
- Handoff card.

## Acceptance Check

Do not mark the paper as digested if claims are not tied to chunk refs or if figures/tables were needed but never inspected.
