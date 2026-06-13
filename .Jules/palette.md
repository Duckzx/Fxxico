## 2025-05-14 - Accessible Drawer Focus Management
**Learning:** Drawers and modals require manual focus management to ensure a smooth experience for keyboard and screen reader users. Specifically, focus should move to a logical element (like the close button) when opened and return to the trigger element when closed.
**Action:** Implement a global `lastActiveElement` variable to track the trigger and use `setTimeout` to manage focus timing after CSS transitions.
