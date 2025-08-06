# Playback Control API

## Overview
- Play, pause, skip, seek, shuffle, repeat.
- Now playing queue management.
- Volume and background/lock screen support.

## Endpoints

### POST `/playback/play`
Start playback of a track, album, or playlist.

**Request:**
```json
{
  "trackId": "string" // or albumId, playlistId
}
```

### POST `/playback/pause`
Pause playback.

### POST `/playback/skip`
Skip to next/previous track.

**Request:**
```json
{
  "direction": "next|previous"
}
```

### POST `/playback/seek`
Seek to a position in the current track.

**Request:**
```json
{
  "position": 120 // seconds
}
```

### GET `/playback/now-playing`
Get current track and queue info.

**Response:**
```json
{
  "track": { ... },
  "queue": [ ... ],
  "position": 120,
  "isPlaying": true
}
```

### POST `/playback/queue`
Update the now playing queue (reorder, add, remove).

### POST `/playback/volume`
Set playback volume.

**Request:**
```json
{
  "volume": 0.5 // 0.0 - 1.0
}
```

## Error Cases
- Playback failure: 422 Unprocessable Entity
- Network interruptions: 503 Service Unavailable

## Developer Notes
- Use platform-native audio APIs for background/lock screen.
- Synchronize playback state across all control surfaces. 