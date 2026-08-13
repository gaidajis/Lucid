## 2026-08-13 - Keyboard Accessibility in Edit Mode Cards
**Learning:** When making cards accessible, applying `tabIndex={0}` to the parent container during edit mode creates a focus trap or redundant tab stop that prevents clean access to interactive child elements like Edit/Delete buttons.
**Action:** Dynamically remove parent container focus semantics (`role`, `tabIndex`, and `onKeyDown`) when a card enters edit mode to allow native focus routing to its interactive children.
