# Product definition

## Core promise

Muse AI Recall helps a person answer: “Has a newly announced official food recall affected something I bought or regularly buy?” The person supplies the memory context in ordinary language. Muse uses that context to perform narrow, personal matching.

## Required model

1. **Tell Muse what you bought.** Record the product, brand, purchase date, and any store, lot, or best-by information the person provides.
2. **Tell Muse what you are buying.** Use the upcoming item as a pre-shopping check; do not silently convert it into a confirmed purchase unless the person says they bought it.
3. **Record regular brands.** A brand can remain eligible for checking even when no new purchase was reported.
4. **Periodically check official notices.** Check new FDA openFDA Food Enforcement and USDA FSIS notices since the last successful check.
5. **Match narrowly.** Compare notices against the person’s purchase log and regular-brand list using the rules in `muse-agent/recall-check/match-rules.md`.
6. **Alert only on a match.** Include the official notice and concrete next steps. No match means no user-facing alert.

## Explicit non-goals

- No barcode or pantry scanner.
- No standalone generic recall page or general recall feed.
- No “add to Muse Alert” as a separate product concept.
- No inference that a user owns every product made by a company merely because the company appears in a notice; brand matching must follow the documented confidence rules.
- No medical diagnosis or safety guarantee.

## Web surface

The product is web-only. `site/recall/` is public and can be hosted at `/recall`. `site/recalled/` is the authenticated or embedded personal area at `/recalled`. The supplied HTML is static/embed-ready and does not implement a backend, identity provider, database, or real-time source fetch.

## Premium/pricing placeholder

The public page may describe free and premium tiers, but prices and entitlements must be supplied by the host product configuration. The static files do not hard-code a payment flow or claim that a user has premium access.
