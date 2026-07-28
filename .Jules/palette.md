# Palette Journal 🎨

## 2026-03-04 - Drawer Keyboard Accessibility & Focus Management
**Learning:** Animated drawers using CSS transforms (`transform: translateX(105%)`) are not hidden from some visual accessibility tools or screen readers unless marked with appropriate `role="dialog"` and `aria-modal="true"`. Furthermore, calling `.focus()` on a close button immediately after adding a CSS class (like `.show`) can fail or get lost if the browser has not yet completed initial layout or begun transition. Shifting focus using a small delay (`setTimeout`) ensures the element is ready and interactable.
**Action:** Always include manual focus management with a delay for animated transitions (e.g., `setTimeout(..., 150)`), dynamic dynamic title labeling using `aria-labelledby`, and restoration of focus to the triggering element when the dialog or drawer is closed.
