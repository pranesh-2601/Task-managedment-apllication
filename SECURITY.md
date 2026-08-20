# Security

## Current prototype limitations

This project is a browser-only prototype. User accounts, the current session, and tasks are stored in `localStorage`.

That means:

- Passwords are stored in plaintext in the browser.
- Authentication is not suitable for production.
- Data is isolated to the browser profile/device.
- A user with browser developer-tools access can inspect or modify stored data.

Do not use real passwords or sensitive information with the demo application.

## AI API security

Never place an Anthropic or other provider API key in `task_management_app.html` or any other browser-delivered JavaScript. A client-side key can be extracted by users.

For production AI support, use a server-side endpoint such as:

`Browser -> Your backend -> AI provider`

Store the provider key in a server-side environment variable and validate/authorize requests on the backend.

## Recommended production architecture

- Server-side authentication with secure password hashing (for example, Argon2id or bcrypt).
- Server-managed sessions or short-lived access tokens with appropriate security controls.
- Database-backed users and tasks.
- Server-side authorization checks so a user can only access their own tasks.
- HTTPS in production.
- Input validation on both client and server.
- Rate limiting for authentication and AI endpoints.
- Automated dependency and security checks.
