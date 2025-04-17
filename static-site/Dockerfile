# Use official Nginx image
FROM nginx:alpine

# Remove default Nginx page
RUN rm -rf /usr/share/nginx/html/*

# Copy custom HTML into Nginx's public folder
COPY index.html /usr/share/nginx/html/

# Expose port
EXPOSE 80

# Use default Nginx entrypoint
