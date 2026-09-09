# Week 2 checklist

Complete these activities before requesting Week 3.

## Review the expanded contract

- [X] Read `docs/week-02-api-design.md`.
- [X] Identify the new `Finding` schema and explain its purpose.
- [X] Trace `ReviewJob.findings` to the `Finding` schema.
- [X] Trace the `GET /reviews/{reviewId}` `200` response to `CompletedReviewExample`.
- [X] Confirm that both findings in the completed example follow the `Finding` schXma.
- [X] Explain why `requiresHumanReview` uses `const: true`.

## Review request and error examples

- [X] Trace the `POST /reviews` request to `CreateReviewRequestExample`.
- [X] Confirm that the `400`, `401`, and `404` examples follow the `Error` schema.
- [X] Confirm that each error example's `status` matches its HTTP response code.
- [X] Confirm that no example contains an actual API key or personal information.

## Validate the OpenAPI contract

- [X] Run `npx --yes @redocly/cli lint openapi/openapi.yaml` from the repository root.
- [X] Review every validation message instead of assuming the file is correct.
- [X] Record the validation result below.

**Validation result:** The OpenAPI 3.1 specification passed Redocly validation successfully with no errors.

## Practice the GitHub workflow

- [X] Create a branch named `week-02-complete-openapi`.
- [X] Create or update the issue titled `Complete and validate OpenAPI contract`.
- [X] Review the changed files before committing.
- [X] Commit with the message `Complete and validate OpenAPI contract`.
- [X] Push the branch and open a pull request.
- [X] Confirm that the pull request describes the schemas, examples, and validation result.

## Reflection

Add two or three sentences under each question.

### How does the `Finding` schema improve the API contract?

The `Finding` schema improves the API contract by giving every documentation issue a consistent structure, including its check type, severity, message, and suggested correction. It also uses `requiresHumanReview` to make clear that technical writers must evaluate AI-generated recommendations before accepting or publishing them.

### Why are reusable examples valuable in OpenAPI?

Reusable examples provide a single source that multiple API operations can reference, reducing duplication and inconsistency. When an example is updated in the `components' section, every operation that references it receives the same accurate information.

### What does validation confirm, and what does it not confirm?

Validation confirms that the OpenAPI document follows the required structure, uses valid syntax, and contains working references. However, it does not confirm that the API behaves as documented or that the descriptions and examples are clear, accurate, and useful, so human review and API testing are still necessary.

### How does this contract prepare the API for future agent use without adding an agent yet?

The contract provides stable operation IDs, clearly defined schemas, constrained values, reusable examples, and structured errors that a future AI agent can interpret reliably. It also establishes safety expectations through `requiresHumanReview`, preparing the API for agent-assisted workflows without implementing or connecting an AI agent yet.

## Completion confirmation

- [X] Every checklist item is complete.
- [X] The OpenAPI contract passes validation.
- [X] All four reflections are written.
- [X] The Week 2 pull request is visible on GitHub.
