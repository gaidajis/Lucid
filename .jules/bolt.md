## 2026-06-28 - Memoize expensive data transformations and optimize array grouping
**Learning:** Sequential O(N * Tiers) filter operations on array grouping can be a bottleneck and cause unnecessary recalculations during unrelated state updates.
**Action:** Always memoize expensive data transformations with useMemo in high-level components and prefer a single O(N) pass using a lookup map (e.g., reduce with a pre-populated accumulator).
