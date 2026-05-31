## 2025-05-31 - Drawer Keyboard Accessibility and Focus Management
**Learning:** Drawers and modals in single-page applications often lack native keyboard support. Global listeners for 'Escape' and manual focus management (storing the trigger element and focusing the primary action in the modal) are essential for a polished UX and accessibility compliance.
**Action:** Always implement a focus-restore pattern (saving `document.activeElement`) when opening overlays and ensure 'Escape' key support is added via a global listener.
