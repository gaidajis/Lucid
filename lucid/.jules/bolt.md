## 2024-05-24 - Single Pass Memoized Filtering and Grouping
**Learning:** Sequential `.filter` operations for grouping items by categories resulted in an O(N*Tiers) complexity, and this calculation ran on every render because it wasn't memoized.
**Action:** Always memoize expensive data transformations with `useMemo` in high-level components. For array grouping/aggregation across known categories, prefer a single O(N) pass using a lookup map or an initialized accumulator object rather than sequential `.filter` operations for each category.

## 2024-08-16 - Memoization of List Item Components
**Learning:** Rendering a large list of components like `DataCard` with inline event handlers causes full list re-renders whenever the parent `App` state changes (like opening a modal), because inline functions lose referential equality across renders.
**Action:** Use `React.memo` for list item components (e.g., `DataCard`) and always pass referentially stable event handlers to them using `useCallback` in the parent component to prevent cascading re-renders.
