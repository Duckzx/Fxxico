## 2025-05-15 - Focus Management with CSS Transitions
**Learning:** When using CSS transitions for UI elements like drawers or modals (e.g., `transform: translateX(105%)` to `translateX(0)`), immediate `.focus()` calls may fail or be ignored by screen readers if the element is not yet fully in the viewport or considered "visible" by the browser's focus engine.
**Action:** Use a short `setTimeout` (e.g., 100ms) to delay the focus shift until the transition has started and the element is interactive, ensuring a smooth experience for keyboard and screen reader users.
