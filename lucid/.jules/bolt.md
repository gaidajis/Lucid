## 2024-07-07 - Optimize filter and grouping in App.tsx
**Learning:** In the `lucid/` project, unmemoized expensive array transformations like sequential O(N * Tiers) filter operations run on every unrelated state update (e.g. toggling a modal or sidebar), unnecessarily blocking the render loop and running when intro/landing pages are active.
**Action:** Always memoize expensive data transformations with `useMemo` in high-level components and prefer a single O(N) pass utilizing a lookup map rather than sequential filters.
