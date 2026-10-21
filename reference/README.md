# Shared reference tables

These tables are maintained in the shared SRAM repository and apply to SRCE
and SRYSO. GitHub is their shared distribution point; do not maintain an
independently editable composer registry in Drive or in a child project.

## Composer identity

`COMPOSERS.csv` is the common composer authority for both projects' catalog
composer fields and `PDFs/` composer directory names. The initial registry
contains 37 reviewed identities from the naming audit approved by Isaac on
2026-10-20. It is a seed, not a complete catalog of every composer in either
project. Names not yet registered need review and an addition, not an arbitrary
substitution to an existing person.

| Field | Meaning |
|---|---|
| COMPOSER-ID | Permanent identity key; never change or reuse it when a spelling changes. |
| DISPLAY-NAME | Preferred human-readable catalog label, including accents where adopted. |
| SORT-NAME | Explicit sorting label; do not try to derive surname particles automatically. |
| DIRECTORY-NAME | Preferred composer directory token; separators between names are hyphens. Existing consistent surname-only tokens can remain. |
| AUTHORITY-URL | Supporting source URL from the reviewed catalog, when available; not a claim that every external source was independently verified. |
| NOTES | Coverage and identity notes. |

`COMPOSER-ALIASES.csv` links alternate spellings and former directory tokens to
the same COMPOSER-ID. For example, both `Rachmaninoff` and `Rachmaninov` resolve
to `CMP-0004`; `Rachmaninoff` is the preferred display/directory token.

Alias matching is exact Unicode text unless a tool explicitly implements and
documents a reviewed normalization step. `STATUS=ACCEPTED` applies within the
shared repertoire context. `STATUS=CONTEXT-REQUIRED` means a work/source must
confirm the person before resolving a bare surname such as Bach, Mozart, or
Williams. A fuzzy match is a review suggestion, never an automatic merge.
Johann Sebastian Bach uses directory token `J-S-Bach`, with `JS-Bach` and
`J.S.-Bach` as accepted aliases. Other Bachs require separate IDs.
Canonical IDs can be used directly by tools even while Sheets still display
names. These CSVs do not themselves install Sheet validation or run migrations.

Keep aliases in their own rows rather than embedding a delimiter-separated
list in COMPOSERS.csv. To add a verified person, assign the next unused ID,
choose display/sort/directory names, and add reviewed aliases. Preserve IDs
when sorting the table. Do not regenerate IDs from row position or spelling.

Composer identity is an exception to the general child reference override
rule: neither project should replace these tables with a conflicting local
composer authority. Project-specific arrangements or display needs refer to
the common identity. Arrangers, performers, multiple-person credits, and
traditional/collective attribution require distinct roles; do not manufacture
a single composer person for a compound credit.

The initial live naming corrections were applied to composer cells only.
Historical local catalog exports were not refreshed, and still require
reconciliation before use as current data. Existing scripts may not yet consume
these tables. Do not treat an old export as an instruction to undo the reviewed
live corrections.

## Other shared rules

- `INSTRUMENTS.csv` defines instrument tokens, families, and player counts.
- `SCORE-ORDER.csv` defines this project's instrument ordering.
- `STYLE-FAMILIES.csv` and `ENTRY-TYPES.csv` define other shared vocabulary.
- `PROJECT-LOCATIONS.csv` records location mappings; its older topology labels
  still need reconciliation with current Drive state.

For these other vocabularies, a deliberate exact-name child CSV replaces the
shared file for that project; there is no row-level merge.
