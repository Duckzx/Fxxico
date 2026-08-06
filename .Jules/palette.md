# Palette's Journal - Critical Learnings

## 2026-03-01 - Drawer Focus Management Delay
**Learning:** Animated side drawers/dialogs are not immediately interactable or focused properly by browsers if `.focus()` is called immediately when the drawer's `show` class is toggled. A transition delay means the browser might not recognize it as visible or in-bounds yet. Adding a short `setTimeout` delay of 100ms-300ms before focusing elements resolves this race condition.
**Action:** When working with CSS-transitioned side drawers, always delay focus shifting to the drawer's close button or first interactive element using a short `setTimeout`.

## 2026-03-01 - Conditional Escape Key Dismissal
**Learning:** A global 'Escape' key listener that triggers a dialog closing action must check if the dialog is actually active/visible first (e.g., checking if container has the 'show' class). Otherwise, pressing Escape when the drawer is already closed can cause accidental trigger/focus state jumps and disrupt user experience.
**Action:** Always conditionally verify element visibility or active state in modal dismiss key handlers.
