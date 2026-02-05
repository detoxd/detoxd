# ============================================================================
# Detoxd Hardened Image - Iteration 1
# Generated from Trivy analysis - targeting 15 fixable vulns
# ============================================================================

ARG BASE_IMAGE=postgres:17-alpine
FROM ${BASE_IMAGE}

LABEL maintainer="detoxd"
LABEL detoxd.iteration="1"
LABEL detoxd.fixable.count="15"
LABEL detoxd.unfixable.count="0"

# Final cleanup
RUN rm -rf /tmp/* /var/tmp/* 2>/dev/null || true
