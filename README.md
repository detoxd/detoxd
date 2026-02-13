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
| 13 | `mongo:8.0` | 73 | 67 | 6 | 8% |
| 14 | `mongo:8.2-noble` | 225 | 219 | 6 | 3% |
| 15 | `mongo:8.2.3` | 241 | 219 | 22 | 9% |
| 16 | `mongo:8.2.3-noble` | 241 | 219 | 22 | 9% |
| 17 | `mongo:8.2.4` | 225 | 219 | 6 | 3% |
| 18 | `mongo:8.2.4-noble` | 225 | 219 | 6 | 3% |
| 19 | `mongo:8.2.5` | 73 | 67 | 6 | 8% |
| 20 | `mongo:8.2.5-noble` | 73 | 67 | 6 | 8% |
| 21 | `mysql:9.0` | 219 | 85 | 134 | 61% |
| 22 | `mysql:9.6-oracle` | 20 | 20 | 0 | 0% |
| 23 | `mysql:9.6-oraclelinux9` | 20 | 20 | 0 | 0% |
| 24 | `mysql:9.6.0` | 20 | 20 | 0 | 0% |
| 25 | `mysql:9.6.0-oracle` | 20 | 20 | 0 | 0% |
| 26 | `mysql:9.6.0-oraclelinux9` | 20 | 20 | 0 | 0% |
| 27 | `nginx:1.28-alpine` | 0 | 0 | 0 | 0% |
| 28 | `nginx:1.28.1-alpine3.23` | 0 | 0 | 0 | 0% |
| 29 | `nginx:1.28.2-alpine3.23` | 0 | 0 | 0 | 0% |
| 30 | `nginx:1.29-alpine` | 0 | 0 | 0 | 0% |
| 31 | `nginx:1.29-alpine3.23` | 0 | 0 | 0 | 0% |
| 32 | `nginx:1.29.4-alpine` | 0 | 0 | 0 | 0% |
| 33 | `nginx:1.29.4-alpine3.23` | 0 | 0 | 0 | 0% |
| 34 | `nginx:1.29.5-alpine` | 0 | 0 | 0 | 0% |
| 35 | `nginx:1.29.5-alpine3.23` | 0 | 0 | 0 | 0% |
| 36 | `node:22-alpine` | 11 | 13 | -2 | -18% |
| 37 | `postgres:17-alpine` | 16 | 16 | 0 | 0% |
| 38 | `postgres:17.7-alpine` | 16 | 16 | 0 | 0% |
| 39 | `postgres:17.7-alpine3.21` | 42 | 16 | 26 | 62% |
| 40 | `postgres:17.7-alpine3.22` | 16 | 16 | 0 | 0% |
| 41 | `postgres:17.7-alpine3.23` | 16 | 16 | 0 | 0% |
| 42 | `postgres:17.8-alpine` | 16 | 16 | 0 | 0% |
| 43 | `postgres:17.8-alpine3.22` | 16 | 16 | 0 | 0% |
| 44 | `postgres:17.8-alpine3.23` | 16 | 16 | 0 | 0% |
| 45 | `python:3.11-slim` | 72 | 69 | 3 | 4% |
| 46 | `python:3.11.14-slim` | 72 | 69 | 3 | 4% |
| 47 | `python:3.12-slim` | 69 | 67 | 2 | 3% |
| 48 | `python:3.12.12-slim` | 69 | 67 | 2 | 3% |
| 49 | `python:3.13-slim` | 68 | 67 | 1 | 1% |
| 50 | `python:3.13.11-slim` | 68 | 67 | 1 | 1% |
| 51 | `python:3.13.12-slim` | 68 | 67 | 1 | 1% |
| 52 | `python:3.14-slim` | 68 | 67 | 1 | 1% |
| 53 | `python:3.14.2-slim` | 68 | 67 | 1 | 1% |
| 54 | `python:3.14.3-slim` | 68 | 67 | 1 | 1% |
| 55 | `python:3.15.0a5-slim` | 68 | 67 | 1 | 1% |
| 56 | `python:3.15.0a6-slim` | 67 | 67 | 0 | 0% |
| 57 | `redis:8.2.3-alpine3.22` | 0 | 0 | 0 | 0% |
| 58 | `redis:8.4-alpine` | 0 | 0 | 0 | 0% |
| 59 | `redis:8.4-alpine3.22` | 0 | 0 | 0 | 0% |
| 60 | `redis:8.4.0-alpine` | 0 | 0 | 0 | 0% |
| 61 | `redis:8.4.0-alpine3.22` | 0 | 0 | 0 | 0% |
| 62 | `redis:8.4.1-alpine3.22` | 0 | 0 | 0 | 0% |
| 63 | `redis:8.6-alpine` | 0 | 0 | 0 | 0% |
| 64 | `redis:8.6-alpine3.23` | 0 | 0 | 0 | 0% |
| 65 | `redis:8.6.0-alpine` | 0 | 0 | 0 | 0% |
| 66 | `redis:8.6.0-alpine3.23` | 0 | 0 | 0 | 0% |
| 67 | `ubuntu:24.04` | 25 | 11 | 14 | 56% |
| 68 | `ubuntu:24.10` | 0 | 0 | 0 | 0% |

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
*Last updated: 2026-02-13*
