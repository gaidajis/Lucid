## 2024-05-24 - Single Pass Memoized Filtering and Grouping
**Learning:** Sequential `.filter` operations for grouping items by categories resulted in an O(N*Tiers) complexity, and this calculation ran on every render because it wasn't memoized.
**Action:** Always memoize expensive data transformations with `useMemo` in high-level components. For array grouping/aggregation across known categories, prefer a single O(N) pass using a lookup map or an initialized accumulator object rather than sequential `.filter` operations for each category.

## 2026-08-22 - Memoize Large List Items
**Learning:** Passing inline arrow functions to list items (like DataCard) breaks React.memo(), causing the entire list to re-render when unrelated parent state changes (e.g., sidebar toggles or typing in search).
**Action:** Always wrap list item components in React.memo and pass stable function references using useCallback for their event handlers.
