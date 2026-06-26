## 2025-05-15 - Accessible Drawer & Keyboard Navigation
**Learning:** In single-page applications with custom drawers/modals, users expect the Escape key to close the overlay and focus to be managed. Simply toggling a 'show' class is insufficient for accessibility; focus must be trapped or at least moved to the new content to assist screen readers and keyboard users.
**Action:** Implement a global Escape key listener, manage focus when opening/closing drawers, and ensure interactive elements have clear focus indicators.
