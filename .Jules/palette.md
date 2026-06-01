## 2025-05-14 - Accessible Drawer Component
**Learning:** Drawers and modals implemented with basic CSS transitions and JavaScript require manual focus management and ARIA roles to be accessible. Users expect to close these components with the 'Escape' key and have their focus restored to the trigger element.
**Action:** Implement 'role="dialog"', 'aria-modal="true"', focus restoration, and an 'Escape' key listener for all modal-like components.
