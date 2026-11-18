---
title: "Product Detail"
parent: "Application"
summary: "Displays a specific product and its purchase information on an individual product page."
tags: ["product", "catalog"]
related:
  - file: "Home & Featured Collections"
    type: related_to
  - file: "Category Listing"
    type: related_to
sources: ["exploration"]
version: 44
confidence: high
has_open_conflicts: false
updated_at: "2026-11-18T09:28:30.810Z"
---

## Business Rules
- On /products/noir-chronograph-watch, clicking the button "View image 1" leaves the address and visible page text unchanged and triggers no API call.
- On `/products/noir-chronograph-watch`, clicking the “Details & Materials” button produced no API calls after the step.
- On `/products/cassiopeia-stud-earrings`, the site navigation links to BOOK AN APPOINTMENT (`/contact`), SHIPPING & RETURNS (`/policies/shipping`), NEW IN (`/new-in`), RINGS (`/categories/rings`), NECKLACES (`/categories/necklaces`), BRACELETS (`/categories/bracelets`), EARRINGS (`/categories/earrings`), WATCHES (`/categories/watches`), ATELIER NOIR (`/collections/atelier-noir`), Wishlist (`/auth/sign-in`), and Cart (`/cart`).
- The page at `/products/celestine-tennis-bracelet` has the document title “Aurellis — Fine Jewelry.”
- On `/products/celestine-tennis-bracelet`, clicking the `7in` button leaves the page address and visible text unchanged and makes no API calls.
- On /products/celestine-tennis-bracelet, clicking the button “7.5in” made no API calls during the observed interaction.
- On `/products/stellar-pendant-necklace`, clicking the `16in` button leaves the address and visible page text unchanged and makes no API call; the page still shows buttons `16in` and `18in`.
- On the Celestine Tennis Bracelet product detail page, clicking the “The Story” button expands a region titled “The Story” and shows the paragraph “The piece every collection owes itself.” The click makes no API calls.
- On /products/ophelia-solitaire-ring, the probe for clicking button "7" recorded no API calls after the step; the probe output does not establish the resulting visible state.
- On the /products/atelier-noir-cuff page, the site navigation exposes links for BOOK AN APPOINTMENT (/contact), SHIPPING & RETURNS (/policies/shipping), NEW IN (/new-in), RINGS (/categories/rings), NECKLACES (/categories/necklaces), BRACELETS (/categories/bracelets), EARRINGS (/categories/earrings), WATCHES (/categories/watches), ATELIER NOIR (/collections/atelier-noir), Wishlist (/auth/sign-in), and Cart (/cart).
- On `/products/atelier-noir-cuff`, clicking the `Small` button leaves the page address and displayed text unchanged and makes no API call after the click. Opening the page made two `GET /api/cart` requests, each returning 200 with 0 items at `$.items`.
- On `/products/solstice-hoop-earrings`, clicking the `25mm` button leaves the page address and displayed text unchanged and triggers no API call.
- On the Solstice Hoop Earrings product page, clicking the “30mm” button triggered no API calls.
- The Horizon Watch Gold product page is rendered with product data supplied by the page itself; the two observed `/api/cart` responses did not match data displayed on the page.

## Entities
- The product detail screen is available at `/products/stellar-pendant-necklace` and the inspected browser document title is `Aurellis — Fine Jewelry`.
- The Ophelia Solitaire Ring product detail page is available at `/products/ophelia-solitaire-ring`.
- The route `/products/aurora-eternity-ring` is an Aurellis product-detail page; its browser document title is “Aurellis — Fine Jewelry”.
- The product detail page is available at `/products/citrine-cocktail-ring` and has the document title “Aurellis — Fine Jewelry.”
- The product detail page is for the Noir Signet Ring.
- The product detail screen is available at `/products/noir-pave-hoops` for the product identified by the slug `noir-pave-hoops`.
- The product detail screen at `/products/topaz-station-necklace` presents the Topaz Station Necklace.
- The Maris Pearl Drops product-detail page is available at /products/maris-pearl-drops.
- The `/products/solstice-hoop-earrings` route is a product detail page for Solstice Hoop Earrings.
- The Horizon Watch Gold product page is available at `/products/horizon-watch-gold`.
- The Noir Pavé Huggie Hoops product detail identifies the item as Earrings, priced at $3,200, with SKU AUR-EAR-004 and In stock status. Its displayed description is “Compact 12mm huggie hoops set with black diamonds along the outer edge.” The Details & Materials section lists metal as Blackened 18k white gold, gemstones as black diamond, dimensions as 12mm, and total Carat as 0.6.

