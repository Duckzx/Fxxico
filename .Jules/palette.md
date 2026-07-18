# Palette Journal

## 2026-07-18 - Animated Drawer Focus Management
**Learning:** Animated dynamic drawers utilizing CSS transitions (e.g., `transform: translateX(105%)` to `0%`) can cause screen readers and programmatic focus methods to fail if `.focus()` is called instantly. Browsers may not consider transitioning elements interactable or visible yet.
**Action:** Implement a short `setTimeout` delay of 100ms-300ms before focusing elements like the close button or any interactive element inside transitioning drawers to coordinate focus management with the visual transition start. Also, always track `lastActiveElement` globally to return focus cleanly upon closing.
