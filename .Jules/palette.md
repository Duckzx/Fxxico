# Palette's Journal

## 2024-07-27 - Focus Management Delay in CSS-Transitioned Drawers
**Learning:** Interactive elements nested inside custom drawers or modals that utilize CSS transforms or transitions (such as `transform: translateX(105%)` transitioning to `0`) may fail to receive programmatic focus instantly via `.focus()`. Sighted screen readers and browsers sometimes ignore immediate focus calls because the element is still physically offscreen or undergoing rendering calculation during the start of the CSS transition.
**Action:** Always implement a brief timeout (100ms - 300ms) matching or slightly preceding the transition duration when shifting focus to elements inside animating containers to ensure they are fully interactable, and maintain a global pointer (`lastActiveElement`) to restore user focus upon drawer dismissal.
