# Use the official AlmaLinux base image
FROM almalinux:latest

# Install Nginx from the AlmaLinux repository
RUN dnf install -y nginx

# Expose port 80 for HTTP traffic

# Start Nginx when the container starts
CMD ["nginx", "-g", "daemon off;"]
RUN chmod 644 /etc/nginx/nginx.conf
RUN rm -rf /etc/nginx/nginx.conf
RUN rm -rf /etc/nginx/conf.d/default.conf
COPY default.conf /etc/nginx/nginx.conf
ADD static /usr/share/nginx/html/
RUN rm -rf /usr/share/nginx/html/index.html
ENV CATALOGUE_HOST="catalogue"


