# Sources

## FDA

Use the official FDA openFDA Food Enforcement API/data for food enforcement reports and recall-related records:

- https://open.fda.gov/apis/food/enforcement/
- https://www.fda.gov/safety/recalls-market-withdrawals-safety-alerts

The integration should retain the source record identifier, publication or report date, last update when available, product and brand fields, reason, classification, and source URL. Treat source updates as updates to the same notice rather than automatically creating duplicate alerts.

## USDA FSIS

Use official USDA Food Safety and Inspection Service recall and public health alert notices:

- https://www.fsis.usda.gov/recalls
- https://www.fsis.usda.gov/food-safety/safety-and-health/recalls-and-public-health-alerts

Retain the notice title, release date, establishment or brand information, product details, reason, health-risk language, recall class or equivalent when provided, and the official notice URL.

## Cadence and provenance

The host configures the periodic cadence. Each run records `last_checked_at`, source success or failure, and the newest source item considered. A failed source must not advance the successful checkpoint. The alert should link to the official notice, not only to a cached summary.

The product notes cite project-provided 2025 recall context, including the stated FDA and USDA counts and impact figures. Those contextual figures are not used as matching logic; production copy should re-verify them against current official reporting before publication.
