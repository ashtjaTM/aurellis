---
title: "Home & Featured Collections"
parent: "Application"
summary: "The storefront home page presents Aurellis branding and entry points to product categories, collections, appointment booking, policies, wishlist, and cart."
tags: ["storefront", "home", "navigation"]
related:
  - file: "Product Detail"
    type: related_to
  - file: "Cart"
    type: related_to
  - file: "Shipping Policy"
    type: related_to
  - file: "Contact"
    type: related_to
  - file: "New In"
    type: related_to
  - file: "Concierge Chat"
    type: related_to
sources: ["exploration"]
version: 20
confidence: high
has_open_conflicts: false
updated_at: "2026-11-18T07:31:53.548Z"
---

## Sub-features
- Primary navigation
- Featured collections

## Business Rules
- The home page navigation links to appointment booking at /contact, shipping and returns at /policies/shipping, New In at /new-in, the Rings, Necklaces, Bracelets, Earrings, and Watches categories, the Atelier Noir collection, Wishlist at /auth/sign-in, and Cart at /cart.
- On the homepage newsletter signup form, the only input is named `email`, has the placeholder “Your email”, is type `email`, and is required; no minlength, maxlength, or pattern constraint was present. The form’s submit button is labelled “Subscribe”.
- On the homepage, the newsletter signup section (“Stay in the atelier” / “First looks, slower stories”) has one field, “Your email”: it is an email input and is required. No additional length, pattern, or range constraint was observed.
- On `/`, clicking the "Open chat" button triggers `GET /api/chat/topics`; the observed request returned HTTP 200 with an empty `topics` array. The page content did not match any fields from that response.

## Terminology
- Aurellis

## Unexplored / Unknown
- select "Currency" on / - the turn failed: ProviderShared.stream: Failed to read openai/openai-responses stream
- form "Subscribe" on /: rejection (empty) - needs a sandbox or a person: it would change data in a protected environment
- form "Subscribe" on /: rejection (required) - needs a sandbox or a person: it would change data in a protected environment
- form "Subscribe" on /: rejection (type) - needs a sandbox or a person: it would change data in a protected environment
- form "Send message" on /: rejection (empty) - needs a sandbox or a person: it would change data in a protected environment
- form "Send message" on /: rejection (maxlength) - needs a sandbox or a person: it would change data in a protected environment

## Changelog
- v20 (2026-11-18): Regenerated from typed knowledge items (4 observed). [sources: exploration]
- v19 (2026-11-18): Regenerated from typed knowledge items (4 observed). [sources: exploration]
- v18 (2026-11-18): Regenerated from typed knowledge items (4 observed). [sources: exploration]
- v17 (2026-11-18): Regenerated from typed knowledge items (4 observed). [sources: exploration]
- v16 (2026-11-18): Regenerated from typed knowledge items (4 observed). [sources: exploration]
- v15 (2026-11-18): Regenerated from typed knowledge items (4 observed). [sources: exploration]
- v14 (2026-11-18): Regenerated from typed knowledge items (4 observed). [sources: exploration]
- v13 (2026-11-18): Regenerated from typed knowledge items (4 observed). [sources: exploration]
- v12 (2026-11-18): Regenerated from typed knowledge items (4 observed). [sources: exploration]
- v11 (2026-11-18): Regenerated from typed knowledge items (4 observed). [sources: exploration]
- v10 (2026-11-18): Regenerated from typed knowledge items (3 observed). [sources: exploration]
- v9 (2026-11-18): Regenerated from typed knowledge items (2 observed). [sources: exploration]
- v8 (2026-11-18): Regenerated from typed knowledge items (1 observed). [sources: exploration]
- v7 (2026-11-18): Regenerated from typed knowledge items (1 observed). [sources: exploration]
- v6 (2026-11-18): Regenerated from typed knowledge items (1 observed). [sources: exploration]
- v5 (2026-11-18): Regenerated from typed knowledge items (1 observed). [sources: exploration]
- v4 (2026-11-18): Regenerated from typed knowledge items (1 observed). [sources: exploration]
- v3 (2026-11-18): Regenerated from typed knowledge items (1 observed). [sources: exploration]
- v2 (2026-11-18): Regenerated from typed knowledge items (1 observed). [sources: exploration]
- v1 (2026-11-18): Regenerated from typed knowledge items (1 observed). [sources: exploration]
