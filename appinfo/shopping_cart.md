# Shopping Cart — Workflow and Validation Context

## Purpose
Validate the customer's cart actions and ensure the cart displays the correct products, selected options, quantities, and price totals. Verify only behaviors actually supported by Aurellis Fashion.

## Candidate workflow
1. Select a product from a listing.
2. Open its details.
3. Choose required options (if present).
4. Add it to cart.
5. Confirm feedback and cart contents.
6. Change quantity or remove item.
7. Verify updated totals.
8. Continue toward checkout if supported in the test environment.

## Cart information to observe
- Product title and identifier
- Variant selections
- Unit price and currency
- Quantity
- Line subtotal
- Cart subtotal/total
- Discount, shipping, and tax lines if displayed
- Availability/stock messages
- Cart empty state

## Candidate business rules (confirm against the application)
- Quantity must satisfy allowed minimum and maximum.
- Cart must not accept unavailable product/variant.
- Required product options must be provided.
- Quantity changes should update line and cart totals.
- Removing an item should remove it from the visible cart and recalculate totals.
- Re-adding the same item may merge quantity or create a separate line; capture the observed rule.
- Cart persistence across refresh, browser session, or sign-in should be tested against expected product behavior.
- Price and availability may be revalidated before checkout.

## Negative and edge tests
- Add-to-cart without required option.
- Attempt quantity zero, negative, non-numeric, or above limit (where possible).
- Add out-of-stock item.
- Cart update request fails.
- Cart becomes empty after removal.
- Price/stock changes between product view and cart.
- Cart data remains correct after refresh or navigation.

## API/UI consistency
When a cart API is identified, compare its actual response to the UI: item identity, selected variant, quantity, unit price, subtotal, and cart total. Use only documented or observed endpoints.
