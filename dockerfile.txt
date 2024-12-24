# Use an official Nginx image as the base image
FROM nginx:alpine

# Copy static files to the Nginx web root
COPY index.html /usr/share/nginx/html/index.html

# Expose port 80
EXPOSE 80

# Start Nginx when the container launches
CMD ["sh", "-c", "nginx -g 'daemon off;'"]
