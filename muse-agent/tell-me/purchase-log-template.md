# Purchase log template

```yaml
purchase_id: "<host-generated-id>"
purchase_date: "YYYY-MM-DD or unknown"
product: "<user-provided product description>"
brand: "<user-provided brand or unknown>"
store: "<user-provided store or unknown>"
lot_or_best_by: "<user-provided lot/date code or unknown>"
source: "user_report"
confirmed_purchase: true
recorded_at: "<host timestamp>"
notes: "<only user-provided context>"
```

Do not add recall status to the purchase record itself; recall evaluations belong to a check result so they can be updated when official notices change.
