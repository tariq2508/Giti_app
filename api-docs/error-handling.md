# Error Handling & Recovery

## Overview
- Centralized error response format.
- Common error codes and messages.
- Recovery and retry strategies.

## Error Response Format
```json
{
  "error": {
    "code": 401,
    "message": "Invalid credentials"
  }
}
```

## Common Error Codes
| Code | Message                  | Description                        |
|------|--------------------------|------------------------------------|
| 400  | Bad Request              | Invalid input or parameters        |
| 401  | Unauthorized             | Invalid credentials/session        |
| 403  | Forbidden                | Insufficient permissions           |
| 404  | Not Found                | Resource not found                 |
| 409  | Conflict                 | Duplicate or conflicting resource  |
| 410  | Gone                     | Resource removed                   |
| 422  | Unprocessable Entity     | Corrupt/unreadable file            |
| 423  | Locked                   | Account locked                     |
| 500  | Internal Server Error    | Unexpected server error            |
| 503  | Service Unavailable      | Network/server unavailable         |
| 504  | Gateway Timeout          | Operation timed out                |

## Recovery Strategies
- Retry on network errors.
- Provide actionable error messages to users.
- Log errors for debugging (no sensitive info).

## Developer Notes
- Centralize error handling logic for consistency.
- Use user-friendly language in all error messages.
- Provide actionable recovery steps for each error type.
- Log all errors with sufficient context (but no sensitive info).
- Ensure UI remains responsive during error states and recovery attempts. 