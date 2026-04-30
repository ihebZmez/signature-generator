FROM nginx:alpine

# Copy nginx config
COPY docker/nginx.conf /etc/nginx/conf.d/default.conf

# Copy ONLY the built app
COPY dist/ /usr/share/nginx/html

EXPOSE 80