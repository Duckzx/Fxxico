## 2025-05-14 - Keyboard-Accessible File Upload Labels
**Learning:** In projects using the pattern of a hidden file input wrapped in a label, keyboard users are blocked because the label is not focusable by default.
**Action:** Add `tabindex="0"`, `role="button"`, and a 'keydown' listener to the label to proxy clicks to the hidden input for Enter/Space keys.
