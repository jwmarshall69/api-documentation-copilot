# Project brief

## Problem

API documentation reviews are often manual and inconsistent. Technical writers must locate missing examples, vague descriptions, terminology problems, and incomplete error guidance across many files.

## Proposed solution

API Documentation Copilot will provide a human-in-the-loop review workflow. Its fictional DocuGuard API accepts documentation content, creates an asynchronous review job, and returns structured findings that a technical writer can accept, revise, or reject.

## Target audience

### Primary audience: API technical writers

They need to review documentation efficiently, apply a style guide consistently, and retain editorial control.

### Secondary audience: API developers

They need early feedback about incomplete endpoint descriptions, examples, and error responses before requesting a documentation review.

## Primary user tasks

1. Submit a documentation passage for review.
2. Select the checks to perform.
3. Retrieve the review status and findings.
4. Interpret each finding and revise the source manually.

## Success criteria

- A new developer can submit a review without reading the implementation.
- The OpenAPI contract contains realistic requests, responses, and errors.
- Documentation and API examples remain consistent.
- AI-generated findings are clearly presented as recommendations.
- The Git history demonstrates an intentional Docs-as-Code workflow.

## Ethical and quality principles

- Keep a human responsible for final editorial decisions.
- Do not send secrets or personal information in review content.
- Distinguish generated recommendations from verified facts.
- Explain limitations, confidence, and evaluation results.
- Prefer accurate, actionable feedback over large quantities of findings.

## Out of scope for Week 1

- A working API server
- An LLM connection
- RAG or a vector database
- Postman collections
- Automated deployment
- A published documentation website

