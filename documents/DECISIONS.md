# Decisions

This file records settled cross-project rules. Unresolved matters belong in
`OPEN-QUESTIONS.md`; implementation work belongs in `NEXT-STEPS.md`.

## Repository roles

- `~/SRAM-Repertoire-Projects` is the shared documentation, reference, and
  cross-project planning layer.
- `SRCE-Repertoire-Project/` and `SRYSO-Repertoire-Project/` are functionally
  distinct projects and separate Git repositories.
- The existing local hierarchy is sufficient. No directory migration is
  required merely to make the projects more symmetrical.
- The unrelated teaching-pedagogy project remains separate and is not part of
  this unification effort.

## Git and Google Drive

- Git tracks architecture, metadata, normalized data where appropriate,
  reference tables, scripts, documentation, and history.
- Operational PDFs live in Google Drive and are not committed to Git.
- SRCE and SRYSO are backed up as separate private GitHub repositories. Their
  backup boundaries intentionally include useful context and history; a file's
  presence in Git does not by itself make that file canonical.
- The Drive folder with ID `1H-3FfjZNclOw2k8qa9XDtWmpKfet93AI` is the
  designated logical hub for the two projects. It currently contains Drive
  shortcuts to the independently located SRCE and SRYSO project roots; it does
  not need to physically contain either root.
- Drive conventions and shortcuts may express the logical hierarchy. Literal
  shared-parent containment is not required.
- Unclassified, historical, or otherwise unresolved Drive material may be
  consulted as context, but it is not canonical and must not be deleted until
  it has been reconciled against the live project spreadsheet and documented
  conventions.
- Canonical local-to-Drive root mappings live in
  `../reference/PROJECT-LOCATIONS.csv`.

## Shared and project-specific reference data

- Files under the top-level `reference/` directory are the default shared
  reference data for SRCE and SRYSO.
- A child project overrides a shared CSV by placing a CSV with the exact same
  filename in the child project's `reference/` directory.
- An exact-name child override replaces the shared file in full for that
  project. The system does not automatically merge the two files row by row.
- An accidental or obsolete same-named copy is not a deliberate override and
  should be handled as drift or sediment during a later audit.
- Normalization rules belong in CSV reference tables and documentation, not
  hard-coded in scripts.

## Project distinctions

- SRCE treats instrumentation as a first-class directory and catalog field.
- SRCE has no active generated-browser workflow. Its obsolete browser generator
  and generated output were retired; any future web front end should be
  designed from current requirements rather than reviving that implementation.
- SRYSO uses `CURRENT/` for the canonical active edition; `Versions/` and
  `Arrangements/` preserve other relationships where appropriate.
- The projects may share conventions and data without being forced into
  identical directory structures.

## Canonicality and migration

- The newest deliberate revision generally wins; a newer accidental copy or
  sediment does not become canonical merely because of its timestamp.
- Survey first and migrate last.
- Remove or relocate material only after its role and destination are
  unambiguous.
- Preserve project-specific fields when they express a real difference rather
  than mere naming drift.
