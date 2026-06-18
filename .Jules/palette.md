## 2025-05-14 - Accessible Drawer Focus Management
**Learning:** For drawers using CSS transitions, a short delay (e.g., 100ms) before focusing the internal close button ensures the element is properly rendered and interactable by the browser's focus engine. Additionally, global Escape listeners must conditionally check for the drawer's active state to prevent focus side effects when closed.
**Action:** Use `setTimeout` for focus management in transitioned UI components and always guard global key listeners with visibility checks.
