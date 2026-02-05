# Detoxd: postgres:17.7-alpine

## Hardened Image

| Metric | Before | After | Fixed |
|--------|--------|-------|-------|
| Total Vulnerabilities | 15 | 15 | 0 |
| Fixable | 15 | 15 | 0 |
| Unfixable | 0 | 0 | - |

**Reduction: 0%**

## Quick Start

```bash
docker pull detoxd/postgres:17.7-alpine-detox.1
docker run -it detoxd/postgres:17.7-alpine-detox.1
```

## Remaining Vulnerabilities

These remain because **no upstream fix is available**:

```

```

## Files

- `Dockerfile` - Hardened Dockerfile
- `scan/before.json` - Initial vulnerability scan
- `scan/after.json` - Final vulnerability scan
