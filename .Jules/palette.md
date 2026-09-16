## 2025-05-18 - Accessible Icon Buttons & Focus Visibility in Creator OS
**Learning:** Single-page dashboard applications heavily rely on icon-only action controls (like delete icons, item toggles, export buttons) which default to unlabelled elements for screen reader users and lack explicit focus outlines.
**Action:** Always complement icon-only buttons with explicit `aria-label` and `title` attributes, add `role="checkbox"` and `aria-checked` to custom toggles, and enforce a global `*:focus-visible` ring using CSS variables for key accessibility.
