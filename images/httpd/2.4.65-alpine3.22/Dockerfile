# ============================================================================
# Detoxd Hardened Image - Iteration 1
# Generated from Trivy analysis - targeting 38 fixable vulns
# ============================================================================

ARG BASE_IMAGE=httpd:2.4.65-alpine3.22
FROM ${BASE_IMAGE}

LABEL maintainer="detoxd"
LABEL detoxd.iteration="1"
LABEL detoxd.fixable.count="38"
LABEL detoxd.unfixable.count="0"

# Fix OS packages with known vulnerabilities
RUN apk update && \
    apk upgrade --no-cache busybox busybox-binsh c-ares libcrypto3 libexpat libssl3 libxml2 ssl_client && \
    rm -rf /var/cache/apk/*

# Final cleanup
RUN rm -rf /tmp/* /var/tmp/* 2>/dev/null || true