## Unexplored / Unknown
- button "Add to bag" on /products/noir-chronograph-watch - needs a sandbox or a person: it would change data in a protected environment
- button "Save to wishlist" on /products/noir-chronograph-watch - needs a sandbox or a person: it would change data in a protected environment
- button "Write a review" on /products/noir-chronograph-watch - needs a sandbox or a person: it would change data in a protected environment
- button "5" on /products/ophelia-solitaire-ring - no evidence of network after 2 attempts - last error: The page could not be inspected: UI click button "5": its target is disabled (waited 15 s)
- Unknown: The product detail page for /products/noir-chronograph-watch is present, but its product-specific content and behavior have not yet been captured beyond the page snapshot.
- Unknown: The content revealed by the “Details & Materials” button on `/products/noir-chronograph-watch` is not captured in the available probe result.
- Seen only in code, not checked in the running application: On /products/noir-chronograph-watch, clicking the "Shipping & Returns" button made no additional API calls.
- Unknown: The visible content shown after clicking the "Shipping & Returns" button is not established by the recorded probe output.
- Unknown: On /products/celestine-tennis-bracelet, the “View image 2” button is present, but the recorded click produced no visible page change and no API call; whether it changes the product image is unconfirmed.
- Unknown: The effect of clicking button "6" on the Ophelia Solitaire Ring product page is not established; the inspection recorded no API calls after the click step.
- Unknown: On /products/aurora-eternity-ring, the requested button labeled "8" was not identified or activated by the probe; its function, resulting display, and any associated API calls are unknown.
- Seen only in code, not checked in the running application: On /products/atelier-noir-cuff#fc2701e85be5, clicking the "Medium" button made no API calls after the interaction; the probe did not report a visible post-click change.
- Unknown: The inspected /products/heritage-link-bracelet page's product-specific visible content and controls are not available in the recorded probe details, so its displayed product information and interactions remain unverified.
- Unknown: The product name, price, description, variant options, availability, and purchase controls shown on the Maris Pearl Bracelet detail page are not specified in the recorded observation summary.
- Unknown: The product-specific content and available interactions on /products/halo-drop-earrings are not established in the evidence available from this probe.
- Unknown: The captured snapshot for /products/horizon-watch-steel does not provide product-specific details such as price, variants, availability, or purchase controls; these remain unexplored for this product.

