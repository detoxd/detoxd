# mysql:9.0 (Detoxed)

## Quick Start

```bash
docker pull detoxd/mysql:9.0-detox.1
docker run -d detoxd/mysql:9.0-detox.1
```

## Image Info

| Property | Value |
|----------|-------|
| Original | `mysql:9.0` |
| Detoxed | `detoxd/mysql:9.0-detox.1` |
| Scan Date | 2026-02-04 |

## Scan Results

| Metric | Before | After | Fixed |
|--------|--------|-------|-------|
| Total Vulnerabilities | 211 | 81 | 130 (61.6%) |
| Critical | 3 | 3 | 0 |
| High | 96 | 36 | 60 |
| Medium | 98 | 40 | 58 |
| Low | 14 | 2 | 12 |

> See `scan/before.json` and `scan/after.json` for full vulnerability details.
