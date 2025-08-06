# User Journey 02: Authentication/Login

## Conceptual Image
A clean login screen with a white background. The login form is centered in a rounded card with a soft shadow. Input fields for username and password use the light gray background and blue border. The “Login” button is green, and a subtle blue link for “Forgot password?” is below. The app logo (a music note in green and blue) is at the top.

## Overview
This journey describes how a user authenticates with their NAS using local credentials to access their music library. Authentication is required for secure access to user-specific folders.

---

## Step-by-Step Flow
1. **Prompt for Credentials**
   - After NAS connection setup, user is prompted to enter their NAS username and password (if not already provided).
2. **Credential Submission**
   - User submits credentials via a secure form.
3. **Authentication Request**
   - App sends credentials to the NAS over a secure (HTTPS) connection.
4. **Authentication Success**
   - User is granted access to their music library and redirected to the main library screen.
5. **Session Management**
   - App securely stores session/token for future requests (if supported by NAS).

---

## Edge Cases & Error Handling
- **Invalid Credentials:**
  - Show error and allow user to retry.
  - Option to reset or re-enter credentials.
- **Account Lockout:**
  - Inform user if account is locked due to too many failed attempts.
- **Network/Server Errors:**
  - Handle timeouts, server unavailability, or protocol errors.
- **Session Expiry:**
  - Prompt user to re-authenticate if session/token expires.

---

## Developer Notes
- Use secure storage for credentials and tokens (Keychain/Keystore).
- Never log or expose passwords in logs or UI.
- Support session persistence and auto-login where possible.
- Modularize authentication logic for future OAuth or multi-factor support.
- Provide clear feedback for all authentication states. 