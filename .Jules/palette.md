## 2025-06-17 - Manual Focus Management in Vanilla JS Transitions
**Learning:** When using CSS transitions for UI elements like drawers or modals, a small delay (e.g., 100ms) is often necessary before programmatically moving focus to internal elements to ensure they are fully "interactive" or "displayed" in the DOM's layout engine.
**Action:** Always use a setTimeout delay when moving focus into an element that is being shown via a CSS transition to ensure focus is correctly captured.
