# User Journey 07: Favorites

## Conceptual Image
A favorites screen with a white background and a grid of cards for favorite tracks, albums, and artists. Each card has a heart icon in green at the top right. Album art and artist images are rounded with a blue border. The “Favorites” title is in green, and empty state shows a light blue heart illustration.

## Overview
This journey describes how a user marks tracks, albums, or artists as favorites for quick access, and how they interact with their favorites list.

---

## Step-by-Step Flow
1. **Mark as Favorite**
   - User taps a heart/star icon on a track, album, or artist to add it to favorites.
2. **Access Favorites**
   - User navigates to the 'Favorites' section from the library or main menu.
3. **View Favorites**
   - User sees a list of all favorited tracks, albums, and artists, grouped by type.
4. **Play from Favorites**
   - User selects a favorite item to start playback or view details.
5. **Remove from Favorites**
   - User taps the heart/star icon again to remove an item from favorites.

---

## Edge Cases & Error Handling
- **No Favorites:**
  - Show a friendly message if the favorites list is empty.
- **Removed Items:**
  - Handle gracefully if a favorited item is deleted from the library (e.g., show as unavailable or remove from favorites).

---

## Developer Notes
- Store favorites persistently (local storage or synced with NAS if supported).
- Ensure favorites are updated in real-time across all views.
- Provide clear visual feedback when adding/removing favorites.
- Modularize favorites logic for future enhancements (e.g., smart favorites, recommendations). 