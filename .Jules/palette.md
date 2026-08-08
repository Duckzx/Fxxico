# Palette UX Journal 🎨

## 2026-03-31 - Focus Delays in Animated Drawers
**Learning:** Transitioning drawers using CSS properties (`transform: translateX`) require a short delay (e.g. 100ms-300ms) before programmatically focusing inside them. If focus is called immediately on click, browsers may ignore the `.focus()` call because the element is still transitioning or not yet considered interactable.
**Action:** Always wrap `.focus()` inside a `setTimeout` of 150ms when opening animated sidebar drawers or dialog panels.

## 2026-03-31 - Custom Interactive Label Key Activation
**Learning:** Hidden inputs inside clickable labels require manual key event propagation if the wrapper label uses a custom `role="button"` and `tabindex="0"` for keyboard navigation. Screen readers and keyboards expect Enter or Space keys to activate the input trigger explicitly.
**Action:** Assign unique IDs, listen for keydown events, block default behavior on Space, and trigger `.click()` on the nested input manually.
