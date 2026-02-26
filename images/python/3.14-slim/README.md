# Detoxd: python:3.14-slim

## Hardened Image

| Metric | Before | After | Fixed |
|--------|--------|-------|-------|
| Total Vulnerabilities | 78 | 77 | 1 |
| Fixable | 1 | 0 | 1 |
| Unfixable | 77 | 77 | - |

**Reduction: 1%**

## Quick Start

```bash
docker pull detoxd/python:3.14-slim-detox.1
docker run -it detoxd/python:3.14-slim-detox.1
```

## Remaining Vulnerabilities

These remain because **no upstream fix is available**:

```
[LOW] CVE-2011-3374: apt
[LOW] TEMP-0841856-B18BAF: bash
[MEDIUM] CVE-2025-14104: bsdutils
[LOW] CVE-2022-0563: bsdutils
[LOW] CVE-2026-3184: bsdutils
[LOW] CVE-2017-18018: coreutils
[LOW] CVE-2025-5278: coreutils
[LOW] CVE-2011-3374: libapt-pkg7.0
[MEDIUM] CVE-2025-14104: libblkid1
[LOW] CVE-2022-0563: libblkid1
[LOW] CVE-2026-3184: libblkid1
[HIGH] CVE-2026-0861: libc-bin
[MEDIUM] CVE-2025-15281: libc-bin
[MEDIUM] CVE-2026-0915: libc-bin
[LOW] CVE-2010-4756: libc-bin
[LOW] CVE-2018-20796: libc-bin
[LOW] CVE-2019-1010022: libc-bin
[LOW] CVE-2019-1010023: libc-bin
[LOW] CVE-2019-1010024: libc-bin
[LOW] CVE-2019-1010025: libc-bin
[LOW] CVE-2019-9192: libc-bin
[HIGH] CVE-2026-0861: libc6
[MEDIUM] CVE-2025-15281: libc6
[MEDIUM] CVE-2026-0915: libc6
[LOW] CVE-2010-4756: libc6
[LOW] CVE-2018-20796: libc6
[LOW] CVE-2019-1010022: libc6
[LOW] CVE-2019-1010023: libc6
[LOW] CVE-2019-1010024: libc6
[LOW] CVE-2019-1010025: libc6
[LOW] CVE-2019-9192: libc6
[MEDIUM] CVE-2025-14104: liblastlog2-2
[LOW] CVE-2022-0563: liblastlog2-2
[LOW] CVE-2026-3184: liblastlog2-2
[MEDIUM] CVE-2025-14104: libmount1
[LOW] CVE-2022-0563: libmount1
[LOW] CVE-2026-3184: libmount1
[LOW] CVE-2025-6141: libncursesw6
[MEDIUM] CVE-2025-14104: libsmartcols1
[LOW] CVE-2022-0563: libsmartcols1
[LOW] CVE-2026-3184: libsmartcols1
[MEDIUM] CVE-2025-7709: libsqlite3-0
[LOW] CVE-2021-45346: libsqlite3-0
[LOW] CVE-2013-4392: libsystemd0
[LOW] CVE-2023-31437: libsystemd0
[LOW] CVE-2023-31438: libsystemd0
[LOW] CVE-2023-31439: libsystemd0
[LOW] CVE-2025-6141: libtinfo6
[LOW] CVE-2013-4392: libudev1
[LOW] CVE-2023-31437: libudev1
[LOW] CVE-2023-31438: libudev1
[LOW] CVE-2023-31439: libudev1
[MEDIUM] CVE-2025-14104: libuuid1
[LOW] CVE-2022-0563: libuuid1
[LOW] CVE-2026-3184: libuuid1
[MEDIUM] CVE-2025-14104: login
[LOW] CVE-2022-0563: login
[LOW] CVE-2026-3184: login
[LOW] CVE-2007-5686: login.defs
[LOW] CVE-2024-56433: login.defs
[LOW] TEMP-0628843-DBAD28: login.defs
[MEDIUM] CVE-2025-14104: mount
[LOW] CVE-2022-0563: mount
[LOW] CVE-2026-3184: mount
[LOW] CVE-2025-6141: ncurses-base
[LOW] CVE-2025-6141: ncurses-bin
[LOW] CVE-2007-5686: passwd
[LOW] CVE-2024-56433: passwd
[LOW] TEMP-0628843-DBAD28: passwd
[LOW] CVE-2011-4116: perl-base
[LOW] TEMP-0517018-A83CE6: sysvinit-utils
[LOW] CVE-2005-2541: tar
[LOW] TEMP-0290435-0B57B5: tar
[MEDIUM] CVE-2025-14104: util-linux
[LOW] CVE-2022-0563: util-linux
[LOW] CVE-2026-3184: util-linux
[MEDIUM] CVE-2026-27171: zlib1g
```

## Files

- `Dockerfile` - Hardened Dockerfile
- `scan/before.json` - Initial vulnerability scan
- `scan/after.json` - Final vulnerability scan
