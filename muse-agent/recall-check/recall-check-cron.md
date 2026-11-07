# Periodic recall check

Run on the host-configured cadence. A run should:

1. Load active confirmed purchases and active regular brands.
2. Read the last successful check timestamp.
3. Retrieve new or updated FDA openFDA Food Enforcement records and USDA FSIS notices after that timestamp.
4. Normalize source fields without changing the original notice.
5. Apply `match-rules.md` separately to each source record.
6. Send an alert only for a positive, non-duplicate match.
7. Save source IDs, evaluation time, outcomes, and a new successful checkpoint only if the required sources completed successfully.

If a source fails, record the failure and do not claim the check was complete. Avoid repeated alerts for the same source notice and same user context unless the official notice materially changes.
