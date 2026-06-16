## 2025-05-14 - Focus Management in Transitionally Animating Drawers
**Learning:** When opening a drawer with a CSS transition, immediate focus on an internal element can sometimes fail or cause jarring visual jumps if the element isn't fully "stable" or visible in the DOM's layout tree. A small delay (e.g., 100ms) ensures the transition has started and the browser correctly handles the focus move.
**Action:** Use `setTimeout` with a 100ms delay when moving focus to elements inside a sliding drawer or modal to guarantee reliable focus trapping and screen reader announcement.
