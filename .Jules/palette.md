## 2025-05-15 - Accessible Drawer Focus Management
**Learning:** Animated drawers with CSS transitions require a small delay (e.g., 100ms) before moving focus to an internal element. If focused immediately, the focus call might be ignored or the visual transition may cause jitters. Also, restoring focus to the trigger element is critical for keyboard flow.
**Action:** Always capture `document.activeElement` before opening a modal/drawer and use `setTimeout` for focus entry if transitions are present.
