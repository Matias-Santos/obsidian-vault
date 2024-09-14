
## Description

As a user, I want a notification system, so I can receive alerts about important updates or actions taken in the app.

## Acceptance Criteria

- Notifications should appear as toast messages or modals, depending on the context.
- The notification system should support success, warning, and error types.
- Users should be able to dismiss notifications manually or automatically after a set time.
- Notifications should be responsive and work across devices.

## Tasks

- [ ] Create a notification system component that accepts `type`, `message`, and `duration` props.
- [ ] Implement toast-style notifications for success, warning, and error messages.
- [ ] Ensure that notifications are dismissed after a set time or when manually clicked.
- [ ] Test the notification system for performance and usability.

## Notes

- Consider using libraries like `react-toastify` for simpler implementation.
- Notifications should be accessible for screen readers and keyboard users.
