# Use the official Nginx base image
FROM nginx:alpine

# Copy the HTML file to the Nginx default directory
COPY index.html /usr/share/nginx/html/index.html

# Expose port 80 to the outside world
EXPOSE 80

# Start Nginx when the container launches
CMD ["nginx", "-g", "daemon off;"]
