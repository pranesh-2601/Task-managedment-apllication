# Testing plan

The current project is a single browser HTML prototype and does not yet have an automated test runner.

Before converting authentication/storage to a backend, the following behaviors should be covered:

- Registration rejects duplicate email addresses.
- Login rejects invalid credentials and accepts valid demo credentials.
- Logout clears the current session.
- Tasks are isolated by `userId`.
- Create, edit, complete, and delete operations update persisted task state.
- Search and filters return the expected tasks.
- Overdue and today calculations use the user's local date.
- User-provided task content is safely rendered.
- AI requests handle non-2xx responses without exposing credentials.

Recommended next step: split the application into modules and add a browser-capable JavaScript test runner (for example Vitest) before adding backend integration tests.
