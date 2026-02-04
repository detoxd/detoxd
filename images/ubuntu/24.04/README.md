# ubuntu:24.04 (Detoxed)

## Quick Start

```bash
docker pull detoxd/ubuntu:24.04-detox.1
docker run -d detoxd/ubuntu:24.04-detox.1
```

## Image Info

| Property | Value |
|----------|-------|
| Original | `ubuntu:24.04` |
| Detoxed | `detoxd/ubuntu:24.04-detox.1` |
| Scan Date | 2026-02-04 |

## Scan Results

| Metric | Before | After | Fixed |
|--------|--------|-------|-------|
| Total Vulnerabilities | 22 | 14 | 8 (36.4%) |
| Critical | 0 | 0 | 0 |
| High | 0 | 0 | 0 |
| Medium | 10 | 9 | 1 |
| Low | 12 | 5 | 7 |

> See `scan/before.json` and `scan/after.json` for full vulnerability details.
