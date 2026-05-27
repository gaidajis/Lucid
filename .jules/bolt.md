## 2024-05-27 - Memoize Expensive Data Transformations

**Learning:** Memoizing expensive data transformations (like filtering and reducing the Zustand store's items array) in high-level components is crucial to prevent performance bottlenecks during unrelated state updates (such as opening modals or toggling UI states).

**Action:** Always wrap data filtering and grouping logic with `useMemo` in parent components to avoid redundant O(N) calculations on every render.
