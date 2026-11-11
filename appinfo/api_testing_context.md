# Aurellis Fashion — API Testing Context

## Context
The demo owner selected Aurellis Fashion and stated that API specifications and documentation are available on the site. Exact specs, endpoint routes, payloads, and auth details were not retrievable in this preparation. This file describes a process for using the actual spec/request—not assumed endpoint details.

## Supported test-input approaches in Lucius (as described by demo owner)
1. **Specification-driven:** Provide the API spec file/documentation. The agent can use the defined operations, request schemas, and response information to formulate and run API tests.
2. **Request/cURL-driven:** Provide one or multiple API details or cURL commands. The agent can test the supplied requests and validate their behavior. For large request sets, provide the requests and expected checks in a clearly structured batch.
3. **Application URL discovery:** Provide the application URL. The agent explores available network traffic and checks whether API docs/specifications are discoverable. If none are found, it asks for the spec or additional API details.

## Suggested validation categories
- HTTP status code
- Response headers and content type
- Response body/schema and data types
- Required/optional fields
- Positive and negative inputs
- Authentication/authorization behavior (only with authorized credentials)
- Business logic and boundary conditions
- Data consistency between related API operations
- UI-to-API consistency for combined testing

## Spec-driven workflow
1. Locate the official API specification for Aurellis.
2. Confirm API base URL, operations, methods, parameters, request body, schemas, auth, and documented responses.
3. Import/provide the spec to the test agent.
4. Select relevant operations and create test scenarios.
5. Review test assertions and safe test data.
6. Execute against an approved environment.
7. Inspect response results and failures; trace back to the operation and requirement.

## cURL/request-driven workflow
1. Obtain real cURL commands from official docs or authorized browser/network capture.
2. Check that secrets/tokens are removed or safely handled.
3. Provide request(s), expected behavior, and any constraints.
4. Validate returned status, response structure, and relevant data.
5. Test malformed or boundary input only where authorized.

## Application URL exploration workflow
1. Submit the application URL for exploration.
2. Agent checks the application's accessible network activity and documentation/spec hints.
3. If a spec is discovered, review and use it.
4. If a spec cannot be found, provide the official spec, a cURL request, or additional API context.
5. Do not assume that the absence of visible docs means no API exists.

## UI + API testing
For a combined test, carry out an action through the UI (for example, product lookup or cart operation if supported), then validate the corresponding API/backend data. Compare identifiers, selected options, quantities, and prices only where those fields exist in the actual contract.

## API documentation checklist
| Item | Capture from real documentation |
|---|---|
| API base URL | Exact host/base path |
| Operation | Summary/name |
| HTTP method | GET/POST/PUT/PATCH/DELETE etc. |
| Endpoint path | Exact route |
| Authentication | Type and scopes |
| Request params/body | Names, types, required status |
| Response schema | Structure and types |
| Success codes | Documented values |
| Error codes | Documented values |
| Test environment | Safe target and credentials |
