# Next Steps

This is the canonical cross-project roadmap for `~/SRAM-Repertoire-Projects`.
It records unfinished system-level work. Project-specific documents should link
here instead of maintaining competing copies of the same backlog.

## The central project

1. **Settled 2026-09-08:** retain the existing local hierarchy: a shared root
   with SRCE and SRYSO as separate child-project directories and Git
   repositories.
2. **Settled 2026-09-08:** files in the shared `reference/` directory are the
   defaults. A child project overrides a shared CSV by placing a file with the
   exact same filename in its own `reference/` directory. The child file fully
   replaces the shared file for that project; no automatic row-level merge is
   implied.
3. **Settled 2026-09-08:** the designated Google Drive hub represents the
   logical parent of the separate SRCE and SRYSO Drive roots. The projects need
   not share a literal containing folder. Canonical root mappings live in
   `reference/PROJECT-LOCATIONS.csv`.
4. Establish what is canonical locally, what is canonical in Google Drive, and
   how drift is reconciled.
5. Continue consolidating the Markdown documentation and human-facing SOPs.
6. **Settled provisionally 2026-09-09:** Git boundaries exclude operational PDF
   libraries and transient/generated material while retaining documentation,
   reference data, scripts, useful history, and appropriate normalized data.
   SRCE and SRYSO are backed up in private GitHub repositories; the shared SRAM
   repository is backed up separately.
7. Remove obvious sediment when its status is unambiguous. Defer structural
   migration or disputed material until canonicality is settled.

## Architectural premise

Directory hierarchy is not merely organization: it expresses and enforces
architecture. Google Drive can represent that architecture logically through
conventions, documentation, and shortcuts without having to reproduce every
local parent-child relationship literally.

## Order of work

1. Define canonicality and drift-reconciliation rules.
2. Update and consolidate documentation and SOPs around the settled hierarchy,
   override rule, and Drive mapping.
3. Define a backup practice for Drive-hosted assets that Git excludes.
4. Inventory deliberate canonical material, legitimate project-specific
   variation, unresolved drift, and obvious sediment.
5. Perform cleanup and migration in small, auditable stages.

## Workstreams to incorporate

### Shared architecture and data

- Develop a small normalized relational model for composers, works,
  instrumentation, parts, editions, PDF assets, source links, semesters,
  groups, and cross-project relationships.
- Audit the live repertoire spreadsheets for internal consistency, incomplete
  or duplicate entries, instrumentation and work-title accuracy, broken links,
  and agreement between the PDF and PDF-URL fields and their Drive assets.
- Continue evaluating
  `SRCE-Repertoire-Project/data/semesters/SRCE-2026-4-Fall/srce-groups.csv` as a
  practical bridge between the current meeting spreadsheet and a more
  normalized system.

### Documentation and SOPs

- Reconcile the parent, SRCE, and SRYSO documentation so each subject has one
  authoritative home.
- Keep SRCE's short README, handoff, and repository map current. Do not create
  speculative browser documentation while no browser workflow exists.
- Update older SRYSO documents where present practice has overtaken them.
- Document semester operations, group creation, repertoire shortcuts, session
  notes, spreadsheet maintenance, and local/Drive reconciliation.
- Decide which documentation should also be visible in Google Drive and how it
  should be represented there.

### Git and backup

- Keep the shared root, SRCE, and SRYSO as distinct Git repositories with
  clearly documented responsibilities.
- Periodically audit tracked, ignored, and untracked material for drift and
  sediment.
- Keep operational PDFs out of Git while preserving metadata, reference data,
  scripts, documentation, and appropriate normalized semester data.
- Establish separate backup coverage for Drive-hosted assets.

### Project-specific follow-through

- SRCE: treat the old generated-browser workflow as retired. Design any future
  web front end from scratch, and decide whether `EST-DURATION` belongs in the
  catalog.
- Audit the operational PDF libraries for practical printability. Begin with
  machine-readable checks for page size, orientation, mixed-size documents,
  and suspicious page geometry, then visually inspect exceptions and sampled
  files for cropping, miniature source pages, imposed two-page scans, page
  order, legibility, and reliable US Letter printing. Record findings before
  replacing or rewriting files.
- SRYSO: finish current spreadsheet/PDF maintenance and resume browser planning
  after the shared architecture is settled.
- SRYSO: perform a data-integrity audit of the informally named
  `SRYSO-HISTORICAL` section of the `The-Library...` spreadsheet against the
  corresponding repository files. *Finlandia* previously combined a Version-1
  Viola part with Version-2 parts for the other instruments; that discrepancy
  has been corrected. Audit the remaining historical work directories for
  similar mismatches by opening the PDFs and comparing the version label
  printed inside every score and part. Filenames and folder structure alone
  are not sufficient for this check.

### Eventual cleanup and migration

- Audit future same-named reference files in child projects to distinguish
  deliberate overrides from accidental copies.
- Normalize `data/SRYSO-Repertoire-Library.csv` into a conventional table or
  explicitly document its four-line descriptive preamble so generic CSV tools
  do not mistake the first comment row for the header.
