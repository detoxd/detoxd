# Detoxd: mysql:9.0

## Hardened Image

| Metric | Before | After | Fixed |
|--------|--------|-------|-------|
| Total Vulnerabilities | 228 | 85 | 143 |
| Fixable | 228 | 85 | 143 |
| Unfixable | 0 | 0 | - |

**Reduction: 62%**

## Quick Start

```bash
docker pull detoxd/mysql:9.0-detox.2
docker run -it detoxd/mysql:9.0-detox.2
```

## Remaining Vulnerabilities

These remain because **no upstream fix is available**:

```

```

## Files

- `Dockerfile` - Hardened Dockerfile
- `scan/before.json` - Initial vulnerability scan
- `scan/after.json` - Final vulnerability scan
