# Library Browsing API

## Overview
- Browse by folder, artist, album, genre, playlist, favorites.
- Metadata extraction from audio tags.

## Endpoints

### GET `/library/folders`
List folders and files in the selected NAS directory.

**Response:**
```json
[
  {
    "name": "string",
    "type": "folder|file",
    "path": "string"
  }
]
```

### GET `/library/artists`
List all artists.

### GET `/library/albums`
List all albums.

### GET `/library/genres`
List all genres.

### GET `/library/playlists`
List all playlists.

### GET `/library/favorites`
List all favorite items.

### GET `/library/tracks?filter=...`
List tracks, optionally filtered by artist, album, genre, or folder.

**Response:**
```json
[
  {
    "id": "string",
    "title": "string",
    "artist": "string",
    "album": "string",
    "genre": "string",
    "duration": 240,
    "path": "string",
    "artwork": "url"
  }
]
```

## Error Cases
- Empty library: 204 No Content
- Corrupt/unreadable files: 422 Unprocessable Entity
- Tag parsing errors: 206 Partial Content

## Developer Notes
- Index and cache library data for fast navigation.
- Support sorting and filtering. 