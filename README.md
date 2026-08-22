# API Documentation Copilot

An eight-week portfolio project combining API technical writing, OpenAPI, GitHub, Docs-as-Code, retrieval-augmented generation (RAG), and an AI documentation-review agent.

## Current status

**Week 2 — Complete and validate the OpenAPI contract**

The project now contains a complete OpenAPI 3.1 contract for the fictional **DocuGuard API**, including structured findings, reusable examples, and documented error responses.

> Scope rule: Only the files required for the current week are implemented. Later-week directories are described in the roadmap but intentionally not created yet.

## Portfolio story

DocuGuard is a REST API that accepts API-documentation text for review and returns findings such as missing examples, unclear descriptions, inconsistent terminology, and possible style-guide violations. During later weeks, an AI agent will use this API and a retrieval knowledge base to assist—but not replace—a technical writer.

## Week 2 learning objectives

- Expand an API contract without changing its original purpose.
- Model structured findings with reusable OpenAPI schemas.
- Trace `$ref` links among operations, schemas, and examples.
- Confirm that request, response, and error examples follow their schemas.
- Validate an OpenAPI file and interpret validation results.

## Repository contents

```text
api-documentation-copilot/
├── README.md
├── CONTRIBUTING.md
├── .gitignore
├── docs/
│   ├── project-brief.md
│   ├── requirements.md
│   ├── style-guide.md
│   ├── week-01-checklist.md
│   ├── week-02-api-design.md
│   └── week-02-checklist.md
└── openapi/
    └── openapi.yaml
```

## How to review the API contract

1. Open `openapi/openapi.yaml` in Visual Studio Code.
2. Install an OpenAPI extension such as **Swagger Viewer** if desired.
3. Review the endpoint, schemas, examples, and error response.
4. Record suggested changes in `docs/week-01-checklist.md`.

## Eight-week roadmap

| Week | Focus | Status |
| --- | --- | --- |
| 1 | Foundation, requirements, and initial API design | Complete |
| 2 | Complete and validate the OpenAPI contract | In progress |
| 3 | Developer quickstart and task-based documentation | Locked |
| 4 | Authentication, errors, pagination, and Postman | Locked |
| 5 | AI documentation-review agent | Locked |
| 6 | RAG knowledge base and evaluation | Locked |
| 7 | GitHub Actions and documentation site | Locked |
| 8 | Usability testing and portfolio case study | Locked |

## Week 2 completion rule

Week 2 is complete only after every item in `docs/week-02-checklist.md` is checked, the OpenAPI contract passes validation, and the reflection questions are answered. Do not begin Week 3 before that review.
