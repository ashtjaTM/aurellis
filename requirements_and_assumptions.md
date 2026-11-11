# Requirements, Assumptions, and Validation Notes

## User-provided context
- Target website: https://aurellis.fashion
- User indicated the website has API specs/API documentation attached or available.
- Intended usage: create GitHub-hosted Project Knowledge for Lucius AI, generate scenarios, and link scenarios to a Jira story.

## Retrieval limitation
The exact domain could not be directly fetched during file preparation. Public search results surfaced several similarly named domains, which were not assumed to be the target. No third-party lookalike site is used as factual documentation for Aurellis Fashion.

## Provisional assumptions
- The target is a fashion storefront.
- Product browsing, product details, and cart are candidate workflow areas.
- Products may have options such as size/color.
- The site exposes API documentation/specs according to user-provided context.

## Must validate during exploration
- Exact site title/brand and page navigation
- Real categories/collections and sample products
- Search/filter/sort/pagination behavior
- Actual product fields and variant options
- Cart operations and persistence
- Checkout, account, authentication, and payment flows (if in scope)
- API spec location and format (e.g., OpenAPI, Swagger, Postman, or other)
- API base URL, endpoint paths, HTTP methods, request/response schemas
- Authentication and authorization requirements
- Error/status codes, rate limits, and business rules
- Mapping from UI actions to API operations

## Traceability approach
For each finalized requirement:
1. Assign a Jira story/criterion identifier.
2. Map generated scenario(s) to the criterion.
3. Record whether test is UI, API, or UI+API.
4. Capture test data and expected result from verified behavior/specification.
5. Keep assumptions separate from confirmed acceptance criteria.

## Policy
Do not treat proposed behaviors in these files as confirmed requirements until checked against the live site, its API documentation, or the product owner.
