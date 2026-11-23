# hark/

Session alignment data for Ghostdreamer Pro (fork main = Pro line; upstream NeoMarkiss/ghostdreamer).

- beta/docs/manifest.json: current state only. Read it at the start of every session.
- beta/docs/manifest.schema.json: shape rules for the manifest.
- beta/docs/sessions/: one file per session (YYYY-MM-DD.md), append-only.
- beta/docs/decisions/: one file per lasting decision.
- beta/docs/benchmarks/: measured min-spec results per release.

Session loop: read manifest -> work on session/<date> branch -> update statuses and add a session file -> draft PR into main -> owner's merge = alignment met.
