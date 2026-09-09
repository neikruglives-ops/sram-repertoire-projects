# Open Questions

This file is a short register of unresolved architectural decisions. Once a
question is settled, move its answer to `DECISIONS.md` and remove it here. The
work required to reach those decisions belongs in `NEXT-STEPS.md`.

## Google Drive

- Which data, documentation, and SOP files should be mirrored or rendered in
  Drive, and which should remain Git-first?

## Canonicality and drift

- Which kinds of data are authoritative locally, and which are authoritative in
  Google Drive or Google Sheets?
- What review process should resolve conflicting deliberate revisions without
  allowing newer sediment to supplant canonical data?

## Backup beyond Git

- What backup practice should cover Drive-hosted PDFs and other operational
  assets that Git intentionally excludes?

## Project-specific choices

- Should SRCE adopt a `CURRENT/` convention, or would that conflict with its
  instrumentation-first model?
- Should SRCE add an `EST-DURATION` field?
