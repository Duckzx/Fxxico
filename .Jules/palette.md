## 2025-05-15 - Focus Management with Transitions
**Learning:** When using CSS transitions for modals or drawers, focus management requires a small delay (e.g., 100ms) to ensure the element is visible and capable of receiving focus in all browsers, even if the transition hasn't fully finished.
**Action:** Use `setTimeout` when moving focus to an element inside a transitioning container.
