# Aurellis Fashion — Website Overview and QA Context

## Application identity
- **Name:** Aurellis Fashion
- **Target:** https://aurellis.fashion
- **Application type:** Fashion-oriented storefront, as identified by the demo owner.
- **API context:** The demo owner stated that API specs and API documentation are available on this site. The exact spec file, routes, and API schema need to be captured from the application or its documentation.

## User goal
A visitor should be able to discover items offered by the store, inspect product information, make selections if the product offers variants, and proceed through the supported shopping journey.

## Candidate customer journey (verify on the live site)
1. Open the storefront/home page.
2. Navigate to a category, collection, or product listing.
3. Browse product cards and use available search/filter/sort controls.
4. Open a product detail page.
5. Inspect product details, images, pricing, and options such as size/color if present.
6. Select the required options and add the product to cart.
7. Open the cart and validate item, variant, quantity, and pricing.
8. Continue to checkout if this is available in the demo environment.

## Application areas to map during exploration
| Area | What to capture |
|---|---|
| Home/navigation | Navigation links, featured collections, entry points |
| Collections/listing | Product cards, pagination, filters, sorting, empty states |
| Product details | Product identifier, images, description, price, variants, availability |
| Search | Search field, matching behavior, no-result behavior (if present) |
| Cart | Add/update/remove behavior, quantity limits, totals, persistence |
| Checkout | Steps, validation, delivery/payment options; do not submit real payment |
| Account | Login/register/profile behavior only if accessible and in scope |
| Help/policies | Shipping, returns, contact, size guidance if present |
| API documentation | Spec format, service base URL, endpoints, schemas, auth, error responses |

## UI, API, and UI+API test distinction
- **UI testing:** Interact with the storefront as a customer and validate displayed behavior.
- **API testing:** Use the site's documented API spec or discovered API requests to validate endpoints and responses directly.
- **UI+API testing:** Perform a customer action in the UI and verify that the related API/backend data reflects the same product, selection, cart state, or result.

## QA objectives
- Check functionality and navigation.
- Validate product identity, data, and price consistency.
- Verify positive, negative, and boundary behavior.
- Confirm UI state corresponds to API state where test access permits.
- Capture observed behavior and distinguish it from assumptions.

> Direct access to the exact target domain was unavailable during file preparation. The above is a structured exploratory baseline, not a verified sitemap.
