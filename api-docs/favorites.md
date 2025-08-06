# Favorites API

## Overview
- Mark/unmark tracks, albums, artists as favorites.
- List and manage favorites.

## Endpoints

### GET `/favorites`
List all favorites.

### POST `/favorites`
Add an item to favorites.

**Request:**
```json
{
  "type": "track|album|artist",
  "id": "string"
}
```

### DELETE `/favorites/{type}/{id}`
Remove an item from favorites.

## Error Cases
- No favorites: 204 No Content
- Removed items: 410 Gone

## Developer Notes
- Store favorites persistently (local or NAS sync).
- Provide real-time updates across views. 