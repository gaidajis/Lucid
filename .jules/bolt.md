## 2024-05-21 - Memoizing Zustand Data Transformations
**Learning:** Zustand array items and derived transformations can cause unnecessary re-renders in higher level components if they aren't memoized correctly when unrelated states (like toggle states) change.
**Action:** Always memoize expensive data transformations (like array filters and reduces based on Zustand store data) using `useMemo` in high-level components.
