# REST API Guide

## Overview

The Example Configuration API provides REST endpoints for creating, retrieving, updating, and deleting application configuration resources.

**Base URL**

```text
https://api.example.com/v1
```

## Authentication

Requests require an access token.

```http
Authorization: Bearer <access-token>
```

Do not include access tokens in source code, screenshots, or publicly shared examples.

## Get a configuration

```http
GET /configurations/{configurationId}
```

### Path parameter

| Parameter | Type | Required | Description |
|---|---|---|---|
| `configurationId` | string | Yes | Unique identifier of the configuration. |

### Example request

```bash
curl -X GET "https://api.example.com/v1/configurations/cfg-12345"   -H "Authorization: Bearer <access-token>"
```

### Example response

```json
{
  "id": "cfg-12345",
  "name": "production",
  "status": "active"
}
```

## Response codes

| Code | Meaning | Description |
|---|---|---|
| `200` | OK | The request completed successfully. |
| `400` | Bad Request | The request contains invalid input. |
| `401` | Unauthorized | Authentication is missing or invalid. |
| `404` | Not Found | The requested resource does not exist. |
| `500` | Internal Server Error | The server encountered an unexpected condition. |

## Error handling

When a request fails, inspect the HTTP status code and error response before retrying the request.

Example:

```json
{
  "error": {
    "code": "INVALID_PARAMETER",
    "message": "The configurationId value is invalid."
  }
}
```

## Documentation considerations

API documentation should provide enough information for a developer to understand:

1. What the endpoint does.
2. Which inputs are required.
3. How to authenticate.
4. What a successful response looks like.
5. Which errors can occur.
6. How the endpoint can be tested.
