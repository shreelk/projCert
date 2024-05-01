# Use an official apache PHP runtime image
FROM php:8.0-apache

# Set the working directory in the container
WORKDIR /var/www/html

# Copy your PHP application code into the container
COPY . .

# Install PHP extensions and other dependencies
RUN apt-get update && \
    apt-get install -y libpng-dev && \
    docker-php-ext-install gd

# Expose the port Apache listens on
EXPOSE 80

# Start Apache when the container runs
CMD ["apache2-foreground"]
