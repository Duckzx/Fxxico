# Palette's Journal - Critical Learnings

## 2026-07-31 - Focus Management Transitions in Animated Drawers
 **Learning:** Immediate `.focus()` programmatic calls on interactive elements inside slide-out drawers or animated modal containers often fail in modern browsers. This happens because the elements are not fully interactable/rendered or their coordinates are shifting when the CSS transition is actively animating. Adding a small 100ms-300ms delay aligns the focus action with the transition state, ensuring the screen reader reads the header and focus lands perfectly.
 **Action:** Always wrap initial focus elements inside animated drawers or modals in a `setTimeout` callback of 100ms-300ms to guarantee focus execution post-animation.
