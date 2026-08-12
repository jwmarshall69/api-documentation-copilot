# Week 1 checklist

Complete these activities before requesting Week 2.

## Review the foundation

- [X] Read `README.md` and explain the project in your own words.
- [X] Read `docs/project-brief.md` and confirm the problem and audience make sense.
- [X] Review the functional and documentation requirements.
- [X] Review the style-guide terminology.

## Review the API design

- [X] Open `openapi/openapi.yaml` in Visual Studio Code.
- [ ] Identify the API server URL and authentication method.
- [ ] Identify the two initial operations.
- [ ] Trace `CreateReviewRequest` from request to example.
- [ ] Trace `ReviewJob` from response to example.
- [ ] Confirm that the `400` error example follows the `Error` schema.

## Practice the GitHub workflow

- [X] Create a new GitHub repository named `api-documentation-copilot`.
- [X] Add these starter files using GitHub Desktop or Visual Studio Code.
- [X] Commit with the message `Add Week 1 project foundation`.
- [X] Push the repository to GitHub.
- [X] Create an issue titled `Review Week 1 API design`.

## Reflection

Add two or three sentences under each question.

### What problem does this project solve?

This project solves the challenge of creating accurate, complete, and consistent API documentation. The API Documentation Copilot uses AI to review OpenAPI specifications, identify missing information, and suggest improvements while keeping a technical writer responsible for the final approval.

### Why is a human-in-the-loop workflow important?

A human-in-the-loop workflow is important because AI-generated content may contain errors, incomplete information, or misleading recommendations. A technical writer reviews and approves the AI’s suggestions to ensure the final API documentation is accurate, clear, and appropriate for developers.

### Which part of the OpenAPI file was easiest to understand?

The `info` section was the easiest part of the OpenAPI file to understand because it clearly identifies the API’s title, version, and purpose. It provides a simple overview before moving into more technical sections, such as paths, parameters, and response schemas.

### Which part needs more explanation or practice?

The `components` section needs more explanation and practice because it defines reusable schemas, security settings, and other shared elements referenced throughout the OpenAPI file. I need more experience understanding how `$ref` connects these reusable components to endpoints, requests, and responses.

## Completion confirmation

- [ ] Every checklist item is complete.
- [X] All four reflections are written.
- [X] The Week 1 commit is visible on GitHub.

