# Product Catalog, Collection Listing, and Product Details

## Scope
This knowledge covers product discovery and inspection in Aurellis Fashion. Confirm the actual page structure and fields from the live site before treating the details as requirements.

## Collection/listing behavior to explore
- Navigation into product collections or category pages.
- Product cards and their click targets.
- Product image/title/price display.
- Discount or sale price representation, if applicable.
- Search, filter, sort, and pagination controls, if present.
- Loading, empty, and error states.

## Product detail context to capture
For each sample product, record:
- Product title and product ID/SKU (if exposed)
- Product detail URL
- Description and specifications
- Image gallery or thumbnails
- Price and currency
- Sale price / original price, if applicable
- Variant dimensions (such as size or color), if applicable
- Availability/stock indicators
- Add-to-cart control and validation behavior

## Candidate functional rules
1. Selecting a card should open details for the same product.
2. Product title and identifier should remain consistent between listing and detail page.
3. Price and currency should match across listing and details.
4. Variant selection should update the selected option state where variants exist.
5. Unavailable options should be clearly represented and not submitted if disallowed.
6. Any displayed discount should be arithmetically consistent with the displayed prices.
7. Missing or broken product content should be reported.

## Candidate negative scenarios
- Listing returns no products.
- Search/filter results contain no matches.
- Product detail link points to an unavailable item.
- Required variant is not selected.
- Product or variant becomes unavailable during the customer flow.
- Product image or detail data fails to load.

## API correlation
If product APIs are documented/discovered, map listing and detail UI fields to response fields. Record actual endpoint, method, request parameters, response schema, status codes, and product identifier. Do not invent route names or payload fields.
