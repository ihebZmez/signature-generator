FROM nginx:alpine

# Install wget for the healthcheck
RUN apk add --no-cache wget

# Copy nginx config and built app
COPY docker/nginx.conf /etc/nginx/conf.d/default.conf
COPY dist/ /usr/share/nginx/html

# Send logs to Docker instead of files
RUN ln -sf /dev/stdout /var/log/nginx/access.log && \
    ln -sf /dev/stderr /var/log/nginx/error.log

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]