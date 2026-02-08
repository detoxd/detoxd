# ============================================================================
# Detoxd Hardened Image - Iteration 1
# Generated from Trivy analysis - targeting 19 fixable vulns
# ============================================================================

ARG BASE_IMAGE=mysql:9.6-oraclelinux9
FROM ${BASE_IMAGE}

LABEL maintainer="detoxd"
LABEL detoxd.iteration="1"
LABEL detoxd.fixable.count="19"
LABEL detoxd.unfixable.count="0"

# Fix Python packages (only if pip is available)
RUN if command -v pip >/dev/null 2>&1 || command -v pip3 >/dev/null 2>&1; then \
    pip install --no-cache-dir --upgrade PyNaCl==1.6.2 pip==25.3 && \
    rm -rf /root/.cache/pip /tmp/*; \
    fi

# Final cleanup
RUN rm -rf /tmp/* /var/tmp/* 2>/dev/null || true
