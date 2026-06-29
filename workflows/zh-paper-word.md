# Foreign Paper To Chinese Word Workflow

Goal: convert a foreign academic paper into a Chinese journal-style DOCX while preserving structure, figures, tables, equations, citations, and references.

## Inputs

- Source PDF, LaTeX, or Pandoc-compatible manuscript.
- Clean working directory.
- Translation provider or manual translation process chosen by the user.

## Process

```text
prepare workspace
-> extract layout and assets
-> fill zh_translated.json
-> build reference DOCX
-> build LaTeX intermediate
-> export DOCX
-> post-process OOXML
-> inspect final DOCX
```

## Steps

1. Prepare a clean workdir and keep source files unchanged.
2. Extract reading order, sections, captions, references, equations, tables, and image crops.
3. Translate into a structured JSON contract instead of editing the final DOCX directly.
4. Build a reference DOCX for Chinese typography, margins, captions, tables, and references.
5. Export through Pandoc and post-process Word XML where ordinary APIs cannot express the layout.
6. Inspect final DOCX before delivery.

## Output

- `zh_translated.json`
- extracted assets
- intermediate `paper.tex`
- final `paper_zh.docx`
- inspection report

## Acceptance Check

The final Word document must not silently drop figures, tables, equations, captions, references, or low-confidence extraction warnings.
