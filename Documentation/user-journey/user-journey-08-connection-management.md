# User Journey 08: Connection Management

## Conceptual Image
A settings screen with a section titled “Connections” in blue. Each NAS/server connection is shown as a card with a green NAS icon, server name, and status (green check or red warning). “Add Connection” is a green button at the bottom. Cards have rounded corners and subtle blue shadows.

## Overview
This journey describes how a user manages their NAS/server connections, including adding, editing, and removing connections.

---

## Step-by-Step Flow
1. **Access Connection Settings**
   - User navigates to the 'Connections' or 'Settings' section.
2. **Add New Connection**
   - User taps 'Add Connection', enters NAS/server details, and saves.
   - App tests the connection before saving.
3. **Edit Connection**
   - User selects an existing connection to edit details (e.g., IP, credentials, folders).
   - App tests the updated connection before saving changes.
4. **Remove Connection**
   - User deletes a connection with confirmation prompt.
5. **Switch Connection**
   - User can switch between multiple saved connections.

---

## Edge Cases & Error Handling
- **Duplicate Connections:**
  - Prevent saving connections with duplicate details.
- **Invalid Details:**
  - Show errors for invalid or unreachable NAS/server details.
- **Connection Removal:**
  - Confirm before deleting a connection; handle active sessions gracefully.

---

## Developer Notes
- Store connection details securely (Keychain/Keystore).
- Modularize connection logic for future protocol support.
- Provide clear feedback for all connection actions.
- Ensure UI is responsive and handles errors gracefully. 