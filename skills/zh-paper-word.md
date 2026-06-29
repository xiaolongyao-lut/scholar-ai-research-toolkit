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

## Dependencies

- Python 3.11+.
- PyMuPDF for PDF layout and asset extraction.
- Pandoc for DOCX export.
- python-docx and OOXML post-processing for Word layout details.
- Optional OCR engine for scanned pages.
- User-selected translation model or manual translation; no provider key belongs in this repository.

## Inputs

- Source PDF, LaTeX, or Pandoc-compatible manuscript.
- Clean working directory.
- Translation JSON following the skill contract.

## Outputs

- Extracted layout/assets.
- `zh_translated.json`.
- Intermediate `paper.tex`.
- Final Chinese DOCX and inspection report.

## Boundary

This card documents the public workflow only. Private papers, generated OCR assets, translated drafts, and provider credentials stay local.
