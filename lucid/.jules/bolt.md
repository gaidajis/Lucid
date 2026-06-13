## 2026-06-13 - [Memoization of data transformations in App.tsx]
**Learning:** Found that `filteredItems` and `itemsByTier` in `App.tsx` are re-calculated on every render, which means expensive array operations are executed even on unrelated state changes like opening modals.
**Action:** Always memoize expensive data transformations (like filtering and reducing the Zustand store's items array) with `useMemo` in high-level components to prevent performance bottlenecks.
