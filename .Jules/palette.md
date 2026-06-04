## 2025-05-15 - Focus Management in Vanilla JS Drawers
**Learning:** CSS transitions can interfere with immediate element focusing. When a drawer or modal uses `transition` to slide into view, attempting to `focus()` an internal element immediately may fail or occur before the element is fully interactive.
**Action:** Use a short `setTimeout` (e.g., 100ms) to delay the focus call until the transition has started and the element is ready to receive focus. Always restore focus to the trigger element upon closing to maintain keyboard navigation flow.
