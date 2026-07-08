# Decisions

## PDFs are not committed to Git

PDFs live in Google Drive. Git tracks metadata, scripts, reference tables, and documentation.

## Repository knowledge belongs in CSV files

Normalization rules should live in `reference/*.csv`, not in Python or Perl scripts.

## SRCE uses instrumentation as a first-class directory level

Because chamber repertoire is defined by performing forces.

## SRYSO uses CURRENT/ as the canonical edition

Because orchestra repertoire tends to have one active performing set.

## Harp abbreviation

SRCE uses `HP` for harp in `reference/SCORE-ORDER.csv`.
