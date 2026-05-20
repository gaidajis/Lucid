## 2024-05-20 - Unnecessary Recalculations of Data Iteration in Root Component
**Learning:** In a single-page app where the root `App.tsx` handles complex state (like numerous modals and nested UI toggles), not memoizing expensive derivation logic (like data filtering and grouping) causes those calculations to re-run unnecessarily whenever any minor UI state changes (e.g. toggling the Add/Edit modal).
**Action:** Always wrap heavy data transformations (`filter`, `reduce`) that depend on store values with `useMemo`, specifically at the top level where state changes are frequent.
