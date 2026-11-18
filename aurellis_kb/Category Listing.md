---
title: "Category Listing"
parent: "Application"
summary: "Browse and discover jewelry and watch products through category and collection listings."
tags: ["catalog", "category", "jewelry", "sorting", "categories", "products", "listing", "collections"]
related:
  - file: "Product Detail"
    type: related_to
  - file: "Product Search"
    type: related_to
sources: ["exploration"]
version: 46
confidence: high
has_open_conflicts: false
updated_at: "2026-11-18T09:23:45.175Z"
---

## Sub-features
- Product listing
- Product sorting

## Business Rules
- On /categories/rings, the category listing screen has a dropdown labeled “Featured” for product sorting; its available options were not opened during this observation.
- On /categories/rings, selecting checkbox "950 platinum (1)" applies the query parameter `metal=950+platinum`; the checkbox option displays a count of 1.
- On /categories/rings, selecting the checkbox "Blackened 18k yellow gold (1)" changes the URL to /categories/rings?metal=Blackened+18k+yellow+gold. The option displays “(1)”; a separate resulting product total was not exposed by the probe.
- On /categories/rings, selecting the checkbox option "diamond (3)" applies the gemstone=diamond query parameter; the option displays a count of 3.
- On /categories/rings, selecting the "black diamond (1)" checkbox changes the URL to /categories/rings?gemstone=black+diamond; selecting it again clears the gemstone filter and returns the URL to /categories/rings.
- On /categories/rings, selecting the "citrine (1)" checkbox filters the listing to 1 piece and sets the URL query to ?gemstone=citrine; with the checkbox unchecked, the listing shows 4 pieces.
- On /categories/rings, selecting the Gemstone checkbox "black diamond (1)" leaves 1 piece in the listing: Noir Signet Ring (from $3,200).
- On /categories/rings, choosing “Newest” in the “Featured” sort dropdown changes the URL to /categories/rings?sort=newest; choosing “Price · Low to High” changes it to /categories/rings?sort=price_asc; choosing “Price · High to Low” changes it to /categories/rings?sort=price_desc. Choosing “Featured” leaves the URL at /categories/rings.
- On `/categories/rings?metal=950+platinum`, selecting the `diamond (1)` checkbox applies the `gemstone=diamond` query parameter while retaining `metal=950+platinum`; the label reports a count of 1. The selection made no API call after the checkbox step. Page load made two `GET /api/cart` requests (200, 0 items at `$.items`), which were not matched to the filtered listing.
- On /categories/rings?metal=18k+yellow+gold, selecting the "diamond (2)" checkbox adds gemstone=diamond to the URL query; selecting the same checkbox while gemstone=diamond is present removes that query parameter.
- With metal=18k+yellow+gold, both the unchecked and checked states of the "diamond (2)" checkbox display 2 pieces; the displayed results are Aurora Eternity Ring and Solstice Citrine Cocktail Ring.
- On /categories/rings, the “Price · Low to High” sorting combobox exposes the options “Featured”, “Newest”, “Price · Low to High”, and “Price · High to Low”. From the starting URL /categories/rings?sort=price_asc, choosing “Newest” resulted in /categories/rings?sort=newest and choosing “Price · High to Low” resulted in /categories/rings?sort=price_desc; choosing “Featured” and “Price · Low to High” left the URL at /categories/rings?sort=price_asc.
- On the Rings category listing, the sort control offers Featured, Newest, Price · Low to High, and Price · High to Low; choosing them sets the URL to /categories/rings, ?sort=newest, ?sort=price_asc, and ?sort=price_desc respectively. Each option left 4 pieces visible.
- On the Rings category listing, changing the sort option made no API request; loading the listing made two GET /api/cart requests, each returning 200 with 0 items at $.items. No category-products API response was observed.
- On the Rings category listing, the sort control offers Featured, Newest, Price · Low to High, and Price · High to Low; selecting each option leaves 4 pieces in the results.
- On /categories/rings, the sort combobox offers Featured, Newest, Price · Low to High, and Price · High to Low. Selecting Price · Low to High sets the address query to ?sort=price_asc; selecting Price · High to Low sets it to ?sort=price_desc.
- On `/categories/necklaces`, selecting the checkbox `Blackened 18k white gold (1)` adds the query parameter `metal=Blackened+18k+white+gold` to the URL.
- On /categories/necklaces, clicking the "aquamarine (1)" checkbox changes the URL to /categories/necklaces?gemstone=aquamarine; the inspection recorded no API calls after the click.
- On /categories/necklaces, selecting the "Blackened 18k white gold (1)" checkbox adds `metal=Blackened+18k+white+gold` to the URL; unselecting it removes the `metal` parameter.
- The /categories/bracelets screen displays the bracelets category listing with a "Featured" dropdown; the dropdown is closed on initial load and must be opened to inspect its options.
- On /categories/watches, selecting the Metal checkbox "DLC-coated stainless steel (1)" sets the URL parameter `metal=DLC-coated stainless steel` and leaves 1 piece in the result list.
- On /categories/watches, checking "Stainless steel (1)" adds the query parameter metal=Stainless+steel to the URL; unchecking it removes that parameter.
- On /categories/watches, toggling the "Stainless steel (1)" checkbox made no API calls after the page opened. Initial page load made two GET /api/cart calls, both 200 with 0 items.
- On /categories/earrings, selecting the "18k white gold (1)" checkbox changes the URL to include `metal=18k+white+gold` and filters the category from 5 pieces to 1 piece; clearing the checkbox returns the listing to 5 pieces. The checkbox interaction made no API calls after the click (page-load GET /api/cart calls are separate).
- On /categories/watches, when the "Stainless steel (1)" checkbox is selected, the result count is 1 piece (Horizon 36 — Stainless Steel); when it is unselected, the result count is 3 pieces.
- Selecting the Rings filter "18k yellow gold" sets the page URL query to metal=18k+yellow+gold, shows 2 pieces, and displays Aurora Eternity Ring (From $4,800) and Solstice Citrine Cocktail Ring (From $7,600); the visible Price (USD) range becomes $4,800 — $7,600, and the Gemstone choices update to diamond (2) and citrine (1).
- Selecting the Aurora Eternity Ring card from the filtered Rings listing navigates to /products/aurora-eternity-ring, whose page title is "Aurellis — Fine Jewelry".

