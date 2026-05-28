## 2026-05-28 - [Accessible Custom Components]
**Learning:** Adding `onclick` to non-interactive elements like `div` requires `role="button"`, `tabindex="0"`, and `onkeydown` handlers to maintain keyboard and screen reader accessibility.
**Action:** Always include ARIA roles and keyboard support when making static elements interactive.
