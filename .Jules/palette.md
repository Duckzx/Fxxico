# Palette Journal - Critical Learnings

## 2026-03-02 - Animated Drawer Focus Management Timing
**Learning:** Animated drawers (such as those using CSS `transform: translateX(...)` with `transition: 0.25s`) may not be recognized as interactable or visible by browser engines immediately when a JavaScript click occurs. Immediate programmatic `.focus()` calls on elements inside such a drawer can fail because the element is still deemed hidden or outside the viewport by the layout/rendering engine.
**Action:** When working with drawers or modals with CSS transitions, always wrap focus redirection inside a short `setTimeout` delay of 100ms-300ms. This ensures focus transfers successfully after the transition begins and the viewport recognizes the element.

## 2026-03-02 - Escape Key Drawer Conditionally Triggered
**Learning:** Adding a global listener for the 'Escape' key to close active drawers/modals is a standard accessibility best practice. However, if the keydown event is not properly filtered by checking if the modal/drawer is actually open (e.g. checking for a presence class like `.show`), it can cause focus jumping, state inconsistencies, or unexpected behavior when pressing 'Escape' under normal document state.
**Action:** Always verify that the modal or drawer has the active state class (such as `classList.contains('show')`) before firing the closing sequence and returning the focus back to the original trigger.
