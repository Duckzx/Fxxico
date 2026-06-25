## 2025-05-15 - Accessible Drawer Pattern
**Learning:** Vanilla JS drawers with CSS transitions require a small delay (e.g., 100ms) before focusing internal elements like close buttons to ensure they are visible and focusable by the browser. Additionally, global focus indicators (`:focus-visible`) and focus restoration are essential for maintaining context in static, single-page dashboards.
**Action:** Always implement a focus-trap or at least focus-management with `setTimeout` and `lastActiveElement` restoration when adding modals or drawers to static projects.
