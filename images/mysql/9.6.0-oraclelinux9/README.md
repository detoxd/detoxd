# Detoxd: mysql:9.6.0-oraclelinux9

## Hardened Image

| Metric | Before | After | Fixed |
|--------|--------|-------|-------|
| Total Vulnerabilities | 20 | 20 | 0 |
| Fixable | 20 | 20 | 0 |
| Unfixable | 0 | 0 | - |

**Reduction: 0%**

## Quick Start

```bash
docker pull detoxd/mysql:9.6.0-oraclelinux9-detox.1
docker run -it detoxd/mysql:9.6.0-oraclelinux9-detox.1
```

## Remaining Vulnerabilities

These remain because **no upstream fix is available**:

```

```

## Files

- `Dockerfile` - Hardened Dockerfile
- `scan/before.json` - Initial vulnerability scan
- `scan/after.json` - Final vulnerability scan
