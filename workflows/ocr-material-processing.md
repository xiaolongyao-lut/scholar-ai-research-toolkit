# OCR Material Processing Workflow

Goal: handle scanned or mixed PDF materials without guessing the OCR path.

## Inputs

- Material id or source PDF.
- OCR policy preference if the default is not enough.
- User authorization for any expensive or remote OCR operation.

## Tool Chain

```text
literature.ocr_status
-> literature.ocr_engines
-> literature.ocr_health
-> literature.ocr_material
```

## Steps

1. Check OCR status to understand default policy and current runtime configuration.
2. List available engines and their readiness.
3. Run health checks for the selected engine before executing OCR.
4. Use local OCR first when privacy matters and quality is acceptable.
5. Execute OCR only after the engine, cost, privacy, and output location are clear.
6. Re-index or rescan materials after OCR output is produced.

## Output

- OCR policy and selected engine.
- Readiness blockers or configuration actions.
- OCR execution record.
- Updated searchable text or material chunks.

## Acceptance Check

Do not claim OCR capability from configuration alone. There must be either a health result or an execution record for the chosen path.
