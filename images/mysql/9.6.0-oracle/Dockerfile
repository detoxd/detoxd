# ============================================================================
# Detoxd Hardened Image
# Auto-generated Dockerfile with security fixes
# ============================================================================

ARG BASE_IMAGE=mysql:9.6.0-oracle
FROM ${BASE_IMAGE}

# Metadata
LABEL maintainer="detoxd"
LABEL org.opencontainers.image.source="https://github.com/detoxd/detoxd"
LABEL org.opencontainers.image.title="Detoxd mysql"
LABEL org.opencontainers.image.description="Hardened mysql image with vulnerability fixes"
LABEL detoxd.base.image="mysql:9.6.0-oracle"

# ============================================================================
# GENERIC SECURITY FIXES (AUTO-DETECT PACKAGE MANAGER)
# ============================================================================

# Try to update packages using available package manager
RUN \
    if command -v apk >/dev/null 2>&1; then \
        apk update && apk upgrade --no-cache; \
    elif command -v apt-get >/dev/null 2>&1; then \
        apt-get update && apt-get upgrade -y && apt-get clean && rm -rf /var/lib/apt/lists/*; \
    elif command -v yum >/dev/null 2>&1; then \
        yum update -y && yum clean all; \
    elif command -v dnf >/dev/null 2>&1; then \
        dnf update -y && dnf clean all; \
    elif command -v microdnf >/dev/null 2>&1; then \
        microdnf update -y && microdnf clean all; \
    fi && \
    # Remove unnecessary files
    rm -rf /tmp/* /var/tmp/* 2>/dev/null || true

# Set secure permissions
RUN chmod 700 /root 2>/dev/null || true && \
    chmod 1777 /tmp 2>/dev/null || true

