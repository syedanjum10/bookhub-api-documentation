# Error Handling

## Overview

The BookHub API uses standard HTTP status codes to indicate whether an API request was successful or resulted in an error.

When an error occurs, the API returns a JSON response containing an error code and a message that describes the problem.

## HTTP Status Codes

| Status Code | Meaning | Description |
|---|---|---|
| 200 | OK | The request was successful. |
| 201 | Created | A new resource was successfully created. |
| 400 | Bad Request | The request contains invalid or missing parameters. |
| 401 | Unauthorized | Authentication is required or the access token is invalid. |
| 403 | Forbidden | The authenticated client does not have permission to perform the requested action. |
| 404 | Not Found | The requested resource could not be found. |
| 429 | Too Many Requests | The client has exceeded the API rate limit. |
| 500 | Internal Server Error | An unexpected error occurred on the server. |

## Error Response

When an API request fails, the BookHub API returns an error response in JSON format.

### Example Error Response

```json
{
    "error": {
        "code": "BOOK_NOT_FOUND",
        "message": "The requested book could not be found."
    }
}

## Common Errors

### 404 Bad Request
The server cannot process the request because the request contains invalid or missing information.

</JSON>
{
    "error": {
        "code": "INVALID_REQUEST",
        "message": "The request contains invalid parameters."
    }
}

### 401 Unauthorized
The request requires a valid access token.

```json
{
  "error": {
    "code": "UNAUTHORIZED",
    "message": "A valid access token is required."
  }
}
```

### 404 Not Found
The requested resourse does not exist.

```json
{
    "error":{
        "code": "BOOK_NOT_FOUND",
        "message": "The requested book could not be found."
    }
}
```

### 500 Internal Server Error
An unexpected error occured while processing the request

```json
{
  "error": {
    "code": "INTERNAL_SERVER_ERROR",
    "message": "An unexpected error occurred. Please try again later."
  }
}