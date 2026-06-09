## 2024-05-15 - Context-Aware Interactive Elements
**Learning:** When interactive elements like DataCards transition into a non-interactive edit mode, keeping their focusability, semantic roles, hover styles, and pointer cursors is extremely confusing for users. It signals interactivity where there is none.
**Action:** Always conditionally apply `role="button"`, `tabIndex`, `onKeyDown`, and interactive utility classes (like hover shadows and pointers) based on the element's current interactive state. Disable them entirely when the element serves only as a container in an edit mode.
