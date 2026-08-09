## 2024-05-24 - Single Pass Memoized Filtering and Grouping
**Learning:** Sequential `.filter` operations for grouping items by categories resulted in an O(N*Tiers) complexity, and this calculation ran on every render because it wasn't memoized.
**Action:** Always memoize expensive data transformations with `useMemo` in high-level components. For array grouping/aggregation across known categories, prefer a single O(N) pass using a lookup map or an initialized accumulator object rather than sequential `.filter` operations for each category.

## 2024-05-25 - Prevented Unnecessary List Item Re-renders
**Learning:** Rendering large lists of complex components like `DataCard` (120+ items) can cause significant lag when unrelated app state changes (e.g., sidebar toggling or opening modals) because every card re-renders. The root cause was that `App` passed new inline function references (e.g., `onEdit={(i) => ...}`) to the cards on every render.
**Action:** Extract inline callbacks passed to child list items into stable `useCallback` references and wrap the child component (`DataCard`) with `React.memo`. This ensures the child component only re-renders when its specific item data or the `editMode` state changes.
