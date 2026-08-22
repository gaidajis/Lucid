## 2024-12-21 - Conditional Accessibility Semantics
**Learning:** Applying accessibility primitives (role="button", tabIndex=0) unconditionally to elements that are functionally disabled in certain states (like `DataCard` in `editMode`) creates confusing traps for screen reader users, making them think the element is interactive when it's not.
**Action:** Always conditionally apply interactive semantics (role, tabIndex, onKeyDown) and styling (pointer cursor, focus-visible) based on the element's actual active state (e.g., `!editMode`).
