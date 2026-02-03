# ============================================================================
# Detoxd Hardened Image
# Auto-generated Dockerfile with security fixes
# ============================================================================

ARG BASE_IMAGE=ubuntu:24.10
FROM ${BASE_IMAGE}

# Metadata
LABEL maintainer="detoxd"
LABEL org.opencontainers.image.source="https://github.com/detoxd/detoxd"
LABEL org.opencontainers.image.title="Detoxd ubuntu"
LABEL org.opencontainers.image.description="Hardened ubuntu image with vulnerability fixes"
LABEL detoxd.base.image="ubuntu:24.10"

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

