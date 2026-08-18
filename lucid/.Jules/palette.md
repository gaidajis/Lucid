## 2026-08-18 - Conditional Accessibility on Interactive Elements
**Learning:** Applying accessibility primitives (role, tabIndex, onKeyDown) unconditionally on elements whose interactivity depends on an app state (e.g., `!editMode`) creates a trap where screen reader users can focus elements that don't do anything.
**Action:** Always conditionally apply interactive semantics and styling (like pointer cursor, hover effects, and `focus-visible`) based on the interactive state. For example, `role={!editMode ? "button" : undefined}` and `tabIndex={!editMode ? 0 : undefined}`.
