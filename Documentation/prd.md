# Product Requirements Document (PRD)

## Product Title
**Personal Music Streamer App**

## Overview
A cross-platform music streaming application built with React Native JS, designed for iOS, Android, and Web. The app enables users to stream music directly from their personal server or NAS (with initial focus on Synology and SMB protocol), accessing user-specific folders over the internet (WiFi or mobile data). The app supports background and lock screen playback, providing a seamless listening experience across devices.

---

## Goals & Objectives
- **Universal Access:** Allow users to stream their personal music library from anywhere, on any device.
- **Privacy & Ownership:** Users retain full control over their music files, which are never uploaded to third-party servers.
- **Cross-Platform:** Consistent experience on iOS, Android, and Web.
- **Background/Lock Screen Playback:** Music continues playing when the app is minimized or the device is locked.
- **Open Source & Free:** The app will be open source and free to use.

---

## Target Platforms
- iOS (iPhone, iPad) — **priority for initial release**
- Android (phones, tablets)
- Web (modern browsers)

---

## Key Features (Phase 1)

### 1. **User Authentication & Setup**
- Local authentication (username/password)
- Add and manage multiple server/NAS connections (manual entry only in phase 1)
- User-specific folder selection and access permissions

### 2. **Media Streaming**
- Stream audio files (all common audio types: MP3, FLAC, AAC, WAV, etc.) from remote server/NAS (Synology, SMB protocol)
- Support for playlists, albums, artists, genres, and folder browsing
- Adaptive streaming for varying network conditions
- Caching/buffering for smooth playback

### 3. **Playback Experience**
- Play, pause, skip, seek, shuffle, repeat
- Display track metadata (title, artist, album, artwork) using local tags only
- Gapless playback (nice-to-have, not required for phase 1)
- Lock screen controls (play/pause, skip, artwork display)
- Background playback (audio continues when app is minimized or device is locked)
- Volume control (in-app and system integration)
- CarPlay and Android Auto support

### 4. **Library Management**
- Scan and index user folders on server/NAS
- Search and filter music library
- Create, edit, and delete playlists
- Favorite tracks, albums, and artists
- **No editing of metadata or playlists from the app in phase 1**

### 5. **Connectivity & Security**
- Secure connection to server/NAS (HTTPS is sufficient)
- Support for dynamic DNS and port forwarding
- Handle network interruptions gracefully (auto-reconnect, resume playback)
- User data privacy (no third-party data collection)

### 6. **Cross-Platform UI/UX**
- Responsive and adaptive design for all devices
- Consistent navigation and controls
- Dark/light mode support

### 7. **Notifications & Integration**
- Push/local notifications for playback, errors, or updates
- Integration with system media controls (lock screen, notification shade, Control Center)
- **No scrobbling or third-party integrations in phase 1**

---

## Non-Functional Requirements
- **Performance:** Low latency streaming, fast library browsing
- **Reliability:** Robust error handling, minimal crashes
- **Scalability:** Support for large music libraries
- **Maintainability:** Modular, well-documented codebase
- **Security:** End-to-end encryption for credentials and streams

---

## Technical Requirements
- **Frontend:** React Native JS (with Expo or bare workflow)
- **Backend:** User’s own server/NAS (initial focus: Synology, SMB protocol)
- **Streaming Protocols:** HTTP(s) streaming, adaptive bitrate if possible
- **Media Playback:** Use platform-native audio APIs for background/lock screen support (e.g., `react-native-track-player`)
- **Authentication:** Local authentication (username/password)
- **Networking:** Support for both local and remote (internet) connections
- **Minimum OS Versions:** Support devices released in the last 3-4 years (exact versions to be determined)

---

## User Stories
1. **As a user,** I want to connect my app to my Synology NAS using SMB so I can stream my music library from anywhere.
2. **As a user,** I want to browse my music by artist, album, genre, or folder.
3. **As a user,** I want to control playback from my lock screen or notification shade.
4. **As a user,** I want my music to keep playing when I lock my phone or switch apps.
5. **As a user,** I want to search and create playlists from my library.
6. **As a user,** I want my connection to be secure and private.
7. **As a user,** I want to use the app with CarPlay or Android Auto in my car.

---

## Success Metrics
- Successful connection and streaming from Synology NAS using SMB
- Smooth playback with minimal buffering on WiFi and mobile data
- Positive user feedback on cross-platform experience and lock screen controls
- No user data leaks or privacy issues
- Successful use of CarPlay and Android Auto features

---

## Out of Scope (Phase 1)
- Cloud music storage/streaming (e.g., Spotify, Apple Music)
- Video streaming
- Social features (sharing, comments)
- Metadata fetching from online sources
- Offline downloads/caching of tracks
- Setup wizard for first-time users
- OAuth or third-party authentication
- Editing metadata or playlists from the app
- Scrobbling or third-party integrations (e.g., Last.fm)

---

## Open Questions
- What is the minimum supported OS version for each platform?
- Are there any additional NAS/server types or protocols to support in future phases?
- What are the most important UI/UX features for initial users?

---

## Future Enhancements (Phase 2+)
- Support for additional NAS/server types and protocols (e.g., QNAP, TrueNAS, WebDAV, SFTP)
- OAuth and third-party authentication (Google, Apple, etc.)
- Setup wizard for first-time users
- Metadata fetching from online sources (album art, artist info)
- Offline downloads/caching of tracks with configurable limits
- Gapless playback as a required feature
- Editing metadata and playlists from the app
- Accessibility features (screen reader, large text, etc.)
- Scrobbling and integration with third-party services (e.g., Last.fm)
- Additional integrations (e.g., Chromecast, smart home)
- Web app enhancements

---

## Appendix
- Example NAS: Synology (priority), QNAP, TrueNAS (future)
- Example protocols: SMB (priority), WebDAV, SFTP (future)
- Example libraries: `react-native-track-player`, `react-native-sound`, `react-native-music-control`
- Open source license: To be determined
