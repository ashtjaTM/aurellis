# Test Data Capture and Boundary Matrix — Aurellis Fashion

## Data sourcing
Use product records, identifiers, prices, variants, and API request values from the live site, its spec, or a dedicated test environment. The examples below are categories/templates, not fabricated production values.

## Product data template
| Attribute | Capture value from site/spec |
|---|---|
| Product ID / SKU | Actual identifier |
| Product title | Actual display title |
| Product detail URL | Observed route |
| Price | Actual amount |
| Currency | Actual currency code/symbol |
| Discount/original price | If shown |
| Availability | Actual status |
| Variant dimension | Actual option type (if any) |
| Variant value | Actual option selected |
| API resource/operation | Exact documented/discovered mapping |

## Test data groups
- Product available for purchase
- Product with required option(s), if present
- Product with multiple options, if present
- Out-of-stock product or option, if exposed
- Discounted item, if present
- Item with no matching search result, if search exists
- Invalid/nonexistent product identifier for API negative tests

## Quantity boundaries (adjust to actual site rules)
| Case | Input |
|---|---|
| Minimum allowed | Actual min quantity |
| Normal | Typical positive quantity |
| Maximum allowed | Actual maximum |
| Above maximum | Max + 1 |
| Zero | 0 |
| Negative | -1 |
| Non-numeric | String / malformed input (API only if relevant) |

## API test input categories
- Valid request from official spec or captured cURL
- Missing required field
- Invalid field type
- Invalid identifier
- Invalid/expired credential (only in authorized test setup)
- Unsupported method or content type
- Boundary values for pagination, quantity, or filters when documented

## Test safety
Do not use real payment details or place real orders. Run checkout, destructive, or account-impacting tests only in a designated test environment with explicit authorization.
