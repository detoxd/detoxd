# node:22-alpine (Detoxed)

## Quick Start

```bash
docker pull detoxd/node:22-alpine-detox.1
docker run -d detoxd/node:22-alpine-detox.1
```

## Image Info

| Property | Value |
|----------|-------|
| Original | `node:22-alpine` |
| Detoxed | `detoxd/node:22-alpine-detox.1` |
| Scan Date | 2026-02-03 |

## Scan Results

| Metric | Before | After | Fixed |
|--------|--------|-------|-------|
| Total Vulnerabilities | 11 | 1 | 10 (90.9%) |
| Critical | 0 | 0 | 0 |
| High | 10 | 1 | 9 |
| Medium | 0 | 0 | 0 |
| Low | 1 | 0 | 1 |

> See `scan/before.json` and `scan/after.json` for full vulnerability details.
