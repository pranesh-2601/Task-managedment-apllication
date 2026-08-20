# Task Management Application

A responsive task management web application built with HTML, CSS, and vanilla JavaScript.

## Features

- Local demo authentication and registration
- Create, edit, complete, and delete tasks
- Priority, category, due-date, search, and filtering support
- Task statistics and responsive UI
- Local Storage persistence
- Optional AI suggestions through a backend proxy (see AI integration note)

## Tech Stack

- HTML5
- CSS3
- JavaScript (ES6+)
- Browser Local Storage

## Run locally

No build step is required for the current prototype.

1. Clone the repository.
2. Open `task_management_app.html` in a modern browser, or serve the folder with a local static server.
3. Use the demo account shown on the sign-in screen.

## Important prototype limitations

This version stores users, the current session, and tasks in browser Local Storage. Passwords are therefore not suitable for production authentication, and data is not shared between browsers or devices.

The AI feature must not expose an Anthropic API key in client-side code. For production use, route AI requests through a backend service and store the API key in a server-side environment variable.

## Security notes

- Do not add API keys or passwords to this repository.
- Do not treat Local Storage authentication as production security.
- Use server-side password hashing and session/token management for a production version.

## Future improvements

- Split HTML, CSS, and JavaScript into separate modules.
- Add a backend and database.
- Add secure authentication.
- Add automated unit and integration tests.
- Add a server-side AI integration.
- Add CI checks for JavaScript quality and tests.
