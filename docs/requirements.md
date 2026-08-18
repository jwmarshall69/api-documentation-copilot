# Product and documentation requirements

## Functional requirements

| ID | Requirement | Week introduced |
| --- | --- | --- |
| FR-01 | A client can create a documentation-review job. | 1 |
| FR-02 | A client can retrieve a review job by ID. | 1 |
| FR-03 | A request can select one or more review checks. | 1 |
| FR-04 | A completed job returns structured findings. | 2 — implemented |
| FR-05 | The future agent retrieves relevant style guidance before generating findings. | 6 |
| FR-06 | A human can evaluate recommendations before changing source content. | 5 |

## Documentation requirements

| ID | Requirement | Planned evidence |
| --- | --- | --- |
| DR-01 | Explain the API's purpose and intended users. | README and project brief |
| DR-02 | Provide a copy-ready first request. | Quickstart |
| DR-03 | Document authentication without exposing secrets. | Authentication guide |
| DR-04 | Explain all request fields and response properties. | OpenAPI and endpoint guides |
| DR-05 | Provide realistic success and error examples. | OpenAPI and error guide |
| DR-06 | Explain AI limitations and human-review responsibilities. | Agent guide |
| DR-07 | Keep prose, examples, and the API contract consistent. | Pull-request review and CI |

## Initial user stories

- As an API technical writer, I want to submit a passage for review so that I can identify possible documentation problems.
- As an API technical writer, I want findings grouped by type and severity so that I can prioritize revisions.
- As a developer, I want actionable feedback with an explanation so that I understand how to improve my draft.
- As a reviewer, I want AI recommendations to require human judgment so that unverified changes are not published automatically.

## Definition of done for a documented endpoint

- The purpose and user benefit are clear.
- Parameters and properties include useful descriptions.
- At least one realistic request and response example is present.
- Expected errors are documented.
- Terminology matches the style guide.
- The example conforms to the schema.
