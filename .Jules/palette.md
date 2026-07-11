## 2025-05-14 - Accessible Drawer Focus Management
**Learning:** Animated side drawers using CSS transitions (like `transform: translateX`) often require a short delay (e.g., 100ms) before programmatically focusing internal elements. Immediate `.focus()` calls can fail if the element is not yet considered "visible" or "interactable" by the browser during the initial paint of the transition.
**Action:** Always use a `setTimeout` of at least 100ms when moving focus to an element inside an animated container to ensure reliable focus transitions for keyboard and screen reader users.
