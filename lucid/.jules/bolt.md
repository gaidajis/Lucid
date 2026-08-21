## 2024-05-24 - Single Pass Memoized Filtering and Grouping
**Learning:** Sequential `.filter` operations for grouping items by categories resulted in an O(N*Tiers) complexity, and this calculation ran on every render because it wasn't memoized.
**Action:** Always memoize expensive data transformations with `useMemo` in high-level components. For array grouping/aggregation across known categories, prefer a single O(N) pass using a lookup map or an initialized accumulator object rather than sequential `.filter` operations for each category.

## 2026-08-21 - Cascading Re-renders in Lists
**Learning:** Rendering large lists of custom components (like `DataCard`) without memoization causes full component trees to re-render when the parent's state changes, even if the item props are unchanged. Passing inline functions as event handlers invalidates memoized children because their references change on every render.
**Action:** To prevent cascading re-renders of large lists, always wrap list item components in `React.memo` and pass stable function references using `useCallback` for their event handlers.
