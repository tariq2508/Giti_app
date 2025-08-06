# Technical Stack for Personal Music Streamer App

This document outlines the detailed technology stack required to build the cross-platform music streamer app for iOS, Android, and Web using React Native JS. All recommended technologies are open source and free. This guide is intended to help developers understand, select, and integrate the core technologies and tools for the project.

---

## 1. Frontend (Mobile & Web)

### Framework
- **React Native JS** (MIT)
  - Core framework for building cross-platform mobile apps (iOS, Android)
  - Enables code sharing with React for Web
- **Expo** (MIT, optional)
  - Simplifies development, especially for prototyping and rapid iteration
  - Consider ejecting for advanced native module support
- **React (Web)** (MIT)
  - For web version, using React with React Native Web for code sharing

### UI Libraries
- **React Navigation** (MIT): Navigation and routing for React Native apps
- **React Native Paper** (MIT) or **NativeBase** (MIT): Prebuilt UI components
- **Styled Components** (MIT) or **Emotion** (MIT): CSS-in-JS styling
- **React Native Vector Icons** (MIT): Icon support
- **React Native Safe Area Context** (MIT): Safe area handling for notched devices

### State Management
- **Redux Toolkit** (MIT) or **Zustand** (MIT): Global state management
- **React Context API**: For lightweight state sharing

### Forms & Validation
- **Formik** (MIT) or **React Hook Form** (MIT): Form management
- **Yup** (MIT): Schema validation

### Theming & Accessibility
- **React Native Appearance** (MIT): Dark/light mode support
- **React Native Accessibility**: Accessibility helpers

---

## 2. Media Streaming & Playback

### Audio Playback
- **react-native-track-player** (MIT)
  - Advanced audio playback, background mode, lock screen controls, queue management
  - Supports iOS, Android, and (with limitations) Web
- **react-native-sound** (MIT): Simple audio playback (fallback)
- **react-native-music-control** (MIT): Integrate with system media controls (lock screen, notification shade, CarPlay, Android Auto)

### Streaming Protocols
- **HTTP/HTTPS Streaming**: Core protocol for streaming audio from NAS/server
- **SMB (Samba) Client**
  - **react-native-smb** (MIT, community module) or native bridge for SMB access
  - For direct file access from Synology and other SMB-compatible NAS
- **Buffering & Adaptive Streaming**: Custom logic for smooth playback over varying network conditions

---

## 3. Backend (Optional/Future Enhancements)
The core app is designed to connect directly to the user's NAS (e.g., Synology) and does not require a centralized backend for streaming or authentication. However, if you wish to add features such as user profiles, analytics, push notifications, or remote management, consider the following open source and free backend technologies:

- **Node.js** (MIT): JavaScript runtime for building backend services
- **Express.js** (MIT): Minimalist web framework for Node.js
- **Fastify** (MIT): Fast and low overhead web framework for Node.js
- **Socket.IO** (MIT): Real-time communication (if needed)
- **Strapi** (MIT): Headless CMS for user/content management
- **Hasura** (Apache 2.0): Instant GraphQL on PostgreSQL
- **Nginx** (BSD): Reverse proxy, load balancer, and static file server

---

## 4. Database (Optional/Future Enhancements)
No database is required for the core app, as all music and metadata are stored on the user's NAS. If you add a backend, consider these open source and free databases:

- **PostgreSQL** (PostgreSQL License): Advanced open source relational database
- **SQLite** (Public Domain): Lightweight, file-based database (good for local/offline use)
- **MongoDB Community Edition** (Server Side Public License): NoSQL document database
- **Redis** (BSD): In-memory data store for caching and sessions

---

## 5. Server/Deployment (Optional/Future Enhancements)
If you deploy a backend or web dashboard, use these open source and free tools:

- **Docker** (Apache 2.0): Containerization for consistent deployment
- **Docker Compose** (Apache 2.0): Multi-container orchestration
- **Nginx** (BSD): Web server and reverse proxy
- **Caddy** (Apache 2.0): Automatic HTTPS web server
- **Certbot** (Apache 2.0): Free SSL certificates via Let's Encrypt
- **GitHub Actions** (MIT): CI/CD for automated testing and deployment
- **Netlify** (MIT) or **Vercel** (MIT): Free hosting for static web apps

---

## 6. NAS/Server Integration

### NAS/Server Protocols
- **SMB (Samba)** (GPLv3): Primary protocol for Synology and most NAS devices
- **WebDAV, SFTP, FTP**: Consider for future support (modularize integration)

### File Indexing & Metadata
- **ID3/Audio Tag Parsing**
  - **music-metadata** (MIT, JS library) for reading local tags from audio files
- **Custom Indexing Logic**: For scanning folders, building library structure, and caching metadata

### Security
- **HTTPS/TLS**: Secure all connections to NAS/server
- **Keychain/Keystore**: Secure storage for credentials on device

---

## 7. Authentication & User Management
- **Local Authentication**: Username/password for NAS/server
- **React Native Keychain** (MIT): Secure credential storage
- **Session Management**: Token or session-based, depending on NAS capabilities
- **(Future) OAuth2**: For cloud or third-party login

---

## 8. Networking
- **Axios** (MIT) or **Fetch API**: HTTP requests
- **react-native-background-fetch** (MIT): For background tasks (e.g., library sync)
- **react-native-netinfo** (MIT): Network status monitoring
- **Dynamic DNS/Port Forwarding**: User guidance for remote access

---

## 9. Platform-Specific Modules
- **react-native-device-info** (MIT): Device and OS info
- **react-native-permissions** (MIT): Runtime permissions (storage, network)
- **react-native-file-access** (MIT): File system access
- **react-native-background-actions** (MIT): For background playback and tasks
- **CarPlay/Android Auto Integration**: Via `react-native-music-control` and native modules

---

## 10. Development Tools
- **TypeScript** (Apache 2.0): Strong typing for maintainable code
- **ESLint & Prettier** (MIT): Code linting and formatting
- **Jest** (MIT): Unit testing
- **React Native Testing Library** (MIT): Component testing
- **Detox** (MIT): End-to-end testing for React Native
- **Storybook** (MIT): UI component development and documentation

---

## 11. CI/CD & Deployment
- **GitHub Actions** (MIT): Automated testing, linting, and build pipelines
- **Expo Application Services (EAS)** (MIT): For building and deploying to app stores (if using Expo)
- **Fastlane** (MIT): Automate app store deployment (iOS/Android)
- **CodePush** (MIT): Over-the-air updates for React Native

---

## 12. Documentation
- **Markdown**: For PRD, user journeys, and developer docs
- **Typedoc** (Apache 2.0): For generating API documentation from TypeScript
- **README.md**: Project overview and setup instructions

---

## 13. Future Enhancements & Considerations
- **WebDAV, SFTP, FTP**: Additional NAS protocols
- **Offline Caching**: Local storage for offline playback
- **Metadata Fetching**: Integrate with MusicBrainz, Last.fm, or similar for album art and info
- **OAuth2 & Social Login**: For enhanced authentication
- **Accessibility**: Advanced support for screen readers, large text, etc.
- **Smart Home Integrations**: Chromecast, AirPlay, etc.
- **Analytics**: Privacy-focused usage analytics (optional)

---

## 14. References
- [react-native-track-player](https://github.com/DoubleSymmetry/react-native-track-player)
- [react-native-smb](https://github.com/PeelTechnologies/react-native-smb)
- [music-metadata](https://github.com/Borewit/music-metadata)
- [react-native-music-control](https://github.com/tanguyantoine/react-native-music-control)
- [React Native Paper](https://callstack.github.io/react-native-paper/)
- [Redux Toolkit](https://redux-toolkit.js.org/)
- [Expo](https://expo.dev/)
- [Node.js](https://nodejs.org/)
- [Express.js](https://expressjs.com/)
- [PostgreSQL](https://www.postgresql.org/)
- [Docker](https://www.docker.com/) 