## Entities
- The Earrings category is presented on the category listing screen at /categories/earrings.
- The Rings category listing shows the heading "Rings" and the description "Statement and everyday rings — engagement, eternity, signets, cocktail."; the unfiltered listing shows "4 pieces" and cards for Ophelia Solitaire Ring (From $12,800), Aurora Eternity Ring (From $4,800), Solstice Citrine Cocktail Ring (From $7,600), and Noir Signet Ring (From $3,200).
- On the Rings listing, the Refine area has Metal filters 18k yellow gold (2), 950 platinum (1), and Blackened 18k yellow gold (1); Gemstone filters diamond (3), black diamond (1), and citrine (1); and Price (USD) with displayed range $3,200 — $12,800 and Min price USD and Max price USD inputs.
- The Rings listing displays a sort control with "Featured" selected; the available sort options were not observed.

## Terminology
- Featured

## Unexplored / Unknown
- button "Clear all" on /categories/rings - the turn failed: ProviderShared.stream: Failed to read openai/openai-responses stream
- checkbox "Blackened 18k white gold (1)" on /categories/necklaces - no evidence of result-counts after 2 attempts
- Unknown: The resulting product-list total when the "black diamond (1)" checkbox is selected or cleared is not stated in the recorded probe output; the label itself displays a facet count of 1.
- Unknown: The result count after selecting each sort option was not exposed by the inspection output and remains unverified: Featured, Newest, Price · Low to High, and Price · High to Low.
- Unknown: The options and behavior of the shut “Featured” dropdown on /categories/earrings were not explored in this task.
- Unknown: The watches category listing is not represented by the existing Category Listing screen coverage, so its product contents and category-specific behavior are not established by this task's snapshot.
- Unknown: The result counts for the watches category with "Stainless steel (1)" unchecked and checked were not exposed in the recorded probes.
- Unknown: The user-visible product content, controls, and listing behavior on /collections/cassiopeia are not established by the available observation details.

