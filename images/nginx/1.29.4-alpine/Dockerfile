# ============================================================================
# Detoxd Hardened Image
# Auto-generated Dockerfile with security fixes
# ============================================================================

ARG BASE_IMAGE=nginx:1.29.4-alpine
FROM ${BASE_IMAGE}

# Metadata
LABEL maintainer="detoxd"
LABEL org.opencontainers.image.source="https://github.com/detoxd/detoxd"
LABEL org.opencontainers.image.title="Detoxd nginx"
LABEL org.opencontainers.image.description="Hardened nginx image with vulnerability fixes"
LABEL detoxd.base.image="nginx:1.29.4-alpine"

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
# NGINX-SPECIFIC SECURITY FIXES
# ============================================================================

# Remove default nginx pages
RUN rm -rf /usr/share/nginx/html/* 2>/dev/null || true

# Create non-root user for nginx
RUN adduser -D -H -u 1000 -s /sbin/nologin nginx-user 2>/dev/null || true

# Secure nginx configuration
RUN \
    # Disable server tokens
    sed -i 's/# server_tokens off;/server_tokens off;/' /etc/nginx/nginx.conf 2>/dev/null || true && \
    # Add security headers to default config if possible
    echo 'add_header X-Content-Type-Options nosniff;' > /etc/nginx/conf.d/security.conf 2>/dev/null || true && \
    echo 'add_header X-Frame-Options DENY;' >> /etc/nginx/conf.d/security.conf 2>/dev/null || true && \
    echo 'add_header X-XSS-Protection "1; mode=block";' >> /etc/nginx/conf.d/security.conf 2>/dev/null || true

EXPOSE 80 443

