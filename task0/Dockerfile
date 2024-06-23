# Use the latest version of Ubuntu as a base image
FROM ubuntu:latest

# Update APT package list
RUN apt-get update

# Upgrade all installed packages
RUN apt-get upgrade -y

# Remove unnecessary files after installation
RUN apt-get clean && \
    rm -rf /var/lib/apt/lists/*

# Set the working directory inside the container
WORKDIR /task0

# Copy the entrypoint script into the container
COPY ./entrypoint.sh /task0/entrypoint.sh

# Make the entrypoint script executable
RUN chmod +x /task0/entrypoint.sh

# Run the entrypoint script when the container starts
ENTRYPOINT ["/task0/entrypoint.sh"]

# Command to run when the container starts
CMD echo "Hello, World!"
