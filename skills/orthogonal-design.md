# Skill Card: 正交实验设计 (`orthogonal-design`)

Purpose: design and analyze Taguchi orthogonal experiments.

Best for:

- L4/L8/L9/L12/L16/L18/L25/L27/L32/L36/L50/L54/L64/L81 style plans.
- Factor-level tables.
- Signal-to-noise ratio and response analysis.
- Excel/CSV experiment plans.

Core flow:

```text
factors/levels -> compatible array -> plan table -> orthogonality validation -> response analysis
```

Quality rules:

- Validate factor levels and objective direction.
- Do not force an invalid array.
- Record selected array, run count, unique combinations, duplicate count, and validation status.

## Dependencies

- Python 3.11+ for table generation and analysis.
- CSV or Excel-compatible output for experiment handoff.
- Verified Taguchi orthogonal array definitions.
- Optional response data for S/N ratio or response analysis.

## Inputs

- Factor names and levels.
- Objective direction: larger-is-better, smaller-is-better, or nominal-is-best.
- Optional constraints, minimum unique combination count, and response measurements.

## Outputs

- Factor-level experiment plan.
- Orthogonality validation summary.
- S/N ratio or response analysis when measurements are provided.
- Recommended factor-level combination and caveats.

## Boundary

The skill helps design and analyze experiments; it does not replace domain judgment, safety review, equipment constraints, or statistical consultation for high-stakes experiments.
