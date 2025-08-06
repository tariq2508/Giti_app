# User Journey 05: Playback Control

## Conceptual Image
A “Now Playing” screen with a large album art image (rounded corners, subtle shadow) centered on a white background. Below, track title and artist in dark text. Playback controls (play, pause, skip, shuffle, repeat) are circular buttons with green and blue accents. The progress bar is a thin green line. The background has a faint blue gradient at the top.

## Overview
This journey describes how a user interacts with playback controls to listen to music, including play, pause, skip, seek, shuffle, repeat, and using lock screen or car integrations.

---

## Step-by-Step Flow
1. **Start Playback**
   - User selects a track, album, or playlist to play from the library or search results.
   - Playback screen displays current track info (title, artist, album art, progress bar).
2. **Playback Controls**
   - User can play, pause, skip forward/back, seek within a track, shuffle, or repeat.
   - Controls are accessible from the main app UI, lock screen, notification shade, and CarPlay/Android Auto.
3. **Now Playing Queue**
   - User can view and reorder the current play queue.
4. **Track Details**
   - User can view detailed info about the current track (metadata, file info).
5. **Volume Control**
   - User adjusts volume via in-app slider or system controls.
6. **Background & Lock Screen**
   - Playback continues when app is minimized or device is locked.
   - User can control playback from lock screen or car interface.

---

## Edge Cases & Error Handling
- **Playback Failure:**
  - Show error if file cannot be played (unsupported format, network issue).
  - Skip to next track or retry as appropriate.
- **Network Interruptions:**
  - Buffer and auto-reconnect if connection drops.
  - Notify user if playback cannot resume.
- **Unsupported Controls:**
  - Gracefully disable controls not supported on certain platforms (e.g., seek on some car interfaces).

---

## Developer Notes
- Use platform-native audio APIs for background and lock screen support.
- Ensure playback state is synchronized across all control surfaces (app, lock screen, car).
- Handle audio focus and interruptions (e.g., phone calls, other apps).
- Log playback errors for debugging.
- Modularize playback logic for future enhancements (gapless, crossfade, etc.). 