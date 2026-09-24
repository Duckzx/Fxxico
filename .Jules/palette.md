## 2026-09-24 - HTML Escaping for Dynamic Accessibility Labels
**Learning:** In vanilla JavaScript dynamic HTML templates, interpolating raw user input into `aria-label` attributes can break HTML syntax if quotes or special characters are present, while also leaving screen reader descriptions unescaped.
**Action:** Always wrap dynamic strings with an `escapeHTML` helper function before embedding user input into template literals for `aria-label` or element attributes.
