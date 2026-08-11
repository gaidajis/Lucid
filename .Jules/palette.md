## 2026-06-06 - Dynamic Form Error Accessibility
**Learning:** When displaying dynamic error messages for inputs, it's critical to use `aria-invalid` to indicate the error state, `aria-describedby` on the input linking to the error message's ID, and `role="alert"` on the error message itself. This ensures screen readers announce the error immediately when it appears and properly associate it with the field.
**Action:** Always pair dynamic input validation errors with a matching ID, `role="alert"`, and link them back to the input using `aria-describedby` and `aria-invalid`.
