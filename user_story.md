# Jira User Story — Browse Products and Manage Cart

**Suggested issue key:** AUR-001  
**Issue type:** Story  
**Priority:** High (suggested; adjust to team backlog)  
**Component:** Product Listing / Product Details / Cart  
**Target:** Aurellis Fashion — https://aurellis.fashion

## User Story
As a customer visiting Aurellis Fashion, I want to browse available fashion products, view their details, select product options where applicable, and add items to my shopping cart, so that I can review the products I intend to purchase.

## Description
The storefront should support product discovery through its available collection or listing pages. A customer should be able to open a product detail view, inspect relevant information, and select required options such as size or color if the product provides them. The customer should then be able to add the item to the cart and review or update cart contents.

The system should keep product identity, selected options, quantity, and pricing consistent through the supported shopping flow. It should communicate validation or availability issues clearly. Exact page names, variant types, and cart rules must be aligned with observed website behavior and the site's API documentation.

## Acceptance Criteria

### AC1 — Discover products
- Customer can navigate to a product listing/collection page available on the site.
- The page displays available products with the information actually provided by the storefront (e.g., image, title, price).
- Selecting a product opens its corresponding details.
- The application handles empty, loading, and failure states clearly.

### AC2 — View product details
- Product detail view presents the available product information (e.g., title, images, description, price).
- If the product supports variants, the available options are displayed.
- Required option selection is validated before add-to-cart.
- Product identifier and details correspond to the item selected from the listing.

### AC3 — Add an item to cart
- Customer can add an available product to cart.
- Successful add operation provides clear confirmation or visible cart update.
- Cart reflects the correct product, selected options, quantity, and price.
- Unavailable product/variant and invalid selection are handled with an appropriate message.

### AC4 — Manage cart contents
- Customer can view items currently in cart.
- Customer can change quantity within the application's allowed range.
- Customer can remove an item.
- Cart line totals and overall totals update correctly after changes.
- Empty-cart state is shown when no items remain.

### AC5 — Maintain data consistency
- Product identity and price are consistent across listing, details, and cart.
- Selected variants in cart match the options selected on the product page.
- The system applies its actual pricing/discount rules consistently.
- If checkout exists, price and availability are revalidated before order submission.

### AC6 — Error handling
- Invalid or unavailable operations are not silently treated as successful.
- The customer receives understandable feedback when a cart action fails.
- The cart state remains consistent after a failed operation.

## Preconditions
- Target application is accessible.
- At least one product is available.
- Customer can access listing/details and cart features.
- Test execution uses an approved test environment/account where needed.

## Expected Result
Customer can discover products, inspect details, add selected items to cart, and manage the cart with accurate item information and totals.

## QA test scope
- UI: navigation, listing, details, options, cart, validation and state.
- API: documented/discovered product and cart endpoints, schemas, status codes, validation, and business rules.
- UI+API: carry out a UI action and compare resulting API/backend state with visible cart data.

> This story is a proposed QA story. Confirm exact feature behavior with the live Aurellis site and its API docs before linking it as an authoritative Jira requirement.
