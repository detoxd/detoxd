# Detoxd: alpine:3.23.2

## Hardened Image

| Metric | Before | After | Fixed |
|--------|--------|-------|-------|
| Total Vulnerabilities | 24 | 0 | 24 |
| Fixable | 24 | 0 | 24 |
| Unfixable | 0 | 0 | - |

**Reduction: 100%**

## Quick Start

```bash
docker pull detoxd/alpine:3.23.2-detox.1
docker run -it detoxd/alpine:3.23.2-detox.1
```

## Remaining Vulnerabilities

These remain because **no upstream fix is available**:

```

```

## Files

- `Dockerfile` - Hardened Dockerfile
- `scan/before.json` - Initial vulnerability scan
- `scan/after.json` - Final vulnerability scan
