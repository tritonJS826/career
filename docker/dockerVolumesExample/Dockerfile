# Use the Alpine Linux base image
FROM alpine:latest

# Install bash
RUN apk add --no-cache bash

# Copy the script into the container
COPY write_date.sh /usr/local/bin/write_date.sh

# Make the script executable
RUN chmod +x /usr/local/bin/write_date.sh

# Set the entrypoint to the script
ENTRYPOINT ["/usr/local/bin/write_date.sh"]

