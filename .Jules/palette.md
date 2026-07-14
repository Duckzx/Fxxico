# Palette's Journal - Critical UX/Accessibility Learnings

## 2025-05-14 - Focus Management in Animated Drawers
**Learning:** In vanilla JS apps with CSS transitions (like the dashboard's drawer), calling `.focus()` immediately after adding a 'show' class often fails because the element is not yet considered "visible" or "interactable" by the browser until the transition begins or completes.
**Action:** Utilize a small `setTimeout` (100-250ms) when opening drawers to ensure the focus is reliably moved to the close button or first interactive element.
