# Get started with the DocuGuard API

Use the DocuGuard API to submit API-documentation text for review and retrieve structured recommendations. This quickstart shows the expected workflow for the fictional portfolio API; a live server is not available yet.

## Before you begin

You need:

- A command-line terminal with cURL.
- A DocuGuard API key represented in this guide by `YOUR_API_KEY`.
- Documentation text containing at least 20 characters.

Never commit an actual API key to the repository.

## 1. Create a review job

Send a `POST` request to `/reviews`. Select one or more checks from `clarity`, `terminology`, `examples`, and `completeness`.

```bash
curl --request POST \
  --url https://api.docuguard.dev/v1/reviews \
  --header "Content-Type: application/json" \
  --header "X-API-Key: YOUR_API_KEY" \
  --data '{
    "content": "The endpoint gets user stuff and returns it.",
    "contentType": "endpoint-description",
    "checks": ["clarity", "terminology", "examples"]
  }'
```

The API accepts the request and returns `202 Accepted` because the review runs asynchronously:

```json
{
  "id": "rev_01J8Z7K3F2ACM9P4T6QX",
  "status": "queued",
  "createdAt": "2026-08-11T08:00:00Z"
}
```

Save the `id`; you need it to retrieve the review.

## 2. Retrieve the review

Replace `REVIEW_ID` with the `id` returned in the previous response.

```bash
curl --request GET \
  --url https://api.docuguard.dev/v1/reviews/REVIEW_ID \
  --header "X-API-Key: YOUR_API_KEY"
```

While processing continues, `status` can be `queued` or `processing`. When it becomes `completed`, the response includes structured findings:

```json
{
  "id": "rev_01J8Z7K3F2ACM9P4T6QX",
  "status": "completed",
  "createdAt": "2026-08-11T08:00:00Z",
  "completedAt": "2026-08-11T08:00:03Z",
  "findings": [
    {
      "id": "find_01J8Z8AC4G7N2M5Q9R3B",
      "check": "clarity",
      "severity": "high",
      "message": "The phrase \"user stuff\" does not identify the resource.",
      "suggestion": "Name the resource returned by the endpoint.",
      "requiresHumanReview": true
    }
  ]
}
```

## 3. Evaluate the findings

Treat each finding as a recommendation. A technical writer must evaluate the message and suggestion before changing or publishing the source documentation.

## Next steps

- See [Create a review job](endpoints/create-review.md) for request-field details.
- See [Retrieve a review job](endpoints/get-review.md) for statuses and result fields.
- Authentication and detailed error recovery will be expanded in Week 4.
