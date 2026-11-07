# Tell-Muse acceptance tests

## Confirmed purchase

**Given** the user says, “I bought North Farm frozen berries on 2026-11-05 at Market A.”

**Expect** a confirmed purchase record with product, brand, date, and store. Lot/best-by remains unknown. The item is not added to regular brands automatically.

## Planned purchase

**Given** the user says, “I’m buying North Farm yogurt tomorrow.”

**Expect** a planned item or immediate pre-shopping check, but no confirmed purchase record until the user confirms the purchase.

## Clarification

**Given** the user says, “I bought frozen food.”

**Expect** Muse to preserve the statement and ask for brand/product detail needed for useful matching; it must not invent a brand.
