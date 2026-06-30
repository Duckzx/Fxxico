## 2025-05-15 - Improving Drawer Accessibility and Focus Management
**Learning:** In static dashboards with animated drawers, manual focus management is essential. Immediate `.focus()` calls often fail during CSS transitions; a short delay (e.g., 100ms) ensures the element is ready to receive focus. ARIA roles like `dialog` and `aria-modal` are critical for screen reader context.
**Action:** Always save the `lastActiveElement` before opening a modal/drawer and restore it on close. Use `setTimeout` for focusing elements inside transitioning containers.
