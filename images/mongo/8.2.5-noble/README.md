# Detoxd: mongo:8.2.5-noble

## Hardened Image

| Metric | Before | After | Fixed |
|--------|--------|-------|-------|
| Total Vulnerabilities | 75 | 61 | 14 |
| Fixable | 63 | 49 | 14 |
| Unfixable | 12 | 12 | - |

**Reduction: 18%**

## Quick Start

```bash
docker pull detoxd/mongo:8.2.5-noble-detox.2
docker run -it detoxd/mongo:8.2.5-noble-detox.2
```

## Remaining Vulnerabilities

These remain because **no upstream fix is available**:

```
[LOW] CVE-2016-2781: coreutils
[MEDIUM] CVE-2025-68972: gpgv
[LOW] CVE-2022-3219: gpgv
[LOW] CVE-2025-0167: libcurl4t64
[LOW] CVE-2024-2236: libgcrypt20
[MEDIUM] CVE-2025-8941: libpam-modules
[MEDIUM] CVE-2025-8941: libpam-modules-bin
[MEDIUM] CVE-2025-8941: libpam-runtime
[MEDIUM] CVE-2025-8941: libpam0g
[LOW] CVE-2024-56433: login
[LOW] CVE-2024-56433: passwd
[MEDIUM] CVE-2025-45582: tar
```

## Files

- `Dockerfile` - Hardened Dockerfile
- `scan/before.json` - Initial vulnerability scan
- `scan/after.json` - Final vulnerability scan
