# Palette's Journal

## 2026-08-12 - Focus Management in Animated Drawers and Modals
**Learning:** Animated CSS drawers (e.g. elements with `transition: transform` or sliding movements) require a brief delay (100ms-300ms) before programmatically focusing inside them using `.focus()`. If focused immediately when the transition starts, browsers may not consider the element visible or interactable, causing focus commands to fail. Additionally, tracking and restoring the previous active element (`lastActiveElement`) before opening a drawer ensures keyboard navigation flow is not disrupted when the dialog is dismissed.
**Action:** Always wrap programmatic focus transitions into drawers or modals in a `setTimeout` of ~200ms and implement `lastActiveElement` capture and restore handlers.

## 2026-08-12 - Custom File Input Trigger Accessibility
**Learning:** Custom file input triggers wrapped in `<label>` elements are not natively fully keyboard-accessible unless configured with explicit `tabindex="0"`, `role="button"`, and targeted `keydown` event listeners matching 'Enter' and 'Space' activation behaviors.
**Action:** Ensure custom label triggers have `tabindex="0"`, `role="button"`, and keydown event handlers triggering `.click()` on the associated file input.
