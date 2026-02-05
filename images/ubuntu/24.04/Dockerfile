# ============================================================================
# Detoxd Hardened Image - Iteration 1
# Generated from Trivy analysis - targeting 14 fixable vulns
# ============================================================================

ARG BASE_IMAGE=ubuntu:24.04
FROM ${BASE_IMAGE}

LABEL maintainer="detoxd"
LABEL detoxd.iteration="1"
LABEL detoxd.fixable.count="14"
LABEL detoxd.unfixable.count="12"

# Fix OS packages with known vulnerabilities
RUN apt-get update && \
    apt-get install -y --only-upgrade libc-bin libc6 libssl3t64 || apt-get upgrade -y && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

# Final cleanup
RUN rm -rf /tmp/* /var/tmp/* 2>/dev/null || true
