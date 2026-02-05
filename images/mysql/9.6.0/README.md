# Detoxd: mysql:9.6.0

## Hardened Image

| Metric | Before | After | Fixed |
|--------|--------|-------|-------|
| Total Vulnerabilities | 18 | 18 | 0 |
| Fixable | 18 | 18 | 0 |
| Unfixable | 0 | 0 | - |

**Reduction: 0%**

## Quick Start

```bash
docker pull detoxd/mysql:9.6.0-detox.1
docker run -it detoxd/mysql:9.6.0-detox.1
```

## Remaining Vulnerabilities

These remain because **no upstream fix is available**:

```

```

## Files

- `Dockerfile` - Hardened Dockerfile
- `scan/before.json` - Initial vulnerability scan
- `scan/after.json` - Final vulnerability scan
