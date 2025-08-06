# Settings & Preferences API

## Overview
- Get/set user preferences (theme, streaming quality, notifications).
- Reset to defaults.

## Endpoints

### GET `/settings`
Get current user preferences.

### PUT `/settings`
Update user preferences.

**Request:**
```json
{
  "theme": "light|dark|system",
  "streamingQuality": "auto|high|medium|low",
  "notifications": true
}
```

### POST `/settings/reset`
Reset preferences to default values.

## Error Cases
- Invalid input: 400 Bad Request
- Save failure: 500 Internal Server Error

## Developer Notes
- Store preferences persistently (local or cloud sync).
- Modularize for easy addition of new options. 