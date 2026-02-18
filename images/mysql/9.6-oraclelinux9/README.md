# Detoxd: mysql:9.6-oraclelinux9

## Hardened Image

| Metric | Before | After | Fixed |
|--------|--------|-------|-------|
| Total Vulnerabilities | 29 | 20 | 9 |
| Fixable | 29 | 20 | 9 |
| Unfixable | 0 | 0 | - |

**Reduction: 31%**

## Quick Start

```bash
docker pull detoxd/mysql:9.6-oraclelinux9-detox.2
docker run -it detoxd/mysql:9.6-oraclelinux9-detox.2
```

## Remaining Vulnerabilities

These remain because **no upstream fix is available**:

```

```

## Files

- `Dockerfile` - Hardened Dockerfile
- `scan/before.json` - Initial vulnerability scan
- `scan/after.json` - Final vulnerability scan
