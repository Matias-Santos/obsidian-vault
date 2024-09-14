
## Description

As a developer, I want to optimize the performance of the design system, so users can experience faster load times and smoother interactions.

## Acceptance Criteria

- The app should lazy-load heavy components (e.g., carousels, images) to improve performance.
- Minimize unnecessary re-renders of components by memoizing where necessary.
- Ensure that all media assets (images, videos) are optimized and compressed.
- Audit the app for performance issues using tools like Lighthouse.

## Tasks

- [ ] Implement lazy loading for components like carousels and modals.
- [ ] Memoize expensive components and functions to avoid re-renders.
- [ ] Compress and optimize media assets for faster loading.
- [ ] Run performance audits and fix any bottlenecks.

## Notes

- Use React’s `useMemo` and `useCallback` hooks to optimize re-renders.
- Ensure that the design system remains highly responsive on mobile and tablet devices.
