## 2025-05-14 - Accessible Drawers and Focus Management

**Learning:** Standalone dashboards often lack standard accessibility features like ARIA roles and manual focus management for dynamic components (drawers/modals). Simple CSS transitions (e.g., `transform: translateX(105%)`) don't hide elements from assistive technology, making `role="dialog"` and `aria-modal="true"` critical. Additionally, immediate `.focus()` calls can fail during CSS transitions; a small delay (100ms) ensures the element is ready to receive focus.

**Action:** Always implement a "lastActiveElement" pattern to restore focus when closing drawers. Use `role="dialog"` and link it to a dynamic header using `aria-labelledby`. Include a global `Escape` key listener that checks for the component's visible state.
