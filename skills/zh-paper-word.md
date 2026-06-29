# Skill Card: 中文论文 Word 转写 (`zh-paper-word`)

Purpose: convert foreign academic papers into Chinese journal-style Word documents while preserving academic structure.

Best for:

- English paper to Chinese DOCX translation.
- Double-column PDF layout extraction.
- Figure, table, equation, caption, citation, and reference preservation.

Core flow:

```text
prepare workspace -> extract layout/assets -> translate structured JSON -> build LaTeX -> export DOCX -> inspect DOCX
```

Quality rules:

- Do not hardcode provider credentials.
- Translate through a structured intermediate contract.
- Inspect the final DOCX for missing figures, tables, equations, captions, and references.
