## 2024-05-24 - Single Pass Memoized Filtering and Grouping
**Learning:** Sequential `.filter` operations for grouping items by categories resulted in an O(N*Tiers) complexity, and this calculation ran on every render because it wasn't memoized.
**Action:** Always memoize expensive data transformations with `useMemo` in high-level components. For array grouping/aggregation across known categories, prefer a single O(N) pass using a lookup map or an initialized accumulator object rather than sequential `.filter` operations for each category.

## 2026-08-11 - React.memo and useCallback for DataCard
**Learning:** Passing inline arrow functions to list components like DataCard breaks React.memo because a new function reference is created on every render, leading to cascading re-renders.
**Action:** Always wrap list item components in React.memo and pass stable function references using useCallback for their event handlers to prevent performance bottlenecks during unrelated state updates.
