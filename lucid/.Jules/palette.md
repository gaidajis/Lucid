
## 2026-07-07 - Dynamic Accessibility for Conditional Interactive Elements
**Learning:** When interactive components (like DataCard) become non-interactive due to state changes (like entering `editMode`), retaining visual cues like `cursor-pointer` and hover styles without the associated click action confuses users. Additionally, leaving accessibility semantics like `role="button"` and `tabIndex` when the click is disabled degrades the screen reader and keyboard experience.
**Action:** Ensure dynamic states conditionally disable interactive semantics (`role`, `tabIndex`, `onKeyDown`) and CSS classes (`cursor-pointer`, hover effects) when their associated actions are disabled.
