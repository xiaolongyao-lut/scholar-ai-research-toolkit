# Academic Writing And Export Workflow

Goal: turn source-grounded evidence into an outline, checked prose, and Word output.

## Inputs

- Research question or section goal.
- Evidence pack refs.
- Target language and journal/style constraints.

## Tool Chain

```text
literature.evidence_pack_build
-> literature.outline_generate
-> literature.academic_writing_lint
-> literature.citations_sources
-> literature.export_docx
```

## Steps

1. Build or refresh the evidence pack before drafting.
2. Generate an outline that maps claims to evidence refs.
3. Draft each section with explicit claim scope and citation intent.
4. Run academic writing lint for unsupported claims, weak transitions, citation issues, and vague phrasing.
5. Check citation sources and overlap where needed.
6. Export DOCX only after evidence and lint checks pass or known exceptions are recorded.

## Output

- Evidence-backed outline.
- Draft sections.
- Lint findings and fixes.
- Citation/source check notes.
- Exported DOCX.

## Acceptance Check

No major claim should appear in the exported document without a source ref or a recorded reason why it is background/common knowledge.
