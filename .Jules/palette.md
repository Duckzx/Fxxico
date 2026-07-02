## 2025-05-15 - Drawer Focus Management Delay
**Learning:** Immediate `.focus()` calls on elements inside a drawer often fail if there's a CSS transition (like `transform: translateX`) happening simultaneously. A small delay (100ms) ensures the element is ready to receive focus after the transition starts.
**Action:** Use `setTimeout(() => element.focus(), 100)` when moving focus to elements within a sliding drawer or modal.

## 2025-05-15 - Global Escape Listener Optimization
**Learning:** When adding a global 'Escape' key listener to close a modal, check for the modal's visibility class (e.g., `.show`) before triggering the close logic. This prevents unnecessary focus jumps or logic execution when the modal is already closed.
**Action:** `if (e.key === 'Escape' && modal.classList.contains('show')) { close(); }`
