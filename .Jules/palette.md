## 2025-05-14 - Drawer Accessibility & Focus Management

**Learning:** When using CSS transitions for UI elements like drawers or modals, immediate calls to `.focus()` can fail because the element is not yet considered "visible" or "interactable" by some browsers or assistive technologies until the transition starts or completes. A small delay (e.g., 100ms) ensures focus is reliably caught by the intended element (like a close button) after the transition begins.

**Action:** Use `setTimeout(() => el.focus(), 100)` when moving focus to elements that are being revealed via CSS transitions. Also, always restore focus to the trigger element when the component closes to maintain a logical tab order.
