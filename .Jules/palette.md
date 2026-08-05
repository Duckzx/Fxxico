# Palette's Journal - Critical Learnings

## 2026-08-05 - Focus Management and CSS Transitions in Dynamic Drawers
**Learning:** Animated drawers using CSS transitions (e.g. `transform: translateX(105%)`) are not immediately interactable or visible to screen readers during the onset of the transition. Immediate `.focus()` calls on close buttons can fail or be ignored by the browser. A short `setTimeout` delay of 100ms-300ms resolves the issue and ensures correct accessible focus transitions.
**Action:** Always introduce a 150ms delay using `setTimeout` when programmatically focusing interactive elements inside animated drawers or modals to ensure reliable keyboard navigation.

## 2026-08-05 - Keyboard Accessibility on Custom Styled Interactive Elements
**Learning:** Styling elements like `<label>` or `<div>` to look like buttons provides great visual flexibility, but renders them completely inaccessible to keyboard users unless explicitly annotated.
**Action:** Decorate custom interactive wrappers with `role="button"` and `tabindex="0"`, and attach event listeners to handle `Enter` and `Space` key presses to trigger the associated action.
