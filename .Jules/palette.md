## 2025-05-14 - Accessible Drawer Patterns
**Learning:** Custom UI drawers without built-in accessibility require manual focus management to be usable by screen readers and keyboard users. This includes adding `role="dialog"`, `aria-modal="true"`, and ensuring focus moves into the drawer on open and returns to the trigger on close. A small delay (e.g., 100ms) for focusing the initial element in the drawer is often needed to account for CSS transitions.

**Action:** Always implement focus traps or at least manual focus management for modals/drawers. Use `lastActiveElement` to restore focus and add a conditional global `Escape` listener.
