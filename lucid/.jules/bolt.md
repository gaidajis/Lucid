## 2024-07-03 - Memoizing Data Transformations
**Learning:** Sequential filter operations (like array `.filter` followed by `reduce` with nested `.filter`) in high-level components cause performance bottlenecks during unrelated state updates because they execute on every render.
**Action:** Always memoize expensive data transformations (like filtering and reducing the Zustand store's items array) with `useMemo` in high-level components, and prefer a single O(N) pass using a lookup map rather than sequential O(N * Tiers) filter operations.
