# Jupyter Research Notebook Workflow

Goal: create reproducible notebooks for experiments, data analysis, and research notes.

## Inputs

- Experiment question.
- Data sources and allowed paths.
- Expected outputs: figures, tables, metrics, or narrative notes.

## Steps

1. Create a clean notebook from a template.
2. Put assumptions, data provenance, and environment notes in the first markdown cells.
3. Keep data loading, cleaning, analysis, visualization, and conclusion in separate sections.
4. Save derived outputs under a predictable `outputs/` folder or project artifact folder.
5. Run the notebook from top to bottom before treating it as evidence.
6. Export only scrubbed results when sharing publicly.

## Output

- `.ipynb` notebook.
- Generated figures/tables.
- Short conclusion cell with limitations.
- Reproducibility notes.

## Acceptance Check

A notebook is handoff-ready only when it can run top-to-bottom and every input path or dataset source is documented.
