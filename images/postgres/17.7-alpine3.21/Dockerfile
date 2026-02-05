# ============================================================================
# Detoxd Hardened Image - Iteration 2
# Generated from Trivy analysis - targeting 15 fixable vulns
# ============================================================================

ARG BASE_IMAGE=detoxd/postgres:17.7-alpine3.21-detox.1
FROM ${BASE_IMAGE}

LABEL maintainer="detoxd"
LABEL detoxd.iteration="2"
LABEL detoxd.fixable.count="15"
LABEL detoxd.unfixable.count="0"

# Final cleanup
RUN rm -rf /tmp/* /var/tmp/* 2>/dev/null || true
