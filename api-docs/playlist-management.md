# Playlist Management API

## Overview
- Create, edit, delete playlists.
- Add/remove/reorder tracks.

## Endpoints

### GET `/playlists`
List all playlists.

### POST `/playlists`
Create a new playlist.

**Request:**
```json
{
  "name": "string"
}
```

### PUT `/playlists/{id}`
Edit playlist name or reorder tracks.

### POST `/playlists/{id}/tracks`
Add tracks to a playlist.

**Request:**
```json
{
  "trackIds": ["string", ...]
}
```

### DELETE `/playlists/{id}/tracks/{trackId}`
Remove a track from a playlist.

### DELETE `/playlists/{id}`
Delete a playlist.

## Error Cases
- Duplicate names: 409 Conflict
- Track not found: 404 Not Found
- Delete confirmation: 200 OK with confirmation required

## Developer Notes
- Store playlists persistently (local or NAS sync).
- Support drag-and-drop or swipe for reordering. 