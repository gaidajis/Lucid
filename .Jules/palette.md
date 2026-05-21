## 2026-05-21 - Interactive Elements Accessibility
**Learning:** Any non-button element (like a `div` or `motion.div`) that has an `onClick` handler needs to be made fully accessible to keyboard users. This means it must act like a button.
**Action:** Always pair `onClick` on non-button elements with `role="button"`, `tabIndex={0}`, an `onKeyDown` handler that listens for 'Enter' and 'Space' keys, and `focus-visible` utility classes for clear visual focus indication.
