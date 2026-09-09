# SRAM Repertoire Projects

This is the shared architecture, reference-data, and planning layer for two
spreadsheet-centered repertoire systems:

- `SRCE-Repertoire-Project/` — chamber ensemble repertoire
- `SRYSO-Repertoire-Project/` — youth string orchestra repertoire

The child directories are functionally distinct projects and separate Git
repositories. The Studio repertoire project is intentionally outside this
shared system.

## Operating model

- The spreadsheet is each project's catalog and practical working interface.
- Google Drive stores operational PDFs and the live Google Sheets.
- Git stores documentation, reference data, scripts, normalized data where
  appropriate, and change history.
- Top-level `reference/*.csv` files are shared defaults. A child project may
  deliberately replace one for itself with an exact-name file in its own
  `reference/` directory; there is no automatic row-level merge.

Canonical mappings between local roots and Google Drive roots live in
`reference/PROJECT-LOCATIONS.csv`.

## Cold-start reading order

1. `AGENTS.md`
2. `documents/DECISIONS.md`
3. `documents/NEXT-STEPS.md`
4. `reference/PROJECT-LOCATIONS.csv`
5. The applicable child project's `AGENTS.md`, `README.md`, and
   `documents/CODEX-HANDOFF.md`

Unresolved architectural questions live in `documents/OPEN-QUESTIONS.md`.
