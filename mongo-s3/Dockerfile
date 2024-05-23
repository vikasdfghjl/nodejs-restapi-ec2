FROM mongo

# Install the AWS CLI
RUN apt-get update && apt-get install -y

# Create data directory and set permissions
RUN mkdir -p /data/db
RUN chown -R mongodb:mongodb /data/db
RUN mkdir -p /data/db
RUN chown -R 999:999 /data/db 
RUN chmod -R 700 /data/db   


# Expose MongoDB port
EXPOSE 27017

# Set the entrypoint to use S3 as the data volume
CMD ["mongod", "--bind_ip_all", "--dbpath", "/data/db"]
