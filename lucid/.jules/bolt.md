## 2024-05-24 - Memoizing Data Transformations
**Learning:** High-level components (like App.tsx) in this architecture that process the entire item store into filtered and tiered groups on every render can cause significant performance bottlenecks when unrelated state updates occur (e.g., UI interactions).
**Action:** Always memoize expensive data transformations (`filteredItems` and `itemsByTier`) using `useMemo` in high-level components. This ensures array operations only re-run when the underlying items or filter criteria change.
