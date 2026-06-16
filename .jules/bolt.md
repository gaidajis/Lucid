## 2024-06-16 - O(N) Single-Pass Data Transformation
**Learning:** Chaining `.filter` and `.reduce` inside a React component's render function (O(N) + O(N * Tiers)) can cause significant performance bottlenecks as the item list grows, especially when the results aren't memoized and trigger unnecessary re-renders.
**Action:** Always memoize expensive data transformations with `useMemo` and prefer a single O(N) pass using a lookup map or a pre-populated accumulator for filtering and grouping simultaneously.
