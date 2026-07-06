# Palette Journal - Critical UX/Accessibility Learnings

This journal records critical UX and accessibility insights discovered during development.

## 2025-07-06 - Accessible Drawer and Focus Management
**Learning:** Animated elements (like the drawer) often require a small delay (`setTimeout`) before focusing internal elements to ensure the transition doesn't interfere with the focus logic. Additionally, global keyboard listeners should be conditional to avoid unintended side effects when the element is inactive.
**Action:** Use a 100ms delay when focusing elements inside animated containers and check for the presence of "active" classes before triggering keyboard shortcuts.
