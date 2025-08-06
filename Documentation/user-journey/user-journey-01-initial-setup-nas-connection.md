# User Journey 01: Initial Setup & NAS Connection

## Conceptual Image
A mobile screen with a white background and a centered card. The card has rounded corners and a subtle blue shadow. At the top, a friendly illustration of a NAS device with a green checkmark. Below, input fields for NAS address, username, and password, styled with light gray backgrounds and blue borders. A large green “Connect” button sits at the bottom. The app bar is light blue with the title “Connect to NAS”.

## Overview
This journey covers the process by which a new user installs the app and connects it to their Synology NAS using the SMB protocol. This is the first step required to access and stream music.

---

## Step-by-Step Flow
1. **App Installation**
   - User downloads and installs the app from the App Store or Google Play.
2. **Launch & Welcome**
   - User opens the app and is greeted with a welcome screen.
   - Option to start setup or view help/documentation.
3. **Manual NAS Connection**
   - User is prompted to enter NAS connection details:
     - NAS IP address or hostname
     - SMB share name
     - Username and password
     - (Optional) Port number
   - User can test the connection before saving.
4. **Folder Selection**
   - Upon successful connection, user is shown a list of available folders/shares.
   - User selects one or more folders to index for music.
5. **Save & Proceed**
   - Connection details and folder selections are saved securely on the device.
   - User proceeds to authentication/login (if required).

---

## Edge Cases & Error Handling
- **Invalid Credentials:**
  - Show clear error if username/password is incorrect.
  - Allow user to retry or reset credentials.
- **Network Issues:**
  - Handle timeouts, unreachable NAS, or incorrect IP gracefully.
  - Provide troubleshooting tips (e.g., check WiFi, firewall, NAS status).
- **Unsupported NAS/Protocol:**
  - Inform user if the NAS does not support SMB or is incompatible.
- **No Folders Found:**
  - Show message and allow user to re-enter connection details or try a different share.
- **Duplicate Connections:**
  - Prevent saving duplicate NAS/server entries.

---

## Developer Notes
- Store credentials securely (use Keychain/Keystore).
- Validate all user input before attempting connection.
- Use async operations for network calls; provide loading indicators.
- Modularize connection logic for future protocol support (e.g., WebDAV, SFTP).
- Log connection attempts and errors for debugging (do not log sensitive info).
- Ensure UI is responsive to both success and failure states. 