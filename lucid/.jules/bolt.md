## 2024-05-24 - Single Pass Memoized Filtering and Grouping
**Learning:** Sequential `.filter` operations for grouping items by categories resulted in an O(N*Tiers) complexity, and this calculation ran on every render because it wasn't memoized.
**Action:** Always memoize expensive data transformations with `useMemo` in high-level components. For array grouping/aggregation across known categories, prefer a single O(N) pass using a lookup map or an initialized accumulator object rather than sequential `.filter` operations for each category.

## 2024-05-24 - Memoizing List Items
**Learning:** Rendering large lists with inline arrow functions for event handlers (like `onEdit`, `onDelete`) causes the child component to receive new function references on every render, leading to cascading re-renders of the entire list even if the item data hasn't changed.
**Action:** Wrap list item components like `DataCard` in `React.memo` and pass stable function references using `useCallback` for their event handlers from the parent component.
