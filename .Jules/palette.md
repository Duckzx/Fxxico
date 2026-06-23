## 2025-05-24 - Vanilla Modal/Drawer Focus Management
**Learning:** In vanilla JavaScript projects without UI libraries, manual focus management is essential for accessibility. Modals and drawers must save the trigger element, move focus to a primary action (like the close button) upon opening, and restore focus upon closing. A small delay (100ms) ensures the browser handles focus correctly during CSS transitions.
**Action:** Always implement a `lastActiveElement` pattern with `setTimeout` for focus transitions in static dashboard projects.
