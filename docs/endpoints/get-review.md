# Retrieve a review job

Retrieves the status and available results of an existing documentation-review job.

```http
GET /reviews/{reviewId}
```

## Path parameter

| Parameter | Type | Required | Description |
| --- | --- | --- | --- |
| `reviewId` | string | Yes | Review job ID returned by `POST /reviews`. It begins with `rev_`. |

## Status values

| Status | Meaning |
| --- | --- |
| `queued` | The job is waiting to be processed. |
| `processing` | The review is in progress. |
| `completed` | Processing finished and findings are available. |
| `failed` | Processing could not be completed. |

## Completed response fields

| Property | Type | Description |
| --- | --- | --- |
| `id` | string | Unique review job ID. |
| `status` | string | Current processing state. |
| `createdAt` | string | Date and time the job was created in ISO 8601 format. |
| `completedAt` | string | Date and time processing finished in ISO 8601 format. |
| `findings` | array | Structured recommendations returned by the review. |

Each finding includes an ID, check type, severity, message, suggested revision, and `requiresHumanReview` value. A finding is advisory and does not automatically change documentation.

## Example completed response

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

## Errors

| Status | Meaning |
| --- | --- |
| `401` | The API key is missing or invalid. |
| `404` | No review job exists for the supplied ID. |

Detailed error recovery guidance will be added in Week 4.
