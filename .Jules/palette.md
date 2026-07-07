## 2025-05-15 - Drawer Focus Management and Transitions
**Learning:** Immediate focus calls on elements becoming visible via CSS transitions (like translateX) can sometimes fail or result in inconsistent behavior if the browser hasn't yet accounted for the element's new interactive state.
**Action:** Use a small timeout (e.g., 100ms) to ensure the transition has started and the element is ready to receive focus. Always restore focus to the trigger element upon closing to maintain a predictable keyboard navigation path.
