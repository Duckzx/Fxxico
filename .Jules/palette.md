## 2026-03-30 - Focus Management with Animated Drawer Dialogs

**Learning:** When opening animated drawers or modal overlays using CSS transforms (e.g. `transform: translateX(105%)`), calling `.focus()` immediately on trigger click can fail if browsers do not recognize elements during transition initiation. Adding a slight delay (100ms-150ms) ensures smooth focus placement on the drawer close button, and storing `lastActiveElement` allows restoring focus seamlessly when closed via button or Escape key.

**Action:** Always capture `document.activeElement` prior to opening dynamic dialogs/drawers, focus the close trigger after a brief timeout, restore focus on close, and handle the Escape key for accessible keyboard navigation.
