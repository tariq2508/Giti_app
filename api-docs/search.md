# Search API

## Overview
- Search tracks, albums, artists, folders, playlists.
- Real-time, fuzzy, and grouped results.

## Endpoint

### GET `/search?q=...`

**Response:**
```json
{
  "tracks": [ ... ],
  "albums": [ ... ],
  "artists": [ ... ],
  "folders": [ ... ],
  "playlists": [ ... ]
}
```

## Error Cases
- No results: 204 No Content
- Slow search: 504 Gateway Timeout

## Developer Notes
- Index library data for fast search.
- Optimize for large libraries (debounce, async). 