## Changelog
- v46 (2026-11-18): Regenerated from typed knowledge items (31 observed, 6 unknown). [sources: exploration]
- v45 (2026-11-18): Regenerated from typed knowledge items (31 observed, 6 unknown). [sources: exploration]
- v44 (2026-11-18): Regenerated from typed knowledge items (26 observed, 6 unknown). [sources: exploration]
- v43 (2026-11-18): Regenerated from typed knowledge items (26 observed, 6 unknown). [sources: exploration]
- v42 (2026-11-18): Regenerated from typed knowledge items (26 observed, 6 unknown). [sources: exploration]
- v41 (2026-11-18): Regenerated from typed knowledge items (26 observed, 5 unknown). [sources: exploration]
- v40 (2026-11-18): Regenerated from typed knowledge items (26 observed, 5 unknown). [sources: exploration]
- v39 (2026-11-18): Regenerated from typed knowledge items (25 observed, 5 unknown). [sources: exploration]
- v38 (2026-11-18): Regenerated from typed knowledge items (25 observed, 5 unknown). [sources: exploration]
- v37 (2026-11-18): Regenerated from typed knowledge items (24 observed, 5 unknown). [sources: exploration]
- v36 (2026-11-18): Regenerated from typed knowledge items (24 observed, 5 unknown). [sources: exploration]
- v35 (2026-11-18): Regenerated from typed knowledge items (24 observed, 5 unknown). [sources: exploration]
- v34 (2026-11-18): Regenerated from typed knowledge items (22 observed, 4 unknown). [sources: exploration]
- v33 (2026-11-18): Regenerated from typed knowledge items (21 observed, 4 unknown). [sources: exploration]
- v32 (2026-11-18): Regenerated from typed knowledge items (21 observed, 3 unknown). [sources: exploration]
- v31 (2026-11-18): Regenerated from typed knowledge items (20 observed, 2 unknown). [sources: exploration]
- v30 (2026-11-18): Regenerated from typed knowledge items (20 observed, 2 unknown). [sources: exploration]
- v29 (2026-11-18): Regenerated from typed knowledge items (19 observed, 2 unknown). [sources: exploration]
- v28 (2026-11-18): Regenerated from typed knowledge items (19 observed, 2 unknown). [sources: exploration]
- v27 (2026-11-18): Regenerated from typed knowledge items (18 observed, 2 unknown). [sources: exploration]
- v26 (2026-11-18): Regenerated from typed knowledge items (17 observed, 2 unknown). [sources: exploration]
- v25 (2026-11-18): Regenerated from typed knowledge items (16 observed, 2 unknown). [sources: exploration]
- v24 (2026-11-18): Regenerated from typed knowledge items (16 observed, 2 unknown). [sources: exploration]
- v23 (2026-11-18): Regenerated from typed knowledge items (16 observed, 2 unknown). [sources: exploration]
- v22 (2026-11-18): Regenerated from typed knowledge items (16 observed, 2 unknown). [sources: exploration]
- v21 (2026-11-18): Regenerated from typed knowledge items (16 observed, 2 unknown). [sources: exploration]
- v20 (2026-11-18): Regenerated from typed knowledge items (15 observed, 1 unknown). [sources: exploration]
- v19 (2026-11-18): Regenerated from typed knowledge items (15 observed, 1 unknown). [sources: exploration]
- v18 (2026-11-18): Regenerated from typed knowledge items (14 observed, 1 unknown). [sources: exploration]
- v17 (2026-11-18): Regenerated from typed knowledge items (12 observed, 1 unknown). [sources: exploration]
- v16 (2026-11-18): Regenerated from typed knowledge items (11 observed, 1 unknown). [sources: exploration]
- v15 (2026-11-18): Regenerated from typed knowledge items (9 observed, 1 unknown). [sources: exploration]
- v14 (2026-11-18): Regenerated from typed knowledge items (9 observed, 1 unknown). [sources: exploration]
- v13 (2026-11-18): Regenerated from typed knowledge items (8 observed, 1 unknown). [sources: exploration]
- v12 (2026-11-18): Regenerated from typed knowledge items (8 observed, 1 unknown). [sources: exploration]
- v11 (2026-11-18): Regenerated from typed knowledge items (8 observed, 1 unknown). [sources: exploration]
- v10 (2026-11-18): Regenerated from typed knowledge items (7 observed, 1 unknown). [sources: exploration]
- v9 (2026-11-18): Regenerated from typed knowledge items (6 observed, 1 unknown). [sources: exploration]
- v8 (2026-11-18): Regenerated from typed knowledge items (5 observed, 1 unknown). [sources: exploration]
- v7 (2026-11-18): Regenerated from typed knowledge items (5 observed, 1 unknown). [sources: exploration]
- v6 (2026-11-18): Regenerated from typed knowledge items (4 observed). [sources: exploration]
- v5 (2026-11-18): Regenerated from typed knowledge items (3 observed). [sources: exploration]
- v4 (2026-11-18): Regenerated from typed knowledge items (2 observed). [sources: exploration]
- v3 (2026-11-18): Regenerated from typed knowledge items (1 observed). [sources: exploration]
- v2 (2026-11-18): Regenerated from typed knowledge items (1 observed). [sources: exploration]
- v1 (2026-11-18): Regenerated from typed knowledge items (1 observed). [sources: exploration]
