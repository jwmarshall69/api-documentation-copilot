# API Documentation Copilot

An eight-week portfolio project combining API technical writing, OpenAPI, GitHub, Docs-as-Code, retrieval-augmented generation (RAG), and an AI documentation-review agent.

## Current status

**Week 1 — Project foundation and API design**

The project currently defines the product concept, target audience, documentation requirements, repository conventions, and the initial OpenAPI 3.1 contract for the fictional **DocuGuard API**.

> Scope rule: Only the files required for the current week are implemented. Later-week directories are described in the roadmap but intentionally not created yet.

## Portfolio story

DocuGuard is a REST API that accepts API-documentation text for review and returns findings such as missing examples, unclear descriptions, inconsistent terminology, and possible style-guide violations. During later weeks, an AI agent will use this API and a retrieval knowledge base to assist—but not replace—a technical writer.

## Week 1 learning objectives

- Translate a product idea into API and documentation requirements.
- Identify the audience and its primary tasks.
- Organize a Docs-as-Code repository.
- Create an initial OpenAPI 3.1 specification.
- Use Git commits to preserve meaningful project history.

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
│   └── week-01-checklist.md
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
| 1 | Foundation, requirements, and initial API design | In progress |
| 2 | Complete and validate the OpenAPI contract | Locked |
| 3 | Developer quickstart and task-based documentation | Locked |
| 4 | Authentication, errors, pagination, and Postman | Locked |
| 5 | AI documentation-review agent | Locked |
| 6 | RAG knowledge base and evaluation | Locked |
| 7 | GitHub Actions and documentation site | Locked |
| 8 | Usability testing and portfolio case study | Locked |

## Week 1 completion rule

Week 1 is complete only after every item in `docs/week-01-checklist.md` is checked and the reflection questions are answered. Do not begin Week 2 before that review.

