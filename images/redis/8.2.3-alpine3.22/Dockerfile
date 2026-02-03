# ============================================================================
# Detoxd Hardened Image
# Auto-generated Dockerfile with security fixes
# ============================================================================

ARG BASE_IMAGE=redis:8.2.3-alpine3.22
FROM ${BASE_IMAGE}

# Metadata
LABEL maintainer="detoxd"
LABEL org.opencontainers.image.source="https://github.com/detoxd/detoxd"
LABEL org.opencontainers.image.title="Detoxd redis"
LABEL org.opencontainers.image.description="Hardened redis image with vulnerability fixes"
LABEL detoxd.base.image="redis:8.2.3-alpine3.22"

# ============================================================================
# SECURITY FIXES FOR ALPINE-BASED IMAGE
# ============================================================================

# Update all packages to latest versions (fixes known CVEs)
RUN apk update && \
    apk upgrade --no-cache && \
    # Remove unnecessary packages
    apk del --purge \
        wget \
        curl \
        busybox-extras \
        2>/dev/null || true && \
    # Remove package cache
    rm -rf /var/cache/apk/* && \
    # Remove unnecessary files
    rm -rf /tmp/* /var/tmp/* && \
    # Remove shell history
    rm -f /root/.ash_history /root/.bash_history

# Security hardening
RUN \
    # Remove setuid/setgid bits from binaries
    find / -perm /6000 -type f -exec chmod a-s {} \; 2>/dev/null || true && \
    # Remove unnecessary accounts
    for user in games news uucp proxy www-data list irc gnats nobody; do \
        deluser $user 2>/dev/null || true; \
    done && \
    # Restrict cron
    rm -rf /etc/cron.* /etc/crontabs 2>/dev/null || true && \
    # Remove init scripts
    rm -rf /etc/init.d /lib/rc /etc/conf.d /etc/inittab /etc/runlevels /etc/rc.conf 2>/dev/null || true

# Set secure permissions
RUN chmod 700 /root && \
    chmod 1777 /tmp

# ============================================================================
# REDIS-SPECIFIC SECURITY FIXES
# ============================================================================

# Secure redis configuration
RUN \
    # Disable dangerous commands in redis.conf if exists
    if [ -f /etc/redis.conf ]; then \
        echo 'rename-command FLUSHDB ""' >> /etc/redis.conf && \
        echo 'rename-command FLUSHALL ""' >> /etc/redis.conf && \
        echo 'rename-command DEBUG ""' >> /etc/redis.conf && \
        echo 'rename-command CONFIG ""' >> /etc/redis.conf; \
    fi

EXPOSE 6379

