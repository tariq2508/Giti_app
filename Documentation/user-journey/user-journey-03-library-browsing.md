# User Journey 03: Library Browsing

## Conceptual Image
A tabbed interface with “Folders”, “Artists”, “Albums”, “Genres”, and “Playlists” tabs at the top, highlighted in blue. The main area shows a grid of album cards with album art (rounded corners, subtle shadow), album title, and artist name. The background is white, with plenty of white space. The app bar is light blue with a search icon.

## Overview
This journey describes how a user navigates and explores their music library after successful authentication and NAS connection. The user can browse by folder, artist, album, genre, or playlist.

---

## Step-by-Step Flow
1. **Library Home**
   - User lands on the main library screen after login.
   - Library is organized into tabs or sections: Folders, Artists, Albums, Genres, Playlists, Favorites.
2. **Folder Browsing**
   - User selects the 'Folders' tab to view the directory structure as on the NAS.
   - User navigates through folders to find music files.
3. **Artist/Album/Genre Browsing**
   - User selects 'Artists', 'Albums', or 'Genres' to view categorized lists generated from local tags.
   - User can tap into any artist/album/genre to see associated tracks.
4. **Playlist Browsing**
   - User selects 'Playlists' to view and manage their playlists.
5. **Favorites**
   - User selects 'Favorites' to quickly access marked tracks, albums, or artists.
6. **Track Selection**
   - User taps a track to start playback or view details.

---

## Edge Cases & Error Handling
- **Empty Library:**
  - Show a friendly message if no music is found in the selected folders.
- **Corrupt/Unreadable Files:**
  - Skip and optionally notify user if a file cannot be read or indexed.
- **Slow Loading:**
  - Use loading indicators and consider lazy loading for large libraries.
- **Tag Parsing Errors:**
  - Handle missing or malformed metadata gracefully (e.g., show 'Unknown Artist').

---

## Developer Notes
- Index and cache library data for fast navigation.
- Use efficient data structures for large libraries.
- Modularize views for each browsing mode (folders, artists, etc.).
- Support sorting and filtering in each view.
- Ensure UI is responsive and accessible.
- Log errors for debugging but do not expose technical details to users. 