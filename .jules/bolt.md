## 2024-03-24 - Optimizing Array Grouping in Zustand Apps
**Learning:** In applications using a global store like Zustand and computing derived state in the render path, sequential $O(N)$ operations (like mapping/filtering an array multiple times) cause unnecessary re-renders and CPU overhead.
**Action:** Always memoize expensive data transformations with `useMemo` in high-level components. For array grouping/aggregation, prefer a single $O(N)$ pass using a lookup map (e.g., `reduce` with a pre-populated accumulator) rather than sequential $O(N \times \text{Categories})$ filter operations.
