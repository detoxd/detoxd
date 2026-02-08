# ============================================================================
# Detoxd Hardened Image - Iteration 2
# Generated from Trivy analysis - targeting 84 fixable vulns
# ============================================================================

ARG BASE_IMAGE=detoxd/mysql:9.0-detox.1
FROM ${BASE_IMAGE}

LABEL maintainer="detoxd"
LABEL detoxd.iteration="2"
LABEL detoxd.fixable.count="84"
LABEL detoxd.unfixable.count="0"

# Fix Python packages (only if pip is available)
RUN if command -v pip >/dev/null 2>&1 || command -v pip3 >/dev/null 2>&1; then \
    pip install --no-cache-dir --upgrade PyNaCl==1.6.2 certifi==2024.7.4 cryptography==43.0.1 && \
    rm -rf /root/.cache/pip /tmp/*; \
    fi

# Final cleanup
RUN rm -rf /tmp/* /var/tmp/* 2>/dev/null || true
