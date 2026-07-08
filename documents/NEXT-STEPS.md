# Next Steps

## Immediate repository cleanup

- Finish committing AGENTS.md files in the parent, SRCE, and SRYSO repositories.
- Add missing SRCE documentation:
  - `ARCHITECTURE.md`
  - `DIRECTORY-CONVENTIONS.md`
  - `REPOSITORY-CONVENTIONS.md`
  - `BROWSER-WORKFLOW.md`
- Push the parent, SRCE, and SRYSO repositories.

## Codex onboarding

- Keep the existing Codex context focused on SRYSO for now.
- Create or onboard a separate SRCE Codex context after SRCE documentation is complete.
- Introduce Codex to the parent `SRAM-Repertoire-Projects` repository as the shared context layer.

## Relational readiness

Ask Codex, when it has access to both SRCE and SRYSO context, to review the repositories without modifying files and propose a normalized relational schema.

The schema review should study:

- `data/*.csv`
- `reference/*.csv`
- `documents/*.md`
- `scripts/`

It should pay special attention to:

- composers
- works
- instrumentation
- part naming
- score order
- PDF assets
- candidate editions
- canonical editions
- source links
- project-specific fields

The review should return:

1. proposed tables;
2. primary keys;
3. relationships;
4. fields that should remain project-specific;
5. fields shared by both projects;
6. migration risks;
7. smallest useful prototype.

## SRYSO

- Finish spreadsheet population.
- Upload PDFs to Google Drive.
- Begin browser v0.5 planning.

## SRCE

- Put full project infrastructure under Git.
- Add documentation scaffold.
- Review browser-generation script.
- Consider adding `EST-DURATION`.
