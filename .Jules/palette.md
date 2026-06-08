## 2025-05-15 - Accessible Drawer Management in Static HTML

**Learning:** In projects without UI frameworks, modal-like components (drawers) often lack essential accessibility features like focus traps, initial focus, focus restoration, and keyboard listeners (Escape key). A 100ms `setTimeout` is often necessary when opening the drawer to ensure the CSS transition has started and the target element is focusable.

**Action:** Always implement manual focus management: store the trigger element, move focus to the primary interactive element (e.g., close button) on open, and restore focus to the trigger on close. Add a global 'Escape' key listener conditioned on the drawer's visibility.
