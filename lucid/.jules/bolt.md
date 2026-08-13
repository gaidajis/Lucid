## 2024-05-24 - Single Pass Memoized Filtering and Grouping
**Learning:** Sequential `.filter` operations for grouping items by categories resulted in an O(N*Tiers) complexity, and this calculation ran on every render because it wasn't memoized.
**Action:** Always memoize expensive data transformations with `useMemo` in high-level components. For array grouping/aggregation across known categories, prefer a single O(N) pass using a lookup map or an initialized accumulator object rather than sequential `.filter` operations for each category.
## 2025-01-08 - Stable Function References for Memoized List Items
**Learning:** Even when child list items (like `DataCard`) are wrapped in `React.memo`, they will still re-render unnecessarily if the parent component passes inline arrow functions as event handler props (e.g., `onEdit`, `onDelete`), because a new function reference is created on every parent render.
**Action:** Always wrap event handler functions with `useCallback` in the parent component when passing them down to `React.memo`-wrapped list items to maintain stable function references and prevent cascading re-renders.