## Changelog
- v44 (2026-11-18): Regenerated from typed knowledge items (10 unknown, 27 observed). [sources: exploration]
- v43 (2026-11-18): Regenerated from typed knowledge items (10 unknown, 26 observed). [sources: exploration]
- v42 (2026-11-18): Regenerated from typed knowledge items (10 unknown, 26 observed). [sources: exploration]
- v41 (2026-11-18): Regenerated from typed knowledge items (10 unknown, 24 observed). [sources: exploration]
- v40 (2026-11-18): Regenerated from typed knowledge items (10 unknown, 23 observed). [sources: exploration]
- v39 (2026-11-18): Regenerated from typed knowledge items (9 unknown, 23 observed). [sources: exploration]
- v38 (2026-11-18): Regenerated from typed knowledge items (9 unknown, 22 observed). [sources: exploration]
- v37 (2026-11-18): Regenerated from typed knowledge items (8 unknown, 22 observed). [sources: exploration]
- v36 (2026-11-18): Regenerated from typed knowledge items (8 unknown, 21 observed). [sources: exploration]
- v35 (2026-11-18): Regenerated from typed knowledge items (8 unknown, 20 observed). [sources: exploration]
- v34 (2026-11-18): Regenerated from typed knowledge items (7 unknown, 20 observed). [sources: exploration]
- v33 (2026-11-18): Regenerated from typed knowledge items (6 unknown, 20 observed). [sources: exploration]
- v32 (2026-11-18): Regenerated from typed knowledge items (6 unknown, 19 observed). [sources: exploration]
- v31 (2026-11-18): Regenerated from typed knowledge items (6 unknown, 18 observed). [sources: exploration]
- v30 (2026-11-18): Regenerated from typed knowledge items (6 unknown, 17 observed). [sources: exploration]
- v29 (2026-11-18): Regenerated from typed knowledge items (6 unknown, 16 observed). [sources: exploration]
- v28 (2026-11-18): Regenerated from typed knowledge items (6 unknown, 15 observed). [sources: exploration]
- v27 (2026-11-18): Regenerated from typed knowledge items (6 unknown, 15 observed). [sources: exploration]
- v26 (2026-11-18): Regenerated from typed knowledge items (6 unknown, 14 observed). [sources: exploration]
- v25 (2026-11-18): Regenerated from typed knowledge items (6 unknown, 14 observed). [sources: exploration]
- v24 (2026-11-18): Regenerated from typed knowledge items (6 unknown, 13 observed). [sources: exploration]
- v23 (2026-11-18): Regenerated from typed knowledge items (6 unknown, 13 observed). [sources: exploration]
- v22 (2026-11-18): Regenerated from typed knowledge items (6 unknown, 13 observed). [sources: exploration]
- v21 (2026-11-18): Regenerated from typed knowledge items (5 unknown, 13 observed). [sources: exploration]
- v20 (2026-11-18): Regenerated from typed knowledge items (5 unknown, 12 observed). [sources: exploration]
- v19 (2026-11-18): Regenerated from typed knowledge items (5 unknown, 11 observed). [sources: exploration]
- v18 (2026-11-18): Regenerated from typed knowledge items (4 unknown, 11 observed). [sources: exploration]
- v17 (2026-11-18): Regenerated from typed knowledge items (4 unknown, 10 observed). [sources: exploration]
- v16 (2026-11-18): Regenerated from typed knowledge items (4 unknown, 9 observed). [sources: exploration]
- v15 (2026-11-18): Regenerated from typed knowledge items (4 unknown, 8 observed). [sources: exploration]
- v14 (2026-11-18): Regenerated from typed knowledge items (4 unknown, 7 observed). [sources: exploration]
- v13 (2026-11-18): Regenerated from typed knowledge items (4 unknown, 7 observed). [sources: exploration]
- v12 (2026-11-18): Regenerated from typed knowledge items (4 unknown, 7 observed). [sources: exploration]
- v11 (2026-11-18): Regenerated from typed knowledge items (4 unknown, 6 observed). [sources: exploration]
- v10 (2026-11-18): Regenerated from typed knowledge items (3 unknown, 6 observed). [sources: exploration]
- v9 (2026-11-18): Regenerated from typed knowledge items (3 unknown, 5 observed). [sources: exploration]
- v8 (2026-11-18): Regenerated from typed knowledge items (3 unknown, 4 observed). [sources: exploration]
- v7 (2026-11-18): Regenerated from typed knowledge items (3 unknown, 3 observed). [sources: exploration]
- v6 (2026-11-18): Regenerated from typed knowledge items (3 unknown, 3 observed). [sources: exploration]
- v5 (2026-11-18): Regenerated from typed knowledge items (3 unknown, 3 observed). [sources: exploration]
- v4 (2026-11-18): Regenerated from typed knowledge items (2 unknown, 2 observed). [sources: exploration]
- v3 (2026-11-18): Regenerated from typed knowledge items (1 unknown, 1 observed). [sources: exploration]
- v2 (2026-11-18): Regenerated from typed knowledge items (1 unknown). [sources: exploration]
- v1 (2026-11-18): Regenerated from typed knowledge items (1 unknown). [sources: exploration]
