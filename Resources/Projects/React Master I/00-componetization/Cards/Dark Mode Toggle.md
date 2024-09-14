## Description
As a user, I want to toggle between light and dark modes, so I can comfortably use the app in different lighting conditions.

## Acceptance Criteria
- The toggle should be easily accessible from the header or settings page.
- The dark mode setting should be saved to localStorage or cookies, so it persists across sessions.
- The design system should adapt all components (buttons, cards, forms, etc.) to both light and dark themes.

## Tasks
- [ ] Implement the toggle switch for light and dark modes.
- [ ] Integrate the theme provider to switch between light and dark styles.
- [ ] Save the user’s preference in localStorage or cookies.
- [ ] Ensure that all components adjust correctly to the selected theme.

## Notes
- Use CSS variables or styled-components for easy theme switching.
- Test for contrast and readability in both light and dark modes.
