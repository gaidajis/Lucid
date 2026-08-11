## 2024-05-22 - motion.div Accessibility Pattern
**Learning:** Found that non-interactive components like `div` or `motion.div` are often given an `onClick` handler without semantic role, `tabIndex`, or keyboard event support, making them completely inaccessible to screen reader and keyboard-only users.
**Action:** Always pair `onClick` on non-button elements (like `div` or `motion.div`) with `role="button"`, `tabIndex={0}`, an `onKeyDown` handler (for `Enter` and `Space`), and `focus-visible` utility classes to ensure full keyboard accessibility.
