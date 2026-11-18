---
title: "Product Search"
parent: "Application"
summary: "Search products by keyword and refine the resulting product listing."
tags: ["search", "products"]
related:
  - file: "Category Listing"
    type: related_to
sources: ["exploration"]
version: 12
confidence: high
has_open_conflicts: false
updated_at: "2026-11-18T09:30:19.129Z"
---

## Sub-features
- Keyword search
- Search result filters

## Business Rules
- When a keyword search returns no matching products, the results screen displays “No pieces match that search.” and “Try a different keyword or broaden your filters.”
- Opening `/search` displays the heading “Find a piece” and the count “20 pieces”, a “Refine” area with a “Clear all” button, a sort combobox currently showing “Featured”, and a list of product links.
- Selecting the “Noir Chronograph 40” product link from the search results navigates to the product detail page at `/products/noir-chronograph-watch`.
- Selecting the "18k yellow gold (9)" checkbox changes the search URL to `/search?metal=18k+yellow+gold`.
- On /search, checking the "Blackened 18k white gold (2)" checkbox applies the metal=Blackened+18k+white+gold filter and shows 2 pieces: Noir Pavé Huggie Hoops and Noir Collar Necklace.
- Selecting checkbox "950 platinum (4)" from the search page adds `metal=950+platinum` to the URL; clicking it again removes the metal query parameter. Neither checkbox change makes an additional API call after the page loads.
- On `/search`, selecting the checkbox `18k yellow gold (9)` changes the search URL to `/search?metal=18k+yellow+gold`.
- Clicking the “950 platinum (4)” checkbox on /search sets the URL query parameter to `metal=950+platinum`; the inspection reported no API calls after the click.
- On /search, clicking the checkbox "diamond (7)" leaves the page at /search?gemstone=diamond.
- On `/search`, selecting the `diamond (7)` Gemstone checkbox applies the `gemstone=diamond` query filter and the search results show `7 pieces`.
- With the `diamond (7)` filter selected on `/search`, the result cards include Cassiopeia Diamond Studs (`From $4,800`), Celestine Tennis Bracelet (`From $19,800`), Stellar Diamond Pendant (`From $5,400`), Ophelia Solitaire Ring (`From $12,800`), Aurora Eternity Ring (`From $4,800`), Halo Drop Earrings (`From $16,200`), and Solstice Citrine Cocktail Ring (`From $7,600`).
- Selecting the Cassiopeia Diamond Studs result opens `/products/cassiopeia-stud-earrings`.
- After selecting `diamond (7)`, the Product Search page shows Metal filter options `950 platinum (4)`, `18k yellow gold (2)`, and `18k white gold (1)`; Gemstone options `diamond (7)`, `black diamond (4)`, `aquamarine (2)`, `pearl (2)`, `citrine (1)`, and `topaz (1)`; a `Price (USD)` range of `$4,800 — $19,800` with `Min price USD` and `Max price USD` inputs; and a `Featured` sort control.
- On /search, selecting the "diamond (7)" checkbox sets the URL filter to /search?gemstone=diamond and the results show "7 pieces".

## Terminology
- Search results

## Unexplored / Unknown
- checkbox "18k yellow gold (9)" on /search - no evidence of result-counts after 2 attempts
- checkbox "950 platinum (4)" on /search - no evidence of result-counts after 2 attempts
- checkbox "Blackened 18k yellow gold (2)" on /search - missing: options-tried, result-counts
- checkbox "black diamond (4)" on /search - not explored yet
- checkbox "aquamarine (2)" on /search - not explored yet
- checkbox "pearl (2)" on /search - not explored yet
- checkbox "diamond (4)" on /search - not explored yet
- checkbox "black diamond (2)" on /search - not explored yet
- the step after draft model:control:/search#be4dd8336453#checkbox:diamond (7):filter-search-results-by-diamond on /search - not explored yet
- Unknown: The visible result total after selecting "18k yellow gold (9)" and any API request that supplies those search results are not established: the probe recorded no API calls after the checkbox click, and did not expose a result count.
- Unknown: The number of search results remaining after selecting `18k yellow gold (9)` was not exposed by the available inspection output.
- Unknown: The remaining product-result count after selecting “950 platinum (4)” could not be established from the available inspection output.
- Unknown: The number of search results after selecting or clearing "diamond (7)" was not exposed in the inspection output.

## Changelog
- v12 (2026-11-18): Regenerated from typed knowledge items (14 observed, 4 unknown). [sources: exploration]
- v11 (2026-11-18): Regenerated from typed knowledge items (14 observed, 4 unknown). [sources: exploration]
- v10 (2026-11-18): Regenerated from typed knowledge items (13 observed, 4 unknown). [sources: exploration]
- v9 (2026-11-18): Regenerated from typed knowledge items (9 observed, 4 unknown). [sources: exploration]
- v8 (2026-11-18): Regenerated from typed knowledge items (9 observed, 4 unknown). [sources: exploration]
- v7 (2026-11-18): Regenerated from typed knowledge items (8 observed, 3 unknown). [sources: exploration]
- v6 (2026-11-18): Regenerated from typed knowledge items (7 observed, 2 unknown). [sources: exploration]
- v5 (2026-11-18): Regenerated from typed knowledge items (6 observed, 1 unknown). [sources: exploration]
- v4 (2026-11-18): Regenerated from typed knowledge items (5 observed, 1 unknown). [sources: exploration]
- v3 (2026-11-18): Regenerated from typed knowledge items (4 observed, 1 unknown). [sources: exploration]
- v2 (2026-11-18): Regenerated from typed knowledge items (3 observed). [sources: exploration]
- v1 (2026-11-18): Regenerated from typed knowledge items (1 observed). [sources: exploration]
