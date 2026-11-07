# Recall-check acceptance tests

## New records only

**Given** a successful checkpoint at `2026-11-05T00:00:00Z` and a source record updated at `2026-11-06T00:00:00Z`.

**Expect** the record to be evaluated. Older records are not re-alerted unless materially updated.

## Source failure

**Given** FDA retrieval fails while USDA succeeds.

**Expect** the run to record the failure and not advance the all-source successful checkpoint or claim completion.

## No general dump

**Given** new recalls exist but none match the active purchase log or regular brands.

**Expect** no user-facing alert and no general recall digest.
