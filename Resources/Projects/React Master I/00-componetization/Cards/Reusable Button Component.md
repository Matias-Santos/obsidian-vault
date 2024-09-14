## Description

As a developer, I want to create a reusable button component so that I can maintain consistency and easily apply buttons across the entire application.

## Acceptance Criteria
- The button component should accept `label`, `onClick`, and `variant` props (e.g., primary, secondary, danger).
- The component should support disabled states and loading states.
- The button should be fully accessible with keyboard and screen readers.
- Buttons should have consistent styling, padding, and margins across the app.


- ## Tasks

- [ ] Implement the button component with different styles for variants.
- [ ] Add loading and disabled states with proper visual feedback.
- [ ] Ensure accessibility compliance (focus states, aria-label).
- [ ] Add unit tests for each button variant.

## Notes

- Consider providing default sizes (small, medium, large) via props.
- Test performance under heavy loads (e.g., multiple buttons rendered).