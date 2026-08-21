## 2024-05-24 - Conditional Interactive Semantics
**Learning:** Applying accessibility primitives (`role="button"`, `tabIndex`, `onKeyDown`) and styles (`cursor-pointer`, `focus-visible`) unconditionally to elements that are functionally disabled in certain states (e.g., viewing items while in `editMode`) creates traps and confusion for screen reader and keyboard users.
**Action:** Always conditionally apply interactive semantics and styling strictly based on the element's active state (e.g., applying them only when `!editMode` is true).
