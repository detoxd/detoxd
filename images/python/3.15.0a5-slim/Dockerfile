# ============================================================================
# Detoxd Hardened Image
# Auto-generated Dockerfile with security fixes
# ============================================================================

ARG BASE_IMAGE=python:3.15.0a5-slim
FROM ${BASE_IMAGE}

# Metadata
LABEL maintainer="detoxd"
LABEL org.opencontainers.image.source="https://github.com/detoxd/detoxd"
LABEL org.opencontainers.image.title="Detoxd python"
LABEL org.opencontainers.image.description="Hardened python image with vulnerability fixes"
LABEL detoxd.base.image="python:3.15.0a5-slim"

# ============================================================================
# SECURITY FIXES FOR DEBIAN/UBUNTU-BASED IMAGE
# ============================================================================

# Update all packages to latest versions (fixes known CVEs)
RUN apt-get update && \
    apt-get upgrade -y --no-install-recommends && \
    apt-get dist-upgrade -y && \
    # Remove unnecessary packages
    apt-get purge -y --auto-remove \
        wget \
        curl \
        netcat* \
        telnet* \
        2>/dev/null || true && \
    # Clean up apt cache
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* && \
    # Remove unnecessary files
    rm -rf /tmp/* /var/tmp/* && \
    # Remove shell history
    rm -f /root/.bash_history

# Security hardening
RUN \
    # Remove setuid/setgid bits from binaries
    find / -perm /6000 -type f -exec chmod a-s {} \; 2>/dev/null || true && \
    # Remove unnecessary accounts (keeping system-critical ones)
    for user in games gnats irc list news proxy uucp; do \
        userdel -r $user 2>/dev/null || true; \
    done

# Set secure permissions
RUN chmod 700 /root && \
    chmod 1777 /tmp

# ============================================================================
# PYTHON-SPECIFIC SECURITY FIXES
# ============================================================================

# Update pip and setuptools
RUN pip install --no-cache-dir --upgrade pip setuptools wheel && \
    # Remove pip cache
    rm -rf /root/.cache/pip

# Create non-root user
RUN useradd -r -u 1000 -s /sbin/nologin pythonuser 2>/dev/null || true

# Set Python to unbuffered output
ENV PYTHONUNBUFFERED=1
ENV PYTHONDONTWRITEBYTECODE=1

WORKDIR /app
USER pythonuser

