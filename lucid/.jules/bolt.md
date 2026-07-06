## 2024-07-06 - O(N * Tiers) sequential filter bottlenecks

**Learning:** The lucid project's primary app component `App.tsx` previously suffered from an O(N * Tiers) bottleneck during re-renders because it filtered all items and then iterated through all tiers, re-filtering the items list for each tier sequentially on every render without memoization.
**Action:** When working with the Zustand store items and categories (tiers), always memoize expensive data transformations with `useMemo`. For array grouping/aggregation, prefer a single O(N) pass using a lookup map (e.g., `reduce` with a pre-populated accumulator and a single loop over items) rather than sequential O(N * Tiers) filter operations.
