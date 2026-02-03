# postgres:17.7-alpine3.21 (Detoxed)

## Quick Start

```bash
docker pull detoxd/postgres:17.7-alpine3.21-detox.1
docker run -d detoxd/postgres:17.7-alpine3.21-detox.1
```

## Image Info

| Property | Value |
|----------|-------|
| Original | `postgres:17.7-alpine3.21` |
| Detoxed | `detoxd/postgres:17.7-alpine3.21-detox.1` |
| Scan Date | 2026-02-03 |

## Scan Results

| Metric | Before | After | Fixed |
|--------|--------|-------|-------|
| Total Vulnerabilities | 41 | 15 | 26 (63.4%) |
| Critical | 2 | 0 | 2 |
| High | 8 | 4 | 4 |
| Medium | 28 | 11 | 17 |
| Low | 3 | 0 | 3 |

> See `scan/before.json` and `scan/after.json` for full vulnerability details.
