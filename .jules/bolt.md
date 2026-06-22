## 2024-06-22 - Optimizing Multiple Array Filters
**Learning:** Sequential O(N * Tiers) `filter` operations on large data structures combined with unrelated state updates (e.g., toggling modals) can cause noticeable performance bottlenecks and unnecessary UI re-renders.
**Action:** Always memoize expensive data transformations (like filtering and grouping arrays) with `useMemo` in high-level components. For aggregations, prefer a single O(N) pass using a lookup map (e.g., a pre-populated accumulator with `reduce` or `for...of` loops) instead of multiple sequential operations.
