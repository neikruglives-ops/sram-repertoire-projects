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
  `reference/` directory; there is no automatic row-level merge. Composer
  identity is shared without child overrides: see the
  [composer registry and alias rules](reference/README.md).

Canonical mappings between local roots and Google Drive roots live in
`reference/PROJECT-LOCATIONS.csv`.

## Google Drive realization

- [SRAM logical hub](https://drive.google.com/drive/folders/1H-3FfjZNclOw2k8qa9XDtWmpKfet93AI?usp=drive_link)
- [SRCE Repertoire Library](https://drive.google.com/drive/folders/1U6MCU8AEuq918N9xrRDtgYcSSp08-9B7?usp=drive_link)
- [SRYSO Repertoire Library](https://drive.google.com/drive/folders/1oovVwCzW3XUhpxWe35O6VHkTBlk92KoD?usp=drive_link)

The hub is the logical parent of the two project libraries and currently
contains Google Drive shortcuts to them. The project libraries remain in their
independent physical locations; literal shared-parent containment is not
required. Treat unclassified or historical Drive material according to the
interim canonicality rule in `documents/DECISIONS.md`.

## Cold-start reading order

1. `AGENTS.md`
2. `documents/DECISIONS.md`
3. `documents/NEXT-STEPS.md`
4. `reference/PROJECT-LOCATIONS.csv`
5. The applicable child project's `AGENTS.md`, `README.md`, and
   `documents/CODEX-HANDOFF.md`

Unresolved architectural questions live in `documents/OPEN-QUESTIONS.md`.

New collaborators should also read [Newcomer guide](documents/NEWCOMER-GUIDE.md)
for conventions to keep in mind and the proposed shared composer registry.
