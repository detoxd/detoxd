# Detoxd: postgres:17.8-alpine

## Hardened Image

| Metric | Before | After | Fixed |
|--------|--------|-------|-------|
| Total Vulnerabilities | 16 | 16 | 0 |
| Fixable | 16 | 16 | 0 |
| Unfixable | 0 | 0 | - |

**Reduction: 0%**

## Quick Start

```bash
docker pull detoxd/postgres:17.8-alpine-detox.1
docker run -it detoxd/postgres:17.8-alpine-detox.1
```

## Remaining Vulnerabilities

These remain because **no upstream fix is available**:

```

```

## Files

- `Dockerfile` - Hardened Dockerfile
- `scan/before.json` - Initial vulnerability scan
- `scan/after.json` - Final vulnerability scan
