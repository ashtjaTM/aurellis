# Test Scenario Candidates — Aurellis Fashion

Scenario candidates for Lucius AI. They are not asserted as verified tests. Discover real endpoint paths, methods, schemas, authentication, and expected values from Aurellis' API docs/spec or application traffic.

## UI — Product discovery
1. Navigate to a product listing/collection and verify visible product cards.
2. Open a product from a card and verify the detail view belongs to the same item.
3. Verify product title, images, price, currency, and description fields that are present.
4. Verify search/filter/sort behavior if the controls exist.
5. Verify no-result, loading, and error states where triggerable.

## UI — Product and cart
6. Select a product option (if applicable) and verify selected state.
7. Attempt add-to-cart with required option missing.
8. Add an available product and verify success feedback/cart entry.
9. Verify cart item product identity and option selection.
10. Update quantity and verify displayed line subtotal and total.
11. Remove an item and verify cart update.
12. Remove all items and verify empty cart.
13. Refresh/navigate and check cart persistence against intended behavior.
14. Attempt a stock/quantity boundary condition where safely available.

## API — Spec-driven testing
15. Import the actual API specification and validate the documented product-list operation.
16. Retrieve a product by its actual identifier and validate response schema and data types.
17. Submit invalid identifier/parameters and verify documented error response.
18. Validate documented availability/variant operation, if present.
19. Exercise actual cart add/update/remove endpoints, if documented.
20. Validate positive, negative, boundary, and authorization cases against the documented contract.

## API — Request/cURL-based testing
21. Provide a real captured/documented cURL request and validate its response.
22. Test a set of multiple real API requests in a batch, checking each request's status, response shape, and key assertions.
23. Verify handling of missing/invalid headers or parameters according to documented behavior.
24. Verify response content type, status code, and error payload shape.

## UI + API — Cross-layer
25. Add a product through UI and compare cart item against actual cart API response.
26. Change quantity in UI and verify the API/backend cart state updates.
27. Remove product in UI and verify it is absent from API cart state.
28. Compare product price from API with listing/detail/cart display.
29. Verify selected variant/identifier in UI matches the submitted API payload and returned cart item.

## Suggested tags
`@aurellis` `@product-listing` `@product-details` `@cart` `@pricing` `@availability` `@ui` `@api` `@ui-api` `@negative` `@boundary`
