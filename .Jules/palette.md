## 2026-05-20 - Keyboard Accessibility on Clickable Divs
**Learning:** In the Lucid app, `motion.div` elements with `onClick` handlers were frequently used for components like DataCard without accompanying keyboard events (`onKeyDown`), `tabIndex`, or ARIA roles, making them inaccessible to keyboard users.
**Action:** Always pair `onClick` handlers on non-button elements (like `div` or `motion.div`) with `role="button"`, `tabIndex={0}`, an `onKeyDown` handler (supporting 'Enter' and 'Space'), and `focus-visible` utility classes to ensure full keyboard accessibility.
