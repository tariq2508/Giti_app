# User Journey 04: Search

## Conceptual Image
A search screen with a prominent search bar at the top (rounded, light gray background, blue border). Below, search results are grouped by type (tracks, albums, artists) in separate sections. Each result is displayed in a card with a green highlight for the search term. The background is white, and the “No results” state shows a friendly illustration with a blue music note.

## Overview
This journey describes how a user searches for specific tracks, albums, or artists within their music library. Search helps users quickly find and play desired content.

---

## Step-by-Step Flow
1. **Access Search**
   - User taps the search icon or navigates to the search tab from the library screen.
2. **Enter Query**
   - User types a keyword (track, album, artist, or folder name) into the search bar.
3. **View Results**
   - App displays matching results grouped by type (tracks, albums, artists, folders, playlists).
   - Results update in real-time as the user types.
4. **Select Result**
   - User taps a result to view details or start playback.
5. **Clear Search**
   - User can clear the search bar to return to the full library view.

---

## Edge Cases & Error Handling
- **No Results:**
  - Show a friendly message if no matches are found.
- **Slow Search:**
  - Use loading indicators for large libraries or slow devices.
- **Special Characters:**
  - Handle queries with special characters or case insensitivity.

---

## Developer Notes
- Index library data for fast search (consider fuzzy search for typos).
- Optimize search for large libraries (debounce input, async queries).
- Group and highlight results by type.
- Ensure search is accessible from all main screens.
- Log search errors for debugging but do not expose technical details to users. 