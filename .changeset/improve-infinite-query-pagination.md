---
"@tanstack/react-db": patch
---

fix(react-db): improve useLiveInfiniteQuery pagination and types

- Add `gcTime` config option to control garbage collection timing. Set to `0` to preserve pagination state across navigation.
- Fix race conditions during rapid scrolling by using a ref-based guard to prevent duplicate page fetches
- Prevent `hasNextPage` from flickering to `false` during loading transitions
- Fix type inference for pre-created collections passed to `useLiveInfiniteQuery` (was returning `{ [x: string]: any }[]` instead of correct collection type)
