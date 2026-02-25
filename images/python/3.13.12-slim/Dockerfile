# ============================================================================
# Detoxd Hardened Image - Iteration 1
# Generated from Trivy analysis - targeting 1 fixable vulns
# ============================================================================

ARG BASE_IMAGE=python:3.13.12-slim
FROM ${BASE_IMAGE}

LABEL maintainer="detoxd"
LABEL detoxd.iteration="1"
LABEL detoxd.fixable.count="1"
LABEL detoxd.unfixable.count="68"

# Fix Python packages (only if pip is available)
RUN if command -v pip >/dev/null 2>&1 || command -v pip3 >/dev/null 2>&1; then \
    pip install --no-cache-dir --upgrade pip==26.0 && \
    rm -rf /root/.cache/pip /tmp/*; \
    fi

# Final cleanup
RUN rm -rf /tmp/* /var/tmp/* 2>/dev/null || true
