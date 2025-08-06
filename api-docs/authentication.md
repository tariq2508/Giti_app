# Authentication API

## Overview
- Local authentication using NAS/server credentials (username/password).
- Session/token management for persistent login.
- Secure credential storage (Keychain/Keystore).

## Endpoints

### POST `/auth/login`
Authenticate user with NAS credentials.

**Request:**
```json
{
  "username": "string",
  "password": "string",
  "nasId": "string"
}
```
**Response (Success):**
```json
{
  "token": "string",
  "user": {
    "username": "string",
    "displayName": "string"
  }
}
```
**Response (Error):**
```json
{
  "error": "Invalid credentials"
}
```

### POST `/auth/logout`
Invalidate the current session/token.

**Request:**
```json
{
  "token": "string"
}
```
**Response:**
```json
{
  "success": true
}
```

### GET `/auth/session`
Check if the current session/token is valid.

**Request Header:**
```
Authorization: Bearer <token>
```
**Response (Valid):**
```json
{
  "valid": true,
  "user": { ... }
}
```
**Response (Invalid):**
```json
{
  "valid": false
}
```

## Error Cases
- Invalid credentials: 401 Unauthorized
- Session expired: 401 Unauthorized
- Account lockout: 423 Locked
- Network/server errors: 503 Service Unavailable

## Developer Notes
- Never log or expose passwords.
- Use secure storage for tokens and credentials.
- Support session persistence and auto-login where possible.
- Modularize for future OAuth or multi-factor support. 