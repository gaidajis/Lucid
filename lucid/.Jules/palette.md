## 2026-07-06 - Conditional Accessibility Semantics
**Learning:** Interactive containers like cards need their accessibility semantics (role, tabIndex, keyboard handlers, and focus styles) conditionally removed when they are placed in a non-interactive mode, to prevent screen readers and keyboard users from focusing or interacting with disabled elements.
**Action:** Always conditionally apply `role`, `tabIndex`, `onKeyDown`, and `focus-visible` utility classes to dynamic interactive elements based on their active state.
