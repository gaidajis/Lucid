## 2026-05-24 - DataCard Keyboard Accessibility
**Learning:** Found that an interactive card element (`motion.div`) was using an `onClick` handler for viewing details but lacked `role="button"`, `tabIndex={0}`, and an `onKeyDown` handler, making it inaccessible to keyboard users.
**Action:** Always pair `onClick` on non-button elements with proper ARIA roles, `tabIndex={0}`, `onKeyDown` handlers (for `Enter` and `Space`), and `focus-visible` utility classes to ensure full keyboard accessibility.
