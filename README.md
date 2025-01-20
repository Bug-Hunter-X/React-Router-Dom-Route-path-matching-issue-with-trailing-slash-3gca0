# React Router Dom Route Path Matching Issue
This repository demonstrates a common issue encountered when working with route paths in React Router Dom v6 and above.  Specifically, it highlights how a trailing slash in a route definition can lead to unexpected behavior and prevent matching.

## Problem
The provided `bug.js` example shows that the route `/contact/` will never match if the URL is `/contact`. This is because React Router does strict path matching by default in v6.

## Solution
The `bugSolution.js` demonstrates the solution by using the `useSearchParams` hook to manage query parameters instead of relying on strict path matching.  Alternatively, you can use the `end` option in `Route` to match paths exactly, and handle potential trailing slashes in another way.