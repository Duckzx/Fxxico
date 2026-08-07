# Palette's Journal - Critical Learnings Only

## 2026-08-07 - Focus Management Delay in Animated Drawers
**Learning:** Animated drawers using CSS transitions (like `transform: translateX(105%)` to `translateX(0)`) require a small delay (100ms-300ms) before programmatically setting focus to inner elements (like close buttons). If focused immediately, some browsers fail to focus the element because it isn't considered fully visible or interactable yet, or the transition interferes with scroll alignment.
**Action:** Use a `setTimeout` of 150ms when opening the drawer to set focus to the close button, ensuring smooth transition compatibility and reliable focus retention.
