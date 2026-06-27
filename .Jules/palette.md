## 2025-05-14 - Accessible Drawer in Static Dashboard
**Learning:** For single-file static dashboards with dynamic content, accessible drawers require manual focus management (storing `lastActiveElement`) and a slight delay (e.g., 100ms) before focusing the close button to ensure CSS transitions don't interfere with the focus ring visibility or screen reader announcements.
**Action:** Always store `document.activeElement` before opening a modal/drawer and restore it after closing. Use `setTimeout` for initial focus and dynamically inject IDs for `aria-labelledby` if headings are re-rendered.
