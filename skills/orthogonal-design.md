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
