# NAS/Connection Management API

## Overview
- Add, edit, remove, and list NAS/server connections.
- Test connection before saving.
- Folder selection for music indexing.

## Endpoints

### GET `/connections`
List all saved NAS/server connections.

**Response:**
```json
[
  {
    "id": "string",
    "name": "string",
    "address": "string",
    "status": "connected|disconnected|error"
  }
]
```

### POST `/connections`
Add a new NAS/server connection.

**Request:**
```json
{
  "name": "string",
  "address": "string",
  "username": "string",
  "password": "string",
  "port": 445,
  "protocol": "SMB"
}
```
**Response:**
```json
{
  "id": "string",
  "status": "connected|error",
  "folders": ["Music", "Shared"]
}
```

### PUT `/connections/{id}`
Edit an existing NAS/server connection.

### DELETE `/connections/{id}`
Remove a NAS/server connection.

### POST `/connections/test`
Test NAS/server connection details before saving.

**Request:**
```json
{
  "address": "string",
  "username": "string",
  "password": "string",
  "port": 445,
  "protocol": "SMB"
}
```
**Response:**
```json
{
  "success": true,
  "folders": ["Music", "Shared"]
}
```

## Error Cases
- Duplicate connections: 409 Conflict
- Invalid/unreachable NAS: 400 Bad Request / 503 Service Unavailable
- No folders found: 404 Not Found

## Developer Notes
- Store credentials securely.
- Validate all user input.
- Modularize for future protocol support. 