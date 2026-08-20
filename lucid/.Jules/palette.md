## 2024-08-20 - Conditional Accessibility on Interactive Elements
**Learning:** Applying accessibility primitives (`role="button"`, `tabIndex={0}`, keyboard handlers) unconditionally to elements that are functionally disabled in certain states (like `DataCard` during edit mode) creates traps for screen reader users, making them think an element is interactive when it's not.
**Action:** Always conditionally apply interactive semantics and styling (`cursor-pointer`, `focus-visible` classes) based on the active state of the element (e.g., `role={!editMode ? "button" : undefined}`).
