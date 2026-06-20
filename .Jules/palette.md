## 2025-05-22 - [Drawer & File Input Accessibility]
**Learning:** Hidden file inputs triggered by custom-styled labels are inaccessible by default for keyboard users. Manual wiring of `tabindex="0"`, `role="button"`, and a keydown listener is required. Additionally, focus management in drawers should use a small delay (e.g., 100ms) to ensure the element is focusable after visibility transitions.
**Action:** Always implement manual focus restoration for modals and ensure label-based buttons are keyboard-interactive.
