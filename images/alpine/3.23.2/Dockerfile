# ============================================================================
# Detoxd Hardened Image - Iteration 1
# Generated from Trivy analysis - targeting 24 fixable vulns
# ============================================================================

ARG BASE_IMAGE=alpine:3.23.2
FROM ${BASE_IMAGE}

LABEL maintainer="detoxd"
LABEL detoxd.iteration="1"
LABEL detoxd.fixable.count="24"
LABEL detoxd.unfixable.count="0"

# Fix OS packages with known vulnerabilities
RUN apk update && \
    apk upgrade --no-cache libcrypto3 libssl3 && \
    rm -rf /var/cache/apk/*

# Final cleanup
RUN rm -rf /tmp/* /var/tmp/* 2>/dev/null || true
