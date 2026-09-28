# Changelog — `toxi-middleware`

Per-crate history extracted from the monolith changelog
([meshackbahati/toxi](https://github.com/meshackbahati/toxi/blob/main/CHANGELOG.md)),
which remains the full documentation hub.

## Unreleased

- **toxi-middleware** (`3.1.2`): CSRF token comparison runs without
  early exit, so matching time no longer reveals correct prefix bytes.

## Unreleased

- **toxi-middleware** (`3.1.2`): CSRF tokens draw one RNG fill instead
  of thirty-two generator setups; logger skips method clone and path
  allocation when info logging is disabled.

## Unreleased

- **toxi-middleware** (`3.1.1`): request logger writes through the `log`
  facade instead of blocking standard output per request; server header
  values precomputed once instead of formatted and parsed per response.

## 3.1.5

- **toxi-middleware** (`3.1.1`): `RateLimiter` replaces the global mutex
  with 16 sharded read-write locks, ordered timestamp deques with prefix
  eviction, and reverse minute counting.
