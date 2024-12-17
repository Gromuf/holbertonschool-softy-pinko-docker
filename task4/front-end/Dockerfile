# Use the latest Nginx image
FROM nginx:latest

# Copy the front-end files into the Nginx web directory
COPY ./softy-pinko-front-end /var/www/html/softy-pinko-front-end

# Copy the Nginx configuration file
COPY ./softy-pinko-front-end.conf /etc/nginx/conf.d/default.conf

# Expose the port
EXPOSE 9000
