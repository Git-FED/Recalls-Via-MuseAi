# Match rules

Use conservative matching in this order:

1. **Exact product and brand:** the notice’s product and brand identify the same item as a confirmed purchase.
2. **Specific identifiers:** a matching lot, UPC, best-by, use-by, or date range is strong evidence. A conflicting identifier should downgrade or block a match unless the notice explicitly covers the broader range.
3. **Brand plus clear scope:** a notice clearly naming a regular brand may match when its product category/scope aligns with the user’s regular-brand context.
4. **Text similarity is not enough:** similar names, retailers, distributors, parent companies, or generic categories alone do not establish a match.
5. **Unknowns:** do not treat missing user details as proof of a match. Mark a candidate uncertain and ask for a detail when a safe decision depends on it.

A positive result must retain the evidence fields and official notice URL. No match, uncertain match, or source failure must not become a positive alert. Never match against users who were not provided to the check.
