# Use the official Ubuntu image as a base image
FROM ubuntu:latest

# Update the package list and install necessary packages
RUN apt-get update && \
    apt-get install -y apache2 mariadb-server && \
    rm -rf /var/lib/apt/lists/*

# Expose ports for Apache and MariaDB
EXPOSE 80 3306

# Start Apache and MariaDB services
CMD service apache2 start && service mysql start && tail -f /dev/null
