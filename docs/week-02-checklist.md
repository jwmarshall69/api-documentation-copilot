# Week 2 checklist

Complete these activities before requesting Week 3.

## Review the expanded contract

- [X] Read `docs/week-02-api-design.md`.
- [ ] Identify the new `Finding` schema and explain its purpose.
- [ ] Trace `ReviewJob.findings` to the `Finding` schema.
- [ ] Trace the `GET /reviews/{reviewId}` `200` response to `CompletedReviewExample`.
- [ ] Confirm that both findings in the completed example follow the `Finding` schema.
- [ ] Explain why `requiresHumanReview` uses `const: true`.

## Review request and error examples

- [ ] Trace the `POST /reviews` request to `CreateReviewRequestExample`.
- [ ] Confirm that the `400`, `401`, and `404` examples follow the `Error` schema.
- [ ] Confirm that each error example's `status` matches its HTTP response code.
- [ ] Confirm that no example contains an actual API key or personal information.

## Validate the OpenAPI contract

- [ ] Run `npx --yes @redocly/cli lint openapi/openapi.yaml` from the repository root.
- [ ] Review every validation message instead of assuming the file is correct.
- [ ] Record the validation result below.

**Validation result:** _Write the result here._

## Practice the GitHub workflow

- [ ] Create a branch named `week-02-complete-openapi`.
- [ ] Create or update the issue titled `Complete and validate OpenAPI contract`.
- [ ] Review the changed files before committing.
- [ ] Commit with the message `Complete and validate OpenAPI contract`.
- [ ] Push the branch and open a pull request.
- [ ] Confirm that the pull request describes the schemas, examples, and validation result.

## Reflection

Add two or three sentences under each question.

### How does the `Finding` schema improve the API contract?

_Write your answer here._

### Why are reusable examples valuable in OpenAPI?

_Write your answer here._

### What does validation confirm, and what does it not confirm?

_Write your answer here._

### How does this contract prepare the API for future agent use without adding an agent yet?

_Write your answer here._

## Completion confirmation

- [ ] Every checklist item is complete.
- [ ] The OpenAPI contract passes validation.
- [ ] All four reflections are written.
- [ ] The Week 2 pull request is visible on GitHub.

