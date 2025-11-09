FROM almalinux:8

# Install nginx
RUN yum install -y nginx

# Remove default page (optional)
RUN rm -rf /usr/share/nginx/html/*

# Copy your custom website files (ensure qi/ folder exists in same dir)
COPY qi/ /usr/share/nginx/html/

# Expose port 80
EXPOSE 80

# Run nginx in foreground (so container stays alive)
CMD ["nginx", "-g", "daemon off;"]
