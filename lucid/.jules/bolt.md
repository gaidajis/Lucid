## 2024-06-05 - Optimize App.tsx items filtering and grouping
**Learning:** In top-level components managing a global Zustand store, complex derivations like array filtering and reducing (grouping by tier) cause significant unnecessary computation during state updates (e.g. edit mode toggle, or when unrelated state like modal open/close changes).
**Action:** Always memoize expensive data transformations (`filteredItems`, `itemsByTier`) with `useMemo` in high-level components to prevent performance bottlenecks.
