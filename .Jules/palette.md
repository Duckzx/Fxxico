## 2025-05-18 - Global Focus-Visible Styling for Taillined Dashboards
**Learning:** Adding a global `*:focus-visible` rule in Tailwind `@theme`/`<style>` ensures clear keyboard navigation visibility across all custom and utility-styled buttons without interfering with mouse click states.
**Action:** Use `*:focus-visible { outline: 2px solid var(--color-brand-purple); outline-offset: 2px; }` for dark-themed interfaces using brand color CSS variables.
