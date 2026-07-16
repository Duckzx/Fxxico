# Palette's Journal - Critical UX/Accessibility Learnings

## 2025-05-15 - Animated Drawer Focus Management
**Learning:** Drawers using CSS transitions (like `transform: translateX`) often require a small delay (100ms-300ms) before programmatically focusing internal elements. If `.focus()` is called immediately after adding the 'show' class, the browser may not yet consider the element interactable or visible enough to receive focus, causing the focus attempt to fail silently.
**Action:** Use `setTimeout(() => element.focus(), 200)` when moving focus into an animated container to ensure reliable focus trapping.

## 2025-05-15 - Keyboard Accessibility for File Inputs
**Learning:** Labels used as triggers for hidden file inputs are not keyboard-accessible by default. They do not appear in the tab order and cannot be "clicked" via the keyboard.
**Action:** Add `tabindex="0"` and `role="button"` to the label, and implement a `keydown` listener that triggers the `click()` event on the associated hidden input when 'Enter' or 'Space' is pressed.
