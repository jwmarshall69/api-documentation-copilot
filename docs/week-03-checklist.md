# Week 3 checklist

Complete these activities before requesting Week 4.

## Review the developer journey

- [ ] Read `docs/getting-started.md` from beginning to end.
- [ ] Identify the prerequisite information provided before the first request.
- [ ] Explain why `POST /reviews` returns `202 Accepted` instead of `200 OK`.
- [ ] Trace the review ID from the create response into the retrieve request.
- [ ] Explain what the developer must do after receiving a finding.

## Compare the documentation with OpenAPI

- [ ] Compare the quickstart request with `CreateReviewRequestExample`.
- [ ] Confirm the request-field names, allowed values, and minimum length match the schema.
- [ ] Compare the completed response with `CompletedReviewExample`.
- [ ] Confirm all four review statuses match the `ReviewJob` schema.
- [ ] Confirm the endpoint guides list the same errors as `openapi/openapi.yaml`.

## Review usability and safety

- [ ] Confirm every procedure begins with a clear user goal.
- [ ] Confirm code examples are complete and copy-ready after placeholders are replaced.
- [ ] Confirm placeholders such as `YOUR_API_KEY` and `REVIEW_ID` are explained.
- [ ] Confirm no real credentials or personal information appear in the documentation.
- [ ] Confirm the documentation clearly states that the API server is fictional.

## Practice the GitHub workflow

- [ ] Create a branch named `week-03-developer-docs`.
- [ ] Create an issue titled `Write developer quickstart and endpoint guides`.
- [ ] Review the changed files before committing.
- [ ] Commit with the message `Add developer quickstart and endpoint guides`.
- [ ] Push the branch and open a pull request.
- [ ] Confirm the pull request describes the developer journey and consistency review.

## Reflection

Add two or three sentences under each question.

### How does the quickstart help a developer achieve a successful first request?

_Write your answer here._

### Why must the endpoint guides remain consistent with the OpenAPI contract?

_Write your answer here._

### What makes an API example copy-ready and safe?

_Write your answer here._

### How does task-based documentation differ from listing API fields alone?

_Write your answer here._

## Completion confirmation

- [ ] Every checklist item is complete.
- [ ] All quickstart and endpoint examples match the OpenAPI contract.
- [ ] All four reflections are written.
- [ ] The Week 3 pull request is visible on GitHub.
