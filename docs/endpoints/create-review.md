# Create a review job

Creates an asynchronous job that evaluates API-documentation content against selected quality checks.

```http
POST /reviews
```

## Request headers

| Header | Required | Description |
| --- | --- | --- |
| `Content-Type` | Yes | Must be `application/json`. |
| `X-API-Key` | Yes | API key used to authenticate the request. |

## Request body

| Property | Type | Required | Description |
| --- | --- | --- | --- |
| `content` | string | Yes | API-documentation text to review; minimum 20 characters. |
| `contentType` | string | Yes | Documentation type: `endpoint-description`, `tutorial`, or `error-message`. |
| `checks` | array of strings | Yes | One or more unique checks: `clarity`, `terminology`, `examples`, or `completeness`. |

## Example request

```json
{
  "content": "The endpoint gets user stuff and returns it.",
  "contentType": "endpoint-description",
  "checks": ["clarity", "terminology", "examples"]
}
```

## Example response

The API returns `202 Accepted` and a queued review job:

```json
{
  "id": "rev_01J8Z7K3F2ACM9P4T6QX",
  "status": "queued",
  "createdAt": "2026-08-11T08:00:00Z"
}
```

Use the returned `id` with `GET /reviews/{reviewId}` to retrieve the result.

## Errors

| Status | Meaning |
| --- | --- |
| `400` | The request body is invalid. |
| `401` | The API key is missing or invalid. |

Detailed error recovery guidance will be added in Week 4.
