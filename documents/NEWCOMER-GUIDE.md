# James, Claude, and the repertoire project

James is already building here—start by looking at his current work, not by
assuming a fresh project. This system is young, and new ideas, refactoring,
and replacement of awkward parts are welcome. Isaac has put considerable
thought into the musical data conventions; carrying that care forward should
make your own tools easier to build and trust. Keep what helps, improve what
doesn't, and make the changes understandable to the next collaborator.

## A few things worth carrying forward

- **One composer identity, many spellings.** The shared parent
  [COMPOSERS.csv](../reference/COMPOSERS.csv) and
  [COMPOSER-ALIASES.csv](../reference/COMPOSER-ALIASES.csv) serve both SRCE and
  SRYSO. Stable IDs connect names without confusing people: Rachmaninoff and
  Rachmaninov are one identity; Johann Sebastian and Johann Christian Bach are
  different people. Display names and directory tokens are separate;
  multiply-named directory tokens use hyphens, such as `Anton-Arensky`,
  `Florence-Price`, and `J-S-Bach`. Extend this shared authority rather than
  creating competing project copies.
- **Consistent musical vocabulary.** Use the shared
  [INSTRUMENTS.csv](../reference/INSTRUMENTS.csv) and
  [SCORE-ORDER.csv](../reference/SCORE-ORDER.csv), plus each project's ensemble
  and part-normalization tables. Preserve distinctions such as one pianist
  versus piano four-hands, numbered parts, and solo versus section parts.
  These conventions save repeated guesswork; change them deliberately if a
  better model emerges.
- **Preserve meaning, not just spelling.** Composer, arranger, and performer
  are different roles. A work, its movements, arrangements, and editions are
  related but not interchangeable. Keep provenance, uncertainty, and stable
  asset links. SRCE's instrumentation-first layout and SRYSO's `CURRENT/`
  convention express useful musical distinctions, even if their eventual
  implementation changes.

On **2026-10-20**, we seeded 37 composer identities and 102 aliases, corrected
190 composer cells across the live spreadsheets, and renamed nine composer
folders locally and in Drive. Drive IDs were preserved. Isaac also confirmed
that the current SRYSO Musette is by Johann Sebastian Bach. The registry is
still incomplete, and historical local CSV exports were not refreshed—avoid
reintroducing old spellings through an import. The
[reference guide](../reference/README.md) explains the current rules; validation
and automatic enforcement are still work to build.

## Keep the implementation flexible

There isn't a finished database schema to defend. At hundreds or thousands of
entries, prefer JSON where it does the job clearly. If a database helps, a few
useful tables with JSON fields for variable details may be the right blend.
Use stable keys for real relationships; add structure and validation where
mistakes would hurt. CSV is today's shared reference format, not a permanent
requirement. A future database or JSON representation is welcome if it carries
forward identities, aliases, relationships, and one clear authority.

GitHub holds maintained rules, documentation, and scripts; Drive holds live
Sheets and PDFs. The shared parent, SRCE, and SRYSO are separate repositories;
read their applicable `AGENTS.md` instructions and coordinate with ongoing
work. Try changes in reviewable steps, check affected links and data, and
leave enough explanation for each other. The shared
[NEXT-STEPS.md](NEXT-STEPS.md) is the backlog. The aim is a more robust,
flexible, useful tool—not preservation of every early design choice.
