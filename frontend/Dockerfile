FROM nginx:1.13.3-alpine
MAINTAINER NS InfoPlus

# Add portaal nginx config
ADD nginx.conf /etc/nginx/nginx.conf

# Copy static application content
COPY /dist/ /usr/share/nginx/html
