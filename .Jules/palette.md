## 2026-07-23 - CSS Transitions and Focus Timing in Custom Drawers
**Learning:** Animated drawers that use CSS transforms/transitions (`transform: translateX(...)`) require a small timeout (e.g., 100ms-300ms) before programmatically setting focus inside them. If focus is called immediately, the browser may ignore the `.focus()` request because the container is not yet fully visible or considered interactable during the start of the CSS transition.
**Action:** Always wrap `.focus()` actions inside animated drawer/modal open handlers in a `setTimeout(..., 150)` to ensure seamless keyboard focus transitions.

## 2026-07-23 - Focus Trap and Restoration in Overlay Dialogs
**Learning:** For overlay components (like Drawers or Modals) to be truly accessible under WCAG and screen-reader standards, we must record the trigger element (`document.activeElement`) immediately before opening the overlay, and restore focus to this recorded element upon closure. Additionally, handling the Escape key globally to dismiss the active overlay completes the native-like experience.
**Action:** Use a global variable to keep track of the trigger element before dialog invocation, and invoke `.focus()` on it during the close event cycle. Ensure global key listeners for 'Escape' are in place to close the open dialog dynamically.
