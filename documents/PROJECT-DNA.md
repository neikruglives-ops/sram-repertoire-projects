# Project DNA

## Core principles

- Repository knowledge belongs in CSV tables and documentation, not hard-coded scripts.
- Scripts should be deterministic, idempotent, and boring.
- The spreadsheet is the catalog.
- Google Drive stores operational PDFs.
- Git stores architecture, metadata, scripts, and history.
- Each project distinguishes canonical materials from historical, alternate, or candidate materials.
- In SRYSO, `CURRENT/` represents the canonical active edition.
- `Versions/` and `Arrangements/` are used where appropriate to preserve historical revisions and alternate realizations.
- In SRCE, instrumentation is a first-class organizing level.
- Normalize vocabulary before automating.
- Survey first, migrate last.

## Future relational model: cross-references

Some current spreadsheet fields are really early signs of future relationship tables.

`SRCE-HANDLING` is one example. In the current SRYSO spreadsheet, it is a lightweight free-text field used to flag possible SRCE relevance without interrupting SRYSO cataloging work.

In a future relational model, this would likely become a cross-reference table rather than a single spreadsheet field.

Possible structure:

```text
project_cross_references
    source_project
    source_work_id
    target_project
    target_work_id
    handling_status
    notes
```

The repertoire system may eventually need three kinds of relationship tables:

1. **SRCE-internal relationships**

   Relationships entirely inside the SRCE repertoire project.

   Examples:
   - alternate instrumentations
   - related arrangements
   - source/candidate/canonical edition relationships
   - metadata-only records linked to physical PDF locations

2. **SRYSO-internal relationships**

   Relationships entirely inside the SRYSO repertoire project.

   Examples:
   - source score → arrangement
   - candidate edition → canonical edition
   - historical version → current edition
   - movement/work relationships
   - programming-season relationships

3. **Cross-project relationships**

   Relationships linking SRCE and SRYSO records.

   This is expected to be a smaller table.

   Examples:
   - an SRYSO score that may also work for SRCE
   - an SRCE chamber arrangement derived from SRYSO materials
   - a work already represented in both projects
   - a record that should be referenced but not duplicated
