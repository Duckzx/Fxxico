# Palette Journal - Central de Produção Dashboard

## 2026-08-02 - Drawer Focus Management Delay
**Learning:** Animated drawers using CSS transforms (`transform: translateX(105%)`) are often not immediately interactable or focused properly by browsers if `.focus()` is called instantly upon adding a class like `.show`. Adding a `setTimeout` delay of 150ms allows the animation to begin and ensures focus lands correctly on the close button.
**Action:** Always wrap the focus-shifting code in a `setTimeout` of 100ms-300ms when handling animated modals or drawers.

## 2026-08-02 - Escape Key Drawer Closing Integration
**Learning:** Adding a global keyboard listener for the "Escape" key allows screen reader and keyboard users to dismiss open drawers easily, but it must check if the drawer is active (e.g. has the `.show` class) to prevent unexpected focus shifting or side-effects when the drawer is already closed.
**Action:** Implement `if (drawer.classList.contains('show')) closeDrawer();` inside keydown handlers.
