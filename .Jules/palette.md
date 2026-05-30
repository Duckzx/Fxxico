## 2025-05-30 - [Initial Audit]
**Learning:** Found critical accessibility gaps in the "fxxico" production center interface. Drawers lack semantic roles (dialog/modal) and focus management, causing navigation disorientation for screen reader and keyboard users. Additionally, custom file upload triggers using labels wrapping hidden inputs are inaccessible via keyboard by default.
**Action:** Implement manual focus management (save/restore focus), add ARIA dialog attributes, and ensure all custom interactive elements have proper roles and keyboard handlers.
