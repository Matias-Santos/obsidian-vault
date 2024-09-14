## Description

As a developer, I want an `AuthProvider` wrapper so I can manage authentication state globally across the app.

## Acceptance Criteria

- The `AuthProvider` should expose authentication state and methods like `login`, `logout`, and `getCurrentUser`.
- All components should be able to access the authentication state through React’s context API.
- The provider should handle session persistence (using localStorage or cookies).

## Tasks

- [ ] Implement the `AuthProvider` using React’s context API.
- [ ] Create methods for logging in, logging out, and checking the current user session.
- [ ] Add session persistence logic to remember user sessions.
- [ ] Write unit tests to ensure the provider behaves as expected.

## Notes

- Ensure that authentication state is accessible throughout the entire app.
- Consider integrating with a third-party authentication service (e.g., Firebase, Auth0).