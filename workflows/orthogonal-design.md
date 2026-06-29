# Orthogonal Design Workflow

Goal: design and analyze Taguchi orthogonal experiments with explicit factor levels, response metrics, and objective direction.

## Inputs

- Factors and levels.
- Response metric.
- Objective: larger-is-better, smaller-is-better, or nominal-is-best.
- Constraints, minimum unique combinations, and output format.

## Process

```text
normalize request
-> choose compatible orthogonal array
-> generate factor-level plan
-> validate balance and duplicate runs
-> collect responses
-> compute S/N or response analysis
-> export tables
```

## Steps

1. Normalize factors, levels, constraints, responses, and objective direction.
2. Choose the smallest verified compatible array unless screening quality requires more runs.
3. Generate the plan table and validate orthogonality.
4. Record selected array, run count, factor count, column assignment, unique combinations, and duplicate count.
5. After responses exist, compute S/N ratios or mean/range analysis.
6. Export CSV or Excel-ready tables.

## Output

- Factor-level design table.
- Orthogonality validation.
- Response/SNR analysis.
- Recommended level combination and caveats.

## Acceptance Check

Do not force an invalid array. If no verified array fits, report the required factor-level profile and recommend a specialized OA generator.
