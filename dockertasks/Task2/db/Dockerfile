# Derived from official mysql image (our base image)
# Use mysql 5.7 as the flask-app is not set up to work with later versions
FROM mysql:5.7
# Add a database and root password
# For hints on how to do this, consult the mysql 5.7 image documentation
# Set the default user for the MySQL image
USER mysql
# Set environment variables for the new user
ENV MYSQL_DATABASE=flask-db
ENV MYSQL_PASSWORD=password
ENV MYSQL_ROOT_PASSWORD=password
# Add the content of the .sql file to your image
COPY CreateTable.sql .

# Expose port 3306 to allow connections to the database
EXPOSE 3306

# Start the MySQL server when the container is run
CMD ["mysqld"]
# All scripts copied to docker-entrypoint-initdb.d/ are automatically
# executed during container startup
