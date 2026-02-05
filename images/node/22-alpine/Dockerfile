# ============================================================================
# Detoxd Hardened Image - Iteration 1
# Generated from Trivy analysis - targeting 11 fixable vulns
# ============================================================================

ARG BASE_IMAGE=node:22-alpine
FROM ${BASE_IMAGE}

LABEL maintainer="detoxd"
LABEL detoxd.iteration="1"
LABEL detoxd.fixable.count="11"
LABEL detoxd.unfixable.count="1"

# Fix NPM packages (only if npm is available)
RUN if command -v npm >/dev/null 2>&1; then \
    npm install -g diff@8.0.3 glob@11.1.0 tar@7.5.3 && \
    npm cache clean --force; \
    fi

# Final cleanup
RUN rm -rf /tmp/* /var/tmp/* 2>/dev/null || true
