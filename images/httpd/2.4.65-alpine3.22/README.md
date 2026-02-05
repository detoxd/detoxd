# Detoxd: httpd:2.4.65-alpine3.22

## Hardened Image

| Metric | Before | After | Fixed |
|--------|--------|-------|-------|
| Total Vulnerabilities | 38 | 0 | 38 |
| Fixable | 38 | 0 | 38 |
| Unfixable | 0 | 0 | - |

**Reduction: 100%**

## Quick Start

```bash
docker pull detoxd/httpd:2.4.65-alpine3.22-detox.1
docker run -it detoxd/httpd:2.4.65-alpine3.22-detox.1
```

## Remaining Vulnerabilities

These remain because **no upstream fix is available**:

```

```

## Files

- `Dockerfile` - Hardened Dockerfile
- `scan/before.json` - Initial vulnerability scan
- `scan/after.json` - Final vulnerability scan
