## 2024-05-24 - Interactive Non-Button Elements Need Full Keyboard Support
**Learning:** `motion.div` and other non-button interactive elements with `onClick` lack built-in keyboard support. Users relying on keyboard navigation cannot activate or focus them without proper attributes.
**Action:** Always pair `onClick` on non-button elements with `role="button"`, `tabIndex={0}`, an `onKeyDown` handler (for `Enter` and `Space`), and `focus-visible` utility classes to ensure full keyboard accessibility.
