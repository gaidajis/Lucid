## 2024-05-18 - Keyboard Accessibility for Non-Button Cards
**Learning:** Interactive non-button elements like `motion.div` cards require manual implementation of keyboard semantics (tabIndex, role, onKeyDown) and focus-visible states, which should be conditionally applied based on the component's interactivity state (e.g., disabled during edit mode).
**Action:** Always pair `onClick` on non-button elements with full keyboard accessibility semantics and conditional focus states based on the component's interactive mode.
