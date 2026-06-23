## 2024-06-23 - O(N) Array Grouping & Filtering Memoization
**Learning:** The application was experiencing performance bottlenecks during unrelated state updates because expensive array filtering and grouping into 10 tiers (O(N * Tiers)) was happening synchronously on every render without memoization.
**Action:** Always memoize expensive data transformations (like filtering and reducing the Zustand store's items array) with `useMemo` in high-level components. For array grouping/aggregation, use a single O(N) pass with a lookup map instead of sequential O(N * Tiers) filter operations.
