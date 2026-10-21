# Newcomer guide

This guide is for James, Isaac, and their AI collaborators. It identifies
conventions to keep in mind and explains proposed improvements. The shared
[NEXT-STEPS.md](NEXT-STEPS.md) remains the canonical backlog; this guide does
not introduce a second task list.

## Before changing anything

- Read the shared decisions and the applicable project's AGENTS.md, README,
  and handoff. The shared parent and the two child projects are separate Git
  repositories. Work on a child repository in its own project context.
- Use GitHub for documentation, reference CSVs, scripts, and change history.
  Use the live Sheets for collaborative catalog work and Drive for operational
  PDFs. Local catalog CSVs are snapshots, not automatic instructions to
  overwrite a live Sheet. Reconcile conflicting deliberate revisions.
- Consult shared `reference/` defaults and the applicable child's tables.
  A deliberate exact-name child override replaces a shared table in full;
  there is no automatic row merge. Composer identity is the exception: use
  the shared registry without child overrides.
- Follow `reference/SCORE-ORDER.csv` for instrument ordering and
  `reference/INSTRUMENTS.csv` for instrument tokens. Do not invent competing
  abbreviations. SRCE's ensemble normalization and substitution tables add
  project-specific rules; substitutions require musical judgment.
- Preserve SRCE's instrumentation-first organization and SRYSO's `CURRENT/`
  edition semantics. Do not force identical layouts on the two projects.
- Keep names, identities, and links distinct. A spelling variation does not
  necessarily mean a new composer or work, and matching surnames do not prove
  identity. Check the source before merging records.
- Treat existing conventions as guidance that may not yet be enforced by
  software. Report discrepancies before mass edits; do not assume a familiar
  filename means that a table is populated.

## Shared composer registry

The shared `reference/COMPOSERS.csv` and `reference/COMPOSER-ALIASES.csv` now
contain 37 reviewed identities and their aliases. See
[Reference guide](../reference/README.md) for the maintained schema and usage
rules. SRYSO's older `reference/COMPOSER-NORMALIZATION.csv` and
`WORK-NORMALIZATION.csv` remain empty; they are not alternate authorities.

Maintain the two shared tables in the parent `reference/` directory:

The canonical composer registry lives at
`SRAM-Repertoire-Projects/reference/COMPOSERS.csv`, with its alias table beside
it. Both SRCE and SRYSO use that same authority for composer identity and
preferred names in their live repertoire spreadsheets and in their respective
`PDFs/` directory/file naming conventions. Do not create independent child
composer registries or use the general child-override mechanism to redefine
composer identity. Project-specific presentation needs should refer to the
same shared composer IDs.

The first reviewed corrections have been applied to the live Sheets and
matching local/Drive composer folders. Further migrations require reviewed
mappings. Storing the CSV alone does not enforce names or synchronize resources
automatically; historical local exports have not been refreshed.

| Shared table | Purpose | Columns |
|---|---|---|
| `COMPOSERS.csv` | One record per identified person | `COMPOSER-ID,DISPLAY-NAME,SORT-NAME,DIRECTORY-NAME,AUTHORITY-URL,NOTES` |
| `COMPOSER-ALIASES.csv` | Alternate spellings mapped to that person | `ALIAS,COMPOSER-ID,CONTEXT,STATUS,NOTES` |

Use a stable, spelling-independent ID so a corrected display name does not
change the person's identity. Keep a human-readable display name, a sort name,
and a preferred directory name separate. An authority URL records supporting
identity evidence where available; the shared table remains the project's
reference authority.

For example, future aliases such as `W-A-Mozart`, `WA-Mozart`, and
`W. A. Mozart` could be reviewed against the Wolfgang Amadeus Mozart record.
They are not automatically accepted merely because they look similar.
`Mozart` alone needs context: do not globally equate every occurrence with Wolfgang Amadeus Mozart when another
member of the family could be intended. Ambiguous aliases should remain
unresolved until reviewed. The Johann Sebastian Bach directory token is
`J-S-Bach`; `JS-Bach` and `J.S.-Bach` are accepted aliases. Other Bachs, such as
Johann Christian Bach, must receive separate identities. Isaac confirmed the
current SRYSO Musette attribution as Johann Sebastian Bach.

Begin with the actual composers in both catalogs. Collect existing spellings,
verify identities, and review proposed alias mappings before adoption. Extend
the registry toward 500–1,000 composers as needed; a large unverified list is
less useful than a smaller reliable one. Additions should be reviewed in Git.
Unknown names should be flagged for review rather than silently assigned to
the closest existing name or rejected because they are outside a fixed list.

When extending the tables, verify unique IDs, valid alias references, and
ambiguous mappings, then generate proposed catalog corrections for review.
Spreadsheet validation or scripts can consume those tables later;
they have not yet been implemented. Keep person identity shared across
projects rather than maintaining conflicting composer registries.

Existing filenames and Drive folder names may remain as historical aliases.
Do not mass-rename folders, move PDFs, replace links, or rewrite catalog values
as a side effect of extending the registry. Those are separate migrations with
their own reviewed mapping and verification.

## Other places where names can proliferate

- **Works:** separate identity from title spelling; retain catalog/opus numbers,
  movements, and composer identity. Similar titles do not establish one work.
- **Arrangements and editions:** retain arranger, version, and instrumentation
  distinctions rather than collapsing everything under the source work.
- **Instruments and ensembles:** reuse existing token, score-order, ensemble,
  and part-normalization tables. Preserve repeated instruments, part numbers,
  and solo/section distinctions.
- **Categories and workflow states:** SRCE and SRYSO category tables describe
  different things. SRYSO status, readiness, and work type are also separate
  dimensions; do not merge them merely to simplify labels.

Prioritize composer identities first, then extend the same explicit
identity-and-alias approach where current data shows a concrete problem.

## A useful first task for a new AI collaborator

Read the shared references and project guidance, then report inconsistent
composer spellings and ambiguous identities in the available catalog data.
Propose mappings with evidence and uncertainty. Make no catalog, PDF, folder,
or permission changes during that survey. Use the canonical roadmap for the
subsequent implementation work.
