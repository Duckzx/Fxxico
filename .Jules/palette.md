# Palette's Journal - Critical UX & Accessibility Learnings

## 2025-05-14 - Focus Management in Drawers
**Learning:** Drawers and modals often lack focus management, which disorients keyboard and screen reader users when they open or close. Without moving focus to the drawer, the user might stay on the trigger element or lose their place entirely.
**Action:** Always move focus to the first interactive element (like a close button) upon opening a drawer and restore focus to the trigger element upon closing.
