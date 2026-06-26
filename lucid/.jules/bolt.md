## 2024-06-26 - Component State & O(N*M) Array Transformations
**Learning:** High-level components (like `App.tsx`) triggering O(N*M) array filtering on every render for unrelated state changes (like opening modals).
**Action:** Always memoize `items` filtering/grouping with `useMemo` and optimize O(N*M) filter loops into single O(N) pass reducers with pre-populated maps.
