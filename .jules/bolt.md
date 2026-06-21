## 2024-06-21 - Memoize and Group Items with Single Pass
**Learning:** The lucid/ application performs O(N * Tiers) sequential filtering on the Zustand store items array on every render in high-level components, which causes performance bottlenecks during unrelated state updates.
**Action:** Always memoize data transformations using `useMemo` and prefer a single O(N) pass using a lookup map (e.g., `reduce` with a pre-populated accumulator) rather than sequential filter operations.
