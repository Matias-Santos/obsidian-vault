
## Description

As a user, I want to view custom modals that display detailed information or forms in a focused manner without distractions.

## Acceptance Criteria

- The modal should appear centered on the screen and dim the background to focus user attention.
- The modal should have a close button and should close when clicking outside the modal or pressing `Esc`.
- The modal should support custom content, including text, images, and forms.
- The modal should be responsive and adjust to different screen sizes.

## Tasks

- [ ] Implement the modal component with custom content slots.
- [ ] Add functionality to close the modal by clicking outside or pressing `Esc`.
- [ ] Ensure the modal is responsive and works on mobile.
- [ ] Write unit tests for opening and closing modal states.

## Notes

- Consider animating the modal for smooth transitions.
- Ensure accessibility by focusing on the modal when it’s opened and returning focus when closed.
