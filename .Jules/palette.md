## 2024-05-25 - Interactive Cards Keyboard Accessibility
**Learning:** `motion.div` elements used as interactive cards lacked basic keyboard accessibility, meaning users relying on keyboard navigation could not open details.
**Action:** Always ensure that non-button clickable elements (`div`, `motion.div`) include `role="button"`, `tabIndex={0}`, an `onKeyDown` handler for Space/Enter, and clear `focus-visible` styles.
