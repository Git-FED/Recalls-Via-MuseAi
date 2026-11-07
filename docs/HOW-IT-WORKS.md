# How it works

## 1. Tell Muse

Use natural language such as: “I bought Brand X frozen berries yesterday at Market Y. Best by 2026-08-01.” Muse should ask a short clarification question only when a missing detail materially affects matching. It should preserve what the person actually said and distinguish confirmed purchases from planned purchases.

## 2. Muse records

A purchase record stores the date, product description, brand, store when given, and lot or best-by information when given. The record is a user-provided memory, not proof of ownership or current possession. The regular-brand list stores brands the person says they buy regularly.

## 3. Muse checks

On the configured cadence, Muse retrieves new official FDA openFDA Food Enforcement and USDA FSIS notices. It uses the last successful check timestamp and evaluates only notices published or updated after that timestamp. The check should record its own timestamp and source status.

## 4. Muse matches

Muse first looks for an exact or highly specific product and brand match. If a notice identifies a lot, date code, UPC, or best-by range, those details strengthen or weaken the match. A brand-only notice may match a regular brand when the notice clearly covers that brand and product category, but uncertain or merely similar names must not be treated as a positive match.

## 5. Muse alerts

A match creates a concise alert with the affected item, brand, reason, recall class if stated, what the person should do, and a direct official notice link. The official notice controls. When there are no matches, Muse does not send a general digest.
