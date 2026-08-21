## 2025-02-21 - Focus Visible & Screen Reader Accessibility on Dynamic Dashboard Controls
**Learning:** Icon-only buttons and dynamically generated list controls (like game progress buttons, delete icons, and status filters) in single-page HTML dashboards often lack explicit ARIA labels and clear `:focus-visible` indicators for keyboard navigation.
**Action:** Always include global `:focus-visible` CSS rules and pass descriptive `aria-label` strings into template string renderers for interactive dynamic controls.
