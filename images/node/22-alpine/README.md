# Detoxd: node:22-alpine

## Hardened Image

| Metric | Before | After | Fixed |
|--------|--------|-------|-------|
| Total Vulnerabilities | 17 | 22 | -5 |
| Fixable | 17 | 22 | -5 |
| Unfixable | 0 | 0 | - |

**Reduction: -29%**

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
