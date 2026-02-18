# Detoxd: node:22-alpine

## Hardened Image

| Metric | Before | After | Fixed |
|--------|--------|-------|-------|
| Total Vulnerabilities | 14 | 17 | -3 |
| Fixable | 14 | 17 | -3 |
| Unfixable | 0 | 0 | - |

**Reduction: -21%**

## Quick Start

```bash
docker pull detoxd/node:22-alpine-detox.1
docker run -it detoxd/node:22-alpine-detox.1
```

## Remaining Vulnerabilities

These remain because **no upstream fix is available**:

```

```

## Files

- `Dockerfile` - Hardened Dockerfile
- `scan/before.json` - Initial vulnerability scan
- `scan/after.json` - Final vulnerability scan
