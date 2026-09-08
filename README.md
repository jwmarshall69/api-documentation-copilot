# API Documentation Copilot

An eight-week portfolio project combining API technical writing, OpenAPI, GitHub, Docs-as-Code, retrieval-augmented generation (RAG), and an AI documentation-review agent.

## Current status

**Week 3 — Developer quickstart and task-based documentation**

The project now adds developer-facing guidance for submitting a documentation review and retrieving its results. The OpenAPI contract remains the source of truth for the examples and field definitions.

> Scope rule: Only the files required for the current week are implemented. Later-week directories are described in the roadmap but intentionally not created yet.

## Portfolio story

DocuGuard is a REST API that accepts API-documentation text for review and returns findings such as missing examples, unclear descriptions, inconsistent terminology, and possible style-guide violations. During later weeks, an AI agent will use this API and a retrieval knowledge base to assist—but not replace—a technical writer.

## Week 3 learning objectives

- Write a developer quickstart around a successful first task.
- Convert OpenAPI operations into clear, task-based endpoint documentation.
- Keep prose, field descriptions, and examples consistent with the API contract.
- Explain an asynchronous request workflow without exposing implementation details.
- Review documentation for usability and copy-readiness.

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
│   ├── getting-started.md
│   ├── endpoints/
│   │   ├── create-review.md
│   │   └── get-review.md
│   ├── week-01-checklist.md
│   ├── week-02-api-design.md
│   ├── week-02-checklist.md
│   └── week-03-checklist.md
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
| 2 | Complete and validate the OpenAPI contract | Complete |
| 3 | Developer quickstart and task-based documentation | In progress |
| 4 | Authentication, errors, pagination, and Postman | Locked |
| 5 | AI documentation-review agent | Locked |
| 6 | RAG knowledge base and evaluation | Locked |
| 7 | GitHub Actions and documentation site | Locked |
| 8 | Usability testing and portfolio case study | Locked |

## Week 3 completion rule

Week 3 is complete only after every item in `docs/week-03-checklist.md` is checked, the examples are compared with the OpenAPI contract, and the reflection questions are answered. Do not begin Week 4 before that review.
