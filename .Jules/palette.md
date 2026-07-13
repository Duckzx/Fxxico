## 2025-05-14 - Focus management in animated drawers
**Learning:** Immediate `.focus()` calls on elements within a drawer or modal often fail or are ignored by the browser if the container is still executing a CSS transition (like `transform: translateX`). A short delay (100ms) ensures the transition has started and the element is "ready" to receive focus.
**Action:** Use a `setTimeout(() => element.focus(), 100)` pattern when opening animated UI components to ensure reliable keyboard navigation.
