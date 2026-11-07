# Alert and matching acceptance tests

## Exact match

**Given** a purchase for Brand A Product X and an official notice naming Brand A Product X.

**Expect** one focused alert containing reason, class when supplied, action, and the official notice URL.

## Lot conflict

**Given** the user’s lot is `L100` and the notice covers only `L200`.

**Expect** no positive alert unless the official notice explicitly covers both lots or a broader range.

## Regular brand

**Given** Brand B is active in the regular-brand list and the notice clearly names Brand B for the relevant category.

**Expect** a possible or positive alert according to the evidence; do not require a newly reported purchase.

## Similar name

**Given** the user has Brand C and the notice names a similar but distinct Brand D.

**Expect** no match and no alert.
