## 2024-05-29 - Memoizing App Component List Processing
**Learning:** Unmemoized list processing coupled with state inside the main App component causes unnecessary computation overhead during unrelated state changes (like opening modals).
**Action:** Always memoize expensive operations (e.g. `items.filter`, `array.reduce`) using `useMemo` when working with Zustand stores and top-level UI components to avoid blocking the main thread or causing performance degradation.
