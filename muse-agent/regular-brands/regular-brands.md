# Regular-brand list

A regular-brand entry is created only when the person explicitly says they buy a brand regularly or asks Muse to remember it. Store the normalized brand only alongside the original wording.

```yaml
brand_id: "<host-generated-id>"
brand: "<normalized brand>"
user_wording: "<original wording>"
product_categories: []
added_at: "<host timestamp>"
active: true
```

A regular brand is eligible for brand-level matching when an official notice clearly names that brand and the relevant product scope. Do not alert for a similar-sounding brand, distributor, retailer, or parent company without a documented product match. The user can remove a brand at any time; removed entries must not be used in future checks.
