# Evidence Pack Workflow

Goal: turn a research question into source-grounded refs, evidence items, and an integrity status that can be reused by an AI agent or a human writer.

## Inputs

- Research question or topic.
- Scholar AI project id.
- Optional constraints: paper types, time range, methods, materials, or target section.

## Tool Chain

```text
literature.list_projects
-> literature.search_refs
-> literature.evidence_pack_build
-> literature.evidence_integrity_gate
-> literature.knowledge_context_receipt
```

## Steps

1. List projects and choose the project that owns the source material.
2. Search refs with a focused query. Prefer refs with material id, page/chunk locator, title, and snippet.
3. Build an evidence pack from selected refs.
4. Run the integrity gate before using the pack in writing.
5. When a model will use the pack, request a context receipt so the final answer can cite the loaded context hash.

## Output

- Query and project id.
- Selected refs.
- Evidence pack summary.
- Integrity gate verdict.
- Context receipt hash when model loading needs proof.

## Acceptance Check

The workflow is complete only when every major claim has a ref, page/chunk locator, and an integrity status. Search hits alone are not evidence.
