## 2025-05-14 - Focus Management and CSS Transitions

**Learning:** When using CSS transitions for UI elements like drawers or modals, immediate `.focus()` calls often fail or are ignored because the element is not yet fully visible or "stable" in the DOM's layout. A small delay (e.g., 100ms) ensures the focus is correctly applied after the transition begins.

**Action:** Always utilize a `setTimeout` when moving focus to elements inside a transitioning container to ensure reliable focus management.
