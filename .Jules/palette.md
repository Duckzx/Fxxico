## 2026-07-05 - Accessible Drawer Pattern in Vanilla JS
**Learning:** In standalone HTML/JS dashboards with animated drawers, manual focus management is essential. A 100ms delay when focusing interactive elements within the drawer ensures the focus is correctly applied after the CSS 'transform' transition begins, preventing focus loss.
**Action:** Always implement 'lastActiveElement' tracking to restore focus upon closing, and use 'setTimeout' for focusing the first element inside an animated container.
