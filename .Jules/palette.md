# Palette's Journal - Critical UX/Accessibility Learnings

## 2026-06-15 - Focus management delay in animated drawer
**Learning:** Transitioning drawers using CSS transitions (`transform: translateX(105%)` to `translateX(0)`) requires a brief timeout delay (e.g. 150ms) before dynamically calling `.focus()` on any of their internal interactive children. Immediate focus calls often fail because browsers don't consider elements interactable or visible while the opening animation starts.
**Action:** Always save the `activeElement` trigger, trigger the drawer visibility, and wait 150ms before moving focus to the Close button, restoring it on close.
