# Detoxd: ubuntu:24.04

## Hardened Image

| Metric | Before | After | Fixed |
|--------|--------|-------|-------|
| Total Vulnerabilities | 26 | 12 | 14 |
| Fixable | 14 | 0 | 14 |
| Unfixable | 12 | 12 | - |

**Reduction: 53%**

## Quick Start

```bash
docker pull detoxd/ubuntu:24.04-detox.1
docker run -it detoxd/ubuntu:24.04-detox.1
```

## Remaining Vulnerabilities

These remain because **no upstream fix is available**:

```
[LOW] CVE-2016-2781: coreutils
[MEDIUM] CVE-2025-68972: gpgv
[MEDIUM] CVE-2026-24882: gpgv
[LOW] CVE-2022-3219: gpgv
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
