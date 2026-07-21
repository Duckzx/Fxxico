# Palette's Journal

## 2026-03-01 - Focus delay in animated drawers
**Learning:** Animated drawers that use CSS transitions (e.g. `transform: translateX(105%)` to `translateX(0)`) require a slight delay (e.g. 100ms-300ms) before programmatically focusing elements inside them. Immediate focus calls often fail as browsers do not consider elements interactable until the transition has begun or completed. Additionally, Escape key listeners must check if the element is currently visible/active to prevent unnecessary focus jumps when the drawer is already closed.
**Action:** Always wrap programmatic `.focus()` calls on animated elements with a small `setTimeout` delay, and make window keydown handlers conditional on the drawer visibility state.
