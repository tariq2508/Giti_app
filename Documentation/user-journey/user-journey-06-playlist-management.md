# User Journey 06: Playlist Management

## Conceptual Image
A playlist screen with a white background. At the top, a blue “Create Playlist” button. Below, a list of playlists, each in a card with a green accent bar on the left. Inside each playlist, tracks are listed with drag handles (light blue), and a green “Add Track” button at the bottom. The UI is clean, with rounded corners and subtle shadows.

## Overview
This journey describes how a user creates, edits, and deletes playlists, and adds or removes tracks from playlists within their music library.

---

## Step-by-Step Flow
1. **Access Playlists**
   - User navigates to the 'Playlists' section from the library.
2. **Create Playlist**
   - User taps 'Create Playlist', enters a name, and saves.
3. **Add Tracks**
   - User browses library or search results, selects tracks, and adds them to a playlist.
4. **Edit Playlist**
   - User opens a playlist, can rename or reorder tracks.
5. **Remove Tracks**
   - User removes tracks from a playlist via edit mode or swipe action.
6. **Delete Playlist**
   - User deletes a playlist with confirmation prompt.

---

## Edge Cases & Error Handling
- **Duplicate Names:**
  - Prevent or warn about duplicate playlist names.
- **Empty Playlist:**
  - Show message if playlist has no tracks.
- **Track Not Found:**
  - Handle gracefully if a track is removed from the library but still in a playlist.
- **Delete Confirmation:**
  - Always confirm before deleting a playlist.

---

## Developer Notes
- Store playlists persistently (local storage or synced with NAS if supported).
- Support drag-and-drop or swipe for reordering/removing tracks.
- Modularize playlist logic for future enhancements (smart playlists, sharing).
- Ensure UI is responsive and provides clear feedback for all actions. 