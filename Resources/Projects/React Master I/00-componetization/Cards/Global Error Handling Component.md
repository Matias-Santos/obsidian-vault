
## Description

As a developer, I want to create a global error handling component, so I can catch and display errors consistently across the app.

## Acceptance Criteria

- The error handler should catch both synchronous and asynchronous errors.
- Errors should be logged for debugging purposes, but user-friendly error messages should be displayed to the user.
- The component should be reusable and easily applied to different parts of the application.
- The error handler should integrate with third-party logging services (e.g., Sentry).

## Tasks

- [ ] Implement a global error boundary component using React’s `ErrorBoundary`.
- [ ] Display a fallback UI with error messages when an error occurs.
- [ ] Log errors to the console or a third-party service.
- [ ] Write unit tests for the error handling behavior.

## Notes

- Make sure the error messages are non-technical and user-friendly.
- Test the error handler by simulating failures in various components.
