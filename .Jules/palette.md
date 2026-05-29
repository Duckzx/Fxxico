## 2025-05-14 - [Accessibility in Static Dashboards]
**Learning:** In static HTML dashboards, custom interactive elements (like file upload labels) and dynamic drawers often lack keyboard focus management and ARIA context, making them inaccessible to screen reader and keyboard-only users.
**Action:** Always ensure custom buttons/labels have `role="button"` and `tabindex="0"`, implement focus trapping/restoration for modals/drawers, and use `aria-label` to provide context in repeated grid elements.
