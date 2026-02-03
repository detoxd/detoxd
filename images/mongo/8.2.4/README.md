# mongo:8.2.4 (Detoxed)

## Quick Start

```bash
docker pull detoxd/mongo:8.2.4-detox.1
docker run -d detoxd/mongo:8.2.4-detox.1
```

## Image Info

| Property | Value |
|----------|-------|
| Original | `mongo:8.2.4` |
| Detoxed | `detoxd/mongo:8.2.4-detox.1` |
| Scan Date | 2026-02-03 |

## Scan Results

| Metric | Before | After | Fixed |
|--------|--------|-------|-------|
| Total Vulnerabilities | 205 | 61 | 144 (70.2%) |
| Critical | 0 | 0 | 0 |
| High | 52 | 20 | 32 |
| Medium | 141 | 29 | 112 |
| Low | 12 | 12 | 0 |

> See `scan/before.json` and `scan/after.json` for full vulnerability details.
