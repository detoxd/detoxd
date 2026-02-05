<div align="center">

<img src="detoxd.png" alt="Detoxd Logo" width="200">

# detoxd

>Hardened Docker Images with Reduced Vulnerabilities

</div>

## What is Detoxd?

Detoxd provides **security-hardened Docker images** that have been scanned for vulnerabilities and patched to reduce the attack surface.

This repository serves as a **transparency log** - showing exactly what images were scanned, what vulnerabilities were found, and what fixes were applied.

## Available Images

All images are available with the format: `detoxd/<image>:<tag>-detox.1`

| # | Image | Before | After | Fixed | Reduction |
|---|-------|--------|-------|-------|-----------|
| 1 | `alpine:3.21` | 0 | 0 | 0 | 0% |
| 2 | `alpine:3.22.3` | 0 | 0 | 0 | 0% |
| 3 | `alpine:3.23` | 0 | 0 | 0 | 0% |
| 4 | `alpine:3.23.0` | 24 | 0 | 24 | 100% |
| 5 | `alpine:3.23.2` | 24 | 0 | 24 | 100% |
| 6 | `alpine:3.23.3` | 0 | 0 | 0 | 0% |
| 7 | `httpd:2.4-alpine` | 2 | 0 | 2 | 100% |
| 8 | `httpd:2.4.65-alpine` | 38 | 0 | 38 | 100% |
| 9 | `httpd:2.4.65-alpine3.22` | 38 | 0 | 38 | 100% |
| 10 | `httpd:2.4.66-alpine` | 2 | 0 | 2 | 100% |
| 11 | `httpd:2.4.66-alpine3.22` | 33 | 0 | 33 | 100% |
| 12 | `httpd:2.4.66-alpine3.23` | 2 | 0 | 2 | 100% |
| 13 | `mongo:8.0` | 209 | 203 | 6 | 3% |
| 14 | `mongo:8.2-noble` | 209 | 203 | 6 | 3% |
| 15 | `mongo:8.2.3` | 225 | 203 | 22 | 10% |
| 16 | `mongo:8.2.3-noble` | 225 | 203 | 22 | 10% |
| 17 | `mongo:8.2.4` | 209 | 203 | 6 | 3% |
| 18 | `mongo:8.2.4-noble` | 209 | 203 | 6 | 3% |
| 19 | `mysql:9.0` | 211 | 82 | 129 | 61% |
| 20 | `mysql:9.6-oracle` | 18 | 18 | 0 | 0% |
| 21 | `mysql:9.6-oraclelinux9` | 18 | 18 | 0 | 0% |
| 22 | `mysql:9.6.0` | 18 | 18 | 0 | 0% |
| 23 | `mysql:9.6.0-oracle` | 18 | 18 | 0 | 0% |
| 24 | `mysql:9.6.0-oraclelinux9` | 18 | 18 | 0 | 0% |
| 25 | `nginx:1.28-alpine` | 0 | 0 | 0 | 0% |
| 26 | `nginx:1.28.1-alpine3.23` | 0 | 0 | 0 | 0% |
| 27 | `nginx:1.28.2-alpine3.23` | 0 | 0 | 0 | 0% |
| 28 | `nginx:1.29-alpine` | 0 | 0 | 0 | 0% |
| 29 | `nginx:1.29-alpine3.23` | 0 | 0 | 0 | 0% |
| 30 | `nginx:1.29.4-alpine` | 0 | 0 | 0 | 0% |
| 31 | `nginx:1.29.4-alpine3.23` | 0 | 0 | 0 | 0% |
| 32 | `nginx:1.29.5-alpine` | 0 | 0 | 0 | 0% |
| 33 | `nginx:1.29.5-alpine3.23` | 0 | 0 | 0 | 0% |
| 34 | `node:22-alpine` | 12 | 14 | -2 | -17% |
| 35 | `postgres:17-alpine` | 15 | 15 | 0 | 0% |
| 36 | `postgres:17.7-alpine` | 15 | 15 | 0 | 0% |
| 37 | `postgres:17.7-alpine3.21` | 41 | 15 | 26 | 63% |
| 38 | `postgres:17.7-alpine3.22` | 15 | 15 | 0 | 0% |
| 39 | `postgres:17.7-alpine3.23` | 15 | 15 | 0 | 0% |
| 40 | `python:3.11-slim` | 72 | 69 | 3 | 4% |
| 41 | `python:3.11.14-slim` | 72 | 69 | 3 | 4% |
| 42 | `python:3.12-slim` | 69 | 67 | 2 | 3% |
| 43 | `python:3.12.12-slim` | 69 | 67 | 2 | 3% |
| 44 | `python:3.13-slim` | 68 | 67 | 1 | 1% |
| 45 | `python:3.13.11-slim` | 68 | 67 | 1 | 1% |
| 46 | `python:3.14-slim` | 68 | 67 | 1 | 1% |
| 47 | `python:3.14.2-slim` | 68 | 67 | 1 | 1% |
| 48 | `python:3.15.0a5-slim` | 68 | 67 | 1 | 1% |
| 49 | `redis:8.2.3-alpine3.22` | 0 | 0 | 0 | 0% |
| 50 | `redis:8.4-alpine` | 0 | 0 | 0 | 0% |
| 51 | `redis:8.4-alpine3.22` | 0 | 0 | 0 | 0% |
| 52 | `redis:8.4.0-alpine` | 0 | 0 | 0 | 0% |
| 53 | `redis:8.4.0-alpine3.22` | 0 | 0 | 0 | 0% |
| 54 | `ubuntu:24.04` | 26 | 12 | 14 | 54% |
| 55 | `ubuntu:24.10` | 0 | 0 | 0 | 0% |

## Quick Start

```bash
# Pull any hardened image
docker pull detoxd/nginx:1.25.4-alpine-detox.1

# Use it just like the original
docker run -d -p 80:80 detoxd/nginx:1.25.4-alpine-detox.1
```

## Repository Structure

```
detoxd/
├── README.md           # This file (auto-generated)
├── LICENSE             # Apache 2.0
│
└── images/
    └── <image>/<tag>/
        ├── Dockerfile       # Hardened Dockerfile
        ├── README.md        # Image-specific docs
        ├── metadata.yaml    # Image metadata
        └── scan/
            ├── before.json  # Original vulnerabilities
            └── after.json   # After hardening
```

## Security Hardening Applied

### All Images
- ✅ All packages updated to latest versions
- ✅ Removed setuid/setgid binaries
- ✅ Removed unnecessary user accounts
- ✅ Cleaned package caches
- ✅ Secured file permissions

## What This Repository Is NOT

❌ This is NOT a tool for you to run scans yourself  
❌ The scanning scripts are NOT included in this repo

This repository is purely for **transparency** - to show what we scan and the results.

## License

Apache 2.0 - See [LICENSE](LICENSE)

---
*Last updated: 2026-02-05*
