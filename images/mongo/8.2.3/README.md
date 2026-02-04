# mongo:8.2.3 (Detoxed)

## Quick Start

```bash
docker pull detoxd/mongo:8.2.3-detox.1
docker run -d detoxd/mongo:8.2.3-detox.1
```

## Image Info

| Property | Value |
|----------|-------|
| Original | `mongo:8.2.3` |
| Detoxed | `detoxd/mongo:8.2.3-detox.1` |
| Scan Date | 2026-02-04 |

## Scan Results

| Metric | Before | After | Fixed |
|--------|--------|-------|-------|
| Total Vulnerabilities | 221 | 61 | 160 (72.4%) |
| Critical | 0 | 0 | 0 |
| High | 52 | 20 | 32 |
| Medium | 143 | 29 | 114 |
| Low | 26 | 12 | 14 |

> See `scan/before.json` and `scan/after.json` for full vulnerability details.
