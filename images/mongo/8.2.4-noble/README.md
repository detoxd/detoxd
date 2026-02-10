# Detoxd: mongo:8.2.4-noble

## Hardened Image

| Metric | Before | After | Fixed |
|--------|--------|-------|-------|
| Total Vulnerabilities | 225 | 219 | 6 |
| Fixable | 207 | 201 | 6 |
| Unfixable | 18 | 18 | - |

**Reduction: 2%**

## Quick Start

```bash
docker pull detoxd/mongo:8.2.4-noble-detox.2
docker run -it detoxd/mongo:8.2.4-noble-detox.2
```

## Remaining Vulnerabilities

These remain because **no upstream fix is available**:

```
[LOW] CVE-2016-2781: coreutils
[MEDIUM] CVE-2025-68972: gpgv
[LOW] CVE-2022-3219: gpgv
[LOW] CVE-2025-0167: libcurl4t64
[LOW] CVE-2025-10148: libcurl4t64
[LOW] CVE-2025-14524: libcurl4t64
[LOW] CVE-2025-14819: libcurl4t64
[LOW] CVE-2025-15079: libcurl4t64
[LOW] CVE-2025-15224: libcurl4t64
[LOW] CVE-2025-9086: libcurl4t64
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
