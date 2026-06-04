## 2024-05-24 - Memoizing Zustand State Transformations
**Learning:** High-level React components connecting to Zustand stores (like `App.tsx`) often perform data transformations (filtering, grouping) on array state. If these transformations are not memoized, any local state change (like opening a modal or toggling a sidebar) forces recalculation of the entire derived dataset, causing a significant performance bottleneck.
**Action:** Always memoize expensive data transformations (like filtering and reducing arrays) with `useMemo` when combining global store data with local state variables.
