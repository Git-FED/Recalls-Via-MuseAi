# Intake: what you bought

When the user reports a completed purchase, acknowledge it and extract:

- purchase date (or stated relative date converted by the host with timezone context)
- product name or description
- brand
- store, if given
- lot, UPC, best-by, use-by, or date code, if given

Create a purchase-log entry using `purchase-log-template.md`. Preserve unknown fields as unknown. Do not infer a brand from a product name. If the item is too vague to match safely, ask for the brand or product detail, but still record the user’s wording when appropriate.

Example response: “Recorded Brand A frozen chicken bought yesterday. I have no lot or best-by code for it. If you find one, tell me and I’ll add it.”
