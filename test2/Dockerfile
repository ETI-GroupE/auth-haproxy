# Use an official HAProxy image as the base
FROM haproxy:2.0

# Set the working directory
WORKDIR /usr/local/etc/haproxy

# Copy the HAProxy configuration file
COPY haproxy.cfg .

# Install the MySQL client
RUN apt-get update && \
    apt-get install -y mysql-client && \
    rm -rf /var/lib/apt/lists/*

# Start HAProxy with the configuration file
CMD ["haproxy", "-f", "haproxy.cfg"]