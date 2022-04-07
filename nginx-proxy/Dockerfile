FROM jwilder/nginx-proxy:1.0@sha256:3b8cb95a88d2905900cc761d28f6f3c32bbb2077fbf9f9edf870cea9aa537bf0
LABEL org.label-schema.schema-version="1.0.0"
LABEL org.label-schema.vendor="EasyEngine"
LABEL org.label-schema.name="nginx-proxy"

COPY docker-entrypoint.sh /app/
COPY nginx.tmpl /app/
COPY nginx.conf /etc/nginx/nginx.conf
COPY version.conf /version.conf

RUN apt-get update \
    && apt-get install --no-install-recommends apache2-utils -y && rm -rf /var/lib/apt/lists/*

RUN chmod +x /app/docker-entrypoint.sh
RUN rm -rf /var/log/nginx/access.log /var/log/nginx/error.log && touch /var/log/nginx/access.log /var/log/nginx/error.log
