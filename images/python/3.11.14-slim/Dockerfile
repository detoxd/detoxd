# ============================================================================
# Detoxd Hardened Image - Iteration 3
# Generated from Trivy analysis - targeting 2 fixable vulns
# ============================================================================

ARG BASE_IMAGE=detoxd/python:3.11.14-slim-detox.2
FROM ${BASE_IMAGE}

LABEL maintainer="detoxd"
LABEL detoxd.iteration="3"
LABEL detoxd.fixable.count="2"
LABEL detoxd.unfixable.count="68"

# Fix Python packages (only if pip is available)
RUN if command -v pip >/dev/null 2>&1 || command -v pip3 >/dev/null 2>&1; then \
    pip install --no-cache-dir --upgrade jaraco.context==6.1.0 wheel==0.46.2 && \
    rm -rf /root/.cache/pip /tmp/*; \
    fi

# Final cleanup
RUN rm -rf /tmp/* /var/tmp/* 2>/dev/null || true
