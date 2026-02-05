# Detoxd: postgres:17.7-alpine3.21

## Hardened Image

| Metric | Before | After | Fixed |
|--------|--------|-------|-------|
| Total Vulnerabilities | 41 | 15 | 26 |
| Fixable | 41 | 15 | 26 |
| Unfixable | 0 | 0 | - |

**Reduction: 63%**

## Quick Start

```bash
docker pull detoxd/postgres:17.7-alpine3.21-detox.2
docker run -it detoxd/postgres:17.7-alpine3.21-detox.2
```

## Remaining Vulnerabilities

These remain because **no upstream fix is available**:

```

```

## Files

- `Dockerfile` - Hardened Dockerfile
- `scan/before.json` - Initial vulnerability scan
- `scan/after.json` - Final vulnerability scan
