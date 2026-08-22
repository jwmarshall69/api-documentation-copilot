# Week 2 API design notes

## Purpose of this revision

Week 2 completes the DocuGuard API contract by defining the results returned by a completed review job. The revision also gives every documented error a structured response and moves examples into reusable OpenAPI components.

## Structured findings

The `Finding` schema makes review results predictable for developers and future automation. Each finding identifies the check that produced it, its suggested severity, an explanation, and a proposed revision.

`requiresHumanReview` is always `true`. This rule makes the governance boundary part of the API contract: a suggestion is not an approved documentation change.

## Reusable examples

Examples are stored under `components/examples` and connected to operations with `$ref`. This reduces duplication and provides one source of truth when the same example is reused.

Trace the completed response in this order:

1. Start at `GET /reviews/{reviewId}`.
2. Follow the `200` response schema to `#/components/schemas/ReviewJob`.
3. Follow the `findings` item reference to `#/components/schemas/Finding`.
4. Return to the `200` response and follow `completedReview` to `#/components/examples/CompletedReviewExample`.
5. Compare every example property and value with both schemas.

## Agent-ready design characteristics

This contract is not an AI agent yet. However, its stable operation IDs, constrained values, structured errors, explicit field descriptions, and predictable findings will make it easier for later tools to interpret safely.

## Validation command

From the repository root, run:

```bash
npx --yes @redocly/cli lint openapi/openapi.yaml
```

Validation checks the structure and references in the OpenAPI document. It does not prove that the API behavior or documentation wording is correct, so a technical review is still required.
