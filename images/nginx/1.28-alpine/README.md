# Detoxd: nginx:1.28-alpine

## Hardened Image

| Metric | Before | After | Fixed |
|--------|--------|-------|-------|
| Total Vulnerabilities | 1 | 0 | 1 |
| Fixable | 1 | 0 | 1 |
| Unfixable | 0 | 0 | - |

**Reduction: 100%**

## Quick Start

```bash
docker pull detoxd/nginx:1.28-alpine-detox.1
docker run -it detoxd/nginx:1.28-alpine-detox.1
```

## Remaining Vulnerabilities

These remain because **no upstream fix is available**:

```

```

## Files

- `Dockerfile` - Hardened Dockerfile
- `scan/before.json` - Initial vulnerability scan
- `scan/after.json` - Final vulnerability scan
