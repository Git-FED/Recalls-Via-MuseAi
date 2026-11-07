# Recall-check sources

Primary sources:

- FDA openFDA Food Enforcement: https://open.fda.gov/apis/food/enforcement/
- FDA recalls: https://www.fda.gov/safety/recalls-market-withdrawals-safety-alerts
- USDA FSIS recalls: https://www.fsis.usda.gov/recalls

The host sets the cadence. Each run records:

```yaml
last_checked_at: "<UTC timestamp>"
source_status:
  fda: "success | failed"
  usda_fsis: "success | failed"
new_records_considered: 0
run_id: "<host-generated-id>"
```

Only a fully successful run advances `last_checked_at`. Preserve the official source record ID and the exact notice URL used for every alert.
