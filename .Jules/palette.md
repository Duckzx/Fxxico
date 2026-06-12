## 2026-06-12 - Manual Focus Management in Vanilla JS Drawers

**Learning:** When implementing drawers or modals in a vanilla JavaScript environment without a UI library, manual focus management is essential for accessibility. The drawer must focus its close button (or first interactive element) upon opening to assist keyboard and screen reader users. A small delay (e.g., 100ms) may be necessary to ensure the element is focusable after the CSS transition begins.

**Action:** Save the `document.activeElement` before opening a modal/drawer and restore focus to it when closing. Use `setTimeout` to focus the internal element if transitions are involved. Always add a global `Escape` key listener that conditionally triggers closing only if the element is active (e.g., checking for a visibility class) to avoid focus jumping when the drawer is already closed.
