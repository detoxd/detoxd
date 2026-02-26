# ============================================================================
# Detoxd Hardened Image - Iteration 2
# Generated from Trivy analysis - targeting 49 fixable vulns
# ============================================================================

ARG BASE_IMAGE=detoxd/mongo:8.0.19-noble-detox.1
FROM ${BASE_IMAGE}

LABEL maintainer="detoxd"
LABEL detoxd.iteration="2"
LABEL detoxd.fixable.count="49"
LABEL detoxd.unfixable.count="12"

# Fix NPM packages (only if npm is available)
RUN if command -v npm >/dev/null 2>&1; then \
    npm install -g js-yaml@4.1.1 && \
    npm cache clean --force; \
    fi

# Final cleanup
RUN rm -rf /tmp/* /var/tmp/* 2>/dev/null || true
