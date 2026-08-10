## 2024-05-24 - Single Pass Memoized Filtering and Grouping
**Learning:** Sequential `.filter` operations for grouping items by categories resulted in an O(N*Tiers) complexity, and this calculation ran on every render because it wasn't memoized.
**Action:** Always memoize expensive data transformations with `useMemo` in high-level components. For array grouping/aggregation across known categories, prefer a single O(N) pass using a lookup map or an initialized accumulator object rather than sequential `.filter` operations for each category.

## 2024-08-10 - Memoizing List Item Components
**Learning:** Large lists rendered from global state (like items by tier) cascade re-renders to all list item components (e.g., `DataCard`) whenever a parent state changes (like `editMode` toggling or sidebar state changes), even if the specific list items haven't changed.
**Action:** Always wrap list item components in `React.memo` and pass stable function references using `useCallback` for their event handlers to prevent these unnecessary, cascading re-renders in large lists.
